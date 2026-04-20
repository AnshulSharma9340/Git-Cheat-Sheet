<!-- ================= ULTRA ADVANCED GIT CHEAT SHEET - BEAST MODE ================= -->
<!-- DYNAMIC TYPING HEADER WITH GLITCH EFFECT -->
<div align="center">
  <img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="900">
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=900&size=45&duration=2000&pause=500&color=00FFCC&center=true&vCenter=true&width=1000&lines=⚡+GIT+CHEAT+SHEET+%7C+BEAST+MODE+⚡;MASTER+GIT+WITH+ZERO+FEAR;ALL+COMMANDS+IN+ONE+PLACE;REBASE+%7C+MERGE+%7C+BISECT+%7C+STASH;LIKE+A+TRUE+DEVELOPER+🚀" alt="Typing SVG" />
</div>

<div align="center">
  <img src="https://img.shields.io/badge/STATUS-ULTRA_ADVANCED-critical?style=for-the-badge&logo=github">
  <img src="https://img.shields.io/badge/GIT-2.42%2B-orange?style=for-the-badge&logo=git">
  <img src="https://img.shields.io/badge/LEVEL-HACKER_MODE-blue?style=for-the-badge&logo=hackthebox">
  <img src="https://img.shields.io/badge/MADE%20BY-ANSHUL-ff69b4?style=for-the-badge&logo=asciinema">
  <img src="https://komarev.com/ghpvc/?username=yourusername&label=VIEWS&color=0e75b6&style=for-the-badge" alt="views">
</div>

<div align="center">
  <img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="900">
</div>

<!-- ================= MATRIX RAIN ASCII (STATIC but cool) ================= -->
<pre align="center" style="background:black; color:#0f0; font-family: monospace; padding: 10px;">
┌─────────────────────────────────────────────────────────────────────────────┐
│  ░▒▓█ Git Beast Mode Activated █▓▒░      ░▒▓█ Master The Terminal █▓▒░      │
│  >_ git push --force-with-lease          >_ git rebase -i HEAD~5            │
│  >_ git reflog expire --expire=now       >_ git filter-branch --tree-filter  │
│  >_ git bisect start                      >_ git worktree add feature        │
│  >_ git cherry-pick A..B                  >_ git stash push -m "wip"         │
│  System ready. All commands lethal.                                           │
└─────────────────────────────────────────────────────────────────────────────┘
</pre>

<!-- ================= TABLE OF CONTENTS ================= -->
<details open>
<summary><b>📑 NAVIGATION (click to expand/collapse)</b></summary>
<br>

| SECTION | COMMANDS |
|---------|----------|
| [🔥 CREATE & SETUP](#-create--setup) | `init`, `clone`, `config` |
| [📦 BASIC SNAPSHOTTING](#-basic-snapshoting) | `add`, `commit`, `status`, `diff` |
| [🌿 BRANCHES & MERGING](#-branches--merging) | `branch`, `switch`, `merge`, `rebase` |
| [🌍 REMOTE OPERATIONS](#-remote-operations) | `remote`, `fetch`, `pull`, `push` |
| [🕰️ UNDO & RECOVERY](#️-undo--recovery) | `reset`, `revert`, `restore`, `reflog` |
| [🧠 ADVANCED WEAPONS](#-advanced-weapons) | `bisect`, `cherry-pick`, `worktree`, `filter-branch` |
| [📜 LOG & HISTORY](#-log--history) | `log`, `blame`, `shortlog` |
| [🔧 STASH & CLEAN](#-stash--clean) | `stash`, `clean`, `grep` |
| [⚙️ ALIASES & CONFIG](#️-aliases--config) | `alias`, `config` |
| [🧪 GIT HOOKS & LFS](#-git-hooks--lfs) | `hooks`, `lfs` |

</details>

---

## 🔥 CREATE & SETUP

| Command | Effect | Beast Mode Flag |
|---------|--------|------------------|
| `git init` | Initialize a new repo | `git init --bare` (server) |
| `git clone <url>` | Clone remote repo | `git clone --depth 1` (shallow) |
| `git config --global user.name "Name"` | Set identity | `git config --global core.editor "code --wait"` |
| `git config --global alias.<alias> <cmd>` | Create alias | `git config --global alias.tree "log --graph --oneline"` |

---

## 📦 BASIC SNAPSHOTTING

```bash
# Check status and differences
git status -sb                 # Short branch status
git diff                       # Working vs staging
git diff --staged              # Staging vs last commit
git diff HEAD~1..HEAD          # Compare commits

# Staging area
git add file.txt               # Stage specific
git add .                      # Stage all (careful)
git add -p                     # Interactive staging (beast)
git add -A                     # Stage all including deletions

# Commit like a pro
git commit -m "msg"            # Standard
git commit -am "msg"           # Add + commit (tracked files)
git commit --amend --no-edit   # Fix last commit
git commit --amend -m "new msg"
