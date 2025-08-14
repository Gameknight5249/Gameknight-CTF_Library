# Challenge Name: Tab, Tab, Attack

**Category:** General Skills

**Difficulty:** Easy

**Date Started:** July 16, 2025

**Date Completed:** July 16, 2025

**Writeup Published:** July 17, 2025

**Directions:** 
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/9689f2b453ad5daeb73ca7534e4d1521/Addadshashanammu.zip)

 # Initial Observation: 
It looks like a zip file that's gonna have a lot of directories, subdirectories, and files

 # Strategy (During the Challenge):
1. Unzip the file
2. Check out all of the different files and directories
3. Use ["grep -r"](https://www.geeksforgeeks.org/linux-unix/grep-command-in-unixlinux/) to see which folder or file the flag is hidden in

 # Tools Used:
I did not use any extra tools for this challenge.

# Solution (What I Did During the Challenge): 
My strategy was almost correct:
1. I unzipped the file
2. I checked out all of the files in the zip ( there was only one)
3. I used "grep -r" to search for the flag within the subdirectories.
4. Binary match comes up deep within the subdirectories, thus I had to navigate through all of the subdirectories to get to the binary file
5. I used ["cat"](https://www.linuxteck.com/basic-cat-command-in-linux-with-examples/) to open the binary file, and then you will see your flag
6. (The flag blends in with all of the text, so make sure to search properly.)

# Flag: 

The flag is deep within the subdirectories; within a binary file; use "cat" to open that binary file


# Mistakes I made:

I didn't search for the flag properly within the files; I just kept skimming the text and kept missing the flag.

# What I Learned:

I learned that "grep -r" cannot search through binary files
I learned that I could copy and paste text from a file, such as the binary file in this challenge, and paste it into Google Docs to search for the flag using "Ctrl f". 
