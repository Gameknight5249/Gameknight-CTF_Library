# Challenge Name: Collaborative Development

## Category 📚: General Skills  
## Difficulty 🟢: Easy  
## Solves as of: August 31, 2025 — <img width="1278" height="707" alt="Screenshot 2025-08-31 161808" src="https://github.com/user-attachments/assets/903f462e-5238-478a-b8d0-7e3d208a3589" />
  
    Caption: This challenge has been solved by 20,650 players, indicating it is a popular challenge that many players were able to complete.  
## Guide Published 📝: September 4, 2025

### Challenge Summary 🧩  
This challenge focuses on exploring a Git repository’s branch history to recover hidden information. Instead of directly searching through files, you must navigate between branches and reconstruct the complete flag.  

---  

### Key Objective 🎯  
Learn how to investigate Git branches and use version control commands to uncover hidden or fragmented data.  

---  

### Prerequisites & Tools 🔧  
- Ability to extract files using [`"unzip"`](https://www.geeksforgeeks.org/linux-unix/unzip-command-in-linux/)  
- Familiarity with [`"cd"`](https://www.educative.io/answers/what-is-cd-in-linux), [`"ls"`](https://phoenixnap.com/kb/ls-command), [`"nano"`](https://ioflood.com/blog/nano-linux-command/), and [`"cat"`](https://phoenixnap.com/kb/linux-cat-command)  
- Useful Git commands include:  
  - [`"git log"`](https://git-scm.com/docs/git-log)  
  - [`"git show"`](https://www.atlassian.com/git/tutorials/git-show)  
  - [`"git branch -a"`](https://www.atlassian.com/git/tutorials/using-branches)  
  - [`"git checkout"`](https://www.atlassian.com/git/tutorials/using-branches/git-checkout)  
  - [`"git diff"`](https://www.atlassian.com/git/tutorials/saving-changes/git-diff)  
  - [`"git log -p"`](https://git-scm.com/docs/git-log)  
  - [`"git config"`](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-config)  

---

### Walkthrough 🚀 (with WHY)

1. **Download and `"unzip"` the challenge files.**  
   WHY: This extracts the repository so you can explore its structure.  
    <img width="818" height="1276" alt="Screenshot 2025-08-31 223050" src="https://github.com/user-attachments/assets/e0b780ce-e0b6-47d9-94ae-b645c6ec7be0" />
    <img width="850" height="77" alt="Screenshot 2025-08-31 223102" src="https://github.com/user-attachments/assets/cb17942b-7420-48f7-bdb7-18438e22ac17" />

       Caption: Challenge files extracted with a visible `drop-in` folder.

2. **Navigate into the `drop-in` directory using `"cd"`.**  
   WHY: The actual project folder containing the Git repository is nested inside.  
  <img width="915" height="115" alt="Screenshot 2025-08-31 223655" src="https://github.com/user-attachments/assets/68483db1-edc9-43e1-9ad3-4389053051b9" />
   
       Caption: Terminal view showing navigation into the nested `drop-in` directory.

3. **Locate `flag.py` in the repository.**  
   WHY: This file contains the flag fragments across different branches.  
  <img width="878" height="168" alt="Screenshot 2025-08-31 223735" src="https://github.com/user-attachments/assets/abadacf9-5913-488c-b9f9-d3df55a4861b" />
  
       Caption: The `flag.py` file displayed in the directory listing.

4. **List all branches with `"git branch -a"`.**  
   WHY: The challenge is built around exploring three separate feature branches.  
  <img width="495" height="41" alt="Screenshot 2025-08-31 223807" src="https://github.com/user-attachments/assets/6705135a-7db2-47a4-b1e9-682e57cbf34d" />
  <img width="445" height="200" alt="Screenshot 2025-08-31 223817" src="https://github.com/user-attachments/assets/430d8163-2dc0-45a8-9eb8-9f42a2bae9e5" />

       Caption: Output showing `feature/part-1`, `feature/part-2`, and `feature/part-3`.

5. **View each branch’s version of `flag.py` using `"git show"`.**  
   WHY: Each branch contains a portion of the flag inside `flag.py`.  
  <img width="591" height="41" alt="Screenshot 2025-09-01 095507" src="https://github.com/user-attachments/assets/630d167a-d3b7-4155-bc28-43b96577b57d" />
  <img width="609" height="332" alt="Screenshot 2025-09-01 095518" src="https://github.com/user-attachments/assets/36890dcd-ba2c-4e8f-91a0-8fed93a243c7" />

       Caption: Example output of `git show feature/part-1` revealing part of the flag.

6. **Collect all three parts of the flag and combine them.**  
   WHY: Only by joining the outputs from each branch do you get the complete flag.  
  <img width="609" height="332" alt="Screenshot 2025-09-01 095518" src="https://github.com/user-attachments/assets/34414473-c328-4002-b2ce-691c09443065" />
  <img width="588" height="370" alt="Screenshot 2025-09-01 095640" src="https://github.com/user-attachments/assets/79a02918-059e-4f9b-b4d8-4484ff028dea" />
  <img width="636" height="344" alt="Screenshot 2025-09-01 095658" src="https://github.com/user-attachments/assets/1ad337a3-e5a0-48eb-b84b-98f491c94b92" />

       Caption: All three flag parts joined together to form the complete solution.

---

### Common Mistakes ⚠️  
- Spending time searching through every file instead of using Git commands.  
- Forgetting to research what `"git branch -a"` does, which prevents discovering the branch structure.  
- Assuming the flag would be in the working directory instead of the repository history.  

---

### Lessons Learned ✅  
- Git branches can hide different versions of files, and exploring them is key in many challenges.  
- Commands like `"git show"` and `"git branch -a"` are essential for investigating repositories.  
- Efficient research on commands can save significant time during challenges.  
