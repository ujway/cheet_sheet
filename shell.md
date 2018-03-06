# Shell command cheetsheet

## Overview
Useful command for controll shell

## Command
- `ps aux | grep target_process | grep -v grep | awk '{print "kill -9", $2}' | sh`
  - kill all specific process.
- `echo 127:0:0:1 | awk -F'[:]' '{print $1}'` `#out> 127`
  - extracts 1st field of 127:0:0:1
  - `-F` is a delimiter.
- `pkill -f {process}`
  - kill process by process name.
- lsof -i:80 -P
  - Specify processes with a port.
- hoge=$(command) && ${hoge}
  - Execute a command with a previous stdout.
