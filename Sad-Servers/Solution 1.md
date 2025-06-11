# Solution: Stopping the Process Writing to `/var/log/bad.log`

## Problem
A background process was continuously writing to `/var/log/bad.log`, filling disk space. The task was to:
- Identify the process
- Terminate it 
- Avoid deleting the log file

## Steps Taken

### 1. Checked running processes

```bash
ps auxf
```

No obvious culprit found

### 2. Attempted to check open files

```bash
lsof /var/log/bad.log
```

Command hung - likely due to high I/O

### 3. Monitored the log file

```bash
tail -f /var/log/bad.log
```

Confirmed file was being actively written

### 4. Used fuser to identify process

```bash
fuser -v /var/log/bad.log
```

Output showed PID 7 had the file open

### 5. Terminated the process

```bash
kill -9 7
```

### 6. Verified solution
```bash
tail -f /var/log/bad.log
```

![Sad Server-S1](images.png/Sad%20Server-S1.png)