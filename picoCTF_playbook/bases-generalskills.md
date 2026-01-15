# Bases

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: January 12, 2026 — <img width="947" height="682" alt="image" src="https://github.com/user-attachments/assets/f42775d5-255d-4306-b971-14dadeedc3de" />

    Caption: This challenge has been solved by 108,371 players, showing it is widely completed and designed as an introductory problem.
## Guide Published 📝: January 15, 2026

## Challenge Summary 🧩
This challenge focuses on recognizing and decoding [`"base64"`](https://builtin.com/software-engineering-perspectives/base64-encoding), a common text encoding used to represent data in an ASCII-friendly format. 

---

## Key Objective 🎯
Decode the given `"base64"` string and wrap the result in `"picoCTF{}"` to produce the flag.

---

## Prerequisites & Tools 🔧
- A web browser
- An online [`"base64 decoder"`](https://www.base64decode.org/)

## Walkthrough 🚀 (with WHY)
1. Recognize the encoded string as `"base64"` based on the prompt and the character pattern.
   **WHY:** Correctly identifying the encoding early prevents wasted time trying unrelated decoders or overthinking the problem.
   <img width="928" height="668" alt="image" src="https://github.com/user-attachments/assets/693eff53-9925-40a5-b2f5-3919f5fb0c84" />

        Caption: Notice that the encoding is base64
   

3. Open a `"base64 decoder"` and paste in the encoded text: `bDNhcm5fdGgzX3IwcDM1`.
   **WHY:** A decoder quickly converts `"base64"` back into readable text, which is the core skill this challenge is testing.  
   <img width="1211" height="573" alt="image" src="https://github.com/user-attachments/assets/7856977c-3c82-41c4-8a07-c030ca196683" />

       Caption: The base64 decoder is set up with the challenge string ready to be decoded.

4. Decode the text and copy the decoded output.
   **WHY:** The decoded output is the meaningful message you need, and it becomes the inner content of the final flag format.  
  <img width="1213" height="648" alt="Screenshot 2026-01-12 151559" src="https://github.com/user-attachments/assets/bbdc0213-f13a-47a6-9134-057aa36dfe87" />
    
       Caption: The decoded output shows the readable text produced after decoding the base64 input.

5. Format the final submission as `"picoCTF{...}"` using the decoded output inside the braces.
   **WHY:** picoCTF commonly requires a specific wrapper, and submitting only the decoded text would be marked incorrect.  
 <img width="942" height="655" alt="Screenshot 2026-01-12 151743" src="https://github.com/user-attachments/assets/e89c0708-33a6-4d4d-a7f8-63318c371a9a" />
    
       Caption: The decoded text is wrapped in picoCTF{} to match the required flag format.

## Common Mistakes ⚠️
- Submitting the decoded text without wrapping it in `"picoCTF{}"` results in a wrong answer even if the decoding was correct.
- Copying the encoded string with an extra space or missing character causes the `"base64 decoder"` output to be incorrect or empty.
- Assuming `"base64"` must end in `"=="` can distract you, since padding depends on length and may not appear.

## Lessons Learned ✅
- `"base64"` padding like `"=="` depends on the input length, so not seeing it doesn’t mean the string isn’t base64.
- Using a `"base64 decoder"` is the fastest way to validate your encoding guess and move straight to the solution.
- Correct flag formatting (like `"picoCTF{}"`) is part of the challenge, not an afterthought.
