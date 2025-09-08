# Level 8 → Level 9

**Goal:**  
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

**Solution:**  
I used the command `uniq -u` to find the unique line in the file data.txt, but here is the catch: the file needs to be sorted first before using uniq, otherwise it won't work. So I piped the output of sort to uniq -u:
```
sort data.txt | uniq -u
```
>4CKMh1JI91bUIZZPXDqGanal4xvAg0JM