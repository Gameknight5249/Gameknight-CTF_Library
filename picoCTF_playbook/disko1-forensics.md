# Challenge Name: DISKO 1

## Category 🕵️: Forensics  
## Difficulty 🟢: Easy  
## Solves as of: September 3, 2025 — <img width="1277" height="629" alt="image" src="https://github.com/user-attachments/assets/6505d428-fa6b-4912-b327-aa7d9716116e" />
  
    Caption: This challenge has been solved by 15,681 players, indicating it is accessible to many players yet demands persistence to complete.  
## Guide Published 📝: September 6, 2025

## Challenge Summary 🧩  
This challenge provides a compressed [`"disk image"`](https://www.techtarget.com/whatis/definition/disk-image) and asks you to locate the hidden flag. The key skill is recognizing the `".gz"` file format and applying [`"strings"`](https://labex.io/tutorials/linux-linux-strings-command-with-practical-examples-422934) with filtering to extract readable data.

---

## Key Objective 🎯  
Use [`"gunzip"`](https://www.geeksforgeeks.org/linux-unix/gunzip-command-in-linux-with-examples/) to extract a [`".gz"`](https://cloudmersive.com/article/What-is-GZIP-Format-and-What-Risks-does-it-Pose) disk image and combine `"strings"` with [`"grep -i"`](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/) to quickly search for the flag.

---

## Prerequisites & Tools 🔧  
- Familiarity with `"disk image"` handling  
- Ability to use `"gunzip"` for `".gz"` archives  
- Comfort with `"strings"` to extract readable text  
- Using `"grep -i"` to filter results  
- Understanding of [`"pipes"`](https://www.geeksforgeeks.org/linux-unix/piping-in-unix-or-linux/) to chain commands

## Walkthrough 🚀 (with WHY)

1. **Download the challenge file.**  
 **WHY:** You need the provided compressed disk image to begin analysis.  
   <img width="2525" height="351" alt="image" src="https://github.com/user-attachments/assets/c80ad6b1-b6ba-40dc-8ea2-f4ce7075d3e2" />
 
       Caption: Challenge-provided ".gz" disk image saved locally for analysis.

2. **Decompress the file using `"gunzip"`.**  
    **WHY:** The image is in `".gz"` format; extraction is required before scanning its contents.  
   <img width="472" height="97" alt="Screenshot 2025-09-06 141310" src="https://github.com/user-attachments/assets/479ce8e2-d167-4881-8487-046afb758f4b" />
  
       Caption: Successful extraction of the disk image using "gunzip".

3. **Run `"strings"` on the decompressed image.**  
    **WHY:** `"strings"` scans binaries for human-readable text, a common place where flags appear.  
   <img width="488" height="50" alt="image" src="https://github.com/user-attachments/assets/cccf9731-3d9e-45c1-88a3-7f5d478402f1" />
 
       Caption: "strings" output reveals readable substrings from the disk image.
       Caption: Once you use the "strings" command, you will realize why we use "pipe".
 
5. **Pipe `"strings"` into `"grep -i"` to search for the flag.**  
    **WHY:** Using `"pipes"` lets you filter `"strings"` output efficiently; `"grep -i"` ignores case to avoid missing matches.  
  <img width="621" height="71" alt="Screenshot 2025-09-06 142639" src="https://github.com/user-attachments/assets/e3ebdc0d-c2ed-4347-b304-da31465be7b2" />
 
       Caption: Filtered "strings" output via "grep -i" surfaces the flag.

## Common Mistakes ⚠️  
- Not checking how to handle the `".gz"` extension first, leading to confusion before analysis.  
- Using generic editors like `"cat"` or `"nano"` instead of targeted tools, which wastes time.

## Lessons Learned ✅  
- Practiced extracting `".gz"` archives with `"gunzip"`.  
- Learned how to use `"pipes"` to chain commands for faster searching.  
- Strengthened understanding of `"strings"` for pulling readable data out of binary files.
