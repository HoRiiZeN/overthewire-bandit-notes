# Level 7 → Level 8

**Goal:**  
The password for the next level is stored in the file data.txt next to the word millionth  

**Solution:**  
I kept overthinking for quite some time. But it was actually simple. Just use `grep` to find the word "millionth" in the file `data.txt`:
```
grep millionth data.txt
```
alternatively, I achieved the same result using `cat` and piping it to `grep`, but imo `grep` alone is more efficient:
```
cat data.txt | grep millionth
```

>dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc