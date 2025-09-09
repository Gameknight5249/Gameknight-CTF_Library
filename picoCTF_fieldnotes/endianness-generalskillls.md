# Challenge Name: endianness

**Category:** General Skills

**Difficulty:** Easy

**Date Started:** July 17, 2025

**Date Completed:** July 17, 2025

**Writeup Published:** July 17, 2025

**Directions:** Know of little and big endian? [Source](https://artifacts.picoctf.net/c_titan/80/flag.c) nc titan.picoctf.net 60471


 # Initial Observation: 
It looks difficult because I don't know anything about little and big endian; I have researched what those two things are and how they work. Reading the hints, it looks like I have to use the ASCII table to convert values into hexadecimal. Also, the second hint gives an article, but it's not good since it's behind a paywall

 # Strategy (During the Challenge):
1. Check out the challenge
2. Open up the ASCII Table and get ready to convert values into hexadecimal values
3. Research what little endian and big endian are

 # Tools Used:

This table allows you to convert values into hexadecimal [ASCII Table](https://www.ascii-code.com/)

# Solution (What I Did During the Challenge): 
1. I opened up the challenge
2. I copied the value given onto a piece of paper
3. I determined the hexadecimal values for each letter
4. To find the little endian: You have to **reverse the order** of hexadecimal values
5. An example: ( "cbsjx" is the string in the challenge) = ( 6362736a78 - hexadecimal value)
6. By reversing it, I mean: (786a736263 - hexadecimal value) - this is the answer for the little-endian representation
7. To find the big-endian representation, you keep the same order ( 6362736a78 - hexadecimal value)



# Flag: 

After finding the little and big endian representations, the challenge will present you with the flag

# Mistakes I made:

1. I made a huge mistake while doing this challenge that cost me a lot of time: While I was researching, I found out that you have to reverse data in 4-byte chunks, and if you have you have 1 - 3 extra bits, you don't reverse them.
2. But in CTFS, unless it says the byte chunk size, you reverse every hexadecimal value. 

   
# What I Learned:

I learned that everything online isn't always right and that I should always check the context in which concepts and commands are being used in. 
