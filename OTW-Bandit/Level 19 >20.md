# Level 19 > 20

**Goal:**  
To gain access to the next level, you should use the setuid binary in the home directory.  
Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (`/etc/bandit_pass`), after you have used the setuid binary.

---

### What I Did:

- First, checked the contents of the home directory:

```bash
  ls -l
```

Saw a setuid binary named `bandit20-do`:

```bash
  -rwsr-x--- 1 bandit20 bandit19 7408 May  7  2020 bandit20-do
```

Ran it without any arguments to see how it works:

```bash
  ./bandit20-do
```

It returned usage information:

```bash
  Run a command as another user.
  Usage: ./bandit20-do <command>
```

Used it to run the `cat` command as bandit20 to read their password file:

```bash
  ./bandit20-do cat /etc/bandit_pass/bandit20
```

This worked and printed the next level’s password.

**Password Found:**  
`cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8`

![Bandit Level 19 to 20](images.png/bandit-level%2019%20>%2020.png)