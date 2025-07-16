# Challenge Name: repetitions

**Category:** General Skills

**Difficulty:** Easy

**Date Started:** July 16, 2025

**Date Completed:** July 16, 2025

**Writeup Published:** July 16, 2025

**Directions:** Can you make sense of this file? Download the file [here](https://artifacts.picoctf.net/c/475/enc_flag).

 # Initial Observation: 
I saw that within the challenge, it said it was base64. One of the hints also said, "Multiple decoding is good." At that point, I knew that there was going to be a base 64 code and I had to decode it multiple times; I just had to research what base 64 code was. 

 # Strategy (During the Challenge):
1. Open the file up
2. Research what base64 was.
3. Use an online decoder
4. Hopefully, find the answer after decoding it twice or thrice. 

 # Tools Used:

  [Base64 decoder](https://www.base64decode.org/)

# Solution (What I Did During the Challenge): 
My strategy was mostly correct.
1. I pasted the file in my webshell browser
2. There was a file called "enc_flag"
3. I opened it; it had a base64 code.
4. I copied and pasted the code into a decoder.
5. I decoded the code, and it gave me another base64 code.
6. I tried the new base64 code again, and it gave me another base64 code.
7. I kept decoding the new code about seven or eight times, and I eventually got the flag 

# Flag: 

You have to keep decoding the new base64 code over and over again; after seven to eight times, you will receive the flag

# Mistakes I made:
I almost stopped decoding the base64 code after three or four times
   
# What I Learned:
I learned the tell-tale sign of a base64 code: the two equal to signs at the end: "==" 
