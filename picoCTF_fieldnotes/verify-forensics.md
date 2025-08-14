# Challenge Name: Verify 

**Category:** Forensics

**Difficulty:** Easy

**Date Completed:**  July 23, 2025

**Writeup Published:** July 27, 2025

**Directions:** 

People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate.
ssh -p 59270 ctf-player@rhea.picoctf.net
Using the password 83dcefb7. Accept the fingerprint with yes, and ls once connected to begin. Remember, in a shell, passwords are hidden!
Checksum: 467a10447deb3d4e17634cacc2a68ba6c2bb62a6637dad9145ea673bf0be5e02
To decrypt the file once you've verified the hash, run ./decrypt.sh files/<file>.

 # Initial Observation: 
1. Looks like I have to connect to the server.
2. I have to check the ["hash"](https://www.redhat.com/en/blog/hashing-checksums) of every file.
3. I might need to ["pipe"](https://www.geeksforgeeks.org/linux-unix/piping-in-unix-or-linux/) commands to solve this challenge.

 # Strategy (During the Challenge):
1. Connect to the server using the correct commands and password.
2. Check if the ["checksum"](https://linuxsecurity.com/features/what-are-checksums-why-should-you-be-using-them) of the files matches the one that is given.
3. From their research, the commands that are given in the directions to obtain the flag.


 # Tools Used:

ChatGPT: To research several commands and concepts that are used in this challenge.

# Solution (What I Did During the Challenge): 
1. Connect to the challenge.
2. Type in ["sha256sum files/*"](https://help.ubuntu.com/community/HowToSHA256SUM)  - this will get the hash of every single file in that directory.
3. I took all of the "hashes" from the files, pasted them in Google Docs, and searched for a "hash" that matched the one in the directions.
4. Once you find that file, use the command "./decrypt.sh files/<file>".
5. This will decrypt the file and give you the flag.

# Flag: 

Once you find the file that matches the "hash" from the directions, decrypt it, and you will obtain the flag.

# Mistakes I made:
1. Kept typing in the wrong code when trying to decrypt the file with the correct "hash".
2. I did not research or read the hint about "checksums" at first: I did it when I was stuck, but it should have been my first step.
3. I did not fully understand "/decrypt.sh files/<file>".

# What I Learned:

1. I learned what "Checksums" are.
2. I learned what "hash" is.
3. I learned what "sha256sum <directory>/*" does.
4. I learned what "sha256sum <file>" does.
