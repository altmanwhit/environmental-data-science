# Git Cheatsheet for This Repo

> Quick reference for the commands you'll use 90% of the time.

---

## Daily Workflow (The 3 Commands)

```bash
git add .                                      # Stage all changed files
git commit -m "Add groundwater forecast notebook"  # Save a snapshot with a message
git push                                       # Upload to GitHub
```

---

## First-Time Setup (One-Time Only)

```bash
# 1. Configure your identity
git config --global user.name "Your Name"
git config --global user.email "you@email.com"

# 2. Clone this repo to your computer
git clone https://github.com/yourusername/environmental-data-science-journey.git

# 3. Move into the folder
cd environmental-data-science-journey
```

---

## Useful Commands

```bash
# See what's changed since your last commit
git status

# See your commit history
git log --oneline

# Pull the latest from GitHub (if you work on multiple machines)
git pull

# Create a new branch (for experiments you're not sure about)
git checkout -b experiment-new-model

# Switch back to main branch
git checkout main

# Undo changes to a file (careful — this is permanent)
git checkout -- filename.py
```

---

## Writing Good Commit Messages

**Bad:**
```
git commit -m "update"
git commit -m "stuff"
git commit -m "wip"
```

**Good:**
```
git commit -m "Add Prophet time series model for monitoring well MW-07"
git commit -m "Fix detection limit handling in anomaly detection pipeline"
git commit -m "Complete Phase 1 ESG schema design notebook"
git commit -m "Add Azure Data Factory pipeline for ESG data ingestion"
```

Rule of thumb: finish the sentence *"If applied, this commit will..."*

---

## What NOT to Commit

The `.gitignore` handles most of this automatically, but be aware:

- ❌ Real client data (even anonymized — be cautious)
- ❌ Azure connection strings or API keys
- ❌ `.env` files with credentials
- ❌ Large model files (>50MB) — use Azure ML or a model registry instead
- ✅ Notebooks with synthetic/public data
- ✅ Scripts and utility functions
- ✅ READMEs and documentation
- ✅ Small sample data files labeled `sample_` or `synthetic_`

---

## If Something Goes Wrong

```bash
# See exactly what changed in each file
git diff

# Undo your last commit (keeps your changes, just un-commits them)
git reset HEAD~1

# Nuclear option: throw away ALL uncommitted changes (irreversible)
git checkout -- .
```

---

*When in doubt: `git status` first. It tells you exactly what state you're in.*
