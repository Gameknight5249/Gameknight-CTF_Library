
# Challenge Name: PW Crack 1

**Category:** General Skills

**Difficulty:** Easy

**Date Completed:**  July 23, 2025

**Writeup Published:** July 25, 2025

**Directions:**  

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py), and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.

 # Initial Observation: 

Based on the hints, I need to view the code for the password checker. 
Maybe there is something within the code of the password checker that will allow me to obtain the flag.


 # Strategy (During the Challenge):
1. Download the password checker and the encrypted flag onto the same directory.
2. Open the ["source code"](https://www.techtarget.com/searchapparchitecture/definition/source-code) for the password checker.
3. Look for any clues that will help me obtain the flag. 

 # Tools Used:

I did not use any extra tools for this challenge. 

# Solution (What I Did During the Challenge): 

1. I made a directory using ["mkdir"](https://www.geeksforgeeks.org/linux-unix/mkdir-command-in-linux-with-examples/): this makes a directory. I called the directory "a"
2. I then downloaded the password checker and encrypted flag onto that directory
3. I then opened the "source code" of the password checker using ["nano"](https://linuxize.com/post/how-to-use-nano-text-editor/)
4. I noticed that the password was given within the "source code."
5. I then ran the password checker using "[python3](https://medium.themayor.tech/python3-command-and-control-how-to-guide-4fd4fe32ec71) <filename>."
6. I entered the password that I noticed within the "source code."
7. Doing that, the program gave me the flag for the challenge.
<img width="1885" height="442" alt="Screenshot 2025-07-23 115243" src="https://github.com/user-attachments/assets/898272a1-353a-4512-9bc7-6ea33a508495" />
<img width="814" height="540" alt="Screenshot 2025-07-23 115331" src="https://github.com/user-attachments/assets/fb9b9f88-bf9a-4930-94d5-305d40184470" />

# Flag: 

Once you have the password checker and the encrypted flag in the same directory, run the password checker, enter the password, and you will be able to obtain the flag.

# Mistakes I made:

I did not put the password checker and the encrypted flag into the same directory at first.

# What I Learned:

I learned that the "source code" most of the time has a lot of hints about the challenge.

I learned that you could leave "comments" in code for other non-developers to understand it.
