# Challenge Name: PW Crack 2

**Category:** General Skills

**Difficulty:** Easy

**Date Completed:**  July 30, 2025

**Writeup Published:** August 1, 2025

**Directions:**  

Can you crack the password to get the flag?
Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.

 # Initial Observation: 
- It looks just like the PW Crack 1; I don't think finding the flag will be the same, though.
- The hints make it clear that the ["encoding"](https://www.techtarget.com/searchnetworking/definition/encoding-and-decoding) is important
- The password checker and encrypted flag have to be in the same directory - that's easy to do.

 # Strategy (During the Challenge):
1. Download the password checker and the encrypted flag into the same directory.
2. Check the "encoding" of the encrypted flag.
3. Hopefully, find a clue that will allow me to obtain the flag.


 # Tools Used:

ChatGPT: To quickly convert a ["Unicode code point"](https://pro.arcgis.com/en/pro-app/latest/help/data/geodatabases/overview/a-quick-tour-of-unicode.htm#:~:text=In%20Unicode%2C%20a%20character%20maps,four%20numbers%20and/or%20letters.) to the corresponding characters

# Solution (What I Did During the Challenge): 
1. Download both the password checker and the encrypted file.
2. Check the ["source code"](https://www.techtarget.com/searchapparchitecture/definition/source-code) of the password checker.
3. You will notice that the password is written in ["character function"](https://www.geeksforgeeks.org/python/chr-in-python/).
 <img width="952" height="1083" alt="Screenshot 2025-07-30 223929" src="https://github.com/user-attachments/assets/1c3e7628-01ba-4517-837a-663dae1cf23f" />

4. I used ChatGPT to quickly convert "character function" to its corresponding characters.
5. Then, I ran the password checker using ["python3"](https://cs.stanford.edu/people/nick/py/python-command.html#:~:text=The%20first%20word%20%22python3%22%20means,any%20output%20to%20the%20terminal.) and entered the password that I got from ChatGPT.
6. Doing that allowed me to obtain the flag. 

# Flag: 

- After converting the  "character function" to its corresponding characters, entering the password into the password checker, you will be able to obtain the flag.

# Mistakes I made:

- I spent a lot of time trying to figure out what the encoding was in the encrypted flag file: turned out it was random text.
- I was overly focused on the encrypted flag file, because the flag was there in the PW Crack 1.

# What I Learned:

- I learned about "character function".
- I learned how to leverage AI to help me complete picoCTF challenges.
- I learned how to view "source code" and gain insights from it. 
