# 🚀 Git & GitHub Lab Guide  

## 🎯 **Lab Objectives**
By the end of this lab, you will be able to:
- Create a **GitHub Account** and a **public repository**
- Install **Git** and **Visual Studio Code (VS Code)** on your laptop
- Initialize a **local Git repository** and commit code changes
- Connect and push code to your **remote GitHub repository**

---

## 🧩 **Prerequisites**
- Laptop with internet connection  
- Basic familiarity with terminal or command prompt  
- Valid email address for GitHub signup  

---

## 🪪 **Step 1: Create a GitHub Account**

1. Visit 👉 [https://github.com](https://github.com)
2. Click **Sign Up** and complete registration using your email.
3. Choose a **username** (e.g., `learner01`) and verify your account.
4. Once created, log in and open your GitHub **Dashboard**.

> 🧠 *GitHub is your cloud-based code hosting platform — where you’ll store and share your projects.*

---

## 📁 **Step 2: Create a New Repository**

1. Click the **+** icon on top-right → **New repository**
2. Fill the details:
   - **Repository name:** `hello-world`
   - **Description:** *My first Git & GitHub lab repository*
   - **Visibility:** Public ✅
   - (Optional) Check *Add a README file*
3. Click **Create repository**

✅ Your repository URL will look like:
`https://github.com/<your-username>/hello-world.git`


---

## 🔑 **Step 3: Generate a Personal Access Token (PAT)**

A PAT(instead of password) is required for authentication when pushing via HTTPS.

1. Go to **Profile → Settings → Developer Settings → Personal Access Tokens**
2. Click **Tokens (classic)** → **Generate new token**
3. Set a name like `gitlab-token`
4. Select the following scopes:
   - ✅ `repo` (or `public_repo` if your repo is public)
5. Set expiry (e.g., 90 days)
6. Click **Generate Token**
7. **Copy** the token immediately — you won’t see it again.

> 🧠 When Git asks for your password, **paste this PAT** (it stays invisible — that’s normal).

---

## 💻 **Step 4: Install Git and Visual Studio Code**

### 🪟 On Windows
1. **Install Git**
- Download and install **Git** → [https://git-scm.com/downloads](https://git-scm.com/downloads)
- Run the setup (`.exe`) and **accept all default options**.
- Verify installation: *Note:* (You can run this command either in *Windows Command Prompt* or in the *VS Code Terminal* after installation.))
  ```bash
  git --version
  ```
2. **Install Visual Studio Code**
   - Download from → [https://code.visualstudio.com/Download](https://code.visualstudio.com/Download)
   - Run the installer and launch **VS Code**.

> 🧠 *After installation, you may need to restart your computer to make Git Bash available in VS Code.*

---
## ⚙️ Step 5: Configure Git (One-time Setup)

1. **Open the VS Code Terminal:**
   - In VS Code, press `Ctrl + ~` (tilde) or go to **View → Terminal**  
   - From the terminal dropdown (▼), select **Git Bash**.
2. **Set your Git identity (your name and email):**    
```bash
git config --global user.name "Your Full Name"
```
```bash
git config --global user.email "your-email@example.com"
```
4. simple credential storing (or use manager)(optional):
```bash
git config --global credential.helper store     
```
5. Check configuration:
```bash
git config --list
```
✅ You should see your name and email listed.

---

## 📂 Step 6: Setup a Local Project

📝 Create a File Using VS Code

1. Open VS Code.
2. From the top menu, click File → Open Folder... → select your project folder (e.g., git-lab).
3. Click New File (📄 icon) in the Explorer sidebar.
4. Name it:
```bash
file1.txt
```
5. Add the following content:
```bash
Hello! Welcome to the GitHub Training.
```
6. Save the file using **Ctrl + S** (Windows)
7. Initialize Git:
```bash
git init
```
---
## 🧾 Step 7: Stage and Commit Files

1. Check repo status:
```bash
git status
```
2. Add files to the staging area:
```bash
git add .
```
3. Commit your changes:
```bash
git commit -m "My first Git commit"
```
4. Verify commit:
```bash
git log --oneline
```
---

## ☁️ Step 8: Connect to Your GitHub Repository

1. Add your GitHub repository as a remote origin:
```bash
2. git remote add origin https://github.com/<your-username>/hello-world.git
```
3. Verify:
```bash
git remote -v
```

---
## 🚀 Step 9: Push Your Code to GitHub

1. Push your local commit to remote GitHub repository:
```bash
git push origin master
```

💡 If your default branch is main, use:
```bash
git push origin main
```
2. When prompted:
* **Username:** Your GitHub username
* **Password:** Your Personal Access Token (PAT)

✅ Go to your GitHub repository — you should now see your files uploaded!

---

(You can run this command either in Windows Command Prompt or in the VS Code Terminal after installation.)
