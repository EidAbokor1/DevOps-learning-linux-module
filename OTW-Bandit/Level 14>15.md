# Level 14 > 15

**Goal:**  
The password for the next level can be retrieved by submitting the password of the current level to port **30000** on **localhost**.

---

### What I Did:

- Understood that I needed to use the password for `bandit14`, which I obtained in the previous level.
- Recognized that I had to send this password to a port on localhost — a job for `nc` (netcat).
- Read the manual page for `nc` using:

```bash
  man nc
```

This helped me understand how `nc` can be used to connect to a specific port and send data.

Used the following command to send the password to port 30000:

```bash
  nc localhost 30000
```

When prompted (or immediately, depending on system configuration), I entered/pasted the password for `bandit14` and hit Enter.

The service responded with the password for `bandit15`

**Password Found:**  
`8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo`

![Bandit Level 14 to 15](images.png/bandit-level%2014%20>%2015.png)
