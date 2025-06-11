# "Saskatoon": Counting IPs - Solution

**Approach Taken**:

1. **Examined the log file**:

```bash
   cat /home/admin/access.log
```

2. **Extracted IP addresses (first column)**:

```bash
   awk '{print $1}' /home/admin/access.log
```

3. **Sorted IPs for counting**:

```bash
    awk '{print $1}' /home/admin/access.log | sort
```

4. **Counted unique IPs**:

```bash
    awk '{print $1}' /home/admin/access.log | sort | uniq -c
```

5. **Sorted by request count (descending)**:

```bash
    awk '{print $1}' /home/admin/access.log | sort | uniq -c | sort -nr
```

6. **Identified the top IP**:

```bash
    awk '{print $1}' /home/admin/access.log | sort | uniq -c | sort -nr | head -1
```

7. **Extracted just the IP address**:

```bash
    awk '{print $1}' /home/admin/access.log | sort | uniq -c | sort -nr | head -1 | awk '{print $2}'
```

8. **Saved the solution**:

```bash
    awk '{print $1}' /home/admin/access.log | sort | uniq -c | sort -nr | head -1 | awk '{print $2}' > /home/admin/highestip.txt
```

9. **Verified the solution**:

```bash
    sha1sum /home/admin/highestip.txt
```

![Sad Server-S2](images.png/Sad%20Server-S2.png)