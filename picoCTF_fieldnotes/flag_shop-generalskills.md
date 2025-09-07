# Challenge Name: flag_shop

**Category:** General Skills

**Difficulty:** Medium

**Date Started:** July 17, 2025

**Date Completed:** July 17, 2025

**Writeup Published:** July 18, 2025

**Directions:** There's a flag shop selling stuff, can you buy a flag? [Source](https://jupiter.challenges.picoctf.org/static/64e724ad327f83ad833d9c6baa072b1f/store.c). Connect with nc jupiter.challenges.picoctf.org 4906.

 # Initial Observation: 
Looks like there is a source code. Maybe I have to edit it to obtain the flag. 
What is ["two's compliment"](https://www.cs.cornell.edu/~tomf/notes/cps104/twoscomp.html)? It is one of the hints, so I am going to research it.

 # Strategy (During the Challenge):
 Play around with the "flag_shop" game
 Research what "two's compliment" is
 Check the Source code; see if I can edit anything that will help me obtain the flag

 # Tools Used:

ChatGPT ( Used heavily to research concepts, commands, and keywords)
       - I used it to research "two compliment"  

# Solution (What I Did During the Challenge): 
 - After 2 hours of research, I found an extremely simple answer
1. Start playing the game
2. Type 2 to buy the flag
3. Type 1 to buy "Definitely not the flag Flag"
4. Buy this number of flags: 100000000000000000    - 17 zeros
5. Your account balance will go up
6. Now, try to buy the "1337 Flag"
7. This will give you the flag
<img width="674" height="719" alt="Screenshot 2025-07-18 111616" src="https://github.com/user-attachments/assets/4fdfc7db-c9a6-499a-a7cc-a73e294576fe" />



# Flag: 

After you increase your account balance, you can buy the flag.

# Mistakes I made:
- Lots of mistakes, but it helped fuel growth
1. I spent a lot of time trying to edit the source code to give me the flag since I did that for a previous challenge.
2. When the game told me "flag not found on this server" I ignored it. ( It was a crucial hint I ignored)
3. I tried to edit the account balance in the source code.
4. I did not spend much time researching how inputs are handled 
   
# What I Learned:
Learned a lot from this challenge:
1. I learned how ["integer overflow"](https://www.acunetix.com/blog/web-security-zone/what-is-integer-overflow/) works and how only specific numbers work to increase the account balance.
2. I learned that there is a "picoCTF" server somewhere and that all files needed for a challenge won't be in the download link or the ["netcat link."](https://phoenixnap.com/kb/nc-command)
3. I learned that CTFs are about exploiting logic flaws, not editing code to obtain a flag
4. I learned about ["signed and unsigned integers"](https://www.geeksforgeeks.org/c/difference-between-unsigned-int-and-signed-int-in-c/)
5. I learned about ["edge cases"](https://en.wikipedia.org/wiki/Edge_case) -
6. I learned how to understand the logic in the complex source code
7. I learned a lot of keywords in "C"
   - [#include <stdio.h>](https://www.scaler.com/topics/stdio-h-in-c/)
   - [int main()](https://www.geeksforgeeks.org/c/main-function-in-c/)
   - [Curly braces {}](https://stackoverflow.com/questions/1677778/why-enclose-blocks-of-c-code-in-curly-braces)
   - [printf()](https://www.geeksforgeeks.org/c/printf-in-c/)
   - [scanf()](https://www.geeksforgeeks.org/c/scanf-in-c/)
   - [fflush(stdin)](https://www.geeksforgeeks.org/c/use-fflushstdin-c/)
   - [while](https://www.w3schools.com/c/c_while_loop.php)
   - [if](https://www.w3schools.com/c/c_conditions.php)
   - [else if](https://www.w3schools.com/c/c_conditions.php)
   - [int](https://www.geeksforgeeks.org/c/int-1-sign-bit-31-data-bits-keyword-in-c/)
