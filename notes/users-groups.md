# User and Group Management

## User Commands
- `sudo useradd username` — Add a new user
- `sudo deluser username` — Remove a user
- `sudo passwd username` — Set or change user password

## Group Commands
- `sudo groupadd groupname` — Create a new group
- `sudo groupdel groupname` — Delete a group

## Adding User to Group
- `sudo usermod -aG groupname username` — Append user to a group
- `sudo gpasswd -a username groupname` — Alternative to add user to group
