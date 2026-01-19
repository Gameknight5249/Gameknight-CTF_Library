# Serpentine

## Category 📚: General Skills
## Difficulty 🟡: Medium
## Solves as of: January 18, 2026 — <img width="1279" height="627" alt="image" src="https://github.com/user-attachments/assets/34e7efac-fdc7-411f-ae40-8d370f08af6d" />

    Caption: This challenge has been solved by 40483 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published 📝: January 19, 2026

---

## Challenge Summary 🧩
This challenge gives you a small [`"Python"`](https://www.w3schools.com/python/python_intro.asp) script where the “flag” logic is present but not actually being shown. The key is to run the program, read what it tells you, then make a minimal source-code change so the script reveals the flag instead of a hint.

---

## Key Objective 🎯
Modify the script’s logic so calling `"print_flag"` results in printing the real flag output.

---

## Prerequisites & Tools 🔧
- A way to download the file (picoCTF webshell or local terminal)
- [`"python3"`](https://www.geeksforgeeks.org/python/introduction-to-python3/) to run the script
- [`"nano"`](https://www.geeksforgeeks.org/linux-unix/nano-text-editor-in-linux/) (or any text editor) to edit the file
- Helpful `"Python"` keywords to recognize in the code:
  - [`"def"`](https://www.geeksforgeeks.org/python/python-def-keyword/), [`"return"`](https://www.geeksforgeeks.org/python/python-return-statement/)
  - [`"for"`](https://www.w3schools.com/python/python_for_loops.asp), [`"in"`](https://www.w3schools.com/python/python_operators.asp), [`"while"`](https://www.w3schools.com/python/python_while_loops.asp)
  - [`"elif"`](https://funtech.co.uk/latest/what-does-elif-mean-in-python), [`"else"`](https://www.w3schools.com/python/ref_keyword_else.asp)

---

## Walkthrough 🚀 (with WHY)

1. Download the script `"serpentine.py"` into your working directory.
    **WHY:** You need the exact file in the challenge so your changes affect the real flag logic.
    
    <img width="875" height="303" alt="image" src="https://github.com/user-attachments/assets/f7c8c3f3-2077-45b2-af06-e1fdba9b7747" />

        Caption: The serpentine.py script is successfully downloaded and ready to inspect.

2. Run the script using `"python3"` and read the output carefully.
    **WHY:** The program’s output acts like a built-in hint, showing you what happens when you try to print the flag and what needs to change.
    
    <img width="659" height="722" alt="image" src="https://github.com/user-attachments/assets/584c2019-5ef7-4a8c-b932-3778a5d72836" />

        Caption: The script runs but prints a hint instead of the flag, confirming the logic is intentionally “miswired.”

3. Open `"serpentine.py"` in `"nano"` and locate where the hint is printed instead of the flag.
    **WHY:** You’re not trying to rewrite the whole program—just identify the exact decision point that chooses hint vs. flag.
    
    <img width="877" height="902" alt="Screenshot 2026-01-18 191201" src="https://github.com/user-attachments/assets/ef95087b-f1e0-47e6-a837-a4fd72ab3919" />

        Caption: The script is open in the editor, allowing you to inspect where the output behavior is controlled.

4. Edit the source code so it prints the flag instead of printing the hint, reusing the existing `"print_flag"` functionality.
    **WHY:** The flag-printing logic already exists; the intended solve is to route execution to it rather than inventing new logic.
    
    <img width="877" height="902" alt="Screenshot 2026-01-18 191201" src="https://github.com/user-attachments/assets/111fab9e-311d-41bb-a4d0-34b6e83966c1" />

        Caption: The original script behavior is shown before any changes, where the program is set up to output a hint.

   <img width="799" height="869" alt="Screenshot 2026-01-18 191345" src="https://github.com/user-attachments/assets/f5d97398-6773-40d6-a340-1f80c0ac343c" />

        Caption: The edited script reuses the existing flag-printing logic so the program reveals the flag when requested.

5. Save the file, rerun the script with `"python3"`, and trigger the flag print again.
    **WHY:** Rerunning confirms your change worked and that the script now outputs the real flag instead of the hint.
    
   <img width="537" height="638" alt="Screenshot 2026-01-18 191756" src="https://github.com/user-attachments/assets/84ad68ef-5f26-42a1-9291-93f57c9e51b2" />

        Caption: The program now prints the flag output, confirming the logic change successfully redirected execution.

---

## Common Mistakes ⚠️
- Spending too long “decoding” the script before learning basic `"Python"` keywords makes the code feel harder than it is.
- Making broad edits instead of reusing `"print_flag"` increases the chance you break the script and lose the intended solve path.
- Forgetting to rerun the script after saving changes leads to thinking your edit didn’t work when it simply wasn’t executed yet.

---

## Lessons Learned ✅
- Researching the language basics first makes source-code challenges faster because keywords like `"def"` and `"return"` reveal the program’s structure immediately.
- When a challenge says “the flag is in the script,” it often means the flag logic exists but execution flow is intentionally pointed away from it.
- Minimal edits are usually the cleanest solve because you’re aligning the program with its intended functionality instead of rewriting it.
