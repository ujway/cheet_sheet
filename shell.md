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
- `lsof -i:80 -P`
  - Specify processes with a port.
- `hoge=$(command) && ${hoge}`
  - Execute a command with a previous stdout.
- `mysql -h {host_name} -u {user_name} -D {db_name} -p`
  - connect to mysql.
  - `-p` requires a password.
- `psql -h {host_name} -U {user_name} -d {db_name}`
  - connect to postgresql.
- `echo hoge | sudo tee rootfile`
  - prevent from access denieal to use this instead of `sudo hoge >> rootfile`
- `ssh-keygen -R {host_name}`
  - reset finger print.
- `{command} > {file_name} 2>&1`
  - write standard output/error of a result to {file_name}.
- `sed -i {""} -e "2s/^/hoge/g" {file_name}`
  - insert hoge to 2L in {file_name}
  - `""` after -i is required for Mac(BSD).
- `git branch --merged | grep -vE '^\*|develop$|master$' | xargs -I % git branch -d %`
  - delete merged branches except from develop and master branch
