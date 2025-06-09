# Linux Commands Reference

A list of essential Linux commands practiced during the Linux module.

## File and Directory Commands
- `pwd` — Print current working directory
- `ls` — List files and folders
- `cd <dir>` — Change directory
- `mkdir <folder>` — Create directory
- `rmdir <folder>` — Remove empty directory
- `rm <file>` — Remove file
- `rm -r <folder>` — Remove folder recursively
- `touch <file>` — Create or update a file
- `cp <src> <dest>` — Copy files or folders
- `mv <old> <new>` — Move or rename files or folders

## Viewing File Contents
- `cat <file>` — Show file contents
- `head <file>` — View first 10 lines
- `tail <file>` — View last 10 lines
- `less <file>` — Scroll through file contents interactively
- `more <file>` — Similar to `less`

## Permissions and Ownership
- `chmod` — Change permissions
- `chown` — Change file owner
- `chgrp` — Change group owner

## Users and Groups
- `useradd <username>` — Add new user
- `deluser <username>` — Delete user
- `passwd <username>` — Change user password
- `usermod -aG <group> <user>` — Add user to group
- `groupadd <group>` — Create new group

## Processes
- `ps aux` — List running processes
- `top` — Interactive process viewer
- `kill <PID>` — Kill process by PID
- `killall <process_name>` — Kill all processes by name

## Networking
- `ssh -i <key.pem> user@ip` — Connect to remote server via SSH
- `ping <host>` — Check network connectivity
- `ifconfig` or `ip addr` — Show network interfaces

## Shell & Environment
- `echo` — Print text or variables
- `env` — Show environment variables
- `export` — Set environment variables

## Input/Output Redirection
- `>` — Redirect output to file (overwrite)
- `>>` — Append output to file
- `<` — Use file as input
- `|` — Pipe output to another command
