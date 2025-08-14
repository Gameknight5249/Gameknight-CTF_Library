# Challenge Name: Secret of the Polyglot

**Category:** Forensics

**Difficulty:** Easy

**Date Completed:** July 25, 2025

**Writeup Published:** July 26, 2025

**Directions:** 
The Network Operations Center (NOC) of your local institution picked up a suspicious file, and they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?
Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/98/flag2of2-final.pdf).

 # Initial Observation: 
1. Looks like it's a file with conflicting ["file extensions"](https://www.techtarget.com/whatis/definition/file-format).
2. I think I just have to change the file to the correct "extension" to get the flag.
3. I also have to find several ways to open the flag.


 # Strategy (During the Challenge):
1. I am going to research how to change the "extension" of a file.
2. I have to figure out what is the correct "extension" is to view the flag.
3. I then have to find the correct way to view the file.

 # Tools Used:

1. ChatGPT: I used it to research how to change the "extension" of a file and to research several ways to open a file.
   
 
# Solution (What I Did During the Challenge): 
1. Open the file that you downloaded in Chrome; you will receive half of the flag.
2. Then open the file in your Notepad or any other code-viewing software; you will notice at the top it says ["PNG"](https://www.adobe.com/creativecloud/file-types/image/raster/png-file.html).
 <img width="425" height="561" alt="Screenshot 2025-07-25 110814" src="https://github.com/user-attachments/assets/dd8fae66-9b06-40c6-b179-76803d355fbc" />

3. Knowing that the file is a "PNG", you have to convert it from ["PDF"](https://www.adobe.com/acrobat/about-adobe-pdf.html#:~:text=PDF%20is%20an%20abbreviation%20that,by%20anyone%20who%20views%20them.) to "PNG".
 <img width="776" height="74" alt="Screenshot 2025-07-25 110954" src="https://github.com/user-attachments/assets/3e03d49c-9e46-46ad-933a-b46b3cc00043" />

4. Once you do that, open the file, and you will receive the other half of the flag.
   
# Flag: 

Once you view the flag in "PDF" and "PNG" form, you will receive the flag.

# Mistakes I made:
1. Instead of changing the file extension to "PNG,"; I changed the file name to "png".
2. I did not understand why ["Adobe PDF Reader"](https://get.adobe.com/reader/) could not open the file.

# What I Learned:
1. I learned that each software can only understand a specific language.
2. I learned that file Extensions help my computer's ["OS"](https://www.geeksforgeeks.org/operating-systems/what-is-an-operating-system/) understand what app or software to use to view the file.
3. I learned that you can give a file any "extension" you desire.
4. I learned how a file can act as both a "PDF" and a "PNG".
