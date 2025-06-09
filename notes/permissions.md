# File Permissions and Ownership

## Understanding Permissions
- `ls -l` — View permissions in format: `rwxr-xr-x`
  - `r` = read, `w` = write, `x` = execute
  - Permissions for user, group, others

## Changing Permissions
- `chmod 755 filename` — Set permissions numerically
- `chmod u+x filename` — Add execute permission for user
- `chmod go-w filename` — Remove write permission for group and others

## Changing Ownership
- `chown user filename` — Change file owner
- `chgrp group filename` — Change group ownership
