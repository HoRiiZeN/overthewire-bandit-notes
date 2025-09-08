# Level 6 → Level 7

**Goal:**  
The password for the next level is stored somewhere on the server and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

**Solution:**  
Since this level was similar to the previous one, I used the `find` command again, but this time I made sure to search from the root directory `/` to ensure all files on the system are checked, not just those in the current directory:
```
find . -type f -user bandit7 -group bandit6 -size 33c
```
It probably printed the file I'm looking for, but the terminal was filled with permission denied messages. So I redirected the errors to `/dev/null` (this means any error messages, like "Permission denied", are sent to a special file called `/dev/null` and not shown in the terminal, which helps keep the output clean):
```
find . -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```
>morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj