# Secret of the Polyglot

## Category 🕵️: Forensics
## Difficulty 🟢: Easy
## Solves as of: December 21, 2025 — <img width="1280" height="747" alt="image" src="https://github.com/user-attachments/assets/774b7141-7981-41cb-8581-81bc3640f254" />

    Caption: This challenge has been solved by 38,351 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published 📝: January 1, 2026

---

## Challenge Summary 🧩
This challenge examines how files can contain multiple valid formats at once and how different programs interpret the same data differently. Instead of relying on automated tools, success depends on recognizing file signatures and understanding how operating systems decide which application should open a file. It reinforces a foundational forensics concept: identifying what a file truly is matters more than what its name suggests.

---

## Key Objective 🎯
Recognize conflicting file signatures and extract information by opening the same file using different formats and viewers.

---

## Prerequisites & Tools 🔧
- A web browser capable of opening files locally  
- A basic text or code editor  
- Familiarity with [`"file extensions"`](https://edu.gcfglobal.org/en/basic-computer-skills/understanding-file-extensions/1/)  
- Awareness that applications interpret files based on internal structure, not just names
  
---

## Walkthrough 🚀 (with WHY)

1) Download the suspicious file and save it locally.  
**WHY:** Working with a local copy allows you to test how different programs interpret the same file without altering its contents.

2) Open the file in a web browser.  
**WHY:** Browsers often attempt to auto-detect file structure, which reveals how part of the file can be interpreted as a `"PDF"`.  
<img width="2559" height="1275" alt="Screenshot 2025-12-20 123204" src="https://github.com/user-attachments/assets/db8b8803-19fe-40eb-ba03-69b91f2877e1" />

       Caption: Viewing the file in a browser reveals one interpretation of the data and exposes part of the flag.

3) Open the same file in a text or code editor.  
**WHY:** Inspecting the raw contents exposes identifying headers, including a `"PNG"` signature embedded at the top of the file.  
<img width="1937" height="1045" alt="Screenshot 2025-12-20 123343" src="https://github.com/user-attachments/assets/9dff9bd7-a719-4f79-be2e-4e4b21ce5ad3" />
 
       Caption: The file header clearly indicates a PNG signature despite the PDF extension.

4) Change the file’s extension from `"PDF"` to `"PNG"`. 
**WHY:** Renaming the extension allows the operating system to associate the file with an image viewer that understands PNG data.  

<img width="769" height="39" alt="image" src="https://github.com/user-attachments/assets/1c73c1ee-21ad-44f1-81f3-828a9beda84a" />

<img width="794" height="35" alt="image" src="https://github.com/user-attachments/assets/9d78f5b3-b0ec-4fa8-8455-1da41b083647" />

    Caption: Changing the extension allows the OS to open the file using a PNG-compatible application.

5) Open the renamed file in an image viewer.  
**WHY:** Viewing the file as a PNG reveals the remaining portion of the flag stored in the alternate format.  
<img width="521" height="503" alt="Screenshot 2025-12-20 131022" src="https://github.com/user-attachments/assets/c3c0173d-812b-44d5-ae82-3d2e604a7a03" />
 
       Caption: Opening the file as a PNG exposes the second half of the flag.

---

## Common Mistakes ⚠️
- Renaming the file incorrectly by changing the filename instead of the actual `"extension"`, which prevents proper format recognition.  
- Assuming that a file can only belong to one format, rather than considering that multiple valid signatures may coexist.  
- Expecting tools like PDF readers to succeed when the file structure does not fully match the advertised format.

---

## Lessons Learned ✅
- File extensions act as hints for the operating system, but applications rely on internal file signatures to determine how data is interpreted.  
- A single file can be intentionally crafted to function as more than one valid format, depending on how it is opened.  
- Basic manual inspection techniques are often sufficient to solve beginner forensics challenges without advanced tooling.
