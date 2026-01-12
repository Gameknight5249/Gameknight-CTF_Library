# 13

## Category 🔐: Cryptography
## Difficulty 🟢: Easy
## Solves as of: January 12, 2026 — <img width="948" height="672" alt="image" src="https://github.com/user-attachments/assets/5e63ee4e-8d22-4928-811c-bb1997e705d5" />

    Caption: This challenge has been solved by 100,172 players, showing it is widely completed and designed as an introductory problem.

## Guide Published 📝: January 12, 2026

## Challenge Summary 🧩
This challenge introduces [`"ROT13"`](https://infosecwriteups.com/understanding-rot13-encryption-method-2023-cfea53b21770), a simple substitution cipher that shifts letters by 13 positions. It’s a quick way to practice recognizing common “toy” ciphers and confidently using the right decoder when the hint tells you exactly what to apply.

---

## Key Objective 🎯
Decode the provided ciphertext using `"ROT13"` to recover the flag.

---

## Prerequisites & Tools 🔧
- A web browser
- An online [`"ROT13 decoder"`](https://cryptii.com/pipes/rot13-decoder)

## Walkthrough 🚀 (with WHY)
1. Identify the cipher from the prompt and hint as `"ROT13"`.
   **WHY:** When a challenge explicitly names the cipher, you should trust the hint and avoid overcomplicating the solution.
   <img width="948" height="672" alt="Screenshot 2026-01-12 143951" src="https://github.com/user-attachments/assets/004a7d1e-95cc-4d8e-9a3d-5837c97aa9f9" />

       Caption: The type of encryption is within the prompt, which makes the challenge easy.

3. Open an online `"ROT13 decoder"` and paste in the ciphertext: `cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}`.
   **WHY:** A `"ROT13 decoder"` instantly reverses the 13-shift, letting you validate the result without writing any code for a basic intro challenge.  
  <img width="1215" height="755" alt="Screenshot 2026-01-12 144738" src="https://github.com/user-attachments/assets/aef83f8e-4fb6-4b2a-80f7-bf3ae5843903" />

       Caption: The online decoder is ready to transform the pasted ROT13 ciphertext into readable text.


## Common Mistakes ⚠️
- Copying extra whitespace or missing characters in the ciphertext causes the `"ROT13 decoder"` output to look wrong or incomplete.
- Using the wrong transform (like Base64 tools) wastes time because the prompt explicitly points to `"ROT13"`.
- Forgetting that `"ROT13"` only shifts letters can confuse you if you expect symbols/braces to change, since punctuation typically stays the same.

## Lessons Learned ✅
- `"ROT13"` is a fast “recognition” cipher, so reading the prompt carefully is often the real challenge.
- When the cipher is named directly, using a trusted `"ROT13 decoder"` is the most efficient and reliable approach.
- Confirming the decoded output matches the expected flag structure is a quick correctness check before submitting.
