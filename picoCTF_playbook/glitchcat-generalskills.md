# Glitch Cat

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: January 18, 2026 — <img width="1277" height="685" alt="image" src="https://github.com/user-attachments/assets/b2111da5-6128-464a-974a-56f8eba88fa2" />

    Caption: This challenge has been solved by 59,474 players, showing it is widely completed and designed as an introductory problem.
## Guide Published 📝: January 19, 2026

---

## Challenge Summary 🧩
This challenge focuses on recognizing when output is actually readable data that’s just been transformed into a different representation, specifically [`"Hex-encoded ASCII"`](https://www.youtube.com/watch?v=LFmjq-3fefE). It also builds the habit of using lightweight decoding workflows, so you can turn “glitched” text into a real flag quickly and confidently.

---

## Key Objective 🎯
Connect to the remote service, identify the encoding, and decode the output into the correct `"picoCTF{...}"` flag.

---

## Prerequisites & Tools 🔧
- Ability to connect with [`"nc"`](https://www.geeksforgeeks.org/linux-unix/practical-uses-of-ncnetcat-command-in-linux/)
- Basic familiarity with [`"ASCII"`](https://www.ascii-code.com/articles/Beginners-Guide-to-ASCII) and [`"hexadecimal"`](https://learn.sparkfun.com/tutorials/hexadecimal/all)
- A decoder option:
  - Online [`"Hex to String Converter"`](https://www.rapidtables.com/convert/number/hex-to-ascii.html)

---

## Walkthrough 🚀 (with WHY)

1. Connect to the service using `"nc"` with the provided host and port.
   **WHY:** The challenge is a live flag-printing service, so the flag is revealed through the remote connection output.

   <img width="1034" height="79" alt="image" src="https://github.com/user-attachments/assets/3d5a3251-0e7c-402d-bf85-1cc0292b5007" />

       Caption: The service prints a “glitched” sequence instead of a normal readable flag.

3. Notice that the service output looks like a series of hex-looking characters rather than plain English text.
   **WHY:** Recognizing the pattern early prevents you from wasting time guessing random formats when the output is clearly structured.

   <img width="1029" height="22" alt="image" src="https://github.com/user-attachments/assets/676870a9-1c7e-4cdf-a2a0-e958f4a5fe64" />

       Caption: The output appears as hex-style characters that don’t form readable text directly.

5. Identify the format as `"Hex-encoded ASCII"` rather than a random or broken string.
   **WHY:** Once you know it’s hex representing ASCII bytes, decoding becomes a straightforward conversion instead of trial-and-error.

   <img width="419" height="198" alt="image" src="https://github.com/user-attachments/assets/ad7c13d4-ed2a-4dea-8fbb-aaceb3798226" />

       Caption: The encoding pattern matches how ASCII characters are represented in hexadecimal.

7. Decode the string using an online `"Hex to String Converter"` by pasting the hex values exactly as provided.
   **WHY:** A converter safely handles the byte-to-character translation and outputs the readable flag text.

   <img width="773" height="944" alt="image" src="https://github.com/user-attachments/assets/e777afaf-3bc3-40db-a298-06e39d207208" />

       Caption: The converter transforms the hex sequence into readable ASCII text, revealing the flag.

---

## Common Mistakes ⚠️
- Adding `"0x"` in front of every hex value can break the converter input format, because many online decoders expect raw hex pairs without prefixes.
- Assuming the output is “corrupted” instead of encoded slows you down, because the flag is already there and just needs decoding.
- Copying the encoded output with extra spaces or missing characters causes incorrect decoding, because even a single wrong hex byte changes the output.

---

## Lessons Learned ✅
- Recognizing `"Hex-encoded ASCII"` is a fast win in beginner challenges, because many “glitch” prompts are really just encoding puzzles.
- Keeping a simple decoding workflow is powerful, because it scales to other common formats like base encodings and byte-level transformations.
