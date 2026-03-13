# 🌿 Guide 03 — Creating a Feature Branch

> **Time to complete:** ~5 minutes
> **Difficulty:** ⭐⭐☆☆☆ Beginner
> **Prerequisite:** Complete [Guide 02 — Cloning and Setup](./02-cloning-setup.md) first

---

## What You'll Learn

- Why branches are essential for contributing
- Common branch naming conventions
- How to create, switch, and manage branches

---

## Why Branches?

Imagine you're writing a book and want to try a completely different ending. You wouldn't erase the original ending — you'd make a photocopy and experiment on that.

**Branches work the same way:**

```
main branch (published book):  A → B → C → D
                                              \
feature branch (your draft):                  E → F → G
```

Your changes live on the feature branch. If they're approved, they get merged into `main`. If not, the branch is simply deleted — `main` is untouched.

---

## Step 1 — Make Sure main Is Up-to-Date

Before creating a branch, sync your `main` with the latest from upstream:

```bash
# Switch to the main branch
git checkout main

# Fetch and merge the latest changes from the original repo
git pull upstream main
```

**Expected output (if already up-to-date):**
```
Already up to date.
```

**Expected output (if there were updates):**
```
Updating a1b2c3d..e4f5g6h
Fast-forward
 README.md | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)
```

---

## Step 2 — Create Your Feature Branch

```bash
# Create a new branch and switch to it immediately
git checkout -b feature/your-feature-name
```

The `-b` flag means "create and switch" — it's a shortcut for running two commands at once:
```bash
# These two commands do the same thing as the -b shortcut above:
git branch feature/your-feature-name      # create
git checkout feature/your-feature-name    # switch
```

**Example:**
```bash
git checkout -b docs/add-my-name-to-contributors
```

**Expected output:**
```
Switched to a new branch 'docs/add-my-name-to-contributors'
```

---

## Branch Naming Conventions

Consistent naming helps everyone understand the purpose of a branch at a glance.

### Standard Prefixes

| Prefix | Use When | Example |
|--------|----------|---------|
| `feature/` | Adding new functionality | `feature/search-bar` |
| `fix/` | Fixing a bug | `fix/null-pointer-crash` |
| `docs/` | Documentation only | `docs/api-reference` |
| `style/` | Formatting, typos, whitespace | `style/fix-indentation` |
| `refactor/` | Restructuring code (no new features) | `refactor/extract-auth-module` |
| `test/` | Adding or fixing tests | `test/unit-tests-for-login` |
| `chore/` | Maintenance tasks | `chore/update-dependencies` |

### Naming Rules

✅ Use lowercase letters and hyphens:
```
feature/add-dark-mode
fix/button-color-on-mobile
```

❌ Avoid spaces, uppercase, or underscores:
```
Feature/Add Dark Mode    ← wrong
fix_button_color         ← avoid (use hyphens)
```

✅ Be descriptive but concise (2–5 words):
```
feature/user-avatar-upload      ← good
feature/x                       ← too vague
feature/allow-users-to-upload-a-profile-avatar  ← too long
```

---

## Step 3 — Verify Your Current Branch

```bash
git branch
```

**Output:**
```
* docs/add-my-name-to-contributors
  main
```

The `*` marks your active branch. You can also check:

```bash
git status
```

**Output:**
```
On branch docs/add-my-name-to-contributors
nothing to commit, working tree clean
```

---

## Useful Branch Commands Reference

```bash
# List all local branches
git branch

# List all branches including remote ones
git branch -a

# Switch to an existing branch
git checkout branch-name
# (Newer syntax, same result:)
git switch branch-name

# Create and switch to a new branch
git checkout -b new-branch-name

# Rename the current branch
git branch -m new-name

# Delete a branch (after it's merged)
git branch -d branch-name

# Force-delete an unmerged branch
git branch -D branch-name
```

---

## ✅ Checkpoint

After completing this guide, you should have:

- [ ] Updated `main` with the latest upstream changes
- [ ] Created a new feature branch with a descriptive name
- [ ] Verified you are on the new branch with `git branch`

---

## 🚀 Next Step

Proceed to **[Guide 04 — Making Changes](./04-making-changes.md)** to start editing files and creating commits.