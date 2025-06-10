# Level 18 > 19

**Goal:**  
The password for the next level is stored in a file `readme` in the home directory.  
Unfortunately, someone has modified `.bashrc` to log you out immediately when you log in via SSH.

---

### What I Did:

- Initially tried to log in normally using:

```bash
  ssh -l bandit18 192.168.64.9/24@bandit.labs.overthewire.org -p 2220
```

This failed due to incorrect syntax or because `.bashrc` automatically logged me out.

Then realized I could bypass the interactive login shell (and thus avoid triggering `.bashrc`) by running the desired command directly during the SSH session:

```bash
  ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat readme"
```

Because this was a non-interactive SSH command, .bashrc didn’t get a chance to log me out before cat `readme` executed.

**Password Found:**  
`cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8`

![Bandit Level 18 to 19](images.png/bandit-level%2018%20>%2019.png)