# Permissions

## Category 📚: General Skills
## Difficulty 🟡: Medium
## Solves as of: October 1, 2025 — <img width="1276" height="684" alt="image" src="https://github.com/user-attachments/assets/8c514f59-8532-44ab-b96f-5eac2bd502d9" />

    Caption: This challenge has been solved by 18,112 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published 📝: October 2, 2025

---

## Challenge Summary 🧩
This challenge teaches how Linux access control and user roles interact by nudging you to move from a normal user to the superuser. You’ll practice verifying identity, checking allowed elevated actions, and using an allowed editor to pivot into a higher-privileged shell to read a protected file.

---

## Key Objective 🎯
Gain `"root"` access long enough to read the protected `"flag.txt"` in `"/root"` by leveraging allowed `"sudo"` capabilities.

---

## Prerequisites & Tools 🔧
- Basic terminal familiarity and comfort reading man pages.
- First-mention concepts/tools:
  - [`"root"`](https://www.baeldung.com/linux/root-user-directory-access#:~:text=In%20Linux%2C%20the%20root%20user,the%20tasks%20of%20a%20superuser.)
  - [`"permissions"`](https://www.redhat.com/en/blog/linux-file-permissions-explained)
  - [`"sudo"`](https://www.beyondtrust.com/blog/entry/unix-linux-privileged-management-should-you-sudo#:~:text=Sudo%20stands%20for%20either%20%22substitute,su%E2%80%9D%20which%20is%20not%20temporary.)
  - [`"sudo -l"`](https://www.geeksforgeeks.org/linux-unix/sudo-command-in-linux-with-examples/)
  - [`"Vim"`](https://www.youtube.com/watch?v=iKp8-S6JiEg)
  - [`"whoami"`](https://phoenixnap.com/kb/whoami-linux)
  - [`"ls"`](https://www.geeksforgeeks.org/linux-unix/ls-command-in-linux/)
  - [`"cat"`](https://phoenixnap.com/kb/linux-cat-command)

---

## Walkthrough 🚀 (with WHY)

1) Connect to the challenge instance provided by picoCTF and authenticate if prompted.  
**WHY:** Establishing a session is required before you can inspect your current privileges and attempt any escalation path.

<img width="901" height="668" alt="image" src="https://github.com/user-attachments/assets/2fa0fea6-1290-4d01-adaa-f366c5b4edac" />
 
    Caption: Connected to the challenge instance and ready to enumerate user context.

2) Run `"whoami"` to confirm your current user.  
**WHY:** Verifying identity sets a baseline; if you’re not `"root"`, you’ll need an escalation path.

<img width="311" height="75" alt="image" src="https://github.com/user-attachments/assets/2dd40af0-8ee3-47e9-8d18-d289732385b9" />
  
    Caption: "whoami" shows the unprivileged user context.

3) Run `"sudo -l"` to list commands you can run with `"sudo"` without a full password or with a provided one. 
**WHY:** `"sudo -l"` reveals allowed elevated actions; any editor or interpreter listed can often be a controlled path to escalation. (the password is in the directions)

<img width="1004" height="153" alt="image" src="https://github.com/user-attachments/assets/de82fd2d-a663-482e-936a-71759fe7fb1c" />
 
    Caption: "sudo -l" enumerates permitted elevated commands for the current user.

4) Launch the allowed editor (e.g., `"sudo vi"` or `"sudo vim"`) as indicated by `"sudo -l"`.  
**WHY:** Many editors support a `"shell escape"`, which can spawn a subshell with the editor’s privileges.

<img width="389" height="28" alt="image" src="https://github.com/user-attachments/assets/8844e79b-a6ba-4212-aa40-44ced16ac0a6" />

<img width="2559" height="1270" alt="image" src="https://github.com/user-attachments/assets/3a369ef1-4f00-4c69-8a27-f372a68ce6be" />

    Caption: "vim" started via "sudo", inheriting elevated privileges.

5) From within `"Vim"`, trigger a `"shell escape"` using `":!bash"` (or `":sh"` depending on configuration).  
**WHY:** A shell escape starts a subshell under the editor’s effective privileges—ideally a `"root"` shell if the editor was run with `"sudo"`.

<img width="2559" height="1270" alt="Screenshot 2025-10-02 202756" src="https://github.com/user-attachments/assets/85710367-4fc2-4dfe-a2b2-a2a88f968bf7" />

 <img width="362" height="51" alt="image" src="https://github.com/user-attachments/assets/7e2ef75f-2f65-428b-ac4f-75314b734851" />

    Caption: Subshell spawned from "vim" using ":!bash".

6) Run `"whoami"` again inside the new shell.  
**WHY:** Confirm that you now have `"root"` privileges before touching protected paths.

<img width="410" height="79" alt="image" src="https://github.com/user-attachments/assets/9bfa2210-ff78-487b-a316-8ae40b6346cc" />

    Caption: "whoami" confirms root privileges after the editor-based escalation.

7) List the superuser’s home directory with `"ls -a /root"` to discover files, including hidden ones.  
**WHY:** The challenge hints at a protected file in `"/root"`; listing confirms file presence and names before reading.

<img width="613" height="65" alt="image" src="https://github.com/user-attachments/assets/28fc2690-f6ef-40cc-a379-73636d598bdc" />
  
    Caption: Root’s home directory listing reveals "flag.txt".

8) Read the flag with `"cat /root/.flag.txt"`.  
**WHY:** With verified access and the file path identified, printing the file outputs the flag to the terminal.

<img width="484" height="65" alt="Screenshot 2025-10-02 203158" src="https://github.com/user-attachments/assets/de5b68aa-d553-4937-ba6f-6b0f3b85cf49" />

    Caption: Displaying the contents of "flag.txt" to obtain the flag.

---

## Common Mistakes ⚠️
- Skipping `"sudo -l"` and missing an easy, intended escalation path via an allowed editor.
- Assuming `"sudo"` is identical to running a command normally, which leads to permission errors on protected paths.
- Forgetting `"ls -a"` and overlooking hidden files that may contain the target or useful hints.
- Exiting `"Vim"` instead of using a `"shell escape"`, which prevents you from inheriting elevated privileges.

---

## Lessons Learned ✅
- Checking `"sudo -l"` early efficiently reveals escalation vectors instead of guessing.
- Editor `"shell escapes"` are powerful; understanding them turns a permitted tool into a controlled privilege escalation.
- Verifying identity with `"whoami"` before and after escalation prevents confusion and confirms success.
