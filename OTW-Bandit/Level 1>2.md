# Level 1 > 2

**Goal:**  
The password for the next level is stored in a file called `-` located in the home directory.

---

### What I Did:

- I first ran `ls` to see the files in the home directory and found a file named `-`.
- Initially, I tried reading it using `cat -`, but I realized this didn’t work as expected because `-` is interpreted as stdin (standard input).
- I checked the `man cat` page and learned that using `-` tells `cat` to read from standard input, not from a file literally named `-`.
- To read the file named `-`, I used `./-`, which treats it as a file in the current directory and avoids confusion with stdin.

**Password Found:**  
`263JGJPfgU6LtdEvgfWU1XP5yac29mFx`

![Bandit Level 1 to 2](images.png/bandit-level%201%20>%202.png)