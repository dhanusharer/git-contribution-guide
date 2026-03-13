# ✏️ Guide 04 — Making Changes

> **Time to complete:** ~15 minutes
> **Difficulty:** ⭐⭐☆☆☆ Beginner
> **Prerequisite:** Complete [Guide 03 — Branching](./03-branching.md) first

---

## What You'll Learn

- How to edit files in a repository
- How to stage (select) your changes
- How to write great commit messages
- How to view your commit history

---

## Your Practice Task

For this walkthrough, you'll add your name to the `contributors.md` file in the sample repo. This is a classic "first contribution" task that's safe, simple, and genuinely useful!

---

## Step 1 — Check the Current State

Before touching any files, see what's going on:

```bash
git status
```

**Expected output (clean branch):**
```
On branch docs/add-my-name-to-contributors
nothing to commit, working tree clean
```

---

## Step 2 — Edit a File

Open the `contributors.md` file in your editor:

```bash
# VS Code
code contributors.md

# Nano (terminal editor — beginner-friendly)
nano contributors.md

# Vim (advanced)
vim contributors.md
```

The file looks like this:

```markdown
# Contributors

Thank you to everyone who has contributed to this project! 🎉

| Name | GitHub | Contribution |
|------|--------|-------------|
| Jane Smith | [@janesmith](https://github.com/janesmith) | Initial setup |
| Bob Jones  | [@bobjones](https://github.com/bobjones)   | Fixed typo in README |
```

**Add your row at the bottom:**

```markdown
| Your Name | [@yourusername](https://github.com/yourusername) | Added name to contributors |
```

Save the file.

---

## Step 3 — See What Changed

```bash
git status
```

**Output:**
```
On branch docs/add-my-name-to-contributors
Changes not staged for commit:
  (use "git add <file>..." to update what will be included in commit)

        modified:   contributors.md
```

Git sees your change! Now see the *details* of what changed:

```bash
git diff
```

**Output:**
```diff
diff --git a/contributors.md b/contributors.md
index a1b2c3d..e4f5g6h 100644
--- a/contributors.md
+++ b/contributors.md
@@ -7,3 +7,4 @@ Thank you to everyone who has contributed!
 | Jane Smith | [@janesmith](https://github.com/janesmith) | Initial setup |
 | Bob Jones  | [@bobjones](https://github.com/bobjones)   | Fixed typo in README |
+| Your Name  | [@yourusername](https://github.com/yourusername) | Added name to contributors |
```

Lines starting with `+` are additions. Lines starting with `-` are deletions. Lines with no symbol are context.

---

## Step 4 — Stage Your Changes

**Staging** means choosing which changes to include in your next commit. Think of it as putting items in a box before sealing and shipping it.

```bash
# Stage a specific file
git add contributors.md

# Or stage all changed files (if you changed multiple)
git add .
```

Verify what's staged:

```bash
git status
```

**Output:**
```
On branch docs/add-my-name-to-contributors
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)

        modified:   contributors.md
```

The file moved from "not staged" to "to be committed" — it's in the box!

---

## Step 5 — Commit Your Changes

A **commit** permanently records your staged changes with a message describing what you did.

```bash
git commit -m "docs: add Jane Doe to contributors list"
```

**Expected output:**
```
[docs/add-my-name-to-contributors 7c3d2f1] docs: add Jane Doe to contributors list
 1 file changed, 1 insertion(+)
```

---

## Anatomy of a Great Commit Message

```
type(optional scope): short summary in present tense

Optional body: explain WHY, not what. The diff shows what changed —
the message should explain the reasoning and context.

Closes #42  ← Reference related issues
```

### The Type

| Type | When to use |
|------|-------------|
| `feat` | Adding a new feature |
| `fix` | Fixing a bug |
| `docs` | Documentation changes only |
| `style` | Formatting (spaces, semicolons — no logic change) |
| `refactor` | Code restructure with no new behavior |
| `test` | Adding or fixing tests |
| `chore` | Build process, dependency updates |

### Examples: Good vs Bad

```bash
# ✅ GOOD — clear, specific, uses type prefix
git commit -m "fix: prevent login crash when email field is empty"
git commit -m "feat: add profile picture upload to settings page"
git commit -m "docs: add Windows installation instructions to README"

# ❌ BAD — vague, no context
git commit -m "fix stuff"
git commit -m "update"
git commit -m "wip"
git commit -m "asdfgh"
```

### Multi-line Commit (for complex changes)

```bash
git commit -m "feat: add dark mode to settings panel

Users requested a dark mode option in issue #87. This adds:
- A toggle in the Settings > Appearance menu
- CSS variables for all theme colors
- Local storage persistence of user preference

Closes #87"
```

---

## Step 6 — View Your Commit History

```bash
git log --oneline
```

**Output:**
```
7c3d2f1 (HEAD -> docs/add-my-name-to-contributors) docs: add Jane Doe to contributors list
a4b5c6d (upstream/main, origin/main, main) Initial commit
```

Your commit appears at the top! `HEAD` points to your latest commit.

For more detail:

```bash
git log --oneline --graph --all
```

**Output:**
```
* 7c3d2f1 (HEAD -> docs/add-my-name-to-contributors) docs: add Jane Doe to contributors list
* a4b5c6d (upstream/main, origin/main, main) Initial commit
```

---

## Undoing Mistakes

Don't panic — Git makes it easy to undo almost anything.

### Unstage a file (before commit)

```bash
git restore --staged contributors.md
```

### Undo changes to a file (before staging)

```bash
git restore contributors.md
```

⚠️ **Warning:** This permanently discards your unsaved edits.

### Amend the last commit (before pushing)

```bash
# Fix a typo in the last commit message
git commit --amend -m "docs: add Jane Doe to contributors list"
```

---

## ✅ Checkpoint

After completing this guide, you should have:

- [ ] Edited `contributors.md` to add your name
- [ ] Staged the change with `git add`
- [ ] Committed with a descriptive message following the `type: summary` format
- [ ] Verified the commit appears in `git log --oneline`

---

## 🚀 Next Step

Proceed to **[Guide 05 — Pushing and Opening a Pull Request](./05-pull-request.md)** to share your contribution with the world!