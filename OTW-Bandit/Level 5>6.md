# Level 5 > 6

**Goal:**  
The password for the next level is stored in a file somewhere under the `inhere` directory and has all of the following properties:

- human-readable  
- 1033 bytes in size  
- not executable

---

### What I Did:

- I used the `find` command to search for files of exactly 1033 bytes:

```bash
  find -type f -size 1033c
```

This returned:

```bash
./maybehere07/.file2
```

I then listed the contents of the `maybehere07` directory:

```bash
ls maybehere07/
```

It showed several files, including hidden ones starting with a dot. I checked the permissions and size of `.file2` with:

```bash
ls -l maybehere07/.file2
```
The file was readable by me.

Finally, I read the file contents:

```bash
cat maybehere07/.file2
```
**Password Found:**  
`HWasnPhtq9AVKe0dmk45nxy20cvUa6EG`

![Bandit Level 5 to 6](images.png/bandit-level%205%20>%206.png)