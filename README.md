Install Git
    ↓
Configure user.name/user.email
    ↓
Create GitHub Account
    ↓
Create GitHub Repository
    ↓
git init
    ↓
git add .
    ↓
git commit
    ↓
git remote add origin <HTTPS URL>
    ↓
Create GitHub PAT
    ↓
git push -u origin main
    ↓
Future: git pull → git add → git commit → git push


# Git to GitHub (HTTPS) Setup Guide

## Step 1: Install Git

### macOS

```bash
git --version
```

If Git is not installed:

```bash
xcode-select --install
```

Verify installation:

```bash
git --version
```

---

## Step 2: Configure Git Identity

```bash
git config --global user.name "Rohit Gupta"
git config --global user.email "your-email@example.com"
```

Verify:

```bash
git config --global --list
```

---

## Step 3: Create a GitHub Account

1. Sign up on GitHub.
2. Verify your email address.

---

## Step 4: Create a Repository on GitHub

1. Log in to GitHub.
2. Click **New Repository**.
3. Enter a repository name.
4. Choose Public or Private.
5. Click **Create Repository**.

Example repository URL:

```text
https://github.com/<username>/ontrack-ai-demo.git
```

---

## Step 5: Create or Open a Local Project

```bash
mkdir ontrack-ai-demo
cd ontrack-ai-demo
git init
```

Verify:

```bash
git status
```

---

## Step 6: Add Files

```bash
echo "# ONTRACK AI DEMO" > README.md
```

Check status:

```bash
git status
```

---

## Step 7: Commit Files

```bash
git add .
git commit -m "Initial commit"
```

Verify:

```bash
git log --oneline
```

---

## Step 8: Connect Local Repository to GitHub

Add remote:

```bash
git remote add origin https://github.com/<username>/ontrack-ai-demo.git
```

Verify:

```bash
git remote -v
```

---

## Step 9: Create a Personal Access Token (PAT)

GitHub does not accept account passwords for Git operations.

1. GitHub Settings
2. Developer Settings
3. Personal Access Tokens
4. Generate Token
5. Grant at least the `repo` permission

Save the generated token securely.

---

## Step 10: Push Code to GitHub

Check your branch:

```bash
git branch
```

Push to GitHub:

```bash
git push -u origin main
```

When prompted:

```text
Username: <your GitHub username>
Password: <your Personal Access Token>
```

---

## Step 11: Store Credentials in macOS Keychain

```bash
git config --global credential.helper osxkeychain
```

This avoids entering your token repeatedly.

---

## Step 12: Daily Workflow

Pull latest changes:

```bash
git pull
```

Make changes and commit:

```bash
git add .
git commit -m "Added feature"
```

Push to GitHub:

```bash
git push
```

---

## Quick Reference

```bash
git add .
git commit -m "message"
git pull
git push
git status
```

## End-to-End Flow

```text
Install Git
    ↓
Configure user.name/user.email
    ↓
Create GitHub Account
    ↓
Create GitHub Repository
    ↓
git init
    ↓
git add .
    ↓
git commit
    ↓
git remote add origin <HTTPS URL>
    ↓
Create PAT Token
    ↓
git push -u origin main
    ↓
Daily: git pull → git add → git commit → git push
```
