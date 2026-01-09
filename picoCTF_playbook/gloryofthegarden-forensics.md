# Glory of the Garden

## Category 🕵️: Forensics 
## Difficulty 🟢: Easy
## Solves as of: September 7, 2025 — <img width="1275" height="590" alt="image" src="https://github.com/user-attachments/assets/4fdb2cfb-3419-44a9-a06e-1372f4644840" />

    Caption: This challenge has been solved by 82,788 players, showing it is widely completed and designed as an introductory problem.
## Guide Published 📝: January 9, 2026

---

## Challenge Summary 🧩
You’re given a [`"JPEG"`](https://www.adobe.com/creativecloud/file-types/image/raster/jpeg-file.html) image that “contains more than it seems.” The fastest path is to inspect the file’s raw bytes with a [`"hex editor"`](https://www.ultraedit.com/blog/what-is-a-hex-editor-and-how-to-use-it/) or a terminal tool such as [`"xxd"`](https://www.geeksforgeeks.org/linux-unix/xxd-command-in-linux/) so any embedded readable text appears alongside the byte view.

---

## Key Objective 🎯
Reveal the flag by dumping the raw bytes of `"garden.jpg"` with `"xxd"` and reading the human-readable text directly from the output.

---

## Prerequisites & Tools 🔧
- [`"Linux terminal"`](https://ubuntu.com/tutorials/command-line-for-beginners) — ability to run basic commands.  
- `"hex editor"` — know what it is and why it helps reveal hidden data.  
- `"xxd"` — command-line utility that prints a hex + text (“hex dump”) view.

---

## Walkthrough 🚀 (with WHY)

1) **Download `"garden.jpg"` to your working directory on the `"picoCTF webshell"` (or local machine).**  
   **WHY:** You need the file locally so tools like `"xxd"` can read its bytes and render a hex + text view.  
   <img width="1862" height="301" alt="image" src="https://github.com/user-attachments/assets/2948f233-f871-44da-b5d9-e8b9e7486ad8" />

       Caption: Downloaded "garden.jpg" into the working directory via the picoCTF webshell.

2) **Run `"xxd"` on `"garden.jpg"` to print its hex + text view.**  
   **WHY:** `"xxd"` aligns byte values with a right-hand text column so any readable strings embedded in the file appear without extra decoding.  

    <img width="444" height="35" alt="image" src="https://github.com/user-attachments/assets/5a40c00e-81dd-4f6d-b8b0-4628c994dd7b" />

       Caption: Executed "xxd" on "garden.jpg" to display bytes with a readable text column.

4) **Scan the right-hand text column of the `"xxd"` output to locate the flag string.**  
   **WHY:** When the flag is stored as plaintext, it shows up directly in the text column—no further transformation needed; in this challenge, it appears near the bottom-right of the output.  

 <img width="742" height="153" alt="Screenshot 2026-01-08 150420" src="https://github.com/user-attachments/assets/c442873e-fce4-482d-94d0-c1cf9848f27e" />
  
    Caption: The flag appears as readable text in the right-hand column of the xxd output.

---

## Common Mistakes ⚠️
- Overlooking the right-hand text column in the `"xxd"` output hides readable strings that can include the flag, so scan that pane carefully instead of focusing only on hex bytes.  
- Running `"xxd"` from a different directory than where `"garden.jpg"` lives triggers file-not-found errors and wastes time, so confirm your working directory matches the file location before executing.  
- Assuming extra decoding or steganography is required adds unnecessary steps when a simple hex dump already reveals plaintext, so start with `"xxd"` before trying heavier tools.

---

## Lessons Learned ✅
- A quick hex dump with `"xxd"` surfaces plaintext embedded in binaries, making it the fastest first check before attempting complex techniques.  
- Understanding what a `"hex editor"` shows—bytes aligned with their readable characters—lets you spot flags efficiently without guesswork.  
- Verifying filenames and paths such as `"garden.jpg"` prevents avoidable errors and keeps attention on analysis rather than environment issues.
