# Challenge Name: CanYouSee

**Category:** Forensics

**Difficulty:** Easy

**Date Completed:**  July 25, 2025

**Writeup Published:** July 26, 2025

**Directions:**  How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/5/unknown.zip).

 # Initial Observation: 
1. The file contains a picture, and within that picture is the flag.
2. Based on the hints, I have to look for something out of the ordinary within the picture to obtain the flag.

 # Strategy (During the Challenge):
 1. Download the file.
 2. View the file on your computer's default app or software.
 3. Try to look for something that is not in its expected form.

 # Tools Used:

 [Base64 Encoder/Decoder:](https://www.base64decode.org/) 

# Solution (What I Did During the Challenge): 
1. I downloaded the file and unzipped it.
2. I used ["nano"](https://www.geeksforgeeks.org/linux-unix/nano-text-editor-in-linux/) to open the picture.
3. I noticed the Attribution URL was encoded in ["Base64"](https://builtin.com/software-engineering-perspectives/base64-encoding).
4. I used an online Base64 decoder.
5. Once I decoded the code, I was able to obtain the flag.

# Another Solution (Using exiftool): 
1. I downloaded the file and unzipped it.
2. I used ["exiftool"](https://support.micasense.com/hc/en-us/articles/4403432185879-How-to-read-and-export-image-metadata-with-Exiftool) to open the ["metadata"](https://www.opendatasoft.com/en/blog/what-is-metadata-and-why-is-it-important-data/) of the picture.
3. Within it, I noticed the Attribution URL to be encoded in "Base64".
4. I used an online decoder to decode it and obtained the flag.

# Flag: 

You can use "nano" or "exiftool" to view the Attribution URL. Then you can decode it using a Base64 decoder, and then you will obtain the flag.

# Mistakes I made:

1. Using ["cat"](https://phoenixnap.com/kb/linux-cat-command) on the picture inside the webshell does not work.

# What I Learned:

1. I learned a powerful command: "exiftool" - used to view "metadata".
2. I learned that there are several methods to obtain a flag.
