
# Challenge Name: Collaborative Development 

**Category:** General Skills

**Difficulty:** Easy

**Date Started:** July 15, 2025

**Date Completed:** July 15, 2025

**Directions:** My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?
You can download the challenge files here:
challenge.zip (https://artifacts.picoctf.net/c_titan/177/challenge.zip)


 # Intial Observation: 
 Given the hints and the directions, I could tell that the flag was somewhere in the edit history. I didn't know what "git" meant in the moment but if felt like I just had to find the edit history in this challenge and go back far enough that the flag will be there.

 # Strategy (During the Challenge) :
 I opied the link in the challenge, pasted it in the webshell and just hoped to find the flag in one of the files because I wasn't sure what to do yet and also I thought it would work because thats how I completed the Blame Game picoCTF challenge. I planed on exploring all the files using "cd","ls", "nano", and "cat" 

 # Tools Used:
ChatGPT: to research and a learn about the differnt git commands: ( Ex: git log or git brach -a) 

# Solution: 
1. paste the link in the webshell
2. "cd" into drop-in
3. then unzip challenge.zip
4. Then you will find another folder named drop-in; "cd" into it.
5. You find a file named: flag.py
6. You use the command: "git branch -a" ; you find three things: feature/part-1, feature/part-2, feature/part-3
7. You use "git show" (feature/part-1) Or any of the other 2 branches.
8. In each branch you will find part of the flag; collect each part and put them together to create the complete flag.

# Flag: 
Once you have found all three pieces; put them together and you will create the compelte flag. 

# Mistakes I made:
1. I spent an hour looking through each file, going through every folder, going through every file in the hopes of find the flag.
2. Another thing I did wrong is that I didn't reasearch what "git branch -a" did as soon as I read the hint. ( Costly mistake)
   
 
# What I Learned:

1. I learned several command: 

"git log" 

"git show" 

"git diff" 

"git branch -a" 

"git log -p" 

"git checkout"

"git config"

"cat"

"nano"

"unzip (filename)" 

"ls -la ( helps find hidden files)" 
