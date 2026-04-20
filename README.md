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

## 📦 BASIC SNAPSHOTING

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
🌿 BRANCHES & MERGING
<div align="center"> <img src="https://raw.githubusercontent.com/tandpfun/skill-icons/main/icons/Git.svg" width="60"> </div>
Operation	Command	Advanced
List branches	git branch -a (all)	git branch -vv (tracking)
Create branch	git branch feature	git checkout -b feature
Switch	git switch feature	git switch -c feature
Delete	git branch -d feature	git branch -D feature (force)
Merge	git merge feature	git merge --squash feature
Rebase	git rebase main	git rebase -i HEAD~3 (interactive)
🔥 Git Branching Strategy (Mermaid)
gitGraph
   commit id: "init"
   branch develop
   checkout develop
   commit id: "add feature A"
   branch feature/login
   checkout feature/login
   commit id: "login UI"
   commit id: "auth logic"
   checkout develop
   merge feature/login tag: "squash & merge"
   checkout main
   merge develop tag: "v1.0.0"
🌍 REMOTE OPERATIONS
bash
git remote -v                  # Show remotes
git remote add upstream <url>  # Add upstream
git fetch origin               # Download objects/refs
git fetch --prune              # Remove stale remote branches
git pull origin main           # Fetch + merge
git pull --rebase              # Fetch + rebase (clean history)
git push origin main           # Upload
git push --force-with-lease    # Safe force push (beast mode)
git push --delete origin <branch>
🕰️ UNDO & RECOVERY
Scenario	Command	Danger Level
Unstage file	git restore --staged file	🟢 Safe
Discard local changes	git restore file	🟡 Moderate
Undo last commit (keep changes)	git reset --soft HEAD~1	🟢 Safe
Undo last commit (destroy changes)	git reset --hard HEAD~1	🔴 High
Undo commit but record undo	git revert <commit>	🟢 Safe
See every action ever	git reflog	🟢 Info
Restore lost commit	git checkout <reflog-hash>	🟡 Moderate
🧠 ADVANCED WEAPONS
<details> <summary><b>⚡ Click to unleash advanced commands</b></summary>
Command	Description
git bisect start	Binary search for bug commit
git bisect bad / git bisect good <hash>	Mark commits
git cherry-pick <commit>	Apply specific commit to current branch
git worktree add ../hotfix main	Parallel working directories
git filter-branch --tree-filter 'rm -f secret.txt' HEAD	Rewrite history (danger)
git reflog expire --expire=now --all	Clean reflog
git gc --aggressive --prune=now	Optimize repo
git submodule add <url>	Add submodule
git lfs track "*.psd"	Track large files
</details>
📜 LOG & HISTORY
bash
# Beautiful logs
git log --oneline --graph --decorate
git log --since="2 days ago"
git log -S "function_name"          # Search code changes
git log --grep="fix"                # Search commit messages

# Who changed what
git blame file.txt
git shortlog -sn                    # Contributor stats
git show <commit>:file.txt          # View file at commit
🔧 STASH & CLEAN
bash
git stash push -m "wip"             # Stash with message
git stash list                      # List stashes
git stash pop                       # Apply + drop
git stash apply stash@{2}           # Apply specific
git stash drop stash@{0}            # Delete stash
git stash clear                     # Nuke all stashes
git clean -fd                       # Remove untracked files/dirs
git clean -fx                       # Also ignored files
⚙️ ALIASES & CONFIG (Pro Level)
bash
# Must-have aliases
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.unstage 'reset HEAD --'
git config --global alias.last 'log -1 HEAD'
git config --global alias.tree "log --graph --oneline --all"

# Pretty diff colors
git config --global color.ui auto
git config --global core.editor "code --wait"

# Merge tool
git config --global merge.tool vscode
🧪 GIT HOOKS & LFS
Hooks (.git/hooks/):

pre-commit – run linters before commit

commit-msg – validate message format

post-receive – deploy after push

Git LFS:

bash
git lfs track "*.psd" "*.zip"
git add .gitattributes
git commit -m "track large files"
🚀 ULTIMATE WORKFLOW EXAMPLE
bash
git checkout -b feature/awesome
git add .
git commit -m "feat: add awesome thing"
git fetch origin main
git rebase origin/main          # linear history
git push origin feature/awesome
# create PR, after merge locally:
git checkout main
git pull --rebase
git branch -d feature/awesome
🧠 PRO TIPS (Beast Mode Mindset)
Golden Rule #1: Never push --force to shared branches – use --force-with-lease.
Golden Rule #2: rebase before merging to keep history clean.
Golden Rule #3: Learn reflog – it saves lives.
Golden Rule #4: Use git add -p to review every change before staging.
Golden Rule #5: Automate with aliases – speed is everything.

📊 GIT STATS (Dynamic Card)
<div align="center"> <img src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=radical&hide_border=true&bg_color=0D1117&title_color=00FFCC&icon_color=FF69B4" width="49%"> <img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=radical&hide_border=true&background=0D1117&stroke=00FFCC&ring=FF69B4&fire=FF69B4&currStreakNum=00FFCC" width="49%"> </div>
🔥 CONTRIBUTION & FORK WORKFLOW
bash
# Fork the repo on GitHub, then:
git clone https://github.com/yourname/repo.git
cd repo
git remote add upstream https://github.com/original/repo.git
git checkout -b patch-1
# make changes
git add .
git commit -m "fix: solve issue #42"
git push origin patch-1
# then open Pull Request on GitHub
🎯 FINAL COMMAND REFERENCE (Poster Style)
Category	Beast Command	Description
Nuclear	git reset --hard @{u}	Reset to upstream
Time travel	git checkout HEAD~3	Go back 3 commits
Copy commit	git cherry-pick <hash>	Pick specific commit
Search	git grep "TODO"	Search codebase
Cleanup	git reflog expire --expire=now --all && git gc --prune=now	Purge everything
<div align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=120&section=footer&text=BEAST%20MODE%20ACTIVATED&fontSize=30&fontColor=ffffff&animation=twinkling" /> </div><div align="center"> <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&duration=2500&pause=800&color=00F7FF&center=true&vCenter=true&width=800&lines=Made+with+%E2%9D%A4%EF%B8%8F+by+Anshul;git+commit+-m+%22master+the+universe%22;git+push+--force+--with-lease+origin+main" /> </div><div align="center"> <img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="900"> </div><!-- ================= END OF BEAST MODE ================= -->
