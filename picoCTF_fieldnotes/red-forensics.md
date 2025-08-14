# Challenge Name: RED

**Category:** Forensics

**Difficulty:** Easy

**Date Completed:** July 27, 2025

**Writeup Published:** August 12, 2025 

**Directions:**  
RED, RED, RED, RED Download the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)


 # Initial Observation: 
1. Looks like it's a red picture.
2. Based on the hints, clues to the flag are within the color: ["RGB"](https://www.figma.com/resource-library/what-is-rgb/).
3. There is also another hint directing me to look at the ["metadata"](https://www.techtarget.com/whatis/definition/metadata) of the file.

 # Strategy (During the Challenge):
1. Download the file.
2. Look for the "RGB" of the picture.
3. Look at the "metadata" of the picture; hopefully have enough clues to find the flag.

 # Tools Used:

- ChatGPT: To research how to look at the "RGB" of a picture

- [Base64 Encoder/Decoder:](https://www.base64decode.org/)

# Solution (What I Did During the Challenge): 
1. Download the file.
2. Use the command: ["zsteg"](https://tldr.dendron.so/notes/common.zsteg.html)
3. I noticed that there was a line in ["base64"](https://builtin.com/software-engineering-perspectives/base64-encoding).
4. I decoded it and got the flag. - used online decoder.

# Flag: 

- Once you use "zsteg" on the ["PNG"](https://www.adobe.com/creativecloud/file-types/image/raster/png-file.html) file, you will notice a line of "base64" code. Decode it and you will receive the flag.

# Mistakes I made:
1. I tried ["binwalk -e"](https://www.kali.org/tools/binwalk/), but that finds embedded files, not the "RGB" of a file.
2. I tried ["xxd"](https://www.geeksforgeeks.org/linux-unix/xxd-command-in-linux/) when I already knew I had to look for the "RGB" of the picture.
3. I kept using ["strings"](https://labex.io/tutorials/linux-linux-strings-command-with-practical-examples-422934) over and over again because I was frustrated I couldn't find the flag. It wasted precious time.


# What I Learned:
- I solidified my knowledge of the command ["exiftool"](https://www.geeksforgeeks.org/linux-unix/installing-and-using-exiftool-on-linux/).
- I solidified my knowledge of the command "zsteg".
