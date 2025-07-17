# Challenge Name: Serpentine

**Category:** General Skills

**Difficulty:** Medium

**Date Started:** July 17, 2025

**Date Completed:** July 17, 2025

**Writeup Published:** July 17, 2025

**Directions:** Find the flag in the Python script! [Download Python script](https://artifacts.picoctf.net/c/36/serpentine.py) 


 # Initial Observation: 
 Looks like it's a Python script.
 Something is probably wrong with the [source code](https://en.wikipedia.org/wiki/Source_code), and I have to fix it to obtain the flag
 I don't know anything about [Python](https://www.python.org/doc/essays/blurb/), so I probably have to research what its keywords are and how to use them.

 # Strategy (During the Challenge):
1. Download the Python script in the browser webshell
2. Open the script using ["nano"](https://linuxize.com/post/how-to-use-nano-text-editor/)
3. Research the keywords of Python so I know what the script is about and how to change it so that I can obtain the flag.

 # Tools Used:

ChatGPT: To research several keywords in Python and understand how to use them.

# Solution (What I Did During the Challenge):
1. Download the file
2. Use "python3" to run serpentine.py
3. Read the hint that it gives you when you try to print the flag.
4. Use "nano" to open up serpentine.py
5. Edit the source code so that instead of printing the hint, it prints the flag instead.
6. This is what it looks like unedited:
<img width="780" height="482" alt="Screenshot 2025-07-17 132626" src="https://github.com/user-attachments/assets/e674f959-5161-42d4-91fc-1b818fb5f5c7" />


7. This is what it looks like when you edit the source code and you reuse the print_flag() code 
<img width="743" height="407" alt="Screenshot 2025-07-17 132131" src="https://github.com/user-attachments/assets/a18b8f56-635d-4555-bdd8-0349612227ca" />




# Flag: 

Once you edit the source code, run the script again
Now, if you try to print the flag, it will print the flag

# Mistakes I made:

I spent a lot of time trying to understand the code when I hadn't researched the keywords in Python yet.
   
# What I Learned:

I learned that researching is the best tool I have
I also learned new keywords in Python:

["def"](https://www.w3schools.com/python/python_ref_keywords.asp): All of the keywords are in this link
"while"
"return"
"for"
"in"
"elif"
'else"


