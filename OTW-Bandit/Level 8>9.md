# Level 8 > 9

**Goal:**  
The password for the next level is stored in the file `data.txt` and is the only line of text that occurs **only once**.

---

### What I Did:

- Checked the available commands on the Bandit site. It suggested tools like `grep`, `sort`, `uniq`, and others.
- Since the file had many repeated lines, I thought `uniq` would help.
- Learned from `man sort` and `man uniq` that `uniq -u` prints unique lines but requires **sorted input**.
- Ran:

```bash
  sort data.txt | uniq -u
```
**Password Found:**  
`4CKMh1JI91bUIZZPXDqGanal4xvAg0JM`

![Bandit Level 8 to 9](images.png/bandit-level%208%20>%209.png)