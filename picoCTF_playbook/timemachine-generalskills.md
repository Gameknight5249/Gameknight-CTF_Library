# Time Machine

## Category 📚: General Skills
## Difficulty 🟢: Easy
## Solves as of: January 19, 2026 — <img width="1279" height="664" alt="image" src="https://github.com/user-attachments/assets/8bb940e1-f98c-4fc1-a3ea-40846f0aa632" />

    Caption: This challenge has been solved by 49364 players, indicating it is a popular challenge that many players were able to complete.
## Guide Published 📝: February 7th, 2026

---

## Challenge Summary 🧩
This challenge tests whether you can read a project’s history using [`"git log"`](https://www.freecodecamp.org/news/git-log-command/) instead of searching through files manually. The key skill is recognizing that commit messages and metadata can contain the exact clue you need, which mirrors real debugging and investigation workflows where the fastest answer is often in version history.

---

## Key Objective 🎯
Use `"git log"` to identify the relevant commit information and extract the flag directly from the log output.

---

## Prerequisites & Tools 🔧
- A terminal environment with [`"Git"`](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F) installed
- Ability to unzip the provided archive
- [`"git log"`](https://www.freecodecamp.org/news/git-log-command/) to view commit history
- [`"git show"`](https://git-scm.com/docs/git-show) (optional) to inspect commit details if needed

---

## Walkthrough 🚀 (with WHY)

1. Download `"challenge.zip"` and unzip it.
    **WHY:** The repository history you need is stored inside the extracted folder, so you must unpack it before Git commands will work.
    
    <img width="829" height="1146" alt="image" src="https://github.com/user-attachments/assets/b8efe9e8-7904-4e8b-b2c4-f374dc9db36c" />

        Caption: The challenge files are extracted and ready to be inspected as a Git repository.

2. Change into the extracted directory and run `"git log"`.
    **WHY:** `"git log"` reveals what you were “last working on” by showing commit history, and this challenge places the flag directly in that output.
    
  <img width="787" height="149" alt="Screenshot 2026-01-19 101231" src="https://github.com/user-attachments/assets/bb7f4d1c-a681-42b1-a58f-8d30f754a155" />

        Caption: The git log output shows a single commit, and the flag is visible directly in the log information.

3. (Optional) Use `"git show"` on the commit if you want to verify what it contains.
    **WHY:** `"git show"` is still a useful verification tool, but in this specific challenge it’s not required because the log already includes the flag.
    
    <img width="735" height="315" alt="Screenshot 2026-01-19 101436" src="https://github.com/user-attachments/assets/a7ac1ffb-6694-452c-bc23-9c3f529191b9" />

        Caption: The commit details can be viewed for confirmation, but the solve does not depend on this step.

---

## Common Mistakes ⚠️
- Overcomplicating the solve by jumping straight to `"git show"` when `"git log"` already contains the flag in plain sight.
- Skimming the `"git log"` output too quickly and missing the flag because you assume it must be inside a file or different commit.
- Running Git commands outside the extracted repository folder, which prevents `"git log"` from working correctly.

---

## Lessons Learned ✅
- `"git log"` can be enough to solve an investigation when key information is stored in commit history rather than in files.
- Knowing `"git show"` is still valuable because it lets you inspect commit content quickly when the log alone isn’t sufficient.
- The fastest path in version-control challenges is often to read what Git already summarizes before digging deeper.
