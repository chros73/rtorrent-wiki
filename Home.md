# RTorrent and LibTorrent Wiki

[![Travis CI](https://api.travis-ci.org/rakshasa/rtorrent.png?branch=master)](https://travis-ci.org/rakshasa/rtorrent)
[![Download](http://img.shields.io/badge/download-v0.9.6-0000ff.svg)](https://github.com/rakshasa/rtorrent/wiki#download-links)

:busts_in_silhouette: :pencil: | This wiki is editable by any GitHub user, and thus the often-expressed wish for a complete and current manual depends on *YOU*. See [Mastering Wikis](https://guides.github.com/features/wikis/) and [Mastering Markdown](https://guides.github.com/features/mastering-markdown/), it's *NOT* :rocket: science. :wink: The [TODO](https://github.com/rakshasa/rtorrent/wiki/TODO) page has a list of pending work items.
---: | :---


rTorrent client uses ncurses and is ideal for use with [tmux](https://tmux.github.io/), [screen](http://www.gnu.org/software/screen/) or  [dtach](http://dtach.sourceforge.net/). It supports saving of sessions, allows the user to add and remove torrents and many more.


**Contents**

 * [User's Manual](#users-manual)
 * [Other Information](#other-information)
 * [Download Links](#download-links)
 * [Packages](#packages)
 * [Disclaimer](#disclaimer)
 * [Stuff](#stuff)


## User's Manual
 * the [User Guide](https://github.com/rakshasa/rtorrent/wiki/User-Guide) explains how to use the ‘curses’ UI, and what the displayed information actually means.
 * the [Configuration Guide](https://github.com/rakshasa/rtorrent/wiki/Config-Guide) helps you to adapt rTorrent to serve your needs.
 * the [Scripting Guide](https://github.com/rakshasa/rtorrent/wiki/Scripting-Guide) allows ‘power users’ to extend rTorrent's configuration with more complex logic, and control it remotely via XMLRPC.


## Other Information

 * List of [Known Issues](https://github.com/rakshasa/rtorrent/wiki/Issues)


## Download Links

**Stable Version**

 * http://rtorrent.net/downloads/libtorrent-0.13.6.tar.gz
 * http://rtorrent.net/downloads/rtorrent-0.9.6.tar.gz

**[All Versions](http://rtorrent.net/downloads/)**


## Packages

rTorrent and libTorrent packages are both available for the following Operating Systems and Distributions:

 * [Debian](https://www.debian.org/) : in Debian testing/unstable: `apt-get install rtorrent`.
 * [Fedora](https://fedoraproject.org/wiki/Fedora_Project_Wiki) : Run `yum install rtorrent` or `yum install libtorrent` to install (it's in Fedora Extra's)
 * [Gentoo](https://gentoo.org/) : in Portage; see latest version on [libTorrent](https://packages.gentoo.org/packages/net-libs/libtorrent) and [rTorrent](https://packages.gentoo.org/packages/net-p2p/rtorrent). 
 * [Mandriva Linux](https://en.wikipedia.org/wiki/Mandriva_Linux) : the latest packages are available from the Cooker contribs.
 * [SUSE Linux](http://suse.com/) : latest packages available from Packman for [libTorrent](http://packman.links2linux.de/package/libtorrent) and [rTorrent](http://packman.links2linux.de/package/rtorrent). 
 * [Ubuntu](http://www.ubuntu.com/) : in Ubuntu Dapper; see latest version on [libTorrent](http://packages.ubuntu.com/search?keywords=libtorrent19&searchon=names&suite=all&section=all) and [rTorrent](http://packages.ubuntu.com/search?keywords=rtorrent&searchon=names&suite=all&section=all)

 * [ArchLinux](https://www.archlinux.org/) : in the Arch User-community Repository; see latest version on  [libTorrent](https://www.archlinux.org/packages/?q=libtorrent) and [rTorrent](https://www.archlinux.org/packages/?sort=&q=rtorrent&maintainer=&flagged=).
 * [Crux](https://crux.nu/) : in the [Crux Ports DB](https://crux.nu/portdb/?command=viewport&name=libtorrent&repo=contrib); see latest version on [libTorrent](https://crux.nu/gitweb/?p=ports/contrib.git;a=tree;f=libtorrent) and [rTorrent](https://crux.nu/gitweb/?p=ports/contrib.git;a=tree;f=rtorrent).
 * [Lunar-Linux](http://www.lunar-linux.org/) : in the moonbase; to install just `lin rtorrent`
 * [Sourcemage GNU/Linux](http://sourcemage.org/) : do a `cast rtorrent` or `cast libtorrent`

 * [FreeBSD](http://www.freebsd.org/) : in [FreshPorts](http://www.freshports.org/); see latest version on [libTorrent](http://www.freshports.org/net-p2p/libtorrent) and [rTorrent](http://www.freshports.org/net-p2p/rtorrent).
 * [NetBSD](http://www.netbsd.org/) : in [pkgsrc](http://www.pkgsrc.org/); `net/rtorrent`.
 * [OpenBSD](http://www.openbsd.org/) : in ports; [net/libtorrent](http://cvsweb.openbsd.org/cgi-bin/cvsweb/ports/net/libtorrent/) and [net/rtorrent](http://cvsweb.openbsd.org/cgi-bin/cvsweb/ports/net/rtorrent/) respectively.
 * [OpenDarwin](https://en.wikipedia.org/wiki/Darwin_%28operating_system%29#OpenDarwin) : in ports; `net/libtorrent` and `net/rtorrent` respectively.

Please report any package related problems to the package maintainers. Listing of a package here does not imply it has been tested or approved by the author.


## Disclaimer

This is not the same "libtorrent" project as the one found on SourceForge.


## Stuff

Feel free to add content as I'm probably not going to write much ATM. Some kind of user guide would be really nice. By committing tickets, wiki changes, etc. you agree to license them under the GNU GPL. Remember to add a short comment describing the changes.

This project is developed by Jari Sundell, "Rakshasa", a student of computer science, math and japanese at the University of Oslo. He can be reached on [sundell.software@gmail.com](mailto:sundell.software@gmail.com), also an unofficial help channel may be found at `#rtorrent@irc.freenode.net` which should be used for user-support. If you didn't get a reply to a mail sent to this address, it may either mean he is busy or that you should have searched the issues.
