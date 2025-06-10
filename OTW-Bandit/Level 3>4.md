# Level 3 > 4

**Goal:**  
The password for the next level is stored in a hidden file in the `inhere` directory.

---

### What I Did:

- I ran `ls` in the home directory and found a subdirectory named `inhere`.

```bash
  ls
  cd inhere/
```
Running a normal ls showed no visible files, so I used the -a flag to reveal hidden files:

```bash
ls -a
```
his revealed a hidden file named `...Hiding-From-You`.

To read the file, I used:

```bash
cat ...Hiding-From-You
```

Even though the filename starts with dots (which usually hide files), no special escaping was needed since it didn’t contain spaces or special characters that the shell misinterprets.

**Password Found:**  
`2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`

![Bandit Level 3 to 4](images.png/bandit-level%203%20>%204.png)