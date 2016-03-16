# rTorrent Configuration Guide
**Contents**

 * [Basic Configuration](#basic-configuration)
 * [Advanced Use-Cases](#advanced-use-cases)
 * [Advanced Topics](#advanced-topics)


## Basic Configuration 

See [rTorrent Configuration Template](https://github.com/rakshasa/rtorrent/wiki/CONFIG-Template) for a modern rTorrent configuration that provides a good starting point. The following sub-sections describe some of the essential settings you must have in a common configuration.

### Using a Session Directory

Adding the `session.path.set` command will enable session management, which means the torrent files and status information for all open downloads will be stored in this directory. When restarting rTorrent all torrents previously loaded will be restored. Only one instance of rTorrent should be used with each session directory, though at the moment no locking is done. An empty string will disable the session handling.


### Watching a Directory for Torrents

The client may be configured to check a directory for new torrents and load them. Torrents loaded in this manner will be *tied* to the file's path. This means when the torrent file is deleted the torrent may be stopped (requires additional configuration), and when the item is removed the torrent file is, too. Note that you can untie an item by using the `U` key (which will delete the tied file), and using `^K` also implictly unties an item.

```ini
# Watch directories (add more as you like, but use unique schedule names)
schedule = watch_start,10,10,((load.start,"./watch/start/*.torrent"))
schedule = watch_load,15,10,((load.normal,"./watch/load/*.torrent"))
```


## Advanced Use-Cases

 * [Watch Directories](https://github.com/rakshasa/rtorrent/wiki/TORRENT-Watch-directories)
 * [Ratio Handling](https://github.com/rakshasa/rtorrent/wiki/RTorrentRatioHandling)
 * [Using DHT](https://github.com/rakshasa/rtorrent/wiki/Using-DHT)
 * [Using XMLRPC with rTorrent](https://github.com/rakshasa/rtorrent/wiki/RPC-Setup-XMLRPC)


## Advanced Topics

 * [Logging](https://github.com/rakshasa/rtorrent/wiki/LOG-Logging)
 * [Migration to the 0.9.x command syntax](https://github.com/rakshasa/rtorrent/wiki/RPC-Migration-0.9)
