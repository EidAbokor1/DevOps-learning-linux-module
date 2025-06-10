# Level 9 > 10

**Goal:**  
The password for the next level is stored in the file `data.txt` in one of the few human-readable strings, preceded by several `=` characters.

---

### What I Did:

- Ran `ls` to see the file:

```bash
  ls
```
Used `cat` to view contents, but it looked like binary or non-readable content:

```bash
  cat data.txt
```

Recalled the hint: look for strings preceded by multiple `=` characters.

Regular `grep` failed due to non-text characters, so I used `-a` to treat the binary file as text:

```bash
  cat data.txt | grep -a '===='
```
Found the password in this output:

**Password Found:**  
`FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey`

![Bandit Level 9 to 10](images.png/bandit-level%209%20>%2010.png)