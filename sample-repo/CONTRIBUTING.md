# Contributing to This Practice Repository

First off — thank you for wanting to contribute! 🎉

This document explains the contribution process for this specific practice repository. For a full beginner's guide to open source contribution, see the [main README](../README.md).

---

## Code of Conduct

This is a **welcoming, inclusive, beginner-friendly space**. All contributors are expected to:

- Be kind and patient (everyone was a beginner once)
- Provide constructive, helpful feedback
- Respect different experience levels and backgrounds
- Ask questions — there are no dumb questions here

Harassment, discrimination, or dismissive behavior of any kind is not tolerated.

---

## What We Accept

This practice repository only accepts contributions to **`contributors.md`**.

We review and merge PRs that:
- ✅ Add exactly one new row to the contributors table
- ✅ Follow the correct table format (see below)
- ✅ Use a descriptive branch name (e.g., `docs/add-jane-doe-to-contributors`)
- ✅ Include a clear PR title and description

We close PRs that:
- ❌ Modify files other than `contributors.md`
- ❌ Delete or rearrange existing entries
- ❌ Include duplicate names already in the list

---

## The Correct Format

Your entry must follow this exact format:

```markdown
| Your Full Name | [@yourusername](https://github.com/yourusername) | City, Country | Brief description |
```

**Example:**
```markdown
| Jane Doe | [@janedoe](https://github.com/janedoe) | Austin, USA | My first contribution! |
```

**Column guidelines:**
- **Name:** Your real name or preferred display name
- **GitHub:** Your GitHub username as a link
- **Location:** City and country (or just country is fine)
- **Contribution:** A short, honest description (1–8 words)

---

## Step-by-Step Process

1. **Fork** this repository (button in the top right on GitHub)
2. **Clone** your fork: `git clone https://github.com/YOUR-USERNAME/first-contribution-guide.git`
3. **Create a branch**: `git checkout -b docs/add-YOUR-NAME-to-contributors`
4. **Edit** `contributors.md` — add your row at the bottom of the table
5. **Commit**: `git commit -m "docs: add YOUR NAME to contributors list"`
6. **Push**: `git push origin docs/add-YOUR-NAME-to-contributors`
7. **Open a PR** on GitHub with a clear title and friendly description

---

## Pull Request Review

After you open a PR:

- A maintainer will review it within a few days
- If changes are needed, they'll leave a comment explaining what to fix
- Make the requested changes on your local branch and push again (the PR auto-updates)
- Once approved, it will be merged 🎉

**Your PR will be merged as long as it follows the format above.** This is a practice repo — we want everyone to succeed!

---

## Getting Help

Stuck? That's okay! Here's how to get help:

1. **Re-read the guide**: [`../README.md`](../README.md)
2. **Check the troubleshooting section**: [`../README.md#common-pitfalls--troubleshooting`](../README.md#-common-pitfalls--troubleshooting)
3. **Open an Issue**: Describe exactly where you're stuck and we'll help

No question is too basic. We genuinely want to help you succeed!