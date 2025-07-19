# Challenge Name: Web Decode

**Category:** Web Explotation 

**Difficulty:** Easy

**Date Started:** July 18, 2025

**Date Completed:** July 18, 2025

**Writeup Published:** July 18, 2025

**Directions:**  Do you know how to use the web inspector? Start searching [here](http://titan.picoctf.net:50759/) to find the flag


 # Initial Observation: 
I have to use a ["web inspector"](https://wpengine.com/resources/how-to-inspect-a-website/) to find the flag
The flag was most certainly somewhere on the website ( maybe in the code) 
This challenge is a lot different from the General Skill challenges I have done so far

 # Strategy (During the Challenge):
1. Open the website
2. Research what a "web inspector" is
3. Use this "web inspector" to find the flag
4. Be aware that the flag is most likely encoded, so I won't be able to spot it in plain text

 # Tools Used:

[ Base64 Decoder/Encoder](https://www.base64decode.org/)

ChatGPT: To research what a "web inspector" is

# Solution (What I Did During the Challenge): 
1. I opened the website
2. I opened the "web inspector" ( you can do it by right-clicking and clicking on "inspect")
3. I went to the "about" page on the website
4. I saw that there was a line of text that ended with "=="
5. I decoded that line of text using a ["Base64"](https://wpengine.com/resources/how-to-inspect-a-website/) decoder.
<img width="822" height="1268" alt="Screenshot 2025-07-18 215057" src="https://github.com/user-attachments/assets/44515532-1fe2-46db-b44d-8bc5419f657f" />


# Flag: 

Once you find the encoded flag within the inspect tool, decode it using an online decoder; you will receive the flag then

# Mistakes I made:

I did not make any mistakes during this challenge; I just learned a lot about "web inspector."
   
# What I Learned:
I learned about "web inspector"

I learned how to identify Base64 code

I learned how to navigate the "web inspector." 

