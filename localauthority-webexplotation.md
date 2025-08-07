# Challenge Name: Local Authority 

**Category:** Web Explotation 

**Difficulty:** Easy

**Date Completed:** August 7th, 2025

**Writeup Published:** August 7th, 2025

**Directions:** 

- Can you get the flag?
Go to this website and see what you can discover.

 # Initial Observation: 
- Looks like I just have to ["inspect"](https://zapier.com/blog/inspect-element-tutorial/) the website and look around to find the flag.

 # Strategy (During the Challenge):
1. "Inspect" the website
2. Look for suspicious files in the Sources tab or maybe the Network Tab
<img width="2559" height="1277" alt="Screenshot 2025-08-07 143931" src="https://github.com/user-attachments/assets/f822faaa-9c6f-4274-aa05-ab3825ddd638" />

 # Tools Used:

- "Inspect" tool 

# Solution (What I Did During the Challenge): 
1. I opened the website
2. I entered a random username and password and clicked Enter
<img width="2558" height="1264" alt="Screenshot 2025-08-07 144336" src="https://github.com/user-attachments/assets/bb308a48-29ec-4ee0-a115-70d714e63681" />
3. I inspected the website and found a file named "secure.js" in the Sources Tab; it had the username and password required to log in.

<img width="2559" height="1271" alt="Screenshot 2025-08-07 144650" src="https://github.com/user-attachments/assets/ce85b20b-82d8-4fb4-9658-30c6bbca48e6" />

4. I opened the website again, typed in the username and password I found from the "secure.js" file, and clicked Enter

5. By doing that, the website gave me the flag

# Flag: 

- By inspecting the website and finding the username and password, then enter the username and password, and the website will give you the flag.

# Mistakes I made:
- I didn't enter a random username and password to check if it would change anything

# What I Learned:
- I learned how powerful the "inspect" tool is and how parts of a website can change as inputs are entered into it. 
