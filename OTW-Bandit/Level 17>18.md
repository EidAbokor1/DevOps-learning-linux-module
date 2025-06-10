# Level 17 > 18

**Goal:**  
There are 2 files in the home directory: `passwords.old` and `passwords.new`.  
The password for the next level is in `passwords.new` and is the only line that has been changed between `passwords.old` and `passwords.new`.

---

### What I Did:

- Listed the files in the home directory.
- Checked the contents of both files to understand the format:

```bash
  cat passwords.new
  cat passwords.old
```

Looked up the manual for `diff` to learn how to compare files:

```bash
man diff
```

Used the `diff` command to identify the line that changed:

```bash
diff passwords.old passwords.new
```

The output showed that only line 42 was different, and the new value from `passwords.new` was:

**Password Found:**  
`x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO`

![Bandit Level 17 to 18](images.png/bandit-level%2017%20>%2018.png)