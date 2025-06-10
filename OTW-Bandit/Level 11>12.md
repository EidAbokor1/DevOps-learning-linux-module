# Level 11 > 12

**Goal:**  
The password for the next level is stored in the file `data.txt`, where all lowercase (`a-z`) and uppercase (`A-Z`) letters have been rotated by 13 positions.

---

### What I Did:

- Listed files to find `data.txt`:

```bash
  ls
```

Checked the contents of the file:

```bash
  cat data.txt
```

The content was readable but looked like ROT13 encoded text.

I figured this out thanks to the OverTheWire helpful material, which mentioned encoding and hinted at ROT13. I researched it and found the ROT13 substitution table.

Used the `tr` command to decode ROT13 by translating letters:

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

**Password Found:**  
`7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4`

![Bandit Level 11 to 12](images.png/bandit-level%2011%20>%2012.png)