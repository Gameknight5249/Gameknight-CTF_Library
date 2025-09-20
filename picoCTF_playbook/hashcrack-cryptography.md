# hashcrack

## Category 🔐: Cryptography
## Difficulty 🟢: Easy
## Solves as of: September 10, 2025  — <img width="948" height="903" alt="image" src="https://github.com/user-attachments/assets/26b3d9d3-8f27-4e19-b7ae-54d69ade3097" />

    Caption: This challenge has been solved by 24,700 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published 📝: September 19, 2025

## Challenge Summary 🧩
You connect to a remote challenge service that presents multiple [`"hashes"`](https://www.techtarget.com/searchdatamanagement/definition/hashing). The core skill is recognizing the underlying [`"hash algorithm"`](https://www.okta.com/identity-101/hashing-algorithms/) from cues like length and character set, then using appropriate tools to recover the original texts associated with the `"hashes"` so you can progress.

---

## Key Objective 🎯
Identify each `"hash algorithm"`, recover the corresponding plaintexts, and submit them to the service until the final flag is revealed.

---

## Prerequisites & Tools 🔧
- Ability to connect with [`"nc"`](https://www.varonis.com/blog/netcat-commands) to a remote host and port.
- Working understanding of `"hashes"` and basic `"hash algorithm"` identification.
- Familiarity with [`"MD5"`](https://www.avast.com/c-md5-hashing-algorithm), [`"SHA-1"`](https://www.encryptionconsulting.com/education-center/what-is-sha/), and [`"SHA-256"`](https://medium.com/@ftieben/sha-256-explained-b804881c7e4d#:~:text=SHA%2D256%20is%20a%20cryptographic,to%20get%20the%20original%20input.).
- Online utilities used (from the solve):
  - [`MD5 Encrypt/Decrypt:`](https://10015.io/tools/md5-encrypt-decrypt)
  - [`SHA-1 Encrypt/Decrypt:`](https://md5hashing.net/hash/sha1/b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3)
  - [`SHA-256 Encrypt/Decrypt:`](https://10015.io/tools/sha256-encrypt-decrypt#google_vignette)

## Walkthrough 🚀 (with WHY)

1) **Connect to the challenge service with `"nc"` using the host and port from the prompt.
   **WHY:** Establishing the connection is required to receive the first `"hash"` and interact with the service.
   
   <img width="791" height="159" alt="image" src="https://github.com/user-attachments/assets/a1b833bb-a5fc-4179-ba4c-1c6d4f1b8dd0" />
  
       Caption: Connected via "nc" to the challenge server and received the first hash to process.

2) **Identify the presented `"hash algorithm"` (e.g., by length/format cues such as 32 hex for `"MD5"`, 40 hex for `"SHA-1"`, 64 hex for `"SHA-256"`).** **WHY:** Correct identification ensures you use a matching tool and avoid wasted attempts with the wrong decoder.

     <img width="784" height="156" alt="Screenshot 2025-09-10 121925" src="https://github.com/user-attachments/assets/f5752e02-3cb2-4d73-b657-c67001a7f72e" />

        Caption: This hash has 32 hex thus it is a "MD5" hash
      
3) **Use a suitable online tool for the detected algorithm to recover the plaintext from the `"hash"`.** **WHY:** The service expects the original text; using a matching decoder streamlines retrieval and reduces guesswork.
   
<img width="1919" height="943" alt="image" src="https://github.com/user-attachments/assets/18394b47-94e8-421c-a7a3-0380239211e5" />
 
       Caption: Used an online decoder for the identified algorithm to retrieve the plaintext from the hash.

4) **Submit the recovered plaintext back to the service session; repeat for each new `"hash"` until the final message appears.** **WHY:** Each correct submission advances the session; after several rounds, the service provides the final output containing the flag.
   
<img width="923" height="245" alt="image" src="https://github.com/user-attachments/assets/effb1455-8a64-46ae-b8e5-85bf2916a4f3" />

       Caption: Entered the recovered plaintext in the service, which accepted it and provided the next hash.
   
  <img width="1069" height="579" alt="Screenshot 2025-09-10 122843" src="https://github.com/user-attachments/assets/768bb575-63f9-4034-bdc4-a15ba5ae6e70" />

       Caption: After completing all rounds, the service displayed the final flag.

## Common Mistakes ⚠️
- Neglecting to check the length and format of the `"hashes"`, which leads to picking the wrong algorithm and wasting time.  
- Copying a `"hash"` with trailing spaces/newlines, causing decoders to reject the input or return incorrect results.  
- Assuming a single decoder works for all algorithms instead of matching the tool precisely to the detected `"hash algorithm"`.

## Lessons Learned ✅
- Rapid recognition of the `"hash algorithm"`—often from length and character set—dramatically speeds up decoding and reduces trial-and-error.  
- Keeping reliable decoders for `"MD5"`, `"SHA-1"`, and `"SHA-256"` readily available creates an efficient loop from reception to submission.  
- A tight loop of connect → identify → decode → submit is an effective pattern for service-based `"hash"` challenges.
