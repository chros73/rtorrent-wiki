**TODO** Explain variants (bg, capture, no_throw, …)

## Syntax

```
execute={command,arg1,arg2,...}
```
This will execute the external command with arguments arg1,arg2,.... It will throw an error if the exit status is not 0, and return 0 itself otherwise. 

```
execute.nothrow={command,arg1,arg2,...}
```
This will execute the external command with arguments arg1,arg2,.... It will return the return value of the command. 

```
execute.capture={command,arg1,arg2,...}
```
This will execute the external command with arguments arg1,arg2,.... It will throw an error if the exit status is not 0, and return the stdout output of the command otherwise. 

```
execute.capture_nothrow={command,arg1,arg2,...}
```
This will execute the external command with arguments arg1,arg2,.... It will return the stdout output of the command.

## Small Tricks

### Get rtorrent to create a pid-file
```
# Creates a pid-file and writes it to /run/user/{user id}/rtorrent.pid
execute = {bash,-c,echo `ps -p "$\{1:-$$\}" -o ppid=` > /run/user/`id -u`/rtorrent.pid}
```