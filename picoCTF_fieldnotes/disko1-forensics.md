# Challenge Name: DISKO 1

**Category:** Forensics

**Difficulty:** Easy

**Date Completed:**  July 27, 2025

**Writeup Published:** July 29, 2025

**Directions:**  
Can you find the flag in this disk image? Download the disk image [here](https://artifacts.picoctf.net/c/538/disko-1.dd.gz).

 # Initial Observation: 
1. Looks like it's a "disk image".
2. I have to research commands and concepts related to ["disk images."](https://www.techtarget.com/whatis/definition/disk-image).
3. The hint also tells me that I will use ["strings"](https://labex.io/tutorials/linux-linux-strings-command-with-practical-examples-422934) to solve this challenge.

 # Strategy (During the Challenge):
1. Download the file.
2. Use ChatGPT to research commands and concepts related to "disk images."
3. Use "strings" to somehow obtain the flag.


 # Tools Used:

ChatGPT: I used it to research concepts and commands relating "disk images". I also used it to research ways to use "strings" and ["gunzip"](https://www.geeksforgeeks.org/linux-unix/gunzip-command-in-linux-with-examples/).

# Solution (What I Did During the Challenge): 
1. I downloaded the file.
2. I used "gunzip" to decompress the file.
3. I typed in the commands: "strings" and ["piped"](https://www.geeksforgeeks.org/linux-unix/piping-in-unix-or-linux/) it with "grep -i" to search the file for the flag.
4. Once I did that, I obtained the flag.

# Flag: 

Once you decompress the file, and "pipe" "strings" and ["grep -i"](https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix) together, you will obtain the flag. 

# Mistakes I made:

1. I did not research  how to unzip [".gz"](https://www.geeksforgeeks.org/techtips/gz-compressed-format/) files when I first saw the ["file extension"](https://www.techtarget.com/whatis/definition/file-format).
2. Used basic commands such as ["cat"](https://phoenixnap.com/kb/linux-cat-command) and ["nano"](https://www.geeksforgeeks.org/linux-unix/nano-text-editor-in-linux/) when I knew they would not help: I wasted time.

# What I Learned:
1. I solidified my knowledge of "pipes".
2. I learned crucial knowledge about how to use the command "strings".
3. I also learned about the command "gunzip".
