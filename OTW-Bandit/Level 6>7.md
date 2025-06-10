# Level 6 > 7

**Goal:**  
The password for the next level is stored somewhere on the server and has all of the following properties:

- owned by user `bandit7`  
- owned by group `bandit6`  
- 33 bytes in size

---

### What I Did:

- At first, I ran:

```bash
  find / -type f -size 33c -user bandit7 -group bandit6
```
This worked but showed a lot of Permission denied messages.

To make the output cleaner, I redirected errors to `/dev/null`:

```bash
find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
```

That gave me the correct file:

```bash
/var/lib/dpkg/info/bandit7.password
```

Then I used cat to read its contents:

```bash
cat /var/lib/dpkg/info/bandit7.password
```

**Password Found:**  
`morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj`

![Bandit Level 6 to 7](images.png/bandit-level%206%20>%207.png)