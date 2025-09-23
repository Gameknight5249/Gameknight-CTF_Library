# information

## Category 🕵️: Forensics
## Difficulty 🟢: Easy
## Solves as of: September 16, 2025 — <img width="1275" height="592" alt="image" src="https://github.com/user-attachments/assets/f3a0ce40-809c-4651-8aef-79c107b624ba" />

    Caption: This challenge has been solved by 134,618 players, showing it is widely completed and designed as an introductory problem.
## Guide Published 📝: September 22, 2025

---

## Challenge Summary 🧩
Files can conceal important clues in [`"metadata"`](https://www.opendatasoft.com/en/blog/what-is-metadata-and-why-is-it-important-data/). This challenge strengthens your ability to recognize encoded artifacts like [`"Base64"`](https://builtin.com/software-engineering-perspectives/base64-encoding) inside image details and translate them into readable information—an everyday habit in forensics and real-world incident response.

---

## Key Objective 🎯
Use [`"exiftool"`](https://vickyaryan7.medium.com/exiftool-a-meta-data-extractor-0f2a173b81c0) to read the image’s `"metadata"`, identify a `"Base64"` string in a non-obvious field, and convert it to readable text to recover the flag.

---

## Prerequisites & Tools 🔧
- Understanding of `"metadata"` fields commonly present in images.
- Access to `"exiftool"` to enumerate image details.
- Familiarity with `"Base64"` patterns (letters, digits, `+`, `/`, optional `=` padding).
- A [`"decoder"`](https://www.base64decode.org/) for converting `"Base64"` text to plaintext.
---

## Walkthrough 🚀 (with WHY)

1) **Download the challenge file `"cat.jpg"` from the prompt link.**  
   **WHY:** Working from the exact artifact is essential; a different copy may not contain the same `"metadata"` and you could miss the embedded clue.  
   <img width="2511" height="291" alt="image" src="https://github.com/user-attachments/assets/bd5c5af5-403e-4b2a-a63f-f27c7c82a3d5" />
 
       Caption: Download confirmation for cat.jpg from the challenge page.

2) **Run `"exiftool"` on the image to list all `"metadata"` fields.**  
   **WHY:** `"exiftool"` exhaustively reveals hidden or non-visible data fields where authors often place clues, saving time over manual inspection.  
   <img width="709" height="640" alt="image" src="https://github.com/user-attachments/assets/897274e8-1f7e-4b6e-91f8-daa970ce83f8" />

       Caption: "exiftool" output listing multiple "metadata" fields for the image.

3) **Scan the output for a `"Base64"`-looking string in an unusual field (e.g., License).**  
   **WHY:** Recognizing a `"Base64"` pattern in the `"metadata"` signals an encoded payload; this is a common picoCTF hiding spot that decodes directly to a flag.  
   <img width="709" height="640" alt="image" src="https://github.com/user-attachments/assets/b4f2bed6-c66e-45e9-8243-fb3578271cd4" />
 
       Caption: License field showing a "Base64"-like value inside the "metadata".

4) **Paste the string into a `"decoder"` and decode from `"Base64"`.**  
   **WHY:** Decoding transforms the encoded value into readable text; in this challenge, the result is the flag. Note that valid `"Base64"` may not end with `"="` or `"=="`.  
   <img width="2559" height="1271" alt="Screenshot 2025-09-16 215756" src="https://github.com/user-attachments/assets/89ab0f85-3280-4824-beb5-5ac215dc63e5" />

       Caption: Decoding the "Base64" string in a "decoder" reveals the flag text.

---

## Common Mistakes ⚠️
- Dismissing a string as not `"Base64"` just because it lacks `"="` or `"=="` padding, which leads to overlooking the correct clue.  
- Skimming only obvious fields and ignoring less common ones in the `"metadata"`, resulting in missing the embedded value.  
- Copying the decoded text with hidden whitespace or a trailing newline, which breaks flag submission.

---

## Lessons Learned ✅
- `"exiftool"` is a fast, reliable first move for image forensics because it surfaces `"metadata"` fields where clues are frequently hidden.  
- Not all `"Base64"` strings use padding, so pattern recognition matters more than expecting a specific ending.  
- Becoming fluent in reading `"metadata"` makes future investigations faster because you know which fields to check first.
