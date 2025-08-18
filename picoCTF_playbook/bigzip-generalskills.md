
# Challenge Name: Big Zip

## Category: General Skills

## Difficulty: Easy

## Solves as of: August 16, 2025 — <img width="1273" height="627" alt="Screenshot 2025-08-16 164221" src="https://github.com/user-attachments/assets/27ded781-2ecc-47cb-95fb-f7277e3c72cd" />
  
    This challenge has been solved by 53,159 players, showing it is widely completed and designed as an introductory problem.

## Guide Published: August 17, 2025

---

## Challenge Summary
You’re given a large [`".zip"`](https://www.dropbox.com/resources/what-is-a-zip-file#:~:text=ZIP%20is%20a%20common%20file,file%20in%20the%20original%20format.) archive containing hundreds of directories and files. The goal is to locate the hidden flag without manually checking each one.

---

## Key Objective
Learn how to use the [`"grep"`](https://www.geeksforgeeks.org/linux-unix/grep-command-in-unixlinux/) command with the recursive option to efficiently search through large sets of files.

---

## Prerequisites & Tools
- [`"unzip"`](https://www.geeksforgeeks.org/linux-unix/unzip-command-in-linux/) for extracting `.zip` archives  
- `"grep"` for searching text patterns in files  
- Basic Linux command line familiarity  

---

## Walkthrough (with WHY)

1. **Unzip the archive**  
   **WHY:** You need the files extracted locally so `"grep -r"` can actually search through them.   
<img width="562" height="99" alt="Screenshot 2025-08-16 164933" src="https://github.com/user-attachments/assets/c6d63c34-b410-437e-8acb-7364469e9431" />
<img width="703" height="1266" alt="Screenshot 2025-08-16 164958" src="https://github.com/user-attachments/assets/43b94f17-0956-4438-b4ef-c583b2054323" />

    Caption: Archive successfully extracted with `"unzip"`.  

2. **Check the extracted contents**  
   **WHY:** Verifying the extraction shows how many files and directories exist, and confirms everything unzipped correctly. With hundreds of files, manual searching isn’t realistic.  
<img width="2358" height="1271" alt="Screenshot 2025-08-17 181309" src="https://github.com/user-attachments/assets/30e7c5ed-67e4-4d23-824a-4229e0bdf2e8" />
  
    Caption: Directory listing of the unzipped archive showing hundreds of files and subfolders.  

3. **Run `"grep -r"` to search for `"picoCTF"`**  
   **WHY:** The `-r` flag makes `"grep"` scan through every subdirectory and file automatically, letting you find the flag quickly instead of opening files one by one.  
<img width="481" height="57" alt="Screenshot 2025-08-17 215923" src="https://github.com/user-attachments/assets/6c8c0cec-191d-45c1-97bc-cb96d43fd07c" />

    Caption: Recursive `"grep -r"` search across all files for `"picoCTF"`.  

4. **Identify the flag**  
   **WHY:** The search output highlights the exact file path and line with the flag, making it easy to copy.  
<img width="1866" height="688" alt="Screenshot 2025-08-17 181543" src="https://github.com/user-attachments/assets/944bf989-97d5-4072-9946-8b3ab8301df6" />

    Caption: Search results showing the file path and line containing the flag.  

---

## Common Mistakes
- Not all files unzipped properly (especially in browser shells), which caused `"grep -r"` to miss the flag.  
- Forgetting the `-r` flag and only searching the current directory.  
- Running the command outside the root of the extracted directory.  

---

## Lessons Learned
- Always confirm that files are fully extracted before searching.  
- `"grep -r"` is a fast and reliable way to search through large, nested directories.  
- Checking your environment (e.g., browser shell vs. local machine) can prevent missed files.  


