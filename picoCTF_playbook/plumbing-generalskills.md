# plumbing

## Category 📚: General Skills
## Difficulty 🟡: Medium
## Solves as of: October 7, 2025— <img width="1275" height="661" alt="image" src="https://github.com/user-attachments/assets/62124450-baaa-433d-9e3e-94b29077278e" />

    Caption: This challenge has been solved by 45,741 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published 📝: January 9, 2026
---

## Challenge Summary 🧩
This challenge teaches how to route one program’s output into another using [`"pipes"`](https://www.geeksforgeeks.org/linux-unix/piping-in-unix-or-linux/) and filter streaming text with [`"grep"`](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/) while connected to a remote service via [`"nc"`](https://www.geeksforgeeks.org/linux-unix/practical-uses-of-ncnetcat-command-in-linux/). Mastering pipelines is a core shell skill that lets you transform, search, and extract signals from noisy output efficiently.

---

## Key Objective 🎯
Use a pipeline with the `"pipe operator"` to stream the remote program’s output into `"grep"` and reveal the flag.

---

## Prerequisites & Tools 🔧
- Understanding of [`"standard streams"`](https://www.putorius.net/linux-io-file-descriptors-and-redirection.html) (input/output flow in the shell)
- A terminal with `"nc"`
- Familiarity with `"grep"` pattern searching
- Comfort using the `"pipe operator"` (`"|"`) to chain commands

---

## Walkthrough 🚀 (with WHY)
1) Connect to the running service with `"nc"` and observe the text it prints.  
   **WHY:** Establishing an interactive stream lets you capture everything the program emits so you can process it on the fly rather than saving to a file first.  
   <img width="737" height="77" alt="image" src="https://github.com/user-attachments/assets/08aeae29-c63a-4d2d-a42a-7a6aeb3aa184" />
  
     Caption: Connected to the remote service using "nc"; the program begins streaming output to the terminal.

2) Chain the connection into `"grep"` using the `"pipe operator"` and search for the flag pattern (for example, "picoCTF").  
   **WHY:** A pipeline feeds the program’s output directly into a search tool so you can instantly filter for the exact line that contains the flag without manual scrolling.  
   <img width="871" height="64" alt="Screenshot 2025-10-07 180834" src="https://github.com/user-attachments/assets/8cb76978-0d55-4c5e-9125-7ae130b62193" />
 
     Caption: Used "nc" piped into "grep" to filter for "picoCTF"; only matching lines remain visible.

3) Read the filtered line and record the flag.  
   **WHY:** After narrowing the stream to relevant content, extracting the single line with the flag becomes trivial and reliable.

---

## Common Mistakes ⚠️
- Jumping in without reviewing how `"pipes"` work, which makes the filtering step confusing and error-prone.  
- Forgetting to actually chain commands with the `"pipe operator"`, leading to manual searching through noisy output.  
- Being unsure how to start the session with `"nc"`, which blocks progress before you can use a pipeline.

---

## Lessons Learned ✅
- Understanding `"pipes"` and `"standard streams"` turns raw program output into structured, searchable data.  
- Combining `"nc"` with `"grep"` via the `"pipe operator"` is a fast, dependable way to surface a hidden flag from a live stream.
