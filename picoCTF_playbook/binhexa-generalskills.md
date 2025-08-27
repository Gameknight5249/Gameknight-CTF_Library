# Challenge Name: binehexa

## Category 📚: General Skills

## Difficulty 🟢: Easy

## Solves as of: August 24, 2025 — <img width="1278" height="671" alt="Screenshot 2025-08-24 222632" src="https://github.com/user-attachments/assets/c9d3b6e0-e22b-48f6-ac2e-54c0128449a0" />

  
    Caption: This challenge has been solved by 21,255 players, indicating it is a popular challenge that many players were able to complete.

## Guide Published 📝: August 24, 2025

---

## Challenge Summary 🧩
This challenge focuses on building fluency with binary math and conversions. By practicing arithmetic and bitwise operations directly in binary and then converting the final result to hexadecimal, you strengthen a foundational skill used in reverse engineering, exploit analysis, and low-level debugging.

---

## Key Objective 🎯 
Develop fluency in binary arithmetic and strengthen your ability to interpret results through hexadecimal representation — a foundational skill for solving low-level CTF challenges.

---

## Prerequisites & Tools 🔧
- [`"binary operations"`](https://www.geeksforgeeks.org/digital-logic/arithmetic-operations-of-binary-numbers/) — understanding addition, subtraction, multiplication, division in binary  
- [`"bitwise operations"`](https://sudorudo.medium.com/bitwise-for-dummies-c1b996c21cbc) — understanding left and right shift  
- [Binary Calculator](https://www.rapidtables.com/calc/math/binary-calculator.html) — for verifying operations  
- [Binary to Hexadecimal Converter](https://www.rapidtables.com/convert/number/binary-to-hex.html) — for final conversion  
- [Bit Shift Calculator](https://circuitdigest.com/calculators/bit-shift-calculator)
---

## Walkthrough 🚀 (with WHY)

1. **Connect to the challenge instance**  
   **WHY:** The server provides you with binary numbers and prompts you for specific operations.  
   <img width="549" height="41" alt="Screenshot 2025-08-24 223151" src="https://github.com/user-attachments/assets/34622e0a-1569-4b38-9713-9d6ff8baa7cb" />
  
       Caption: Connected to challenge instance via `nc titan.picoctf.net 56332`.  

2. **Read the first binary problem**  
   **WHY:** The prompt gives you two binary numbers and an operation (e.g., addition).  
   <img width="1039" height="239" alt="Screenshot 2025-08-25 194949" src="https://github.com/user-attachments/assets/28df3c3b-f900-48cc-9d4b-d621910e4502" />
  
       Caption: Example binary operation prompt with two numbers.  

3. **Solve using a binary calculator**  
   **WHY:** While you could solve by hand, a calculator ensures accuracy and speed during a timed CTF.  
  <img width="928" height="379" alt="Screenshot 2025-08-25 195221" src="https://github.com/user-attachments/assets/e1efe378-88b9-412f-93d6-3b5f40f060dd" />

       Caption: Binary addition performed in an online calculator.  

4. **Read the second binary problem**
   **Why:** The prompt gives you two binary numbers and a bitwise operation (e.g., right-shift)
<img width="442" height="97" alt="Screenshot 2025-08-25 195717" src="https://github.com/user-attachments/assets/9f3df96d-9be4-4796-bd1f-7afc90ef67ab" />

       Caption: Example bitwise operation prompt with two numbers.
   
5. **Perform bitwise operations (e.g., right shift)**  
   **WHY:** The challenge mixes arithmetic and bitwise operations, so knowing both is necessary.  
   <img width="713" height="685" alt="Screenshot 2025-08-25 200106" src="https://github.com/user-attachments/assets/d33f86f1-bbed-4fcb-88d0-b3fa7500bc57" />
  
       Caption: Result of left-shifting the first binary number.  

6. **Repeat for all given operations**  
   **WHY:** The challenge cycles through about six different binary/bitwise tasks. Completing each correctly progresses you.  
   <img width="1049" height="916" alt="Screenshot 2025-08-26 192741" src="https://github.com/user-attachments/assets/70167feb-1522-4808-b0ca-bb13ad332560" />
  
       Caption: Series of binary operation prompts completed step by step.  

7. **Convert binary to hexadecimal for the final step**  
   **WHY:** The last conversion unlocks the flag. Using an online converter ensures quick, accurate transformation.  
   <img width="507" height="152" alt="Screenshot 2025-08-26 192915" src="https://github.com/user-attachments/assets/0dcf1c33-82e2-43a9-98f5-89958287fb1c" />
  

       Caption: Binary number converted to hexadecimal using an online tool.  

---

## Common Mistakes ⚠️ 
- Misinterpreting bitwise operations (especially left/right shift vs arithmetic operations).  
- Entering results in decimal instead of binary.  
- Forgetting to include leading zeros when needed.  
- Skipping verification of results before entering them into the shell.  

---

## Lessons Learned ✅
- Binary operations are easier with a calculator during competitions, but understanding the theory helps avoid mistakes.  
- Bitwise shifts are not the same as multiplication/division — always double-check.  
- Converting between binary and hexadecimal is a common CTF skill worth practicing.  
