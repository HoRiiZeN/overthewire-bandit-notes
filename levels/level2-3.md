# Level 2 → Level 3

**Goal:**  
The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory.

**Solution:**  
The file name had spaces in it so `cat ./--spaces in this filename--` did not work. I had to use `cat ./"--spaces in this filename--"` instead. Found out later that I could put `\` before the spaces to escape them, like this: `cat ./--spaces\ in\ this\ filename--`. but I prefer the quotes method as it's easier.
>MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx