# PW Crack 2

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: October 10, 2025 — <img width="1277" height="663" alt="image" src="https://github.com/user-attachments/assets/3efaf1dd-70eb-44a6-872b-dd4112e48dba" />

    Caption: This challenge has been solved by 64,172 players, showing it is widely completed and designed as an introductory problem.
## Guide Published 📝: December 20, 2025

---

## Challenge Summary 🧩
This challenge tests whether you recognize that the checker’s logic defines the correct input. Rather than attacking the encrypted output, success comes from understanding how the program validates what you type. It reinforces a common PicoCTF pattern: when source code is available, logic usually matters more than data.

---

## Key Objective 🎯
Identify how a program validates user input by reading its logic and infer the expected value directly from the code.

---

## Prerequisites & Tools 🔧
- Both provided files saved in the same [`"directory"`](https://www.howtogeek.com/117435/htg-explains-the-linux-directory-structure-explained/).
- Ability to run [`"python3"`](https://www.youtube.com/watch?v=s9x_YTTvats) locally.
- Comfort skimming simple `"source code"` and recognizing a `"Unicode code point"` to character mapping via `"chr"`.
- A quick [`"converter"`](https://onlinetools.com/unicode/convert-code-points-to-unicode) (or manual mapping) for code points → characters (e.g., ChatGPT as a fast lookup). 

---

## Walkthrough 🚀 (with WHY)

1) Download the password checker (level2.py) and the encrypted flag file into the same "directory".  
**WHY:** Keeping artifacts together ensures the checker can find the encrypted flag without path issues.

<img width="1562" height="628" alt="image" src="https://github.com/user-attachments/assets/3d3ad3a3-0ebe-47c4-beea-bdaf06dd11f8" />
 
    Caption: The checker and encrypted flag placed in the same "directory" so file lookups succeed.

2) Open the checker’s "source code" and scan for the password creation logic.  
**WHY:** The program itself shows how inputs are validated; here it constructs a string from a series of "chr" calls.

<img width="1059" height="590" alt="Screenshot 2025-10-10 110151" src="https://github.com/user-attachments/assets/d6cf6350-0ce9-4210-9d64-fd009acacf1d" />
 
    Caption: The checker reveals a sequence of "chr" calls that encode the expected password.

3) Extract the integers passed to "chr" and translate each "Unicode code point" into its character (make sure the Code Point Base is in hexadecimal).  
**WHY:** Direct translation reconstructs the exact cleartext password without analyzing the encrypted file’s "encoding".

<img width="1821" height="837" alt="image" src="https://github.com/user-attachments/assets/2f8b1c34-e5e2-4c96-9244-067966de2812" />


    Caption: Converting "Unicode code points" yields the precise password string.

4) Run the checker with "python3" and enter the reconstructed password when prompted.  
**WHY:** Supplying the correct password triggers the program’s success path and decrypts the flag.

<img width="591" height="95" alt="Screenshot 2025-10-10 110941" src="https://github.com/user-attachments/assets/88e341af-d362-4301-ac0e-ef17df0fff03" />

    Caption: Executing with "python3" and providing the recovered password.
    
--- 

## Common Mistakes ⚠️
- Chasing the encrypted file’s "encoding" instead of reading the checker’s "source code", which directly exposes how the password is generated.  
- Forgetting to keep both files in the same "directory", causing file-not-found errors and blocking execution.  
- Miscopying or misinterpreting the numbers passed to "chr", which reconstructs an incorrect password and fails validation.

  ---

## Lessons Learned ✅
- Inspecting "source code" first often exposes the exact inputs needed, saving time over brute analysis of ciphertext.  
- Recognizing patterns like "chr" over "Unicode code point" is a portable skill for rebuilding strings in Python-based challenges.  
- Simple project hygiene—keeping artifacts in one "directory"—prevents avoidable errors and accelerates verification.
