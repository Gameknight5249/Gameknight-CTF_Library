# Verify

## Category 🕵️: Forensics
## Difficulty 🟢: Easy
## Solves as of: January 19, 2026 — <img width="1288" height="702" alt="image" src="https://github.com/user-attachments/assets/f8ee411b-7977-49a5-9cc5-27dea115f439" />

    Caption: This challenge has been solved by 57007 players, showing it is widely completed and designed as an introductory problem.
## Guide Published 📝: February 7th, 2026

---

## Challenge Summary 🧩
This challenge trains you to confirm authenticity using [`"SHA-256"`](https://medium.com/@madan_nv/a-deep-dive-into-sha-256-working-principles-and-applications-a38cccc390d4) checksums so you don’t get fooled by lookalike outputs. The key skill is validating files by comparing their hashes against a known-good checksum, which matters in real forensics because verification comes before trusting any decrypted or extracted content.

---

## Key Objective 🎯
Identify the one file whose `"sha256sum"` matches the provided checksum, then decrypt it to reveal the legitimate flag.

---

## Prerequisites & Tools 🔧
- Ability to connect via [`"ssh"`](https://www.cloudflare.com/learning/access-management/what-is-ssh/)
- Basic comfort with file listings like [`"ls"`](https://itsfoss.com/ls-command/)
- [`"sha256sum"`](https://www.computerhope.com/unix/sha256sum.htm) to compute file hashes
- The provided `"decrypt.sh"` script

---

## Walkthrough 🚀 (with WHY)

1. Connect to the remote server using `"ssh"` with the provided host, port, username, and password.
    **WHY:** The files you need to verify and decrypt are hosted remotely, so you must access the environment where `"files/"` and `"decrypt.sh"` exist.
    
    <img width="798" height="582" alt="image" src="https://github.com/user-attachments/assets/ee7f8c2a-1875-403c-911f-1d4714ddf987" />

        Caption: The SSH connection succeeds, confirming you’re in the correct challenge environment.

2. Run `"ls"` to confirm you can see the `"files"` directory and the `"decrypt.sh"` script.
    **WHY:** Verifying the expected files are present prevents you from hashing or decrypting in the wrong location.
    
    <img width="283" height="86" alt="image" src="https://github.com/user-attachments/assets/34193611-b758-4999-a9e3-779dfc3fb376" />

        Caption: The directory listing shows the files folder and the decrypt script needed for the challenge.

3. Compute hashes for every file in `"files/"` using `"sha256sum files/*"`.
    **WHY:** This produces a list of SHA-256 hashes so you can compare each candidate file against the known checksum provided in the directions.
    
    <img width="905" height="1221" alt="image" src="https://github.com/user-attachments/assets/f6876453-2fed-425f-985f-177a2bff967a" />

        Caption: The command outputs SHA-256 hashes for all files in the folder, giving you the dataset needed for checksum matching.

4. Find the one hash that exactly matches the provided checksum and note the corresponding filename. (its in the middle)
    **WHY:** The matching checksum proves which file is legitimate, so you only decrypt the verified file instead of wasting time on decoys.
    
   <img width="751" height="359" alt="Screenshot 2026-02-07 133428" src="https://github.com/user-attachments/assets/438d1fc9-efbd-4e6a-9ae0-1e972a8eedc8" />
 
        Caption: The correct file is identified by an exact checksum match, confirming it’s the legitimate one to decrypt.

5. Decrypt the verified file using `"./decrypt.sh files/<file>"`.
    **WHY:** The decrypt script is the intended way to transform the verified encrypted content into the readable flag output.
    
  <img width="491" height="61" alt="Screenshot 2026-02-07 133747" src="https://github.com/user-attachments/assets/9dabc669-9da1-443d-9f70-b84117851ece" />
 
        Caption: The decrypt script successfully reveals the flag after the correct file is verified by checksum.

---

## Common Mistakes ⚠️
- Decrypting the wrong file because you didn’t confirm an exact checksum match before running `"./decrypt.sh"`.
- Typing the `"./decrypt.sh files/<file>"` path incorrectly, which causes errors even when you found the right checksum.
- Ignoring the checksum hint early and trying random decrypt attempts first, which slows the solve and adds confusion.

---

## Lessons Learned ✅
- `"Checksums"` let you verify authenticity before trusting content, which is a core habit in forensics and secure workflows.
- `"sha256sum"` can be used on a single file or across a directory to quickly compare candidates against a known-good checksum.
- Understanding the meaning of `"./decrypt.sh files/<file>"` makes command-based challenges faster because you can reason about paths and scripts instead of guessing.
