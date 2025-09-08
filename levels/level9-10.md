# Level 9 → Level 10

**Goal:**  
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

**Solution:**  
Using grep itself didn't work because the file is mostly binary data. To extract human-readable strings from a binary file, I used the `strings` command and piped its output to `grep` to filter out the lines that contain '====':
```
strings data.txt | grep '===='
```

>FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey