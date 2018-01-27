# Shell command cheetsheet

## Overview
Useful command for controll shell

## Command
- ps aux | grep target_process | grep -v grep | awk '{print "kill -9", $2}' | sh
