# CanYouSee

## Category 🕵️: Forensics
## Difficulty 🟢: Easy
## Solves as of: January 17, 2026 — <img width="1274" height="628" alt="image" src="https://github.com/user-attachments/assets/18f4ab8f-c798-4413-8471-cad7f1ad10a7" />

    Caption: This challenge has been solved by 40311 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published 📝: January 18, 2026

## Challenge Summary 🧩
This challenge is a classic “hide and seek” forensics task where the flag is embedded in an image’s extra information rather than the visible pixels. The key skill is learning to inspect unusual details like an attribution field and recognize when it’s encoded instead of readable. You practice spotting and decoding “hidden-in-plain-sight” clues, which is a common pattern in forensics challenges.

---

## Key Objective 🎯
Extract an encoded attribution value from an image and decode it to recover the flag.

---

## Prerequisites & Tools 🔧
- A way to unzip files (e.g., [`"unzip"`](https://www.geeksforgeeks.org/linux-unix/unzip-command-in-linux/))
- A text-view method for inspecting the file contents (e.g., [`"nano"`](https://www.geeksforgeeks.org/linux-unix/nano-text-editor-in-linux/))
- A metadata viewer (e.g., [`"exiftool"`](https://www.geeksforgeeks.org/linux-unix/installing-and-using-exiftool-on-linux/))
- A decoder for [`"Base64"`](https://www.base64decode.org/) (you used an online decoder)

## Walkthrough 🚀 (with WHY)
1. Download the provided `"unknown.zip"` file and extract it using `"unzip"`.
   **WHY:** The challenge content is packaged as a zip, so you need to extract it before you can access the image you’re supposed to analyze.
   <img width="1892" height="379" alt="Screenshot 2026-01-16 122324" src="https://github.com/user-attachments/assets/97ca44bd-a9fe-46a2-b890-2224b733ac7b" />

       Caption: Screenshot showing the extracted image file(s) after unzipping.

2. Open the image normally first (your default photo viewer) and confirm the flag is not visibly printed on the image.
   **WHY:** This confirms you should switch from visual inspection to hidden-data inspection, which saves time and prevents you from chasing the wrong approach.
   <img width="1419" height="731" alt="Screenshot 2026-01-16 122410" src="https://github.com/user-attachments/assets/594b4d56-0be4-41a5-b448-8bc58e993007" />

       Caption: Screenshot showing the image appears normal and the flag is not directly visible.

3. Inspect the image file using `"nano"` to look for anything that appears “out of the ordinary,” especially the Attribution URL field.
   **WHY:** Some files contain readable strings or embedded fields when viewed as text, and spotting an “encoded-looking” value is a fast way to discover where the hidden clue lives.
  <img width="1886" height="308" alt="Screenshot 2026-01-16 122545" src="https://github.com/user-attachments/assets/bf0750d7-1053-489e-b477-189e86fb2b7f" />

       Caption: Screenshot showing the Attribution URL field inside the file contents.

4. Notice that the Attribution URL value is encoded in `"Base64"`.
   **WHY:** Recognizing common encodings (like Base64) lets you immediately convert the hidden clue into readable text instead of guessing what it means.
  <img width="717" height="88" alt="Screenshot 2026-01-16 122545" src="https://github.com/user-attachments/assets/2fd250ae-8d3d-40eb-99dc-b9985b97dcaa" />
 
       Caption: Screenshot showing the Attribution URL string that looks like Base64.

5. Paste the Attribution URL value into a Base64 decoder (you used an online decoder) and decode it to recover the flag.
   **WHY:** The challenge hides the flag by storing it in an encoded form, so decoding is the final step that transforms the hidden clue into the actual answer.
 <img width="1230" height="669" alt="Screenshot 2026-01-17 105714" src="https://github.com/user-attachments/assets/3a0de6f2-6a74-4ac8-8a27-551ef71a659b" />
  
       Caption: Screenshot showing the Base64 decoding result that reveals the flag.

---

## Another Solution 🧩 (Using `"exiftool"`)
1. Extract `"unknown.zip"` if you haven’t already.
   **WHY:** You still need access to the raw image file before you can read its `"metadata"`.
  <img width="1892" height="379" alt="Screenshot 2026-01-16 122324" src="https://github.com/user-attachments/assets/bacb13c6-4a47-4ec9-bbaf-34af37c12efc" />

       Caption: Screenshot showing the image file ready for analysis.

2. Run `"exiftool"` on the image to view its [`"metadata"`](https://www.techtarget.com/whatis/definition/metadata), then locate the Attribution URL field.
   **WHY:** `"exiftool"` is designed specifically for pulling structured metadata fields cleanly, which is often faster and clearer than scanning the raw file in a text editor.
  <img width="688" height="538" alt="Screenshot 2026-01-17 105957" src="https://github.com/user-attachments/assets/1b3e4755-da7f-44c4-854a-8dc21ef14c85" />

       Caption: Screenshot showing exiftool output with the Attribution URL field.

3. Identify that the Attribution URL is encoded in `"Base64"`, then decode it using your Base64 decoder to obtain the flag.
   **WHY:** `"exiftool"` helps you reliably extract the exact value, and Base64 decoding converts it into the final readable flag.
   <img width="1230" height="669" alt="Screenshot 2026-01-17 105714" src="https://github.com/user-attachments/assets/c63e7e01-b715-4379-a903-fe52700e3bb0" />

       Caption: Screenshot showing the decoded Attribution URL value revealing the flag.

---

## Common Mistakes ⚠️
- Trying to use `"cat"` on the image in the webshell and expecting readable output, because image files aren’t meant to display cleanly as plain text.
- Skipping the metadata angle and only looking at the visible image, which wastes time when the clue is stored in an attribution field instead of the pixels.
- Copying an incomplete Attribution URL string for decoding, which can break the `"Base64"` decode or produce garbage output.

---

## Lessons Learned ✅
- `"exiftool"` is a powerful forensics tool because it extracts `"metadata"` fields in a clean, structured way that often reveals hidden challenge clues.
- Forensics challenges frequently hide information in “extra” file fields like attribution data, so checking for odd-looking strings can lead directly to the solution.
- Recognizing `"Base64"` quickly is a time-saver, since it’s one of the most common encodings used to hide flags in beginner CTF problems.
