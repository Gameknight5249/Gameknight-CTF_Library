# Challenge Name: First Find

**Category:** General Skills

**Difficulty:** Easy

**Date Started:** July 16, 2025

**Date Completed:** July 16, 2025

**Writeup Published:** July 16, 2025

**Directions:** Unzip this archive and find the file named 'uber-secret.txt'. [Download zip file](https://artifacts.picoctf.net/c/500/files.zip) 


 # Initial Observation: 
 It is a zipfile, I just have to open it and search for the "uber-secret.txt"; 

 "It's not that hard" - Gameknight5249 :)

 # Strategy (During the Challenge):
1. Unzip the file
2. Use [ls](https://phoenixnap.com/kb/ls-command) to look at all of the files in the directory
3. Hopefully, find the file I need somewhere within the directories. 

 # Tools Used:

I did not use any tools in this challenge; I already knew all of the commands needed to solve it. 

# Solution (What I Did During the Challenge: Less efficient): 
I followed the strategy I came up with: it was mostly correct
1. I first unzipped the file.
2. Then I used "ls" to look at all of the files and subdirectories.
3. I then went into the subdirectory: "adequate_books"
4. I went into the subdirectory: more_books
5. I then used ["ls -a"](https://phoenixnap.com/kb/ls-command) to look at all of the hidden files within this subdirectory and found: ".secret"
6. I kept using "ls -a" while I went deeper into the hidden subdirectories and eventually found the file "uber-secret.txt" 
7. Use ["cat"](https://www.linuxteck.com/basic-cat-command-in-linux-with-examples/) to open the file; Your flag will be in there

# Solution (Another way to solve it: More efficient) 

The more efficient and faster way:
1. Unzip the file
2. ["cd"](https://www.educative.io/answers/what-is-cd-in-linux) within the directory files
3. Use ["grep -r"](https://www.geeksforgeeks.org/linux-unix/grep-command-in-unixlinux/) to search for the phrase "picoCTF"
4. You will instantly find the flag

# Flag: 

The flag can be found in the hidden subdirectories OR by using "grep -r" 

# Mistakes I made:

I did not use ls -a to look for hidden files, thus I was confused for a while since I looked through all of the files and "uber-secret.txt" was not there

   
# What I Learned:
I learned to always look for hidden files
I also learned that if I ever have to look for information within a huge number of files, just use "grep -r" 
