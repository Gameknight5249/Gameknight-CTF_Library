# endianness

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: September 9, 2025 — <img width="941" height="868" alt="image" src="https://github.com/user-attachments/assets/40fee5cd-ebc5-4134-96aa-fd7830818609" />

    Caption: This challenge has been solved by 21,179 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published 📝: January 9, 2026

## Challenge Summary 🧩
This challenge tests your understanding of [`"endianness"`](https://www.freecodecamp.org/news/what-is-endianness-big-endian-vs-little-endian/)—how multi-byte data is ordered in memory—by having you convert a short string into its [`"hexadecimal"`](https://www.techtarget.com/whatis/definition/hexadecimal) form and reason about [`"little endian"`](https://www.geeksforgeeks.org/dsa/little-and-big-endian-mystery/) vs. [`"big endian"`](https://www.geeksforgeeks.org/dsa/little-and-big-endian-mystery/) representations. You’ll rely on an [`"ASCII table"`](https://www.asciitable.com/) to translate characters to bytes, then apply the correct byte order to produce each representation. The core skill is reading a prompt carefully and matching the exact byte-order expectation the challenge is asking for.

---

## Key Objective 🎯
Produce the correct `"little endian"` and `"big endian"` byte-string representations of the given input by translating characters to `"hexadecimal"` via an `"ASCII table"` and applying the appropriate `"endianness"` rule.

---

## Prerequisites & Tools 🔧
- Understanding of `"endianness"`
- Knowledge of `"little endian"` and `"big endian"`
- Access to an `"ASCII table"`
- Familiarity with `"hexadecimal"` conversion
- Ability to connect with [`"nc"`](https://phoenixnap.com/kb/nc-command) if the challenge provides a remote service

---

## Walkthrough 🚀 (with WHY)

1. **Open the prompt and (if applicable) connect to the remote service with `"nc"` (e.g., `titan.picoctf.net 60471`).**  
   **WHY:** Seeing the exact instructions and sample I/O ensures you’re matching the required format before doing any conversions. If a host/port is given, using `"nc"` lets you view the interactive prompt and how answers should be submitted.  
   <img width="930" height="196" alt="image" src="https://github.com/user-attachments/assets/877222d3-9a16-4882-8ebe-cdecf753e785" />
  
       Caption: Terminal session showing "nc" connected to the challenge and displaying the instructions.

2. **Write down the given string and translate each character to its `"hexadecimal"` using an `"ASCII table"`.**  
   **WHY:** The endianness operations work on bytes, so you need the exact byte values first; converting with an `"ASCII table"` prevents mistakes from guessing or mixing up decimal vs. hex.  
   <img width="1080" height="737" alt="image" src="https://github.com/user-attachments/assets/4d63f6d9-36ce-4d57-8590-fb4d5c46dc48" />
  
       Caption: Using an "ASCII table" to map each character in the provided string to its hex byte.

3. **Form the byte sequence and compute the `"little endian"` representation by reversing the order of byte pairs.**  
   **WHY:** In `"little endian"`, the least significant byte appears first; treat each byte as two hex digits and reverse byte order—not individual hex nibbles.  
   *Example:* the string “vipsl” maps to hex bytes `76 69 70 73 6C`, which becomes `6C 73 70 69 76` when reversed (i.e., `6C73706976` concatenated).  
   <img width="886" height="229" alt="image" src="https://github.com/user-attachments/assets/aa0b775b-e6bc-4784-99a8-ffaaa1e0663e" />
  
       Caption: Reversing the byte order to produce the little-endian hex "6C 73 70 69 76" (shown as "6C73706976" when concatenated).

4. **Confirm the `"big endian"` representation as the original byte order.**  
   **WHY:** In `"big endian"`, the most significant byte appears first, so the original left-to-right byte sequence is already correct (e.g., `76 69 70 73 6C`, which is `766970736C` concatenated).  
  <img width="869" height="280" alt="Screenshot 2025-09-09 124827" src="https://github.com/user-attachments/assets/fd89a717-7af8-42c5-9176-69b668ebc698" />
 
       Caption: Keeping the original byte order as the big-endian hex "63 62 73 6a 78" (shown as "6362736a78" when concatenated).
   
---

## Common Mistakes ⚠️
- Reversing in fixed 4-byte words because of a generic article when the prompt actually expects reversing every single byte, which yields the wrong little-endian result.  
- Flipping individual hex digits instead of whole bytes (two hex digits), which corrupts the intended byte order and produces an invalid representation.  
- Ignoring strict output formatting (e.g., including spaces or uppercase letters) even though the checker requires an exact hex format.

---

## Lessons Learned ✅
- Always confirm whether the task expects per-byte ordering or fixed-width word ordering, because applying the wrong assumption is a common source of errors.  
- Not everything online fits every problem: verify advice against the prompt’s context so your use of `"endianness"` rules matches the challenge.  
- When in doubt, rely on an `"ASCII table"` and careful, step-by-step conversions to avoid preventable mistakes.
