# Challenge Name: Glitch Cat

**Category:** General Skills

**Difficulty:** Easy

**Date Completed:** August 12, 2025 

**Writeup Published:**

**Directions:** 

- Our flag printing service has started glitching!
$ nc saturn.picoctf.net 63684

 # Initial Observation: 
- Looks like the challenge is about ["ASCII"](https://www.ascii-code.com/articles/Beginners-Guide-to-ASCII) 
- The hints also refer to the glitch being valid in ["Python"](https://www.w3schools.com/python/python_intro.asp), so I should also keep in mind that

 # Strategy (During the Challenge):
1. Connect to the challenge
2. See what the challenge makes me do
3. Try to connect "ASCII" and "Python" to the challenge and use those two concepts to find the flag. 

 # Tools Used:

- [Hex to String Converter](https://www.rapidtables.com/convert/number/hex-to-ascii.html)

# Solution (What I Did During the Challenge): 
1. Connect to the challenge
2. You will notice that the challenge gives you the flag, but it is in some weird ["encoding"](https://www.lenovo.com/us/en/glossary/what-is-encode/?srsltid=AfmBOoqYbXmdnNkIE8lLHLOfnODbwllDGit5BLMrXlTrC2NPYCA1m9jl)
3. The encoding is ["Hex-encoded ASCII"](https://www.youtube.com/watch?v=XJJcyVtTYFY)
4. Now you have two options to convert the encoding into the flag.
5. Option 1: Use ["AI"](https://medium.com/@vitalysimx/leveraging-ai-in-ctf-challenges-where-to-draw-the-line-be5db66a602e) to convert it ( the link is to a website that talks how to properly use AI in CTFs)
6. Option 2: Use an online "Hex to String Converter" 
<img width="823" height="1256" alt="Screenshot 2025-08-12 130421" src="https://github.com/user-attachments/assets/efaa7277-b809-431f-84ac-fc136ca7ee62" />
7. You will receive the flag once you decode the "Hex-encoded ASCII"

# Flag: 

- You will receive the flag by either using "AI" or an online "Hex to String Converter" to decode the "Hex-encoded ASCII"

# Mistakes I made:
- When I was trying to use the online "Hex to String Converter", I tried putting "0x" in front of all of the ["hexadecimal"](https://learn.sparkfun.com/tutorials/hexadecimal/all) values, but that doesn't work

# What I Learned:
- I learned about "ASCII encoding"
- I learned how to use "AI" in CTFs
- I learned how to leverage AI to help me learn and develop my skills.
