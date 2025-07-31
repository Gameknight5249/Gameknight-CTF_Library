# Challenge Name: hashcrack

**Category:** Cryptography

**Difficulty:** Easy

**Date Completed:**  July 29, 2025

**Writeup Published:** 

**Directions:** 

- A company stored a secret message on a server, which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?
Access the server using nc verbal-sleep.picoctf.net 61522

 # Initial Observation: 
1. I need to understand all of the common types of ["hashes."](https://primer.picoctf.org/#_hashing)
2. I also need to find tools to decrypt "hashes."
3. The length of "hash" is a key indicator of what type of ["hash algorithm"](https://www.okta.com/identity-101/hashing-algorithms/) it is

 # Strategy (During the Challenge):
1. Research the different types of "hash algorithms" and how to identify them
2. Search for online tools to decrypt "hashes"
3. Decrypt the "hashes" and complete the challenge

 # Tools Used:

- [MD5 Encrypt/Decrypt:](https://10015.io/tools/md5-encrypt-decrypt)

- [SHA-1 Encrypt/Decrypt:](https://md5hashing.net/hash/sha1/b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3)

- [SHA-256 Encrypt/Decrypt:](https://10015.io/tools/sha256-encrypt-decrypt#google_vignette)

# Solution (What I Did During the Challenge): 
1. I connected to the challenge using the link provided in the directions
2. I identified what type of "hash algorithm" it was
3. I copied the "hash", pasted it in the decoder, and entered the answer that I received from the decoder
4. Did Step 2 three times, and then it gave me the flag


# Flag: 

- Once you decode the "hashes" the challenge gives, you will receive the flag

# Mistakes I made:

- I didn't check the lengths of the "hashes" at first: it wasted time

# What I Learned:
- I learned about the existence of several different "hashing algorithms."
- I learned about several online tools regarding "hashing algorithms." 
- I learned how to identify different "hashing algorithms" 

