# Challenge Name: flag_shop

## Category 📚: General Skills
## Difficulty 🟡: Medium
## Solves as of: September 6, 2025 — <img width="1272" height="621" alt="image" src="https://github.com/user-attachments/assets/8c8532a6-33d7-42ec-bc13-8f7e801b1ae5" />

    Caption: This challenge has been solved by 30,770 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published: September 18, 2025

---

## Challenge Summary 🧩
This challenge is a menu-driven shop where you connect remotely and “buy” items. The core vulnerability hinges on [`"integer overflow"`](https://www.sciencedirect.com/topics/computer-science/integer-overflow) and how balances are stored as signed values under [`"two's complement"`](https://www.cs.cornell.edu/~tomf/notes/cps104/twoscomp.html). By connecting with [`"netcat"`](https://www.varonis.com/blog/netcat-commands) and purchasing an extreme quantity of a cheap item, you can wrap the balance and afford the premium flag.

---

## Key Objective 🎯
Exploit `"integer overflow"` in the shop’s signed balance to **increase** money via wraparound, then purchase the premium flag.

---

## Prerequisites & Tools 🔧
- A way to connect via `"netcat"` to the remote host/port.
- Conceptual grasp of `"two's complement"` and how signed wraparound occurs.
- Familiarity with [`"signed integers"`](https://www.ibm.com/docs/en/aix/7.2?topic=types-signed-unsigned-integers) vs [`"unsigned integers"`](https://www.ibm.com/docs/en/aix/7.2?topic=types-signed-unsigned-integers) for reasoning about wrap behavior.  
- Comfort skimming C source to spot fragile arithmetic and I/O patterns like [`"scanf()"`](https://www.geeksforgeeks.org/c/scanf-in-c/) and [`"printf()"`](https://www.geeksforgeeks.org/c/printf-in-c/).

---

## Walkthrough 🚀 (with WHY)
1. **Connect to the shop service using "netcat".**  
   **WHY:** Interacting with the live service lets you confirm the menu options (e.g., a cheap decoy flag and an expensive premium flag) and observe how your balance changes after purchases.  
   <img width="715" height="566" alt="image" src="https://github.com/user-attachments/assets/07e56e39-d598-4fe5-a536-b5d4bb630e76" />

       Caption: Connected to the remote store via "netcat" and viewing the menu with starting balance.

2. **Explore the menu and note the prices of items (decoy vs. premium flag).**  
   **WHY:** Understanding price points clarifies the target: the premium “1337” flag is intentionally out of reach unless you can manipulate the balance.  
   <img width="617" height="374" alt="image" src="https://github.com/user-attachments/assets/995fc119-9626-497d-aef3-367a5cce29f7" />
   <img width="639" height="354" alt="image" src="https://github.com/user-attachments/assets/97535a23-4935-46da-9fa4-71cbcaac4134" />

       Caption: Menu shows a cheap decoy flag and an expensive premium “1337” flag, setting up the overflow route.

3. **Choose the option to buy the decoy flag (the cheap one).**  
   **WHY:** The shop asks “how many?” for this item; this input is your leverage to trigger `"integer overflow"` on the balance.  
   <img width="511" height="141" alt="image" src="https://github.com/user-attachments/assets/16b12221-1b9d-4ce1-adb9-6562100dabab" />

       Caption: Purchase prompt for the decoy flag where the quantity input will drive the overflow.

4. **When prompted for quantity, enter an extremely large number, e.g., "100000000000000000" (17 zeros).**  
   **WHY:** If the program stores balances in a 32-bit `"signed integers"` variable, multiplying price × quantity can overflow under `"two's complement"`. The wraparound can flip a huge negative into a large positive net effect on your balance.  
   <img width="559" height="473" alt="image" src="https://github.com/user-attachments/assets/912a8d39-abb0-4374-afae-42569d9e1b19" />

       Caption: After entering a huge quantity, arithmetic wraps and the balance increases due to integer overflow.

5. **Return to the menu and select the premium “1337” flag.**  
   **WHY:** With the inflated balance, the purchase should succeed and the service will display the flag.  
 <img width="531" height="382" alt="Screenshot 2025-09-06 224423" src="https://github.com/user-attachments/assets/72673740-1909-4efe-82e8-780033e4b3a7" />
  
       Caption: Successful purchase of the “1337” flag after overflow; the service prints the flag.

---

## Common Mistakes ⚠️
- Trying to *edit* the provided source to “print the flag” instead of exploiting the running service’s logic. The challenge expects interaction, not modification.  
- Ignoring service messages like “flag not found on this server,” which hint that the flag is only available via the live purchase path.  
- Attempting to directly change stored variables in code rather than leveraging `"two's complement"` wraparound through the input quantity.  
- Skipping research on how `"signed integers"` behave at limits, which makes overflow strategies feel like “guessing” instead of controlled exploitation.

---

## Lessons Learned ✅
- `"Integer overflow"` is a practical exploitation primitive: when prices and balances use `"signed integers"`, oversized quantities can wrap arithmetic and invert affordability.  
- Understanding `"two's complement"` turns “magic numbers” into predictable triggers—you’re not brute forcing; you’re steering wraparound.  
- CTFs reward exploiting system **logic**—not altering code—so reading inputs, limits, and arithmetic types is often the fastest path to a solve.



