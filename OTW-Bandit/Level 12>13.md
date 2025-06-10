# Level 12 > 13

**Goal:**  
The password for the next level is stored in the file `data.txt`, which is a **hexdump** of a file that has been **repeatedly compressed**.  
*Tip:* It may be useful to create a directory under `/tmp` in which you can work. Use `mkdir` with a hard-to-guess directory name, or better, use the command `mktemp -d`.

---

### What I Did:

- Created a safe temporary working directory using `mktemp`:

```bash
  mktemp -d
  cd /tmp/tmp.XXXXXXX
```

Copied `data.txt` to that directory:

```bash
cp ~/data.txt .
```

Converted the hexdump back into binary using `xxd -r`:

```bash
cxxd -r data.txt > layer1.bin
```

Analyzed the file type to determine the compression format:

```bash
file layer1.bin
```

Renamed the file with the correct extension based on the file output.
For example, if it was a gzip archive:

```bash
mv layer1.bin layer1.gz
```

Decompressed the file with the appropriate tool (repeated multiple times):

```bash
gunzip layer1.gz
bunzip2 layer2.bz2
tar -xf layer3.tar
```

After every decompression, I used:

```bash
file <filename>
```
to check the new file type and continued accordingly.

Repeated this process through multiple layers until I reached a readable file.

**Password Found:**  
`FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn`

![Bandit Level 12 to 13](images.png/bandit-level%2012%20>%2013.png)