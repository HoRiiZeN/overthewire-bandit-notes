# Level 1 → Level 2

**Goal:**  
Find the password that is stored in a file called `-` inside the home directory.

**Solution:**  
I tried using `cat -` but it didn't work, then I googled "dashed filename", read a brief Medium article and learned that I can use `cat ./-` to read the file, or alternatively `cat /home/bandit2/-`. Basically just find a workaround to access the file without triggering the -flag behavior.
>263JGJPfgU6LtdEvgfWU1XP5yac29mFx