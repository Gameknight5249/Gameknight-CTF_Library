# PW Crack 1

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: October 7, 2025 — <img width="1276" height="666" alt="image" src="https://github.com/user-attachments/assets/1b93089e-0292-4ba2-9b56-1f126e02674d" />

    Caption: This challenge has been solved by 66,947 players, showing it is widely completed and designed as an introductory problem.
## Guide Published 📝: [ADD GUIDE PUBLISHED DATE HERE]
---

## Challenge Summary 🧩
You’re given a simple password-checking script and an encrypted flag that must live in the same folder. By reading the checker’s [`"source code"`](https://www.sonarsource.com/resources/library/source-code/), you can learn exactly what input it expects (often a plainly visible or deterministically derived string) and then use that to unlock the flag—no brute force required.

---

## Key Objective 🎯
Open the `"source code"` of the checker, identify the required password, then run the program and supply that password to reveal the flag.

---

## Prerequisites & Tools 🔧
- Ability to create folders with [`"mkdir"`](https://www.youtube.com/watch?v=7Jm7dpgtZKg)
- A text editor such as [`"nano"`](https://linuxize.com/post/how-to-use-nano-text-editor/) to view the `"source code"`
- Python runtime to execute the checker with [`"python3"`](https://medium.themayor.tech/python3-command-and-control-how-to-guide-4fd4fe32ec71)

---

## Walkthrough 🚀 (with WHY)

1) Create a working folder and place both downloaded files (the checker and the encrypted flag) in the same directory using `"mkdir"` and your file manager or terminal.
**WHY:** Keeping both artifacts side-by-side ensures the checker can find the encrypted flag without extra paths or arguments.  
<img width="2532" height="703" alt="image" src="https://github.com/user-attachments/assets/3553543c-e7ce-42f9-a94b-43e3312e682c" />
 
       Caption: Project folder shows both the password checker and the encrypted flag together in the same directory.

2) Open the checker’s `"source code"` with `"nano"` (or another editor) and read through it carefully.
**WHY:** Directly inspecting the logic reveals what password the script expects and how it validates the input.  
<img width="1013" height="561" alt="image" src="https://github.com/user-attachments/assets/85bb0698-21a4-4864-8a0b-a137330c1393" />

       Caption: The checker is open in "nano"; the validation logic is visible for inspection.

3) Locate the password in the `"source code"` (commonly stored as a constant or assembled from small pieces) and note it.
   **WHY:** Extracting the exact expected string lets you avoid guesswork and immediately satisfy the program’s check.  
<img width="1017" height="576" alt="Screenshot 2025-10-07 185122" src="https://github.com/user-attachments/assets/0874dd34-5840-4eda-9704-decc8f370679" />  

       Caption: The required password is visible within the checker’s logic and recorded for use.

4) Run the checker with `"python3"` and enter the identified password when prompted.
**WHY:** Executing the program with the correct input triggers its success path, causing it to decrypt and print the flag.  
<img width="614" height="132" alt="Screenshot 2025-10-07 185729" src="https://github.com/user-attachments/assets/0fad75ab-f2d0-40e2-a080-fc85b30cfd2e" />
  
       Caption: Executed the checker using "python3" and supplied the discovered password to obtain the flag.

---

## Common Mistakes ⚠️
- Forgetting to keep the checker and the encrypted flag in the same directory, which prevents the program from finding the file.  
- Skimming instead of reading the `"source code"`, which hides the straightforward path to the correct password.  
- Running `"python3"` on the wrong file or from the wrong working directory, leading to file-not-found errors.

---

## Lessons Learned ✅
- Reading `"source code"` first often reveals the intended pathway, saving time versus trial-and-error.  
- Small utilities like `"mkdir"`, `"nano"`, and `"python3"` form a reliable toolbox for organizing, inspecting, and executing challenges efficiently.  
