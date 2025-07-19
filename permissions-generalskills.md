# Challenge Name: Permissions

**Category:** General Skills

**Difficulty:** Medium

**Date Started:** July 18, 2025

**Date Completed:** July 18, 2025

**Writeup Published:** July 18, 2025

**Directions:**
Can you read files in the root file?
Additional details will be available after launching your challenge instance.

 # Initial Observation: 

 It asks me if I can read the "root" file, but I dont know what that is so I am going to research it.
 I also have to figure out a way to view what permissions I have.
 

 # Strategy (During the Challenge):
1. Reasearch what a ["root"](https://www.ssh.com/academy/pam/root-user-account) file is.
2. Reasearch how to view what permissions I have.
3. Figure out a way using the knowledge from my reasearch to find the flag.

# Solution (What I Did During the Challenge): 
1. Connect to the main server by the link that is provided in the directions: ( not in this writeup but you may diretcly receive it from the picoCTF challenge)
2. Type ["whoami"](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/whoami) to check what account you are
3. Type in "sudo vi"
4. Type in the password in the directions
5. Type ":!bash" to exit the "VIM"
6. Type "whoami" to check your account: ( you should see "root")
7. Type ["ls -a /root"](https://www.geeksforgeeks.org/linux-unix/ls-command-in-linux/) ( to see the hident files "root" can access)
8. Type "[cat](https://www.linuxteck.com/basic-cat-command-in-linux-with-examples/) /root/flag.txt" ( to open flag.txt)
9. You will recieve the flag by doing this
<img width="702" height="550" alt="Screenshot 2025-07-18 201257" src="https://github.com/user-attachments/assets/117bd86b-d99e-4d7e-93a0-7ca0e774771d" />

# Flag: 

After gaining root acess, you will be able to see "flag.txt" and be able to open it to recieve the flag.

# Mistakes I made:

I thought that "sudo" commands were the same as regular commands

I forgot to use "ls -a" too look for hidden files and instead just used "ls" ( Cost me a lot of time)

I missed the importance of ["sudo -l"]((https://www.geeksforgeeks.org/linux-unix/sudo-command-in-linux-with-examples/) ) ( it shows what sudo commands you can perform, I thought it wasn't useful) 


# What I Learned:
I learned how "root" meant that I had access to any file.

I learned how to do a ["privlege escalation"](https://www.proofpoint.com/us/threat-reference/privilege-escalation)

I learned how to use ["sudo commands"](https://www.geeksforgeeks.org/linux-unix/sudo-command-in-linux-with-examples/) 

I learned about ["permission"](https://phoenixnap.com/kb/linux-file-permissions) and why we use them

I learned how to escape the ["VIM"](https://opensource.com/article/19/3/getting-started-vim) by using ":!bash<Enter>"

