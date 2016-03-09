# rTorrent Configuration Template

This page contains a modern rTorrent configuration that provides a good starting point.
Its expressed purpose is to replace that years-old rotting piece of garbage that people still use to create their first configuration. Friends don't let friends use that!

It uses `0.9.x` syntax, so be sure to run snippets you add through
the migration script. Be considerate in what you add, this is supposed
to help new users to jump-start their installation, so keep things
out that are not applicable to a wide range of people. Place advanced
use-cases in the appropriate sections of the wiki, like the
[Configuration Guide](https://github.com/rakshasa/rtorrent/wiki/Config-Guide).

```ini
#############################################################################
# A minimal rTorrent configuration that provides the basic features
# you want to have in addition to the built-in defaults.
#
# See https://github.com/rakshasa/rtorrent/wiki/CONFIG-Template
# for an up-to-date version.
#############################################################################

# *** BIG TODO ***

# Limits for file handle resources, this is optimized for
# an `ulimit` of 1024 (a common default). You MUST leave
# a ceiling of handles reserved for rTorrent's internal needs!
network.http.max_open.set = 50
network.max_open_files.set = 600
network.max_open_sockets.set = 300

# Memory resource usage (increase if you have a large number of items loaded)
pieces.memory.max.set = 1800M
network.xmlrpc.size_limit.set = 2M

### END of rtorrent.rc ###
```