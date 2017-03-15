# RTorrent and LibTorrent Wiki

[![Travis CI](https://api.travis-ci.org/rakshasa/rtorrent.png?branch=master)](https://travis-ci.org/rakshasa/rtorrent)
[![Download](http://img.shields.io/badge/download-v0.9.6-0000ff.svg)](https://github.com/rakshasa/rtorrent/wiki#download-links)

The **rTorrent** bittorrent client uses ncurses and is ideal for use with [tmux](https://tmux.github.io/), [screen](http://www.gnu.org/software/screen/) or  [dtach](http://dtach.sourceforge.net/). Alternatively, version 0.9.7+ has a [[built-in daemon mode|Daemon_Mode]] disabling the user interface, so you can only control it via XMLRPC. It supports saving of sessions, allows the user to add/remove torrents, and much more.

:busts_in_silhouette: :pencil: | This wiki is editable by any GitHub user, and thus the often-expressed wish for a complete and current manual depends on *YOU*. See [Mastering Wikis](https://guides.github.com/features/wikis/) and [Mastering Markdown](https://guides.github.com/features/mastering-markdown/), it's *NOT* :rocket: science. :wink: <br /><br /> The [[TODO]] page has a list of pending work items. See [[About this Wiki…|WikiAbout]] for more information on how you can contribute, and the structure of this wiki (i.e. where to put things).
---: | :---

**Page Contents**

 * [User's Manual](#users-manual)
 * [Other Information](#other-information)
 * [Download Links](#download-links)
 * [Installation](#installation)
 * [Packages](#packages)
 * [Disclaimer](#disclaimer)
 * [Stuff](#stuff)


## User's Manual
 * the [[User Guide|User-Guide]] explains how to use the ‘curses’ UI, and what the displayed information actually means.
 * the [[Configuration Guide|Config-Guide]] helps you to adapt rTorrent to serve your needs.
   * [[rTorrent Configuration Template|CONFIG-Template]]
   * [[Watch Directories|TORRENT-Watch-directories]]
   * [[Ratio Handling|RTorrentRatioHandling]]
   * [[Tor Proxying|Tor-based-Proxying-Guide]]
   * [[Using DHT|Using-DHT]]
   * [[Using XMLRPC with rTorrent|RPC-Setup-XMLRPC]]
   * [[Performance Tuning|Performance-Tuning]]
   * [[Favoring one group of torrents over the rest of them|Favoring-group-of-torrents]]
   * [[Auto-Scraping|Auto-Scraping]]
   * [[Logging|LOG-Logging]]
   * [[Migration to the 0.9.x command syntax|RPC-Migration-0.9]]
   * [[Common Tasks in rTorrent|Common-Tasks-in-rTorrent]]
   * [[Choke Groups|Choke-Groups]]
   * [[IP filtering|IP-filtering]]
   * [[rTorrent 0.9 Comprehensive Command list|rTorrent-0.9-Comprehensive-Command-list-(WIP)]]
   * [[Using initial seeding|Using-initial-seeding]]
 * the [[Scripting Guide|Scripting-Guide]] allows ‘power users’ to extend rTorrent's configuration with more complex logic, and control it remotely via XMLRPC.
 * the [[Vagrant|Vagrant]] repository allows easy creation of a test environment for the client.


## Other Information

 * List of [[Known Issues|Issues]]
 * List of [[Todos|TODO]]


## Download Links

**Stable Version**

 * http://rtorrent.net/downloads/libtorrent-0.13.6.tar.gz
 * http://rtorrent.net/downloads/rtorrent-0.9.6.tar.gz

**All Versions**

 * http://rtorrent.net/downloads/


## Installation

See the [[Installing]] wiki page for more information.


## Packages

rTorrent and libTorrent packages are both available for the following operating systems and distributions:

 * [Debian](https://www.debian.org/) and [Ubuntu](https://ubuntu.com) : Run `apt-get install rtorrent`.
 * [Fedora](https://fedoraproject.org/wiki/Fedora_Project_Wiki) : Run `dnf install rtorrent`.
 * [Gentoo](https://gentoo.org/) : in Portage; see latest version on [libTorrent](https://packages.gentoo.org/packages/net-libs/libtorrent) and [rTorrent](https://packages.gentoo.org/packages/net-p2p/rtorrent).
 * [Mandriva Linux](https://en.wikipedia.org/wiki/Mandriva_Linux) : the latest packages are available from the Cooker contribs.
 * [SUSE Linux](http://suse.com/) : latest packages available from Packman for [libTorrent](http://packman.links2linux.de/package/libtorrent) and [rTorrent](http://packman.links2linux.de/package/rtorrent).

 * [ArchLinux](https://www.archlinux.org/) : The latest packages are available by installing with `pacman -S rtorrent`
 * [Crux](https://crux.nu/) : in the [Crux Ports DB](https://crux.nu/portdb/?command=viewport&name=libtorrent&repo=contrib); see latest version on [libTorrent](https://crux.nu/gitweb/?p=ports/contrib.git;a=tree;f=libtorrent) and [rTorrent](https://crux.nu/gitweb/?p=ports/contrib.git;a=tree;f=rtorrent).
 * [Lunar-Linux](http://www.lunar-linux.org/) : in the moonbase; to install just `lin rtorrent`
 * [Sourcemage GNU/Linux](http://sourcemage.org/) : do a `cast rtorrent` or `cast libtorrent`

 * [FreeBSD](http://www.freebsd.org/) : in [FreshPorts](http://www.freshports.org/); see latest version on [libTorrent](http://www.freshports.org/net-p2p/libtorrent) and [rTorrent](http://www.freshports.org/net-p2p/rtorrent).
 * [NetBSD](http://www.netbsd.org/) : in [pkgsrc](http://www.pkgsrc.org/); `net/rtorrent`.
 * [OpenBSD](http://www.openbsd.org/) : in ports; [net/libtorrent](http://cvsweb.openbsd.org/cgi-bin/cvsweb/ports/net/libtorrent/) and [net/rtorrent](http://cvsweb.openbsd.org/cgi-bin/cvsweb/ports/net/rtorrent/) respectively.
 * [OpenDarwin](https://en.wikipedia.org/wiki/Darwin_%28operating_system%29#OpenDarwin) : in ports; `net/libtorrent` and `net/rtorrent` respectively.

Please report any package related problems to the package maintainers. Listing of a package here does not imply it has been tested or approved by the author.


## Disclaimer

This is not the same ``libtorrent`` project as the one used by *Deluge* and some other clients.
If you want to be precise and avoid confusion, refer to *this project's*
library as ``libtorrent-rakshasa``, and the other one's as ``libtorrent-rasterbar``.


## Stuff

Feel free to add content as I'm probably not going to write much ATM. Some kind of user guide would be really nice. By committing tickets, wiki changes, etc. you agree to license them under the GNU GPL. Remember to add a short comment describing the changes.

This project is developed by Jari Sundell, "Rakshasa", a former student of computer science, math and Japanese at the University of Oslo. He can be reached on [sundell.software@gmail.com](mailto:sundell.software@gmail.com), also an unofficial help channel may be found at `##rtorrent@irc.freenode.net` which should be used for user-support.

If you didn't get a reply to a mail sent to this address, it may either mean he is busy, has a rather full inbox or that you should have searched the internet first.