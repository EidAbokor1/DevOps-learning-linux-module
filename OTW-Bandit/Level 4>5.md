# Level 4 > 5

**Goal:**  
The password for the next level is stored in the only human-readable file in the `inhere` directory.  
*Tip: if your terminal is messed up, try the `reset` command.*

---

### What I Did:

- I ran:

```bash
  cd inhere/
  ls
```
This showed 10 files named `-file00` through `-file09`.

I remembered from Level 1 > 2 that filenames starting with `-` can confuse commands by being interpreted as options. So when I used the `file` command to inspect their types, I made sure to prefix them with `./`:

```bash
file ./*
```

That worked perfectly! Among the output, I saw:

```bash
./-file07: ASCII text
```

This told me that `-file07` is the only file containing readable text.

Again, recalling Level 1 > 2, I used `./-file07` to safely `cat` the contents:

```bash
cat ./-file07
```
**Password Found:**  
`4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`

![Bandit Level 4 to 5](images.png/bandit-level%204%20>%205.png)