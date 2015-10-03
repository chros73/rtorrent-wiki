`rtorrent` has issues with **ntfs** partitions.
It's reported that `rtorrent` freezes[1] when downloading on partition formatted with ntfs filesystem. 
Also, if the files are bigger than 4GB[2], data gets corrupted.


***

1. http://askubuntu.com/questions/399775/constant-freezes-when-downloading-torrent-to-ntfs-partition
2. https://bbs.archlinux.org/viewtopic.php?id=192811