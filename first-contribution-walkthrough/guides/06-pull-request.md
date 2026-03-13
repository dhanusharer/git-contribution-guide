# 🚀 Guide 05 — Pushing and Opening a Pull Request

> **Time to complete:** ~10 minutes
> **Difficulty:** ⭐⭐⭐☆☆ Beginner-Intermediate
> **Prerequisite:** Complete [Guide 04 — Making Changes](./04-making-changes.md) first

---

## What You'll Learn

- How to push your branch to GitHub
- How to open a Pull Request (PR)
- How to write a great PR description
- What to expect after submitting

---

## Step 1 — Push Your Branch to GitHub

Your commits currently only exist on your computer. Push them to your GitHub fork:

```bash
# Push your feature branch to your fork (origin)
git push origin docs/add-my-name-to-contributors
```

Replace `docs/add-my-name-to-contributors` with your actual branch name.

**Expected output:**
```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 412 bytes | 412.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'docs/add-my-name-to-contributors' on GitHub by visiting:
remote:      https://github.com/YOUR-USERNAME/REPO-NAME/pull/new/docs/add-my-name-to-contributors
remote:
To https://github.com/YOUR-USERNAME/REPO-NAME.git
 * [new branch]      docs/add-my-name-to-contributors -> docs/add-my-name-to-contributors
```

Git even gives you the direct URL to create a PR! You can click that link, or follow the steps below.

---

## Step 2 — Navigate to Your Fork on GitHub

Go to your fork's URL:
```
https://github.com/YOUR-USERNAME/REPO-NAME
```

After pushing, GitHub displays a helpful banner:

```
┌─────────────────────────────────────────────────────────────────────────┐
│  📁 yourname / Hello-World                                              │
│     forked from octocat/Hello-World                                     │
│                                                                         │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ 🟡 docs/add-my-name-to-contributors had recent pushes 1 min ago   │  │
│  │                                     [Compare & pull request]      │  │
│  └───────────────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────────┘
```

Click **"Compare & pull request"**.

---

## Step 3 — Review the Comparison

GitHub shows you a comparison page before you create the PR:

```
┌─────────────────────────────────────────────────────────────────────────┐
│  Comparing changes                                                      │
│                                                                         │
│  base repository: octocat/Hello-World    base: main         ← target  │
│  head repository: yourname/Hello-World   compare: docs/... ← your PR  │
│                                                                         │
│  ✅ Able to merge. These branches can be automatically merged.          │
│                                                                         │
│  [Create pull request]                                                  │
└─────────────────────────────────────────────────────────────────────────┘
```

Check that:
- **base:** is `main` (or whatever the target branch is — sometimes `dev` or `develop`)
- **compare:** shows your feature branch
- ✅ "Able to merge" — no conflicts!

If you see ❌ conflicts, see the troubleshooting section at the bottom.

---

## Step 4 — Write Your Pull Request

The PR form is where you describe your changes for the maintainers:

```
┌─────────────────────────────────────────────────────────────────────────┐
│  Open a pull request                                                    │
│                                                                         │
│  Title *                                                                │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │ docs: add Jane Doe to contributors list                         │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  Write  Preview                              Styling with Markdown ✓    │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │ ## What does this PR do?                                        │   │
│  │ Adds my name to the contributors list in contributors.md.      │   │
│  │                                                                 │   │
│  │ ## Why?                                                         │   │
│  │ Contributing to this project as part of my first open source   │   │
│  │ contribution! 🎉                                                │   │
│  │                                                                 │   │
│  │ ## Changes                                                      │   │
│  │ - Added one row to contributors.md                             │   │
│  │                                                                 │   │
│  │ ## Checklist                                                    │   │
│  │ - [x] I've read CONTRIBUTING.md                                │   │
│  │ - [x] My change doesn't break any existing functionality       │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  Reviewers   Assignees   Labels   Projects   Milestone                  │
│                                                                         │
│                              [Create pull request]                      │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## Writing a Great PR Description

### Template (Copy & Paste This!)

```markdown
## What does this PR do?
[Brief description of the change]

## Why is this change needed?
[What problem does it solve? What feature does it add?]

