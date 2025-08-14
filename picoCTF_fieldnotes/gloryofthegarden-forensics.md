# Challenge Name: Glory of the Garden

**Category:** Forensics

**Difficulty:** Easy

**Date Completed:**  July 26, 2025

**Writeup Published:**  July 29, 2025

**Directions:**  This [garden](https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg) contains more than it seems.

 # Initial Observation: 

1. It looks like I have to download the file and search for the flag within some information in it.
2. Based on the hints, I need to know what a ["hex editor"](https://www.ultraedit.com/blog/what-is-a-hex-editor-and-how-to-use-it/) is and how to open it; I have to research this.

 # Strategy (During the Challenge):
1. Download the file.
2. Research how to open and use a "hex editor."
3. Use the "hex editor" to find the flag.


 # Tools Used:

ChatGPT: I used it to research what a "hex editor" is and what Linux commands I can use to open it for a file

# Solution (What I Did During the Challenge): 
1. Download the file onto the picoCTF webshell browswer
2. Use the command ["xxd"](https://www.geeksforgeeks.org/linux-unix/xxd-command-in-linux/) on "garden.jpg"
3. Doing this, you will see the flag on the bottom right of the text
<img width="595" height="1234" alt="Screenshot 2025-07-26 211551" src="https://github.com/user-attachments/assets/9cbf8b24-22dd-48e2-86df-1bfbf008ebd6" />


# Flag: 

Using the command "xxd" on "garden.jpg," you will receive the flag

# Mistakes I made:

I didn't make any mistakes, the hints and directions made the challenge straightforward and simple; I just had to learn a couple of new commands to solve this challenge

# What I Learned:

I learned what a "hex editor" is
I learned a new linux command: "xxd"

