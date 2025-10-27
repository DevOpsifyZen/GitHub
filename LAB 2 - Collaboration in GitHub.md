# 🤝 Collaboration in GitHub — Lab Guide  

## 🎯 **Lab Objectives**
By the end of this lab, you will be able to:
- Understand and apply common **branching strategies** (Feature, Release, Hotfix)
- Create and switch branches locally
- Push branches to GitHub and open **Pull Requests (PRs)**
- Perform **code reviews** and merge changes into the main branch

---

## 🧩 **Prerequisites**
Before starting this lab, ensure you have completed **Module 1 (Git & GitHub Basics)** and:
- You have a GitHub account
- Repository `hello-world` already exists on GitHub
- Git & VS Code are installed and configured on your system
- You have successfully pushed an initial commit to the `main` (or `master`) branch

---

## 🌿 **Step 1: Understand Branching Strategies**

### 1️⃣ Feature Branch
- Used to develop new features or enhancements.
- Branch name format: `feature/<feature-name>`

> 🧠 *Branching allows multiple people to work on separate tasks without affecting the main code base.*

---

## 💻 **Step 2: Create a Feature Branch Locally**

1. Open your project folder (`hello-world`) in **VS Code**.
2. Open the **Terminal (bash)**.
3. Check the current branch:
```bash
git branch
```
4. Create and switch to a new feature branch:
```bash
git checkout -b feature
```
✅ You are now working on the feature branch.

---

## ✍️ Step 3: Make and Commit a Change

1. Open the file you created earlier (file1.txt or README.md).
2. Add one more line:
```bash
This is an update from the feature branch.
```
3. Save the file.
4. Stage and commit the change:
```bash
git add .
git commit -m "Added an update message from feature branch"
```

5. Push the branch to GitHub:
```bash
git push -u origin feature
```

✅ Your new branch is now available on GitHub.

---

## 🧾 Step 4: Create a Pull Request (PR)

1. Go to your GitHub repository → you’ll see a banner:

  || “Compare & pull request”

2. Click Compare & pull request.
3. Add details:
   * **Title:** Added update message in file1.txt
   * **Description:** Demonstrating feature branch workflow
4. Click Create Pull Request.

---

## 👀 Step 5: Perform a Code Review

1. Open your newly created Pull Request on GitHub.
2. You’ll see your file change highlighted.
3. Click Files changed → Add comment to review code (optional).
4. Once reviewed, click Approve or Comment.
5. When ready, click Merge Pull Request → Confirm Merge.
6. Delete the branch (optional):
   * GitHub will show a “Delete branch” button after merging — click it.
---

## 🧰 Step 6: Verify and Review Branches

Check which branches exist locally and remotely:
```bash
git branch -a
```

Delete merged local branches (optional cleanup):
```bash
git branch -d feature
```
---

🎉 Congratulations!
You have successfully **Collaboration in GitHub**

