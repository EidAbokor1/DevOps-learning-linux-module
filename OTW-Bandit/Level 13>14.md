# Level 13 > 14

**Goal:**  
The password for the next level is stored in `/etc/bandit_pass/bandit14` and can only be read by user **bandit14**.  
For this level, you don’t get the next password directly, but you receive a **private SSH key** that can be used to log into the next level.  
*Note:* `localhost` refers to the machine you are working on.

---

### What I Did:

- Listed the contents of the home directory:

```bash
  ls
```

Found the private key file:

```bash
  sshkey.private
```

Tried to change its permissions (this failed because I didn’t own the file):

```bash
chmod 600 sshkey.private  # Permission denied  
```

Created a temporary directory to work in:

```bash
mkdir /tmp/mydir
cd /tmp/mydir
```

Copied the key from the home directory into the working directory:

```bash
cp ~/sshkey.private .
```

Successfully changed the permission of the copied key file:

```bash
chmod 600 sshkey.private
```

Used the SSH key to log in as `bandit14` on port `2220`:

```bash
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```

Once logged in as `bandit14`, printed the password stored in the target file:

```bash
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```

**Password Found:**  
`MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS`

![Bandit Level 13 to 14](images.png/bandit-level%2013%20>%2014.png)