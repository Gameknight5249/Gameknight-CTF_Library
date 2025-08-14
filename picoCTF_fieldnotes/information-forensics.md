# Challenge Name: information

**Category:** Forensics

**Difficulty:** Easy

**Date Completed:** July 26, 2025

**Writeup Published:** July 27, 2025

**Directions:** 

Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/a614a27d4cb251d04c7d2f3f3f76a965/cat.jpg)

 # Initial Observation: 

 1. Looks like the file has been modified in some way.
 2. I have to find the modification, and that will most likely lead to the flag.
 3. The hint says to look at the details of the file: Does that mean ["metadata"](https://www.opendatasoft.com/en/blog/what-is-metadata-and-why-is-it-important-data/)?

 # Strategy (During the Challenge):
1. Download the file.
2. Open the metadata using ["exiftool"](https://techarry.com/using-exiftool-in-kali-linux-for-metadata-extraction/).
3. Maybe find clues in the "metadata" that will lead to the flag.
   
 # Tools Used:

 [Base64 Decoder/Encoder:](https://www.base64decode.org/)

# Solution (What I Did During the Challenge):
1. I downloaded the flag.
2. I used "exiftool" to look at the metadata of the file.
3. I noticed that the License was in ["base64"](https://builtin.com/software-engineering-perspectives/base64-encoding).
4. I used the online decoder to decode the code and obtain the flag.

# Flag: 

1. Open the metadata of the file: using the online decoder to decode the code in the License portion of the metadata, and you will obtain the flag.

# Mistakes I made:

1. I did not make any mistakes during this challenge; the hints and my strategy helped me obtain the flag efficiently and effectively.

# What I Learned:
1. I learned that even though there are no "==" at the end of a code does not mean it isn't "base64".
2. I learned that you can edit the "metadata".
