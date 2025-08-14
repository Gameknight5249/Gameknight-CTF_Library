# Challenge Name: plumbing

**Category:** General Skills

**Difficulty:** Medium

**Date Started:** July 17, 2025

**Date Completed:** July 17, 2025

**Writeup Published:** July 17, 2025

**Directions:** 
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to jupiter.challenges.picoctf.org 7480.

 # Initial Observation: 
 I don't know anything about ["pipes"](https://www.linfo.org/pipes.html), thus I have to research that;
 I have to be able to get an output from outside the file, maybe "pipe" will allow me to do that? 

 # Strategy (During the Challenge):
1. Research what "pipe" is.
2. Connect to the challenge using ["nc"](https://phoenixnap.com/kb/nc-command)
3. Try to use "pipe" somehow to obtain the flag

 # Tools Used:
I did not use any extra tools 

# Solution (What I Did During the Challenge): 
1. Connect to the challenge using "nc"
2. Use the concept of "pipes" to use " grep" to search for the flag
<img width="977" height="529" alt="Screenshot 2025-07-17 170639" src="https://github.com/user-attachments/assets/f1d8d5b3-0d01-44fc-9e77-f749267666ed" />


3. "Pipes" basically means you take the output of one command, and that output turns into the input for another command
4. In this situation, I am connecting to the challenge and searching for "picCTF" within the file, which I am not able to do when I first join the challenge.

# Flag: 

After using the concept of "pipes" and "grep" you will be able to obtain the flag.

# Mistakes I made:
When I first tried to solve the challenge, I did not fully understand what "pipes" were, and I just rushed into the challenge
I did not understand how to join the challenge at first.

# What I Learned:
I learned that I should always try to understand the concepts first because it makes it easier to apply them in the challenge or real life.

I learned how to join challenges using "nc".

I learned how to chain commands using the concept of "pipes" or otherwise represented with the symbol "|".
