# Level 7 > 8

**Goal:**  
The password for the next level is stored in the file `data.txt` next to the word **millionth**.

---

### What I Did:

- I first ran `ls` to confirm the presence of `data.txt`.
- Then I used `cat data.txt` to look at the file contents — it was a large file with many word-password pairs.
- To find the password next to the word "millionth", I used:

```bash
  cat data.txt | grep millionth
```

This gave me the line:

```bash
    millionth	dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
**Password Found:**  
`dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc`

![Bandit Level 7 to 8](images.png/bandit-level%207%20>%208.png)
