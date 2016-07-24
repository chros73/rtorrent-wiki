# rTorrent Performance Tuning
**Contents**

 * [rTorrent related settings](#rtorrent-related-settings)
  * [Sample config entries](#sample-config-entries)
 * [System wide settings](#system-wide-settings)
  * [Max open files](#max-open-files)
  * [Networking tweaks](#networking-tweaks)
 * [Name resolving enhancements](#name-resolving-enhancements)
  * [rTrorrent with c-ares](#rtrorrent-with-c-ares)
  * [Local DNS cache](#local-dns-cache)
 * [References](#references)


## rTorrent related settings

rTorrent uses a different philosophy than most other torrent client.

### Sample config entries

Assuming everything is going well we can focus on performance tuning. Let's see the related possible settings at once first.

These settings are used with 74/20 Mbps connection, 4 GB RAM and 1 local disk device.

```ini
# Global upload and download rate in KiB, `0` for unlimited (`download_rate`, `upload_rate`)
throttle.global_down.max_rate.set_kb = 8700
throttle.global_up.max_rate.set_kb   = 2200

# Maximum number of simultaneous downloads and uploads slots (global slots!) (`max_downloads_global`, `max_uploads_global`)
throttle.max_downloads.global.set = 300
throttle.max_uploads.global.set   = 300

# Maximum and minimum number of peers to connect to per torrent while downloading (`min_peers`, `max_peers`)
throttle.min_peers.normal.set = 99
throttle.max_peers.normal.set = 100

# Same as above but for seeding completed torrents (seeds per torrent), `-1` for same as downloading (`min_peers_seed`, `max_peers_seed`)
throttle.min_peers.seed.set = -1
throttle.max_peers.seed.set = -1

# Maximum number of simultanious uploads per torrent (upload slots!) (`max_uploads`)
throttle.max_uploads.set = 50

# Set the numwant field sent to the tracker, which indicates how many peers we want. 
#  A negative value disables this feature. Default: `-1` (`tracker_numwant`)
trackers.numwant.set = 100

# Set the max amount of memory space used to mapping file chunks. This refers to memory mapping, not physical memory
#  allocation. (`max_memory_usage`) This may also be set using ulimit -m where 3/4 will be allocated to file chunks.
pieces.memory.max.set = 2048M

# Maximum number of connections rtorrent can accept/make (`sockets`)
network.max_open_sockets.set = 999

# Maximum number of open files rtorrent can keep open (you have to modify the system wide settings with ulimit!) (`set_max_open_files`)
network.max_open_files.set = 600

# Maximum number of simultanous HTTP request (used by announce or scrape requests) Default: `32` (`set_max_open_http`)
network.http.max_open.set = 99

# Send and receive buffer size for socket. Disabled by default (`0`), this means the default is used by OS 
#  (you have to modify the system wide settings!) (`send_buffer_size`, `receive_buffer_size`)
# Increasing buffer sizes may help reduce disk seeking, connection polling as more data is buffered each time
#  the socket is written to. It will result higher memory usage (not visible in rtorrent process!).
network.receive_buffer.size.set =  4M
network.send_buffer.size.set    = 12M

# Preloading a piece of a file. Default: `0` Possible values: `0` (Off) , `1` (Madvise) , `2` (Direct paging).
pieces.preload.type.set = 2
#pieces.preload.min_size.set = 262144
#pieces.preload.min_rate.set = 5120

# TOS of peer connections. Default: `throughput`. If the option is set to `default` then the system default TOS
#  is used. A hex value may be used for non-standard settings.  (`tos`)
# Possible values: `[default|lowdelay|throughput|reliability|mincost]` or a hex value.
#network.tos.set = throughput

# Max packet size using xmlrpc. Default: `524288` (xmlrpc_size_limit)
network.xmlrpc.size_limit.set = 2M

# Save all the sessions in every 12 hours instead of the default 20 minutes.
schedule2 = session_save, 1200, 43200, ((session.save))

# Prune file status in every 24 hours, this is the default setting.
#schedule2 = prune_file_status, 3600, 86400, ((system.file_status_cache.prune))

# Whether to allocate disk space for a new torrent. Default: `0`
#system.file.allocate.set = 0
```


## System wide settings

To use higher settings for couple of the above settings the system wide limit should be raised for them.

### Max open files

`network.max_open_files` is limited to `ulimit -n`. If you want to increase it you can use `ulimit -n new_value` or apply it permanently via `/etc/security/limits.conf` on Ubuntu (default: `1024`):
```ini
#<domain>      <type>  <item>         <value>
username       soft    nofile         10240
username       hard    nofile         10240
```

### Networking tweaks

`network.receive_buffer.size`, `network.send_buffer.size` are limited to `sysctl -a | grep -i rmem` and `sysctl -a | grep -i wmem`. You have to change `net.core.rmem_max`, `net.ipv4.tcp_rmem`, `net.core.wmem_max`, `net.ipv4.tcp_wmem` in `/etc/sysctl.conf` to the desired values along with some other tweaks:
```ini
# Maximum Socket Receive Buffer. 16MB per socket - which sounds like a lot, but will virtually never consume that much. Default: 212992
net.core.rmem_max = 16777216
# Maximum Socket Send Buffer. 16MB per socket - which sounds like a lot, but will virtually never consume that much. Default: 212992
net.core.wmem_max = 16777216
# Increase the write-buffer-space allocatable: min 4KB, def 12MB, max 16MB. Default: 4096 16384 4194304
net.ipv4.tcp_wmem = 4096 12582912 16777216
# Increase the read-buffer-space allocatable: min 4KB, def 12MB, max 16MB. Default: 4096 16384 4194304
net.ipv4.tcp_rmem = 4096 12582912 16777216

# Tells the system whether it should start at the default window size only for new TCP connections or also for existing TCP connections that have been idle for too long. Default: 1
net.ipv4.tcp_slow_start_after_idle = 0
# Allow reuse of sockets in TIME_WAIT state for new connections only when it is safe from the network stack’s perspective. Default: 0
net.ipv4.tcp_tw_reuse = 1
# Do not last the complete time_wait cycle. Default: 0
net.ipv4.tcp_tw_recycle = 1
# Minimum time a socket will stay in TIME_WAIT state (unusable after being used once). Default: 60
net.ipv4.tcp_fin_timeout = 30
```


## Name resolving enhancements

`rTorrent` sometimes can hang on hostname lookups, even with normal http/https requests. Here it is what we can do about it.

### rTrorrent with c-ares

`c-ares` is a C library for asynchronous DNS requests (including name resolves). [Here](http://web.archive.org/web/20140727040445/http://filesharefreak.com/tutorials/rtorrent-libtorrent-installing-on-linux) you can find instructions how to compile it or just simply use [rtorrent-ps](https://github.com/pyroscope/rtorrent-ps) by @pyroscope, its build script will do everything you need.

### Local DNS cache

In addition to the above, it's strongly advised to use DNS caching either locally or for your whole network (e.g. on a OpenWRT powered router). [Here](https://help.ubuntu.com/community/Dnsmasq#Local_DNS_Cache) you can find instructions how to set it up on Ubuntu.

## References

- [libtorrent manual](http://www.libtorrent.org/tuning.html)
- [lost rTorrent docs](http://web.archive.org/web/20131104130853/http://libtorrent.rakshasa.no/wiki/RTorrentPerformanceTuning)
- [rTorrent research](https://calomel.org/rtorrent_mods.html)
- [c-ares](http://c-ares.haxx.se)
- [Local DNS Cache](https://help.ubuntu.com/community/Dnsmasq#Local_DNS_Cache)
- [Networking tweaks](http://wiki.mikejung.biz/Sysctl_tweaks)