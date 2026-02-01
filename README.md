
# 🐙 Git Cheat Sheet for Terminal

A compact guide for DevOps, ML, and Data Engineering workflows.

---

## 1️⃣ Clone Repositories

```bash
# SSH
git clone git@github.com:username/repo.git

# HTTPS
git clone https://github.com/username/repo.git
````

---

## 2️⃣ Check Status & History

```bash
git status                     # see staged/unstaged changes
git log --oneline --graph --all # visual commit history
git diff                        # show unstaged changes
git diff --staged                # show staged changes
git show <commit_hash>           # show specific commit
```

---

## 3️⃣ Stage & Commit

```bash
git add <file>         # stage a file
git add .              # stage all changes
git commit -m "Message"
git commit --author="Name <email>" -m "Message"
```

---

## 4️⃣ Push & Pull

```bash
git push origin <branch>          # push branch
git push -u origin <branch>       # push new branch
git pull                          # fetch & merge
git pull --rebase                 # fetch & rebase commits
git fetch                         # fetch only
```

---

## 5️⃣ Branching

```bash
git branch                 # list local branches
git branch <new-branch>    # create branch
git checkout <branch>      # switch branch
git switch <branch>        # modern switch
git switch -c <branch>     # create & switch
```

---

## 6️⃣ Merging & Rebasing

```bash
# Merge
git checkout main
git merge feature-branch

# Rebase
git checkout feature-branch
git rebase main
# Resolve conflicts: git add <file> → git rebase --continue
git rebase --abort          # abort if needed
```

---

## 7️⃣ Undo / Fix

```bash
git reset --soft HEAD~1      # undo last commit, keep changes staged
git reset --hard HEAD~1      # undo last commit, discard changes
git checkout -- <file>       # discard file changes
git restore <file>           # modern discard
```

---

## 8️⃣ Remote Management

```bash
git remote -v                     # show remotes
git remote add origin <url>       # add remote
git remote set-url origin <url>   # change remote URL
git branch -r                     # list remote branches
git branch -a                     # list all branches
```

---

## 9️⃣ Stash Changes

```bash
git stash          # save uncommitted changes
git stash list     # list stashes
git stash apply    # apply latest stash
git stash pop      # apply & remove latest stash
```

---

## 🔹 Tags

```bash
git tag v1.0.0
git push origin v1.0.0
```

---

### ✅ Tips

* Always check `git status` before committing/pushing.
* Use `git pull --rebase` to keep history linear.
* Keep feature/bugfix branches short-lived.
* Use SSH for seamless authentication.
