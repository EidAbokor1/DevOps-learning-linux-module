## Level 2  
**Goal:** Find the password for the next level stored in a file called `spaces in this filename`.

**What I Did:**  
- I started by running `ls` to list the files in the home directory and saw a file named `spaces in this filename`.
- I knew that spaces in filenames can cause issues if not handled properly in the shell. If I tried something like:
```bash
  cat spaces in this filename
```  
To solve this, I used quotes to treat the entire filename as a single argument:

```bash
cat "spaces in this filename"
```
Alternatively, escaping the spaces with backslashes also works:

```bash
cat spaces\ in\ this\ filename
```
**Password Found:**  
`MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`

![Bandit Level 2 to 3](images.png/bandit-level%202%20>%203.png)