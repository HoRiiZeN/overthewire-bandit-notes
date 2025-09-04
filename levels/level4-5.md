# Level 4 → Level 5

**Goal:**  
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

**Solution:**  
I knew I had to use the `file` command but couldn’t figure out the right syntax, so I took a sneak peek at a GitHub repo with the solution. Made me feel kinda dumb for not knowing it T^T
```
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ file ./-file*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
```
>4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw