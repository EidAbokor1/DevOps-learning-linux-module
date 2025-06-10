# Level 16 > 17

**Goal:**  
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range **31000 to 32000**.  
First, find out which of these ports have a server listening on them. Then determine which of those use **SSL/TLS**.  
There is only one server that will return the next credentials — others just echo your input.

---

### What I Did:

- Realized that unlike previous levels, this task required scanning for open ports in a specific range and detecting SSL/TLS services.
- Used `nmap` to scan for open ports on localhost in the 31000–32000 range:

```bash
  nmap -p 31000-32000 localhost
```
Identified which ports were open and accepting connections.

Used `openssl s_client` to test each open port for SSL/TLS support:

```bash
  openssl s_client -connect localhost:<port>
```

Found that port 31790 accepted an SSL connection and responded differently.

Connected to port 31790, submitted the current level’s password, and pressed Enter.

The server responded with an RSA private key.

Saved the key into a file:

```bash
    echo "<private key contents>" > bandit17_key.pem
    chmod 600 bandit17_key.pem
```

Used the key to SSH into the next level:

```bash
    ssh -i bandit17_key.pem bandit17@bandit.labs.overthewire.org -p 2220
```
Logged in successfully and obtained the password for the next level.

![Bandit Level 16 to 17](images.png/bandit-level%2016%20>%2017.png)