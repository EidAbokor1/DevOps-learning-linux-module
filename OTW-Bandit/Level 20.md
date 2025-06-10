# Level 20

**Goal:**  
There is a setuid binary in the home directory that does the following: it makes a connection to localhost on the port you specify as a command line argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

---

### What I Did:

- Listed the files to identify the setuid binary:

```bash
  ls -l
```

Found the binary `suconnect` with the setuid bit set.

Started a listener on port 10000 using `nc` (netcat):

```bash
  nc -l -p 10000
```

In another SSH session (or after backgrounding `nc`), ran the binary and passed the same port:

```bash
  ./suconnect 10000
```

Back in the `nc` listener, I saw an incoming connection. When prompted, I pasted the password for bandit20:

```bash
  0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```

After submitting the correct password, the listener outputted the next password, which was sent by the `suconnect` binary.

**Password Found:**  
`EeoULMCra2q0dSkYj561DX7s1CpBuOBt`

![Bandit Level 20](images.png/bandit-level%2020.png)