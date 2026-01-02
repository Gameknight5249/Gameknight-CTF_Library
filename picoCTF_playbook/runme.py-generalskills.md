# runme.py

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: October 21, 2025 — <img width="1280" height="665" alt="image" src="https://github.com/user-attachments/assets/8e87957e-1108-4251-a8c2-a1999a204a43" />

    Caption: This challenge has been solved by 61,212 players, showing it is widely completed and designed as an introductory problem.

## Guide Published 📝: January 1, 2026

## Challenge Summary 🧩
This challenge introduces executing a local [`"Python script"`](https://www.youtube.com/watch?v=biuWNeg8kcM) in a CTF workflow: download the file, verify it’s present, run it with [`"python3"`](https://medium.themayor.tech/python3-command-and-control-how-to-guide-4fd4fe32ec71), and read the output. 

---

## Key Objective 🎯
Download the challenge `"script"` and execute it with `"python3"` to print the flag.

---

## Prerequisites & Tools 🔧
- Access to a terminal or "webshell".  
- Ability to download files via [`"wget"`](https://www.geeksforgeeks.org/linux-unix/wget-command-in-linux-unix/) or a browser.  
- Listing files with [`"ls"`](https://www.geeksforgeeks.org/linux-unix/ls-command-in-linux/).  
- Running the file using `"python3"`.

---

## Walkthrough 🚀 (with WHY)

1) Download the provided "runme.py" using your browser link or "wget" in the "webshell".  
**WHY:** Having the exact challenge file locally lets you execute it and capture its output.  
<img width="894" height="222" alt="image" src="https://github.com/user-attachments/assets/86b1d891-b752-45c5-98ff-61ad99d448d4" />

  
       Caption: Downloading "runme.py" into the working directory from the challenge page.

2) List directory contents with "ls" to confirm "runme.py" is in the current folder.  
**WHY:** Verifying the file prevents path and missing-file errors before execution.  
<img width="871" height="273" alt="image" src="https://github.com/user-attachments/assets/3d2c7451-882f-4eca-9808-013165d72e6d" />

       Caption: Confirming the presence of "runme.py" using ls.

3) Execute the challenge "script" with "python3" and observe the output.  
**WHY:** The program is designed to print the flag when run correctly—no reversing or editing required.  
<img width="1000" height="352" alt="Screenshot 2025-10-21 142816" src="https://github.com/user-attachments/assets/184ff80c-745e-49df-a9a1-271da7cb640e" />

       Caption: Running "python3 runme.py" and reading the printed flag.

---

## Common Mistakes ⚠️
- Trying to run the file before confirming it exists locally, causing “No such file or directory” errors.  
- Using the wrong interpreter name (e.g., "python" instead of "python3"), leading to failures or version mismatches.  
- Executing from a different directory than where the file was saved, which triggers path errors.

---

## Lessons Learned ✅
- Reading the provided hints can streamline the intended download-verify-run sequence.  
- Verifying with "ls" and using the correct interpreter "python3" are reliable habits that prevent easy mistakes.  
- A clean workflow (download → verify → run) is a reusable pattern for many General Skills challenges.
