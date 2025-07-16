# Challenge Name: Blame Game 

**Category:** General Skills

**Difficulty:** Easy

**Challenge Started:** July 15, 2025

**Challenge Completed:** July 15, 2025

**Writeup Published:** July 16, 2025
 

**Directions:**  Someone's commits seems to be preventing the program from working. Who is it? You can download the challenge files here: [challenge.zip](https://artifacts.picoctf.net/c_titan/73/challenge.zip)


 # Initial Observation: 
The directions talk about commits, so I assumed it the challenge required me to use git commands. I didn't know which command, though

 # Strategy (During the Challenge):
 1. Unzip the file
 2. Use git log to look through all the commits
 3. Maybe use grep if there are a lot of logs
 4. Find the flag within one of the commits

 # Tools Used:
I didn't use any extra tools in either of the solutions; I just used my knowledge of commands. 


# Solution (What I did during the challenge):
1. I unzipped the file
2. I used "git log" to look through all of the commits.
3. I quickly scrolled through all of the commits; I did not find the flag at the top or bottom of the commit log.
4. Then I looked through all of the files using "cd" and "ls".
5. I found a file named "HEAD" within the logs folder.
6. I used "cat" to open the file.
7. Within the first three commit logs, my flag was there.

# Solution (A more efficient method)
When I found the flag, I got confused because I had just scrolled through the commit log 5 minutes ago: I found out my intial strategy was good, I just executed it wrong.
1. Unzip the file
2. Use "git log" to look through all of the commits
3. Make sure to scroll carefully through all of the commits since the flag is somewhere in the middle, not at the top or bottom as I assumed before.
4. You will find the flag if you do this and scroll carefully.

# Flag: 

The flag is somewhere in the middle of the commit log.

# Mistakes I made:

I assumed that the flag would be in an easily identifiable place.
I was working hastily; I should slow down and work methodically 

# What I Learned:

I learned that there are multiple solutions to a problem, each with its own pros and cons.



