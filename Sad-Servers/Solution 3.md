# "The Command Line Murders" - Solution

## Investigation Process

**Commands Executed**:
```bash
1. Examined the mystery directory:
   ls
   cd clmystery/

2. Reviewed README and hints:
   vim README.md
   cat ../hint1
   cat ../hint2
   cat ../hint3
   cat ../hint4
   cat ../hint5
   cat ../hint6
   cat ../hint7
   cat ../hint8

3. Analyzed crime scene data:
   grep CLUE crimescene
   head -n 20 people
   head -n 20 vehicles
   grep Annabel people

4. Followed specific leads:
   head -n 173 streets/Mattapan_Street | tail -n 1
   grep "Honda" vehicles
   grep -A 5 "L337" mystery/vehicles

5. Verified the solution:
   echo "Joe Germuska" > ~/mysolution
   md5sum mysolution
```

### Key Findings

### Initial Clues
- Located in `crimescene` file  
- Witness interview mentioned license plate starting with `"L337"`  

### Vehicle Analysis
- Identified Honda vehicles with suspicious plates
- Cross-referenced with owner information

### Person Identification
- Found matching characteristics in people file
- Verified address information from streets data

### Final Answer

```bash
    echo "Joe Germuska" > ~/mysolution
```

### Verification

```bash
md5sum mysolution
# Output: 9bba101c7369f49ca890ea96aa242dd5
```

![Sad Server-S2](images.png/Sad%20Server-S3.png)