# ✅ First-Time Contributor Checklist

> Use this checklist to make sure you haven't missed any steps. Check off each item as you complete it!

---

## 🔧 One-Time Setup

These steps only need to be done once, ever.

- [ ] **Created a GitHub account** at [github.com](https://github.com)
- [ ] **Installed Git** — verify with `git --version` in your terminal
- [ ] **Configured your Git identity:**
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "your@email.com"
  ```
- [ ] **Chosen a code editor** (e.g., VS Code, Sublime Text, Atom)

---

## 🍴 Before You Start Contributing

Do this each time you work on a new contribution to a new repository.

- [ ] **Read the project's README.md** — understand what the project does
- [ ] **Read CONTRIBUTING.md** (if it exists) — every project has different rules
- [ ] **Found an issue to work on** — look for labels like `good first issue`, `beginner`, `help wanted`
- [ ] **Commented on the issue** to let maintainers know you're working on it (prevents duplicate work)
- [ ] **Forked the repository** using the Fork button on GitHub
- [ ] **Cloned your fork** to your computer:
  ```bash
  git clone https://github.com/YOUR-USERNAME/REPO-NAME.git
  ```
- [ ] **Added the upstream remote:**
  ```bash
  git remote add upstream https://github.com/ORIGINAL-OWNER/REPO-NAME.git
  ```
- [ ] **Verified remotes** with `git remote -v` (should see both `origin` and `upstream`)

---

## 🌿 Starting Each Feature or Fix

Do this at the start of every new contribution.

- [ ] **Synced main with upstream:**
  ```bash
  git checkout main
  git pull upstream main
  ```
- [ ] **Created a new branch with a descriptive name:**
  ```bash
  git checkout -b type/short-description
  # Examples:
  # git checkout -b fix/login-button-crash
  # git checkout -b docs/update-installation-guide
  ```
- [ ] **Confirmed you're on the right branch:** `git branch` (look for the `*`)

---

## ✏️ While Making Changes

- [ ] **Made only the changes related to this contribution** (no unrelated edits)
- [ ] **Followed the project's code style** (check existing files for conventions)
- [ ] **Ran existing tests** (if the project has them — check README for how)
- [ ] **Checked `git diff`** to review exactly what changed
- [ ] **Staged the right files:** `git add specific-file.md` (avoid `git add .` for large projects)
- [ ] **Committed with a clear message:**
  ```bash
  git commit -m "type: short description of what and why"
  ```

---

## 🚀 Before Opening the Pull Request

- [ ] **Checked for conflicts** by pulling latest upstream:
  ```bash
  git fetch upstream
  git rebase upstream/main
  ```
- [ ] **Pushed your branch** to your fork:
  ```bash
  git push origin your-branch-name
  ```
- [ ] **Reviewed your own changes** on GitHub (click "Files changed" in the PR preview)

---

## 📝 Writing the Pull Request

- [ ] **Title follows the convention:** `type: short description` (e.g., `fix: prevent crash on empty input`)
- [ ] **Description explains:**
  - [ ] What the PR does
  - [ ] Why the change is needed
  - [ ] How to test it (if applicable)
- [ ] **Referenced the related issue** (if any) with `Closes #42` or `Fixes #42`
- [ ] **Added screenshots** for any UI changes
- [ ] **Checked the PR checklist** (many repos include one in the PR template)

---

## 💬 After Submitting

- [ ] **Monitoring for review comments** — check GitHub notifications
- [ ] **Responding to feedback promptly** and politely
- [ ] **Making requested changes** on your branch and pushing again
- [ ] **Marking review comments as resolved** after addressing them

---

## 🎉 After Your PR is Merged!

- [ ] **Celebrated!** 🎊 You're an open source contributor now!
- [ ] **Updated your local main:**
  ```bash
  git checkout main
  git pull upstream main
  git push origin main
  ```
- [ ] **Deleted your feature branch** (keeping things tidy):
  ```bash
  git branch -d your-branch-name
  git push origin --delete your-branch-name
  ```
- [ ] **Found your next issue to work on** — momentum matters!

---

## 🆘 Quick Help Reference

| Problem | Command |
|---------|---------|
| Where am I? | `git status` |
| What branch? | `git branch` |
| See all changes | `git diff` |
| Undo unstaged changes | `git restore filename` |
| Unstage a file | `git restore --staged filename` |
| See commit history | `git log --oneline` |
| Get latest upstream | `git fetch upstream` |
| Sync main with upstream | `git pull upstream main` |
| List all remotes | `git remote -v` |

---

## 📚 Quick Links

- 📖 [Full Contribution Guide](../README.md)
- 🧪 [Practice Repository](../sample-repo/README.md)
- 🔍 [Good First Issues](https://goodfirstissues.com/)
- 🎮 [Learn Git Interactively](https://ohmygit.org/)
- 📕 [Pro Git Book (Free)](https://git-scm.com/book/en/v2)

---

*Print this out, keep it in a tab, or bookmark it — refer back to it whenever you start a new contribution until these steps become second nature.*

**You've got this! 💪**