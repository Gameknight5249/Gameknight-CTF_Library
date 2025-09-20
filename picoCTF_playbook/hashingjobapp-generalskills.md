# HashingJobApp

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: September 13, 2025 — <img width="1279" height="683" alt="image" src="https://github.com/user-attachments/assets/8cfcb815-e2cb-4c5c-9268-78d53d9910e4" />


    Caption: This challenge has been solved by 52,699 players, showing it is widely completed and designed as an introductory problem.

## Guide Published 📝: September 20, 2025

---

## Challenge Summary 🧩
A challenge centered on [`"hashing"`](https://www.codecademy.com/resources/blog/what-is-hashing) with [`"MD5"`](https://www.avast.com/c-md5-hashing-algorithm), where correctness of computed digests is the core skill being tested. The `"flag"` appears after submitting correct results across multiple prompts.

---

## Key Objective 🎯
Produce correct `"MD5"` digests for the strings provided by the service and submit them through the active connection until the flag is revealed.

---

## Prerequisites & Tools 🔧
- Conceptual understanding of `"MD5"` and how it differs from encryption.
- Ability to connect to remote services with [`"nc"`](https://www.varonis.com/blog/netcat-commands).
- Access to an [`"online hash tool"`](https://www.md5hashgenerator.com/) that computes `"MD5"` for pasted input.

---

## Walkthrough 🚀 (with WHY)
1. **Connect to the service with `"nc"` at `saturn.picoctf.net 52179`.**  
   **WHY:** Opening the live session lets you receive the exact string the server wants you to hash.  
   <img width="744" height="63" alt="image" src="https://github.com/user-attachments/assets/0fd255cd-f5b1-43a8-b43b-4a7b9cfa7e8a" />

       Caption: Connected via "nc" to the challenge host and received the first prompt.


2. **Copy the provided string exactly and compute its `"MD5"` hash using an `"online hash tool"`.**  
   **WHY:** A `"online hash tool"` makes it easier and faster to compute the `"MD5"` hash
   <img width="1764" height="808" alt="image" src="https://github.com/user-attachments/assets/be8d5670-3f9e-4b4a-8110-6e93bdf417a0" />

       Caption: The online tool shows the "MD5" digest for the exact input string.

3. **Paste the resulting digest back into the open `"nc"` session.**  
   **WHY:** Submitting the correct digest advances you to the next round and confirms your process is accurate.  
   <img width="768" height="152" alt="image" src="https://github.com/user-attachments/assets/0ff004ec-788c-4ed8-b965-214e612790dc" />
  
       Caption: The service accepts the submitted "MD5" digest and presents the next prompt.

4. **Repeat the hash-and-submit cycle three to four times until completion.**  
   **WHY:** The challenge is structured as several short rounds to verify consistency and attention to detail under repetition.  
   <img width="711" height="364" alt="Screenshot 2025-09-13 181320" src="https://github.com/user-attachments/assets/93c86e56-bfef-4957-8d99-2d228c668e9d" />
 
       Caption: After several correct rounds, the service indicates final progression.

---

## Common Mistakes ⚠️
- Copying only part of the prompt or adding a trailing space/newline, which changes the digest and produces an incorrect result.
- Using the wrong algorithm (e.g., computing a SHA digest instead of `"MD5"`), which will never match the expected answer.
- Altering letter case or punctuation in the input string, since even a tiny change yields a completely different `"MD5"` value.

---

## Lessons Learned ✅
- Precise input handling matters—`"hashing"` maps the **exact** input to its digest, so meticulous copy-paste discipline is essential.
- A calm, methodical rhythm across repeated rounds reduces avoidable errors and speeds overall completion.
- Understanding what `"MD5"` is (a one-way digest) clarifies why you compute a hash rather than “decrypt” anything in this workflow.
