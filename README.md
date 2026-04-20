# Git Cheat Sheet – Complete Command Reference

## 📁 Setup & Config

| Command | Description |
|---------|-------------|
| `git config --global user.name "Name"` | Set your name |
| `git config --global user.email "email@example.com"` | Set your email |
| `git config --list` | Show current config |
| `git init` | Create new local repository |
| `git clone <url>` | Clone remote repository |

## 📝 Basic Snapshotting

| Command | Description |
|---------|-------------|
| `git status` | Show working directory status |
| `git add <file>` | Stage specific file |
| `git add .` | Stage all changes (new, modified, deleted) |
| `git add -A` | Stage everything (including deletions) |
| `git add -p` | Stage interactively (hunk by hunk) |
| `git commit -m "message"` | Commit staged changes |
| `git commit -am "message"` | Stage tracked files + commit |
| `git commit --amend -m "new msg"` | Amend last commit message |
| `git commit --amend --no-edit` | Add changes to last commit without editing message |
| `git diff` | Show unstaged changes |
| `git diff --staged` | Show staged changes vs last commit |
| `git diff <commit1> <commit2>` | Compare two commits |
| `git restore <file>` | Discard local changes (unstaged) |
| `git restore --staged <file>` | Unstage file |
| `git rm <file>` | Remove file from working dir + staging |
| `git mv <old> <new>` | Rename/move file |

## 🌿 Branching & Merging

| Command | Description |
|---------|-------------|
| `git branch` | List local branches |
| `git branch -a` | List all branches (local + remote) |
| `git branch <branch-name>` | Create new branch |
| `git branch -d <branch>` | Delete branch (safe) |
| `git branch -D <branch>` | Force delete branch |
| `git checkout <branch>` | Switch branch (older way) |
| `git switch <branch>` | Switch branch (modern) |
| `git switch -c <branch>` | Create + switch branch |
| `git merge <branch>` | Merge branch into current |
| `git merge --abort` | Cancel merge |
| `git merge --squash <branch>` | Merge all commits as one |
| `git rebase <branch>` | Rebase current branch onto another |
| `git rebase -i HEAD~n` | Interactive rebase last n commits |
| `git rebase --continue` | Continue rebase after resolving conflicts |
| `git rebase --abort` | Cancel rebase |
| `git cherry-pick <commit>` | Apply specific commit to current branch |

## 🌐 Remote Repositories

| Command | Description |
|---------|-------------|
| `git remote -v` | List remotes |
| `git remote add <name> <url>` | Add remote |
| `git remote remove <name>` | Remove remote |
| `git fetch` | Download objects/refs from remote |
| `git fetch --prune` | Remove stale remote tracking branches |
| `git pull` | Fetch + merge remote branch |
| `git pull --rebase` | Fetch + rebase instead of merge |
| `git push <remote> <branch>` | Push branch to remote |
| `git push -u origin <branch>` | Push + set upstream |
| `git push --force-with-lease` | Safe force push |
| `git push --delete <remote> <branch>` | Delete remote branch |

## ⏪ Undo & Recovery

| Command | Description |
|---------|-------------|
| `git reset --soft HEAD~1` | Undo last commit, keep changes staged |
| `git reset --mixed HEAD~1` | Undo last commit, keep changes unstaged (default) |
| `git reset --hard HEAD~1` | Undo last commit + discard changes (danger) |
| `git reset --hard <commit>` | Reset to specific commit |
| `git revert <commit>` | Create new commit that undoes a previous commit (safe) |
| `git reflog` | Show all HEAD changes (recover lost commits) |
| `git checkout <commit-hash>` | Detached HEAD – view old state |
| `git checkout <commit> -- <file>` | Restore file from specific commit |

## 📜 Log & History

| Command | Description |
|---------|-------------|
| `git log` | Show commit history |
| `git log --oneline` | Compact one line per commit |
| `git log --graph --oneline --decorate` | Graphical history |
| `git log -p` | Show diffs in log |
| `git log --since="2 days ago"` | Limit by date |
| `git log --grep="fix"` | Search commit messages |
| `git log -S "code"` | Search code changes (pickaxe) |
| `git shortlog -sn` | List contributors sorted by commits |
| `git blame <file>` | Show who changed each line |
| `git show <commit>` | Show commit details |

## 📦 Stashing

| Command | Description |
|---------|-------------|
| `git stash` | Stash uncommitted changes |
| `git stash push -m "message"` | Stash with message |
| `git stash list` | List stashes |
| `git stash pop` | Apply latest stash and remove it |
| `git stash apply` | Apply latest stash without removing |
| `git stash apply stash@{2}` | Apply specific stash |
| `git stash drop stash@{0}` | Drop specific stash |
| `git stash clear` | Remove all stashes |

## 🧹 Clean & Ignore

| Command | Description |
|---------|-------------|
| `git clean -n` | Dry run – show untracked files to delete |
| `git clean -fd` | Delete untracked files and directories |
| `git clean -fx` | Also delete ignored files |
| `.gitignore` file | Specify intentionally untracked files |

## 🔍 Advanced Commands

| Command | Description |
|---------|-------------|
| `git bisect start` | Start binary search for bug |
| `git bisect bad` | Mark current commit as bad |
| `git bisect good <commit>` | Mark commit as good |
| `git bisect reset` | End bisect session |
| `git grep "pattern"` | Search codebase |
| `git worktree add <path> <branch>` | Create parallel working directory |
| `git submodule add <url>` | Add submodule |
| `git filter-branch --tree-filter 'rm -f secret.txt'` | Rewrite history (danger) |
| `git gc --prune=now` | Clean unnecessary files |
| `git reflog expire --expire=now --all` | Purge reflog |

## 🔗 Git LFS (Large File Storage)

| Command | Description |
|---------|-------------|
| `git lfs track "*.psd"` | Track large file type |
| `git lfs untrack "*.psd"` | Stop tracking |
| `git lfs ls-files` | List tracked LFS files |
| `git lfs pull` | Fetch LFS files |

## ⚙️ Aliases (Shortcuts)

| Command | Description |
|---------|-------------|
| `git config --global alias.co checkout` | Alias for checkout |
| `git config --global alias.br branch` | Alias for branch |
| `git config --global alias.ci commit` | Alias for commit |
| `git config --global alias.st status` | Alias for status |
| `git config --global alias.unstage 'reset HEAD --'` | Unstage alias |
| `git config --global alias.last 'log -1 HEAD'` | Show last commit |
| `git config --global alias.tree 'log --graph --oneline --all'` | Pretty tree |

---

## 🧠 Quick Reference – Most Used Commands

```bash
git add . && git commit -m "msg" && git push origin main
git pull --rebase
git reset --hard HEAD
git stash pop
git branch -d feature && git push origin --delete feature