## Changes made
- [Specific change 1]
- [Specific change 2]

## Testing
- [x] I've tested these changes locally
- [x] Existing tests pass

## Screenshots (if applicable)
[Include before/after screenshots for UI changes]

## Related issues
Closes #[issue number]
```

### PR Title Conventions

Use the same format as commit messages:

```
docs: add Jane Doe to contributors list
fix: resolve null pointer in login flow
feat: add dark mode to settings panel
```

---

## Step 5 — Submit the PR

Click **"Create pull request"** 🎉

You'll be taken to the PR page:

```
┌─────────────────────────────────────────────────────────────────────────┐
│  docs: add Jane Doe to contributors list                  #42   Open   │
│                                                                         │
│  yourname wants to merge 1 commit into                                  │
│  octocat:main from yourname:docs/add-my-name-to-contributors            │
│                                                                         │
│  [Conversation]  [Commits]  [Files changed]                             │
│                                                                         │
│  yourname commented just now                                            │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ ## What does this PR do?                                          │  │
│  │ Adds my name to the contributors list...                          │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                         │
│  ✅ All checks passed                                                    │
│                                                                         │
│  This branch has no conflicts with the base branch                      │
│  Merging can be performed automatically.                                │
└─────────────────────────────────────────────────────────────────────────┘
```

Your PR is live! Maintainers can now review it.

---

## Step 6 — Responding to Review Feedback

Maintainers may leave comments asking for changes. This is normal and part of the process!

```
┌───────────────────────────────────────────────────────────────────────┐
│  🔴 maintainer-alice requested changes                                │
│                                                                       │
│  "Hi! Thanks for the contribution. Could you also add your GitHub    │
│   profile link in the Link column? Take a look at how others have   │
│   formatted theirs. Thanks!"                                         │
└───────────────────────────────────────────────────────────────────────┘
```

**To update your PR:**

```bash
# 1. Make the requested changes on your local branch
nano contributors.md

# 2. Stage and commit
git add contributors.md
git commit -m "docs: add GitHub profile link per review feedback"

# 3. Push again — the PR updates automatically!
git push origin docs/add-my-name-to-contributors
```

You don't need to create a new PR. Pushing to the same branch updates the existing one.

**Reply to the reviewer** on GitHub to let them know you've addressed their feedback:
```
Done! Added the profile link. Thanks for the quick review!
```

---

## What Happens After Merging?

When a maintainer approves and merges your PR:

```
┌──────────────────────────────────────────────────────────────┐
│  🟣  Merged  maintainer-alice merged 1 commit into main      │
│                                                              │
│  [Delete branch]                                             │
└──────────────────────────────────────────────────────────────┘
```

🎉 **Congratulations — you're an open source contributor!**

You can now:
1. Delete your feature branch (click "Delete branch" or run `git branch -d branch-name`)
2. Update your local `main`: `git pull upstream main`
3. Find your next contribution!

---

## ✅ Checkpoint

After completing this guide, you should have:

- [ ] Pushed your branch to your fork with `git push origin branch-name`
- [ ] Opened a Pull Request with a clear title and description
- [ ] Understood how to respond to review feedback
- [ ] Had your PR merged (or be waiting for review!)

---

## ❓ Troubleshooting

**Q: GitHub says "Can't automatically merge" (conflict warning)**

You'll need to resolve conflicts locally:
```bash
git fetch upstream
git checkout your-branch-name
git rebase upstream/main
# Resolve any conflicts that appear, then:
git add .
git rebase --continue
git push origin your-branch-name --force-with-lease
```

**Q: I pushed to the wrong branch.**

```bash
# Delete the remote branch you pushed to by mistake
git push origin --delete wrong-branch-name

# Push to the correct branch
git push origin correct-branch-name
```

**Q: My PR has too many commits (maintainer asked to squash).**

```bash
# Squash the last 3 commits into one (adjust the number as needed)
git rebase -i HEAD~3
# In the editor, change "pick" to "squash" (or "s") for all but the first commit
# Edit the combined commit message, save, then force push
git push origin your-branch-name --force-with-lease
```