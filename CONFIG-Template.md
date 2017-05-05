# rTorrent Configuration Template

## Overview

This page contains a modern rTorrent configuration that provides a good starting point.
Its expressed purpose is to replace that years-old rotting piece of garbage that people still use to create their first configuration. Friends don't let friends use that!

A detailed explanation of this configuration can be found at
[Config Template Deconstructed](http://rtorrent-docs.readthedocs.io/en/latest/cookbook.html#config-template-deconstructed).

It uses `0.9.x` syntax and is tested using `0.9.6`, so be sure to run snippets you add through
the [migration script](https://github.com/rakshasa/rtorrent/wiki/RPC-Migration-0.9).
Be considerate in what you add, this is supposed
to help new users to jump-start their installation, so keep things
out that are not applicable to a wide range of people. Place advanced
use-cases in the appropriate sections of the wiki, like the
[Configuration Guide](https://github.com/rakshasa/rtorrent/wiki/Config-Guide).


## Using the Template

Use these commands to get a copy of the template to your disk and create the directory for your instance:

```sh
curl -Ls "https://raw.githubusercontent.com/wiki/rakshasa/rtorrent/CONFIG-Template.md" \
    | grep -A9999 '^######' | grep -B9999 '^### END' \
    | sed -re "s:/home/USERNAME:$HOME:" >~/.rtorrent.rc
mkdir ~/rtorrent
```

Then (re-)start rTorrent.

## The Template

Also see [Load ‘Drop-In’ Config Fragments](http://rtorrent-docs.readthedocs.io/en/latest/use-cases.html#drop-in-config)
on how to extend this so you can load extensions to this template
from files in a ``config.d`` directory.

```ini
#############################################################################
# A minimal rTorrent configuration that provides the basic features
# you want to have in addition to the built-in defaults.
#
# See https://github.com/rakshasa/rtorrent/wiki/CONFIG-Template
# for an up-to-date version.
#############################################################################

# Instance layout (base paths)
method.insert = cfg.basedir, private|const|string, (cat,"/home/USERNAME/rtorrent/")
method.insert = cfg.watch,   private|const|string, (cat,(cfg.basedir),"watch/")
method.insert = cfg.logs,    private|const|string, (cat,(cfg.basedir),"log/")
method.insert = cfg.logfile, private|const|string, (cat,(cfg.logs),"rtorrent-",(system.time),".log")

# Create instance directories
execute.throw = bash, -c, (cat,\
    "builtin cd \"", (cfg.basedir), "\" ",\
    "&& mkdir -p .session download log watch/{load,start}")

# Listening port for incoming peer traffic (fixed; you can also randomize it)
network.port_range.set = 50000-50000
network.port_random.set = no

# Tracker-less torrent and UDP tracker support
# (conservative settings for 'private' trackers, change for 'public')
dht.mode.set = disable
protocol.pex.set = no
trackers.use_udp.set = no

# Peer settings
throttle.min_peers.normal.set = 20
throttle.max_peers.normal.set = 60
throttle.min_peers.seed.set = 30
throttle.max_peers.seed.set = 80

# Limits for file handle resources, this is optimized for
# an `ulimit` of 1024 (a common default). You MUST leave
# a ceiling of handles reserved for rTorrent's internal needs!
network.http.max_open.set = 50
network.max_open_files.set = 600
network.max_open_sockets.set = 300

# Memory resource usage (increase if you have a large number of items loaded,
# and/or the available resources to spend)
pieces.memory.max.set = 1800M
network.xmlrpc.size_limit.set = 2M

# Basic operational settings (no need to change these)
session.path.set = (cat, (cfg.basedir), ".session/")
directory.default.set = (cat, (cfg.basedir), "download/")

# Watch directories (add more as you like, but use unique schedule names)
schedule2 = watch_start, 10, 10, ((load.start, (cat, (cfg.watch), "start/*.torrent")))
schedule2 = watch_load, 11, 10, ((load.normal, (cat, (cfg.watch), "load/*.torrent")))

# Logging:
#   Levels = critical error warn notice info debug
#   Groups = connection_* dht_* peer_* rpc_* storage_* thread_* tracker_* torrent_*
print = (cat, "Logging to ", (cfg.logfile))
log.open_file = "log", (cfg.logfile)
log.add_output = "info", "log"
#log.add_output = "tracker_debug", "log"

### END of rtorrent.rc ###
```