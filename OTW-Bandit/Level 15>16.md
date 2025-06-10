# Level 15 > 16

**Goal:**  
The password for the next level can be retrieved by submitting the password of the current level to port **30001** on **localhost** using **SSL/TLS encryption**.

---

### What I Did:

- Realized that unlike the previous level, this time the communication must be encrypted via **SSL**.
- Recalled from documentation that `openssl` provides tools for encrypted connections.
- Used the `openssl` command with `s_client` to initiate an SSL connection to port 30001 on localhost:

```bash
  openssl s_client -connect localhost:30001
```

Once the SSL connection was established, I entered the password for `bandit15` (from the previous level) and pressed Enter.

The server responded with the password for `bandit16`.

**Password Found:**  
`kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx`

![Bandit Level 15 to 16](images.png/bandit-level%2015%20>%2016.png)