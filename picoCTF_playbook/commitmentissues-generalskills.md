# Challenge Name: Commitment Issues  

## Category 📚: General Skills  
## Difficulty 🟢: Easy  
## Solves as of: September 2, 2025 — <img width="1279" height="666" alt="Screenshot 2025-09-02 175906" src="https://github.com/user-attachments/assets/4beeca84-8cdb-4b99-86c3-efb5832007c4" />
  
    Caption: This challenge has been solved by 28,153 players, suggesting it is moderately solved and requires some persistence.  
## Guide Published 📝: September 2, 2025 

---

## Challenge Summary 🧩  
This challenge introduces version control concepts with Git. The flag was “deleted,” but by investigating previous commits, you can uncover it. This task builds on the skills learned in earlier challenges like Collaborative Development.  

---  

## Key Objective 🎯  
Learn how to use [`"git log"`](https://careerkarma.com/blog/git-log/) and [`"git show"`](https://www.atlassian.com/git/tutorials/git-show) to investigate commit history and recover deleted information.  

---  

## Prerequisites & Tools 🔧  
- Ability to extract `.zip` archives  
- Basic familiarity with version control  
- `"git log"` — view commit history  
- `"git show"` — inspect commit contents  

---  

## Walkthrough 🚀 (with WHY)  

1. **Unzip the provided file.**  
   This gives access to the repository containing the commit history.  
   <img width="737" height="1037" alt="Screenshot 2025-09-02 181157" src="https://github.com/user-attachments/assets/dbb86b34-617d-476b-9d91-9fb67cb6df93" />
  
       Caption: Extracting the "challenge.zip" archive to access the Git repository.  

2. **Run `"git log"`.**  
   This reveals the commit history and helps identify any suspicious commits.  
 <img width="452" height="49" alt="Screenshot 2025-09-02 181345" src="https://github.com/user-attachments/assets/1f8202e6-46be-4aea-93c5-06386181c3ef" />
 <img width="604" height="296" alt="Screenshot 2025-09-02 181620" src="https://github.com/user-attachments/assets/8b9a898a-40c2-4a4b-ac39-4f2366ad5749" />
  
       Caption: The Git log showing two commits, including one labeled “Removing sensitive info”.  

3. **Identify the suspicious commit.**  
   Look for commit messages that suggest data removal, such as “Removing sensitive info.”  
   <img width="604" height="296" alt="Screenshot 2025-09-02 181620" src="https://github.com/user-attachments/assets/14586df7-ecb5-4ca9-b06c-35c6f0b7b8ee" />

       Caption: Highlights an important clue to solve the challenge.

4. **Use `"git show"` on the suspicious commit.**  
   This displays the changes made in that commit, including deleted content.  
<img width="480" height="55" alt="Screenshot 2025-09-02 182548" src="https://github.com/user-attachments/assets/bef97653-5960-4f28-ad5a-89ee7df1dee2" />
<img width="697" height="312" alt="Screenshot 2025-09-02 182013" src="https://github.com/user-attachments/assets/fdd8a619-e270-4fef-945c-a26ac8a312e1" />
  
       Caption: Running "git show" on the flagged commit reveals the previously deleted flag.  

---  

## Common Mistakes ⚠️  
- Searching with [`"ls -a"`](https://www.geeksforgeeks.org/linux-unix/ls-command-in-linux/) instead of investigating commit history, which wastes time.  
- Overlooking the commit message and not realizing that “Removing sensitive info” directly points to the flag’s location.  
- Forgetting to use `"git show"` after spotting the suspicious commit.  

---  

## Lessons Learned ✅  
- Commit history is a powerful way to recover deleted or altered information.  
- `"git log"` quickly highlights useful commit messages, while `"git show"` reveals detailed changes.  
- This challenge reinforces the importance of version control knowledge for both development and cybersecurity.  
