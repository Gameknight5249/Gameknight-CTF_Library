# Challenge Name: Commitment Issues 

**Category:** General Skills

**Difficulty:** Easy

**Date Started:** July 16, 2025

**Date Completed:** July 16, 2025

**Directions:** I accidentally wrote the flag down. Good thing I deleted it! You download the challenge files here: [challenge.zip](https://artifacts.picoctf.net/c_titan/75/challenge.zip)


 # Intial Observation: 
 The problem was going to be about binary operation: thus I needed to know how to add, substract, multiply, divide, right shift, and left shift binary numbers. 

 # Strategy:
 Open up the link in the browser webshell - see what operation it wanted me to do - open up an online binary calculator - plug in the numbers- plug in the answers into the browser webshell

 # Tools Used:
 Online Binary Operation Calculators: (https://www.calculator.net/binary-calculator.html)

 Binary to Hexademical Caluclator: (https://www.rapidtables.com/convert/number/binary-to-hex.html)

# Solution: 
1. It gave me 2 binary numbers. I told me to add them: Numbers: ( 00110001, 11000101)
2. The direction said do a left shift on Number 1:
3. Answer: 01100010
4. This repeats six times. Each with different operation relating the two numbers that were given.
5. Lastly it ask to convert a binary answer into hexadecimal number.

# Flag: 
After completing all of the binary operation questions; it will ask you to convert a binary answer to a hexadecimal number; after you enter the number, the flag will be given to you. 

# Mistakes I made:
1. I was doing the binary operations on paper which was slow and error-prone. but using an online calculator increased speed and accurarcy 
   
# What I Learned:
1. I learned that I don't need to reinvent the whell and that using calculators and other likewise tools are useful for solving CTF challenges
