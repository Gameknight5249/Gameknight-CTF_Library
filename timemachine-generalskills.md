
# Challenge Name: Time Machine

**Category:** General Skills

**Difficulty:** Easy

**Date Started:** July 16, 2025

**Date Completed:** July 16, 2025

**Directions:** What was I last working on? I remember writing a note to help me remember... You can download the challenge files here: [challenge.zip](https://artifacts.picoctf.net/c_titan/160/challenge.zip)


 # Initial Observation: 
 It looked like an easier version of the Collaborative Development and Commitment Issues challenge I did previously. By the look of it, I just had to use my knowledge of git commands to solve the challenge

 # Strategy (During the Challenge):
 1. Unzip the files
 2. Use ["git log"](https://git-scm.com/docs/git-log) to find the old commits
 3. Find a suspicious-looking commit that may have a hint about the flag
 4. Open that commit using ["git show"](https://www.atlassian.com/git/tutorials/git-show)

 # Tools Used:
 Didn't use any tools; just my knowledge about git commands

# Solution: 
My strategy was almost correct:
1. You unzip the file
2. Use "git log" to open up the previous commits
3. There is only one commit, and the flag is within the log page; you don't even need to open the commit.

# Flag: 
The flag is within the git log; it's in plain sight. You don't even need to open a commit. 

# Mistakes I made:
I didn't make any mistakes in this challenge; I learned all of my lessons in the other challenges, thus this challenge was a lot easier for me. 
