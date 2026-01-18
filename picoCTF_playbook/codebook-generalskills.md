# Codebook

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: January 17, 2026 — <img width="1275" height="666" alt="Screenshot 2026-01-17 110939" src="https://github.com/user-attachments/assets/1c22dd49-54c4-4745-8b46-770291fe4df3" />

    Caption: This challenge has been solved by 63,050 players, showing it is widely completed and designed as an introductory problem.
## Guide Published 📝: January 18, 2026

---

## Challenge Summary 🧩
This challenge teaches a common execution pattern: a script only works when its companion file is in the same [`"directory"`](https://www.geeksforgeeks.org/linux-unix/linux-directory-structure/). By running a provided [`"python"`](https://www.w3schools.com/python/python_intro.asp) script alongside its required text file, you receive the flag.

---

## Key Objective 🎯
Run a `"python"` script correctly by keeping its required file in the same `"directory"`.

---

## Prerequisites & Tools 🔧
- Comfort downloading files and using a terminal/command prompt
- Basic understanding of `"directory"`
- Ability to run `"python"` using [`"python3"`](https://medium.themayor.tech/python3-command-and-control-how-to-guide-4fd4fe32ec71)
- No extra tools required for this challenge

---

## Walkthrough 🚀 (with WHY)

1. Download `code.py` and `codebook.txt`, then place both files in the same `"directory"` (there is no need to create a new `"directory"` because they are in the home directory).
   **WHY:** The directions explicitly say the script must be run in the same location as the text file, so keeping them together prevents the script from failing due to missing files.

  <img width="2530" height="532" alt="image" src="https://github.com/user-attachments/assets/6b6fe136-f68a-4e47-92dc-5185cf431529" />

    Caption: Both files are shown in the same folder so the script can access the required text file.

2. Run the script from that same `"directory"` using `"python3"`.
   **WHY:** Executing the `"python"` file is the intended solve method, and it reveals the flag once it can read the companion text file.

   <img width="429" height="77" alt="image" src="https://github.com/user-attachments/assets/33c49161-089c-4e5f-bdcd-f6a81788a7e0" />

       Caption: The script is executed from the folder containing both files, and the output displays the flag.

---

## Common Mistakes ⚠️
- Keeping the files in separate `"directory"` locations breaks the solve because the script cannot access the required text file.
- Spending time reading the files manually is inefficient here because the directions explicitly tell you to run the `"python"` script to get the flag.
- Running the script without using `"python3"` can waste time troubleshooting since the solve depends on executing the script correctly.

---

## Lessons Learned ✅
- Placing dependent files in the same `"directory"` matters because scripts may require local files to be present where they are executed.
- Using `"python3"` is a reliable way to run a `"python"` script when the challenge expects execution rather than manual inspection.
- Recognizing this file-dependency pattern helps you solve similar challenges faster because you can check file placement before doing anything else.
