# Level 10 > 11

**Goal:**  
The password for the next level is stored in the file `data.txt`, which contains **base64 encoded** data.

---

### What I Did:

- Ran `ls` to confirm the file was there:

```bash
  ls
```

Used `cat` to look at the file contents:

```bash
cat data.txt
```

Noticed the content looked like random letters — a common sign of base64 encoding.

Tried to decode using `base64`:

```bash
cat data.txt | base64 -d
```

**Password Found:**  
`dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr`

![Bandit Level 10 to 11](images.png/bandit-level%2010%20>%2011.png)