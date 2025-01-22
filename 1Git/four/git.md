---

# Level 1: Git Basics

👋 **Welcome, Developer!**  
Congratulations on embarking on this journey to master the powerful tools of **Git** and **GitHub**. To make it fun and digestible, we’ve designed this guide like a game—each level brings you closer to becoming a Git Guru! Let's jump into **Level 1**, where you'll unlock the foundations of version control.

---

## 🧩 **What’s the difference between Git and GitHub?**

Imagine you're writing a novel:

* **Git** is like your editor: it tracks all the changes, suggests improvements, and helps you jump back to any earlier version.
    
* **GitHub** is like the library where the final novel (and its drafts) are stored. It’s an online platform for collaboration, sharing, and storing code.
    

In short:

* **Git = Version Control Tool (local).**
    
* **GitHub = Cloud-based Repository for sharing (remote).**
    

## 🕹️ **What is Version Control?**

Think of it like a “save game” feature in your favorite video game:

* 🕑 You can save your progress at different stages.
    
* 🔄 If something goes wrong, you can reload an earlier save.
    
* 🤝 You and your team can work on different levels without messing up each other's progress.
    

---

## 🛠️ **Step 1: Download Git**

**For Windows**

1. Go to the [Git official website](https://git-scm.com/downloads).
    
2. Click the "Download for Windows" button.
    
3. Run the installer and follow the default settings (or customize them if you're feeling adventurous).
    

**For Mac**

1. Install **Xcode Command Line Tools** by running:
    
    ```plaintext
    xcode-select --install
    ```
    
2. Or, download Git directly from [git-scm.com](https://git-scm.com/downloads/mac).
    

**For Linux**  
Use your package manager:

* Debian/Ubuntu:
    
    ```plaintext
    sudo apt install git
    ```
    

Fedora:

```plaintext
sudo dnf install git
```

---

## 🛡️ **Step 2: Configure Git**

After installation, tell Git who you are. Run these commands in the terminal (replace with your info):

```plaintext
git config --global user.name "Your Name"  
git config --global user.email "youremail@example.com"
```

🏁 **Checkpoint:** Use this to check your configuration:

```plaintext
git config --list
```

If you see your name and email, you’re good to go!

---

## 🌐 **Step 3: Create a GitHub Account**

1. Go to [GitHub](https://github.com/).
    
2. Click **Sign Up**.
    
3. Fill in your details, choose a strong password, and verify your email.
    
4. Customize your profile with a cool avatar (optional but fun)!
    

---

# **Level 2: Terminology and Git Flow**

👋 **Welcome to Level 2, Developer!**  
You've mastered the basics; now it's time to solidify your skills. This level covers essential Git commands and concepts in a short and concise way—a perfect recap for new team members.

---

## 🧩 **Key Terminology**

### **1\. Git Basics**

* **Check Git Version:**
    
    ```plaintext
    git --version
    ```
    
* **Check Repo Status:**  
    Shows tracked/untracked changes:
    
    ```plaintext
    git status
    ```
    
* **Your Git Config:**  
    Verify name and email settings:
    
    ```plaintext
    git config --list
    ```
    

---

### **2\. Create & Manage a Repository**

* **Initialize a New Repo:**
    
    ```plaintext
    git init
    ```
    
* **Git Flow (Working to GitHub):**
    
    1. **Edit Files (Working Directory - Untracked):**  
        Update files in your project folder.
        
    2. **Stage Changes (Staging Area):**  
        Add files to the staging area:
        
        ```plaintext
        git add <filename>
        ```
        
        Or add all changes:
        
        ```plaintext
        git add .
        ```
        
    3. **Commit Changes (Local Repo):**  
        Save your changes with a message:
        
        ```plaintext
        git commit -m "Your commit message"
        ```
        
    4. **Push Changes (GitHub):**  
        Send your changes to GitHub:
        
        ```plaintext
        git push origin main
        ```
        

---

### **3\. Logs and History**

* **View Commit History:**
    
    ```plaintext
    git log
    ```
    
    * Shorter view:
        
        ```plaintext
        git log --oneline
        ```
        

---

### **4\. Editor Settings**

* **Change Default Code Editor:**  
    Use VS Code for Git commit messages:
    
    ```plaintext
    git config --global core.editor "code --wait"
    ```
    

---

### **5\. Ignore Files**

* **Create** `.gitignore` file to exclude unnecessary files like:
    
    ```plaintext
    node_modules
    .env
    .vscode
    ```
    

---

### **6\. Sync with GitHub**

* **Push Changes (to GitHub):**
    
    ```plaintext
    git push
    ```
    
* **Pull Updates (from GitHub):**
    
    ```plaintext
    git pull
    ```
    

---

## 🔗 **Cloning the ChaiCode Repository**

1. **Clone Command (📥):**  
    Copy a repo from GitHub to your local system:
    
    ```plaintext
    git clone <repository-url>
    ```
    

**Navigate into the Folder (📂):**  
Move into the cloned repo directory:

```plaintext
cd <repository-name>
```

<details data-node-type="hn-details-summary"><summary>🛠️ Optional: Git Behind the Scenes</summary><div data-type="detailsContent">The <code>.git</code> folder is Git's brain, storing everything about your repository. It uses <strong>three key objects</strong>: <strong>Blob</strong> for file contents, <strong>Tree</strong> for folder structure, <strong>Commit</strong> for snapshots linking changes and history. These objects live in <code>.git/objects</code>, making Git efficient by storing changes as snapshots, not whole files! 🚀</div></details>

---

# **Level 3: Branches and Merges**

👋 **Welcome to Level 3, Developer!**  
You’re now entering the exciting world of **branches and merges**. This level covers how to manage branches, their flow in a company like ChaiCohort, and merging techniques for smooth collaboration.

---

## 🧩 **Branch Flow at ChaiCohort**

Here’s ChaiCohort organize branches:

1. `main` (Stable Branch):
    
    * The stable version of the code.
        
    * Used for **deployments** and **production-ready** code.
        
2. `development` (Testing Branch):
    
    * Contains changes being tested or prepared for the main branch.
        
    * Developers merge their completed work here before production.
        
3. **Feature or Employee Branches:**
    
    * Created for individual features, tasks, or experiments.
        
    * Example: `feature-login` or `john-task-42`.
        
    * Keeps work isolated until it’s ready to integrate.
        

---

## 🔨 **Creating and Switching Branches**

1. **Check Existing Branches:**
    
    ```plaintext
    git branch
    ```
    
2. **Create a New Branch:**
    
    ```plaintext
    git branch <branch-name>
    ```
    
3. **Switch to a Branch:**
    
    ```plaintext
    git checkout <branch-name>
    ```
    
    Or use the shortcut:
    
    ```plaintext
    git switch <branch-name>
    ```
    
4. **Create and Switch Simultaneously:**
    
    ```plaintext
    git checkout -b <branch-name>
    ```
    
    Or:
    
    ```plaintext
    git switch -c <branch-name>
    ```
    

---

## 🔄 **Merging Branches**

1. **Switch to the Target Branch:**  
    (e.g., Merge a feature branch into `development`)
    
    ```plaintext
    git checkout development
    ```
    
2. **Merge the Branch:**
    
    ```plaintext
    git merge <branch-name>
    ```
    
3. **Resolve Conflicts (if any):**
    
    * Git marks conflicts in files.
        
    * Edit the files, remove conflict markers (`<<<<`, `====`, `>>>>`).
        
    * Add the resolved files:
        
        ```plaintext
        git add <filename>
        ```
        
    * Complete the merge:
        
        ```plaintext
        git commit
        ```
        

---

# **Level 4: Writing Good Commit Messages**

👋 **Welcome to Level 4, Developer!**  
Writing great commit messages is like leaving a clear trail of breadcrumbs for your team. At ChaiCohort, commit messages help us stay **aligned**, **efficient**, and **collaborative**. Let’s explore how to craft them with a personal touch for our community.

---

## 🖋️ **Rules for Writing Great Commit Messages at ChaiCohort**

1. **Use Present Tense** 🕰️
    
    * Write as if you're describing what the commit does **now**, not what you already did.
        
    * ✅ **"Add login feature"**
        
    * 🚫 **"Added login feature"**
        
2. **Capitalize the First Letter** 📌
    
    * Every commit message should look polished.
        
3. **Keep It Short and Sweet** 💬
    
    * Limit to 50 characters or fewer for the summary line.
        
    * Additional details can go in the description if needed.
        
4. **Use Meaningful Prefixes (Personalized for ChaiCohort)** 🔑  
    Prefixes categorize commits for better readability. Examples:
    
    * `feat:` For adding new features:  
        `feat: Add user authentication`
        
    * `fix:` For bug fixes:  
        `fix: Resolve login page crash`
        
    * `refactor:` For improving code without changing functionality:  
        `refactor: Simplify login logic`
        
    * `docs:` For documentation updates:  
        `docs: Update README with setup instructions`
        
    * `test:` For adding or updating tests:  
        `test: Add tests for authentication`
        
    * `style:` For formatting changes (no logic changes):  
        `style: Fix indentation in Login.js`
        
5. **Use "Why" and "What" When Necessary** 💡
    
    * Provide context when making significant changes.
        
    * Example:
        
        ```plaintext
        feat: Add API integration for user data  
        
        Why: To enable data synchronization with the backend  
        What: Added Axios for requests, created API service.
        ```
        

---

## 🔨 **Example Commit Messages for ChaiCohort**

### For a New Feature

✅ `feat: Add user profile page`

### For Fixing a Bug

✅ `fix: Resolve issue with data loading on dashboard`

### For Improving Code Structure

✅ `refactor: Modularize utility functions`

---

# **Level 5: Pull Requests (PRs)**

👋 **Welcome to Level 5, Developer!**  
You’ve mastered branches, commits, and merges—now it’s time to learn about **Pull Requests (PRs)**. PRs are how we share, review, and merge our changes into shared branches like `main` or `development`. Let’s simplify the process!

---

## 🛠️ **What is a Pull Request (PR)?**

A **Pull Request** is a way to:

1. **Propose your changes** to be added to a shared branch (like `main` or `development`).
    
2. **Start a conversation** with your team about your code.
    
3. **Request a review** to ensure the code is high quality and aligned with the project.
    

---

## 🔨 **How to Create a Pull Request on GitHub**

1. **Push Your Changes to GitHub:**  
    After committing your changes locally, push your branch:
    
    ```plaintext
    git push origin <branch-name>
    ```
    
2. **Go to Your Repository on GitHub:**
    
    * You’ll see a notification: "Compare & pull request." Click it.
        
    * Or go to the **Pull Requests** tab and click **New Pull Request**.
        
3. **Select Branches:**
    
    * Choose your feature branch as the **source**.
        
    * Choose the branch you’re merging into (e.g., `development`) as the **target**.
        
4. **Write a PR Title and Description:**
    
    * **Title:** Short and meaningful, like your commit messages.  
        Example: `feat: Add user registration feature`
        
    * **Description:**
        
        * **What did you do?** (e.g., "Added registration functionality using a new API.")
            
        * **Why did you do it?** (e.g., "Needed for user onboarding.")
            
        * **How to test it?** (e.g., "Go to `/register` and complete the form.")
            
5. **Request a Code Review:**
    
    * Add reviewers from your team to ensure the changes meet standards.
        
    * Tag specific people if your work depends on their input.
        
6. **Submit the PR:**  
    Click **Create Pull Request** and wait for feedback!
    

---

## 📝 **ChaiCohort PR Guidelines**

1. **Be Clear and Concise:**
    
    * Make it easy for reviewers to understand what your changes do and why.
        
2. **Follow the Template:**  
    ChaiCohort’s PR template ensures consistency. Example format:
    
    * **What:** Summary of the changes.
        
    * **Why:** Why the change was needed.
        
    * **How to Test:** Steps to verify it works.
        
3. **Request Reviews Promptly:**  
    Always request feedback from relevant teammates early to avoid delays.
    
4. **Fix Feedback Quickly:**  
    Address comments from reviewers promptly and update your PR.
    

---

# **Congratulations, Developer!**

You’ve completed your onboarding journey through Git and GitHub essentials at ChaiCohort. Here’s a final checklist of **Best Practices** to keep you and the team productive and conflict-free.

---

## 🛡️ **Best Practices for Git & GitHub at ChaiCohort**

> **Commit Regularly:**
> 
> Small, frequent commits make it easier to track progress, debug issues, and collaborate effectively. Avoid large, monolithic commits that bundle unrelated changes.

> **Use Descriptive Commit Messages:**
> 
> Commit messages should clearly explain what was changed and why. Follow the ChaiCohort Commit Message Guidelines from Level 4 to keep our history clean and meaningful.

> **Pull Updates Regularly:**
> 
> Before starting new work or committing changes, always pull the latest updates from your branch:
> 
> ```plaintext
> git pull origin <branch-name>
> ```
> 
> This helps prevent merge conflicts and keeps your work in sync with the team.

---

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">🚀 <strong>Time to level up your collaboration skills!</strong></div>
</div>

Your Git and GitHub journey at ChaiCohort is just getting started, and you’re now equipped to **work smarter**, **code faster**, and **collaborate like a pro**! 🎉

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">🔧 <strong>Stay tuned for more tech docs</strong> to help you conquer new challenges and keep growing as a developer. The adventure never stops— ✨💻</div>
</div>