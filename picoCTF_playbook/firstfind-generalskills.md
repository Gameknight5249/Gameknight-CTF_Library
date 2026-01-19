# First Find

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: January 18, 2026 — <img width="1283" height="630" alt="image" src="https://github.com/user-attachments/assets/cc6da51d-7087-4550-8569-5cb7559f933e" />

    Caption: This challenge has been solved by 64,440 players, showing it is widely completed and designed as an introductory problem.
## Guide Published 📝: January 19, 2026

---

## Challenge Summary 🧩
This challenge teaches you how to navigate a `".zip"` archive with lots of nested folders and use basic `"Linux directories"` skills to locate a specific file. It also reinforces a common CTF habit: checking for [`"hidden files"`](https://phoenixnap.com/kb/show-hidden-files-linux) when something “isn’t there” at first glance.

---

## Key Objective 🎯
Find the file `"uber-secret.txt"` inside the extracted archive and read its contents to obtain the flag.

---

## Prerequisites & Tools 🔧
- A terminal with [`"unzip"`](https://www.geeksforgeeks.org/linux-unix/unzip-command-in-linux/)
- Comfort moving through folders with [`"cd"`](https://www.geeksforgeeks.org/linux-unix/cd-command-in-linux-with-examples/)
- Listing files with [`"ls"`](https://www.geeksforgeeks.org/linux-unix/ls-command-in-linux/) and [`"ls -a"`](https://phoenixnap.com/kb/ls-command)
- Viewing file contents with [`"cat"`](https://www.geeksforgeeks.org/linux-unix/cat-command-in-linux-with-examples/)
- (Optional faster method) Searching text across folders with [`"grep -r"`](https://www.geeksforgeeks.org/linux-unix/grep-command-in-unixlinux/)

---

## Walkthrough 🚀 (with WHY)

1. Extract the downloaded archive so you can access all included folders and files locally.
   **WHY:** You can’t search or navigate the internal folder structure until the `"zip archive"` is unpacked.
   <img width="890" height="782" alt="image" src="https://github.com/user-attachments/assets/86f0cc0f-e4b2-446b-b5c1-4af78cc7e16a" />

       Caption: The archive is extracted and the main challenge directory is now visible.

2. List the contents of the extracted directory and start exploring the folder structure.
   **WHY:** This gives you a map of what exists so you can decide where to look next instead of guessing.
   <img width="759" height="130" alt="image" src="https://github.com/user-attachments/assets/85bd734e-85fd-4cc4-be2e-e31243eba9f8" />

       Caption: The top-level folders are displayed, showing where deeper subdirectories begin.

3. Enter the subdirectory `"adequate_books"`, then go into `"more_books"` as you continue following the nested structure.
   **WHY:** The challenge hides the target deeper in the directory tree, so you have to traverse step-by-step.
   <img width="608" height="103" alt="image" src="https://github.com/user-attachments/assets/86417725-4b2a-4ec9-93ab-91eb79df1618" />

       Caption: You are inside deeper subdirectories where the target file is more likely to be hidden.

4. In `"more_books"`, list *all* files (including hidden ones) and notice the hidden folder `.secret`.
   **WHY:** Hidden files and folders often contain the real payload in beginner challenges, and normal listings can miss them.
   <img width="622" height="119" alt="Screenshot 2026-01-18 111506" src="https://github.com/user-attachments/assets/063052a2-def5-4d9b-ba4a-958ae4b0088d" />

       Caption: A hidden directory appears, which explains why the target was not visible earlier.

5. Keep using a hidden-inclusive listing as you go deeper through the hidden subdirectories until you reach `"uber-secret.txt"`.
   **WHY:** If the hiding pattern repeats, you’ll miss the path again unless you consistently check for hidden directories at each level.
   <img width="938" height="352" alt="Screenshot 2026-01-18 111657" src="https://github.com/user-attachments/assets/2e449178-9ed3-4384-85b0-7109482b2d15" />

       Caption: The target file is finally visible at the end of the hidden directory chain.

6. Open `"uber-secret.txt"` and read the flag inside.
   **WHY:** The goal isn’t just finding the file; it’s extracting the exact flag text from its contents.
  <img width="1042" height="73" alt="Screenshot 2026-01-18 111811" src="https://github.com/user-attachments/assets/7f5bcd76-a787-440f-b500-464fcffb86d5" />
 
       Caption: The flag is displayed from inside the target text file.

7. (More efficient alternative) From the extracted root directory, recursively search for `"picoCTF"` across all files to locate the flag instantly.
   **WHY:** When there are many nested files, a recursive search is faster and more reliable than manual folder-by-folder navigation.
  <img width="993" height="861" alt="Screenshot 2026-01-18 111918" src="https://github.com/user-attachments/assets/a2f0eb7b-fd1e-4622-88c3-9e21d63b01bb" />
 
       Caption: A recursive search returns the exact file path containing the flag, skipping manual navigation.

---

## Common Mistakes ⚠️
- Only using a normal directory listing can hide critical folders, because hidden entries won’t show up and the target will look “missing.”
- Exploring every visible folder manually is slow and error-prone, because deep nesting makes it easy to overlook the correct path.
- Forgetting that hidden directories can be nested multiple layers deep causes repeated confusion, because the same “missing file” problem keeps happening.
- Not using a recursive search when the dataset is large wastes time, because you’re doing work a tool can finish in seconds.

---

## Lessons Learned ✅
- Checking for hidden files early matters, because many beginner CTFs use them as the main trick rather than complicated exploitation.
- Recursive searching is a high-ROI skill, because it scales instantly when a challenge contains many folders and files.
- Systematic navigation beats guessing, because a consistent “list → enter → list again” loop prevents you from missing structure clues.
