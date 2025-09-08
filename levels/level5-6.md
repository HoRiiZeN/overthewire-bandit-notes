# Level 5 → Level 6

**Goal:**  
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable

**Solution:**  
I tried this the `ls` command first, thinking i can find the file by only one criteria (size):
```
$ ls -lah maybehere*/* | grep 1.03K
```
But it returned nothing. Because the size column only shows two decimal places.

Then I tried to use `file` command to filter out human-readable files:
```
file ./maybehere*/* | grep text
```
This time many files appeared to have the word "text" in their description, yet couldn't distinguish which one is 1033 bytes and not executable.

So i ChatGPT'd my way out and asked for a command that can find a file with multiple criteria. It gave me the `find` command:
```
find . -type f -size 1033c ! -executable
```

Not very proud of giving up but at least I learned something new.
>HWasnPhtq9AVKe0dmk45nxy20cvUa6EG