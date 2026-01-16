# Blame Game

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: January 15, 2026 — <img width="937" height="751" alt="image" src="https://github.com/user-attachments/assets/e9d31f2a-b2e4-42c2-81c3-8610bfdfa654" />

    Caption: This challenge has been solved by 27,479 players, indicating it is a popular challenge that many players were able to complete.

## Guide Published 📝: January 16, 2026

## Challenge Summary 🧩
This challenge introduces basic version control forensics by requiring you to inspect commit history to identify the source of an issue. It emphasizes careful navigation of Git logs rather than guessing where important information might be hidden. Understanding how to methodically read commit history is a transferable skill for debugging and auditing real repositories.

---

## Key Objective 🎯
Learn how to inspect Git commit history to locate information hidden within past commits.

---

## Prerequisites & Tools 🔧
- Familiarity with [`"git log"`](https://www.freecodecamp.org/news/git-log-command/)
- Basic terminal navigation using `"cd"` and `"ls"`
- Ability to view file contents using [`"cat"`](https://www.geeksforgeeks.org/linux-unix/cat-command-in-linux-with-examples/)
- A system capable of unzipping `.zip` files

---

## Walkthrough 🚀 (with WHY)

1. Unzip the downloaded challenge files.  
   **WHY:** The repository is packaged as a compressed archive, so extracting it is required before Git commands can be used.  
   <img width="765" height="17" alt="image" src="https://github.com/user-attachments/assets/998e3bd7-4912-4e2a-a93a-af3ca10591a1" />

<img width="787" height="491" alt="image" src="https://github.com/user-attachments/assets/b4e3f90c-707b-4c40-918c-04859f51c18c" />

    Caption: The extracted repository contents after unzipping the challenge archive.

2. Navigate into the extracted directory and run `"git log"`.  
   **WHY:** The directions reference commits, so viewing the commit history is the most direct way to locate suspicious or informative changes.
   
  <img width="485" height="102" alt="image" src="https://github.com/user-attachments/assets/6c2e43b8-71a8-40ca-88bc-ce107396ef4d" />

  
    Caption: The full Git commit history displayed using git log.

3.  Scroll through the entire commit log. The flag is at the bottom 
   **WHY:** To check the entire log and find the flag

    <img width="924" height="351" alt="Screenshot 2026-01-16 120557" src="https://github.com/user-attachments/assets/ddead73d-595f-4d8d-8345-7cdca7273400" />

        Caption: This screenshot shows the flag 

---

## Common Mistakes ⚠️
- Not understanding how `"git log"` operates
- Being unable to extract the file given in the prompt
- Working too quickly and skimming logs, which can cause important details to be overlooked.

---

## Lessons Learned ✅
- Git challenges often reward patience and careful inspection rather than clever shortcuts.
- There can be multiple valid approaches to a problem, but executing a simple strategy correctly is often more effective than overcomplicating the solution.
