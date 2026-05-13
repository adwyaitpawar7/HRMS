# Git Setup Commands Explanation

This guide explains the Git commands used to clone the repository, switch branches, and create a personal feature branch for development.

---

# 📥 1. Clone the Repository

```bash
git clone https://github.com/adwyaitpawar7/HRMS.git
```

## ✅ What This Command Does

- Downloads the complete repository from GitHub to your local machine.
- Creates a local copy of the project.
- Includes:
  - source code
  - commit history
  - branches
  - repository configuration

## 📌 Result

A new folder named:

```text
HRMS
```

will be created in your current directory.

---

# 📂 2. Move Into the Project Directory

```bash
cd HRMS
```

## ✅ What This Command Does

- Changes the terminal location to the cloned repository folder.
- Required before running Git commands related to the project.

## 📌 Result

You are now inside:

```text
HRMS/
```

---

# 🌿 3. Switch to the Development Branch

```bash
git checkout HRMS_DEV
```

## ✅ What This Command Does

- Switches from the default branch (usually `main` or `master`) to:

```text
HRMS_DEV
```

## 📌 Why This Is Important

The `HRMS_DEV` branch is typically used as:

- a shared development branch
- integration branch for new features
- base branch for feature development

Developers should usually create feature branches from the development branch instead of directly from `main`.

---

# 🌱 4. Create Your Own Feature Branch

```bash
git checkout -b Feature/HRMS_DEV_Adwyait
```

## ✅ What This Command Does

This command performs **two actions**:

### 1️⃣ Creates a New Branch

Creates a branch named:

```text
Feature/HRMS_DEV_Adwyait
```

### 2️⃣ Automatically Switches to the New Branch

After creation, Git moves you directly into that branch.

---

## 📌 Why Feature Branches Are Used

Feature branches help:

- isolate developer work
- prevent direct changes in shared branches
- simplify code reviews
- reduce merge conflicts

---

## 📌 Naming Convention

Example:

```text
Feature/HRMS_DEV_Adwyait
```

Structure:

```text
Feature/<BaseBranch>_<DeveloperName>
```

This makes it easy to identify:

- feature type
- base branch
- developer

---

# ⬅ 5. Move Back One Directory

```bash
cd ..
```

## ✅ What This Command Does

Moves one level back from the current directory.

Example:

```text
Before:
HRMS/

After:
Parent Directory
```

---

# 📊 Complete Flow Summary

```text
1. Clone Repository
        ↓
2. Enter Project Folder
        ↓
3. Switch to Development Branch
        ↓
4. Create Personal Feature Branch
        ↓
5. Start Development
```

---

# 🚀 Recommended Workflow After This

## Check Current Branch

```bash
git branch
```

---

## Pull Latest Changes

```bash
git pull origin HRMS_DEV
```

---

## Add Changes

```bash
git add .
```

---

## Commit Changes

```bash
git commit -m "Added new feature"
```

---

## Push Feature Branch

```bash
git push origin Feature/HRMS_DEV_Adwyait
```

---

# ⭐ Best Practices

✅ Always create feature branches from the development branch.

✅ Never directly push changes to:

- `main`
- `master`
- shared development branches

✅ Pull latest changes regularly to avoid conflicts.

✅ Use meaningful commit messages.

---

# 🧠 Example Real Workflow

```bash
git clone https://github.com/adwyaitpawar7/HRMS.git

cd HRMS

git checkout HRMS_DEV

git checkout -b Feature/HRMS_DEV_Adwyait

# Start development...

git add .

git commit -m "Implemented login functionality"

git push origin Feature/HRMS_DEV_Adwyait
```

---

# 👨‍💻 Purpose of This Workflow

This workflow is commonly used in professional teams to:

- maintain code quality
- support multiple developers
- avoid production issues
- enable proper code review process
- maintain clean Git history
