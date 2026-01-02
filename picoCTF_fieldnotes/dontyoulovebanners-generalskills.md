# Challenge Name: dont-you-love-banners

**Category:** General Skills

**Difficulty:** Easy

**Date Completed:**  July 31, 2025

**Writeup Published:** 

**Directions:** 

- Can you abuse the banner?
The server has been leaking some crucial information on tethys.picoctf.net 53626. Use the leaked information to get to the server.
To connect to the running application use nc tethys.picoctf.net 51624. From the above information, abuse the machine and find the flag in the /root directory.

 # Initial Observation: 
- Looks like there are two servers, and one of them is leaking crucial information: may be a hint?
- I need to research and learn about ["symlinks"](https://www.freecodecamp.org/news/symlink-tutorial-in-linux-how-to-create-and-remove-a-symbolic-link/) 

 # Strategy (During the Challenge):
1. Connect the first server that is leaking info: try to use the leaked information to obtain the flag
2. Connect to the second server and try to see what it's asking for.
3. Research "symlinks" and try to understand how they tie into this challenge

 # Tools Used:

- Google: To search for the largest cybersecurity conference in the world, and who was the first hacker known to do ["phreaking"](https://www.ninjaone.com/it-hub/endpoint-security/what-is-phreaking/)
- ChatGPT: To research what "symlinks" are

# Solution (What I Did During the Challenge): 
1. Connect to the server that is leaking information.
2. Connect to the second server: enter the password that was leaked from the first server.
3. The next two questions' answers are ["DEFCON"](https://en.wikipedia.org/wiki/DEF_CON) and ["John Draper"](https://en.wikipedia.org/wiki/John_Draper)
4. Now you've connected to the second server
<img width="773" height="307" alt="Screenshot 2025-07-31 182036" src="https://github.com/user-attachments/assets/9d9f221b-1e4d-4dfc-9152-05fce584f372" />
 
5. Type in the command "ls -la", and you will see all of the files and their respective directories
6. You will notice a "root" directory.
7. Type ["cd /root"](https://linuxize.com/post/linux-cd-command/) to move to the ["root"](https://www.baeldung.com/linux/root-user-directory-access) directory.
8. Type ["ls-la"](https://www.geeksforgeeks.org/linux-unix/ls-command-in-linux/) to view all of the files in the root file
9. Then type ["cat script.py"](https://www.linuxteck.com/basic-cat-command-in-linux-with-examples/) - you will notice a sentence that says "*Please supply banner in /home/player/banner*"

<img width="967" height="1204" alt="Screenshot 2025-08-01 091222" src="https://github.com/user-attachments/assets/aabb2725-eaaa-49d1-b918-3076edfe4096" />
   
10. Then type ["rm -rf"](https://www.geeksforgeeks.org/linux-unix/rm-command-linux-examples/) - you do this so you can later create a symlink to it
11. Create a symlink from the "/root/flag.txt" to "/home/player/banner" using ["ln -s"](https://www.geeksforgeeks.org/linux-unix/ln-command-in-linux-with-examples/)

<img width="572" height="110" alt="Screenshot 2025-08-01 091911" src="https://github.com/user-attachments/assets/fab39571-a497-4085-9d1b-38c0f99cd25f" />

12. Then exit the server using "Ctrl + C"
13. Then reconnect to the server, and you will obtain your flag 

# Flag: 

After creating a "symlink" between two different files, you will obtain the flag

# Mistakes I made:
- Lots of mistakes = Lots of learning
1. Didn't understand how to navigate the "root" directory
2. Got confused between "ln" and "ls"
3. Spent a lot of time thinking about what the first server was about
4. Didn't realize I could just search up the answers for the questions asked by the second server: wasted time

# What I Learned:
- I learned the command to create a symlink: "ln -s"
- I learned how to navigate a "root" file
- I learned some knowledge about "cybersecurity conferences" and a little bit about hacking history
