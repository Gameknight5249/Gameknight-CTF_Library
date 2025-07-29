
# Challenge Name: Big Zip

**Category:** General Skills

**Difficulty:** Easy

**Date Started:** July 16, 2025

**Date Completed:** July 16, 2025

**Writeup Published:** July 16, 2025

**Directions:** Unzip this archive and find the flag. Download [zip file](https://artifacts.picoctf.net/c/505/big-zip-files.zip)

 # Initial Observation:  
It looks like its a huge zip file, with a bunch of directoeries and subdirectories; it looks like I have to find the flag within all of those files using ["grep"](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/). I just have to research what grep does and how to use it.
 
 # Strategy (During the Challenge):
  1. Unzip the file
  2. Check whether looking through each directory and file is feasible.
  3. If it's not, research how to use grep to find the flag within the zip file. 

 # Tools Used:
- ChatGPT: To research what "grep" does. Also, to research all of the modifiers that come with the "grep" command

# Solution (What I Did During the Challenge): 
1. I unzipped the file
2. Found out that there were hundreds of files, thus I used ["grep -r"](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/) to search through every file for the phrase "picoCTF"
3. The command will find every phrase that has "picoCTF"; there is only one, and it is the flag

# Flag: 

- After using "grep -r" on all of the files, you find the flag easily

# Mistakes I made:

- I made a weird mistake/fluke. 
- Not all of the files were inflated on my browser webshell, thus I was missing files. 
- When I tried to use "grep -r" to find the flag, it did not work.
 
   
# What I Learned:

- Always check whether your files are completely unzipped; otherwise, you are missing files that may be important. 

