------

###  <img src="logo4.jpg" alt="Clarusway Logo Footer" width="40"/> **In-Class Exercises for Git Branches and Contributions**

------

# **Git Hands-On Lab Session**

## **Lab Objectives**

By the end of this lab, you will be able to:

- Set up and configure Git on your local machine.
- Create and manage a local Git repository.
- Understand the Git workflow: staging, committing, and tracking changes.
- Work with remote repositories (GitHub).
- Resolve a basic merge conflict.
- Complete a **challenge task** to test your Git skills.

---

## **Lab Setup**

### **1. Install Git (If Not Already Installed)**

- Download Git from [git-scm.com](https://git-scm.com/).
- Verify installation by running:
  ```bash
  git --version
  ```

### **2. Configure Git**

Set your username and email (used in commits):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

---

## **Lab Tasks**

### **Task 1: Initialize a Local Repository**

1. Create a new directory for your project:
   ```bash
   mkdir git-lab
   cd git-lab
   ```
2. Initialize a Git repository:
   ```bash
   git init
   ```
3. Check the status of your repo:
   ```bash
   git status
   ```
   - Expected output: `On branch main` (or `master`) with no commits yet.

---

### **Task 2: Create and Track Files**

1. Create a new file:
   ```bash
   echo "# Welcome to Git Lab" > README.md
   ```
2. Stage the file for commit:
   ```bash
   git add README.md
   ```
3. Commit the changes:
   ```bash
   git commit -m "Initial commit: Added README"
   ```
4. Check the commit history:
   ```bash
   git log
   ```

---

### **Task 3: Modify and Commit Changes**

1. Edit `README.md` (add a new line, e.g., `## Project Description`).
2. Check the changes:
   ```bash
   git diff
   ```
3. Stage and commit the changes:
   ```bash
   git add README.md
   git commit -m "Updated README with project description"
   ```

---

### **Task 4: Work with Remote Repositories (GitHub)**

1. Create a new repository on **GitHub** (do not initialize with a README).
2. Link your local repo to GitHub:
   ```bash
   git remote add origin https://github.com/your-username/repo-name.git
   ```
3. Push your local commits to GitHub:
   ```bash
   git push -u origin main
   ```
4. Verify the changes on GitHub.

---

### **Task 5: Branching and Merging**

1. Create and switch to a new branch:
   ```bash
   git checkout -b feature/add-contributors
   ```
2. Add a new file:
   ```bash
   echo "Contributors: Your Name" > CONTRIBUTORS.md
   ```
3. Commit the changes:
   ```bash
   git add CONTRIBUTORS.md
   git commit -m "Added contributors file"
   ```
4. Switch back to `main` and merge the branch:
   ```bash
   git checkout main
   git merge feature/add-contributors
   ```
5. Push the merged changes to GitHub:
   ```bash
   git push origin main
   ```

---

### **Task 6: Resolve a Merge Conflict (Simulated)**

1. On GitHub, edit `README.md` directly (add a line at the bottom).
2. Locally, edit the same line in `README.md` and commit:
   ```bash
   git add README.md
   git commit -m "Updated README locally"
   ```
3. Attempt to push:
   ```bash
   git push origin main
   ```
   - This will fail due to a conflict.
4. Pull the latest changes and resolve the conflict:
   ```bash
   git pull origin main
   ```
   - Open `README.md`, manually resolve conflicts (keep both changes).
5. Commit and push the resolved file:
   ```bash
   git add README.md
   git commit -m "Resolved merge conflict"
   git push origin main
   ```

---

## **Challenge Task**

### **Scenario:**

You are working on a team project. Your task is to:

1. **Fork** a repository from GitHub
   (https://github.com/clarusway/sda-git-fork-lab.git).
2. **Clone** your fork locally.
3. Create a **new branch** (`feature/your-feature`).
4. Make changes (e.g., add a new file or modify an existing one).
5. **Commit** and **push** your changes to your fork.
6. Open a **Pull Request (PR)** to the original repository.
7. **Resolve a merge conflict** if one arises during the PR.

### **Success Criteria:**

- Your PR is successfully merged into the main project.
- You have resolved at least one merge conflict (simulated if necessary).

---

### **Solution to Git Challenge: Fork, Branch, PR, and Conflict Resolution**

Here's a step-by-step walkthrough of how to successfully complete the challenge:

---

#### **Step 1: Fork the Repository**

1. Go to the instructor's GitHub repository
   (https://github.com/clarusway/sda-git-fork-lab.git).
2. Click **"Fork"** (top-right) to create your copy under your GitHub account.
   - Now, you have `https://github.com/your-username/sda-git-fork-lab`.

---

#### **Step 2: Clone Your Fork Locally**

1. Open your terminal/Git Bash.
2. Clone your fork:
   ```bash
   git clone https://github.com/your-username/sda-fit-fork-lab.git
   cd sda-git-fork-lab
   ```

---

#### **Step 3: Create a New Branch**

1. Create and switch to a feature branch:
   ```bash
   git checkout -b feature/add-docs
   ```
   _(Replace `add-docs` with your feature name, e.g., `fix-typo` or
   `new-feature`.)_

---

#### **Step 4: Make Changes**

1. Add a new file (e.g., `contributors.md`):

   ```bash
   echo "## Contributors\n- Your Name" > contributors.md
   ```

   - Or modify an existing file (e.g., `README.md`).

2. Verify changes:
   ```bash
   git status  # Shows untracked/modified files
   git diff    # Shows line-by-line changes
   ```

---

#### **Step 5: Commit and Push to Your Fork**

1. Stage and commit changes:
   ```bash
   git add contributors.md
   git commit -m "Added contributors list"
   ```
2. Push to your fork (first push requires `-u`):
   ```bash
   git push -u origin feature/add-docs
   ```

---

#### **Step 6: Open a Pull Request (PR)**

1. Go to your fork on GitHub
   (`https://github.com/your-username/sda-git-fork-lab`).
2. Click **"Pull Request"** (you’ll see a prompt comparing your branch to the
   original repo).
3. Fill in:
   - **Title**: "Add contributors list"
   - **Description**: Explain your changes (e.g., "This PR adds a contributors
     file.").
4. Click **"Create Pull Request"**.

---

#### **Verification**

- Your PR should now be **mergeable**.
- Wait for the instructor to review and merge it.
- If approved, your changes will be part of the original project!

---

#### **Key Takeaways**

✅ Forked a repo → Cloned locally → Created a branch.  
✅ Made changes → Committed → Pushed to GitHub.  
✅ Opened a PR → Resolved conflicts (if any).  
✅ Successfully contributed to a team project!

---

## **Lab Conclusion**

- You’ve practiced **Git basics**: init, add, commit, push, pull.
- You’ve worked with **branches** and **merge conflicts**.
- You’ve contributed to a remote repository via **forking and PRs**.
- You’ve completed a **real-world Git challenge**.

Happy coding! 🚀

---

<div align="center">   <img src="logo.png" alt="Clarusway Logo Footer" width="400"/> </div>

---
