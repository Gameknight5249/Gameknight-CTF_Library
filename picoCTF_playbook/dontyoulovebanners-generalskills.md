# dont-you-love-banners

## Category 📚: General Skills
## Difficulty 🟡: Medium
## Solves as of: January 17, 2026 — <img width="1282" height="681" alt="image" src="https://github.com/user-attachments/assets/e70ecc1f-b53b-48f1-a7dd-2227b15c92c2" />

    Caption: This challenge has been solved by 12,090 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published 📝: January 18, 2026

---

## Challenge Summary 🧩
This challenge demonstrates how a poorly handled `"banner"` file can be abused to expose sensitive data. By using [`"symlinks"`](https://cambass.medium.com/understanding-symlinks-and-a-common-use-case-for-linux-4013cd0e695d) to redirect what the program reads, you can trick the server into showing the flag.

---

## Key Objective 🎯
Use `"symlinks"` to redirect a required `"banner"` file to the flag location and reveal the flag.

---

## Prerequisites & Tools 🔧
- Ability to connect to remote services using [`"nc"`](https://phoenixnap.com/kb/nc-command)
- Comfort navigating Linux directories with `"ls -la"` and `"cd"`
- Basic understanding of `"root"` as a protected directory
- Know how to create `"symlinks"` using [`"ln -s"`](https://linuxize.com/post/how-to-create-symbolic-links-in-linux-using-the-ln-command/)

---

## Walkthrough 🚀 (with WHY)

1. Connect to the server that is leaking information.
   **WHY:** The leaked information contains what you need to successfully authenticate into the second service.
   
  <img width="555" height="67" alt="image" src="https://github.com/user-attachments/assets/a26c51aa-09bb-410e-97f2-bc277ea74eeb" />

    Caption: The first connection shows leaked details that will be used as the password for the second server.

2. Connect to the running application using `"nc"` on the provided host and port, then enter the leaked password.
   **WHY:** The second server is gated by the leaked password, and entering it is how you progress into the interactive environment.
   
   <img width="521" height="192" alt="image" src="https://github.com/user-attachments/assets/b80ae829-b4ce-45c4-b685-89b0c428847e" />

       Caption: The second server prompts for a password, and entering the leaked value grants access.

3. Answer the next two questions using `"DEFCON"` and `"John Draper"` (Required research to find answers.
   **WHY:** These answers are required to pass the prompt and get fully connected to the environment.
   
   <img width="709" height="116" alt="image" src="https://github.com/user-attachments/assets/0482ba52-708d-4d9a-852e-98c390fda924" />

       Caption: The application accepts the answers and proceeds to the shell environment.

4. Confirm you are connected, then list files with `"ls -la"`.
   **WHY:** You need visibility into the filesystem layout so you can identify where `"root"` and other relevant paths exist.
   
   <img width="501" height="226" alt="image" src="https://github.com/user-attachments/assets/0bebf43f-b08a-401d-9b76-1aac1118d5b1" />

       Caption: The directory listing shows available folders, including the root directory.

5. Move into the `"root"` directory using `"cd /root"`, then list files again with `"ls -la"`.
   **WHY:** The flag is in the root directory per the directions, so you must navigate there to find what the program is protecting.
   
   <img width="470" height="264" alt="image" src="https://github.com/user-attachments/assets/dada6349-1858-4a15-9d84-92ccf28fd668" />

       Caption: The root directory listing reveals files you can inspect, including the script referenced next.

6. View `"script.py"` using `"cat script.py"` and locate the message about supplying a banner at `/home/player/banner`.
   **WHY:** The script tells you exactly which file path the program reads, which is the key leverage point for a symlink-based trick.
   
   <img width="1027" height="803" alt="image" src="https://github.com/user-attachments/assets/f94680cb-f93a-4e2a-935b-39ec4d2ecec6" />

       Caption: The script output includes the instruction to supply the banner at /home/player/banner.

7. Remove the existing banner file using `"rm -rf"`.
   **WHY:** Removing it clears the path so you can replace it with a symlink that points somewhere more valuable.
   
   <img width="444" height="72" alt="image" src="https://github.com/user-attachments/assets/494d1f1c-57ed-4a10-8def-99874fa64055" />

       Caption: The banner path is cleared so it can be replaced with a symlink.

8. Create a `"symlink"` from `/root/flag.txt` to `/home/player/banner` using `"ln -s"`.
   **WHY:** This redirects the program’s banner read to the flag file, so when the program loads the banner, it effectively reveals the flag.
   
   <img width="576" height="56" alt="image" src="https://github.com/user-attachments/assets/ab333635-24d2-42cc-a2ec-126063a85e18" />

       Caption: The symlink is created so the banner path now points to the flag file.

9. Exit the server using `"Ctrl + C"`, then reconnect to the server.
   **WHY:** Reconnecting triggers the application to read the banner again, which now resolves to the flag through the symlink.
   
   <img width="592" height="89" alt="Screenshot 2026-01-18 105901" src="https://github.com/user-attachments/assets/be25512f-dcb8-469e-848f-a6d979f5814c" />

       Caption: After reconnecting, the application reads the banner path and prints the flag because it now points to the flag file.

---

## Common Mistakes ⚠️
- Confusing `"ln"` and `"ls"` slows progress because you need `"ln -s"` specifically to create a symlink.
- Getting stuck navigating `"root"` wastes time because the solve requires entering `/root` to find the flag and understand the script behavior.
- Overthinking the purpose of the first server delays the solve because its main value is the leaked password for the second server.
- Not searching the trivia answers wastes time because `"DEFCON"` and `"John Draper"` are quick lookups required to proceed.

---

## Lessons Learned ✅
- Using `"ln -s"` enables powerful file redirection tricks because a symlink can make a program read a different file than intended.
- Reading helper files like `"script.py"` is high-leverage because it reveals exact file paths and expectations the program enforces.
- Recognizing when a step is just a gate (like trivia prompts) improves speed because you can resolve it quickly and focus on the real exploit path.
