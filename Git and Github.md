# Git and GitHub - Questions & Answers

A comprehensive Q&A collection covering essential Git and GitHub concepts.

---

## **Q: What is Git and GitHub?**

**Answer:**
- **Git** = Version control tool (installed on your system)
- **GitHub** = Cloud platform to host Git repositories online

---

## **Q: Difference between Git and GitHub?**

**Answer:**
- **Git** = Works locally (offline)
- **GitHub** = Hosting + collaboration (online)

---

## **Q: Alternatives of GitHub?**

**Answer:**
- GitLab
- Bitbucket  
- SourceForge

---

## **Q: Can Git work without internet?**

**Answer:**
- **Yes ✅** (Git is local)
- Internet only needed to push/pull to GitHub

---

## **Q: What is GitHub's cherry-pick command?**

**Answer:**
- It takes one commit from another branch and applies it to your current branch

**Usage:**
```bash
git cherry-pick <commit-hash>
```

---

## **Q: What does `git stash` do?**

**Answer:**
- Saves your uncommitted changes aside (like a clipboard)
- Lets you switch branch safely

**Common commands:**
```bash
git stash           # Save changes
git stash pop       # Restore changes
git stash list      # View all stashes
```

---

## **Q: Explain staging in Git?**

**Answer:**
- A middle area where files are tracked before final commit
- **Flow:** `Working Dir → Staging Area → Commit`

**Visual representation:**
```
Working Directory  →  Staging Area  →  Local Repository
     (git add)           (git commit)
```

---

## **Q: Can we use GitHub without Git?**

**Answer:**
- **Yes**, you can upload/edit files directly on GitHub website
- **But** you lose version control power and advanced Git features

---

## **Q: How does `git init` work?**

**Answer:**
- Creates a hidden `.git` folder in your project
- That's the local repository where Git stores all version control data

**Command:**
```bash
git init
```

---

## **Q: Git stores data in which folder?**

**Answer:**
- `.git` folder (inside project)
- This hidden folder contains all commits, branches, and Git metadata

---

## **Q: How `.gitignore` works?**

**Answer:**
- Lists files/folders to exclude from version control
- Git reads it and ignores those paths during `git add`

**Example `.gitignore`:**
```gitignore
node_modules/
*.log
.env
dist/
.DS_Store
```

---

## **Q: Structure of Git?**

**Answer:**
```
Working Directory → Staging Area (Index) → Local Repo → Remote Repo
```

**Explanation:**
1. **Working Directory** - Where you edit files
2. **Staging Area** - Files prepared for commit
3. **Local Repo** - Your local Git repository
4. **Remote Repo** - Shared repository (like on GitHub)

---

## **Q: Where does Git store data?**

**Answer:**
- In `.git` folder (commits, branches, logs)
- Contains object database with all version history
- Stores configuration and repository metadata

---

## **Q: GitHub commands/functions?**

**Answer:**

| Command | Purpose |
|---------|---------|
| `clone` | Copy repository to local machine |
| `pull` | Bring latest changes from remote |
| `push` | Upload local commits to remote |
| `fork` | Copy repository to your GitHub account |
| `blame` | See who wrote each line of code |

**Usage examples:**
```bash
git clone <repository-url>
git pull origin main
git push origin main
git blame <filename>
```

---

## **Q: Difference between `add`, `commit`, and `push`?**

**Answer:**

| Command | Action | Scope |
|---------|--------|-------|
| `add` | Stage file | Working Dir → Staging Area |
| `commit` | Save snapshot in local repo | Staging Area → Local Repo |
| `push` | Send commits to GitHub | Local Repo → Remote Repo |

**Workflow:**
```bash
git add <filename>           # Stage changes
git commit -m "message"      # Commit locally  
git push origin main         # Push to remote
```

---

## **Q: What's the hashcode in `git log`?**

**Answer:**
- A unique **SHA-1 identifier** for each commit
- 40-character hexadecimal string
- Example: `a1b2c3d4e5f6789012345678901234567890abcd`

**View commits:**
```bash
git log                 # Full details
git log --oneline       # Compact view with short hash
```

---

## Quick Command Reference

### Basic Git Workflow
```bash
# Initialize repository
git init

# Stage and commit
git add .
git commit -m "Your commit message"

# Connect to remote and push
git remote add origin <repository-url>
git push -u origin main

# Daily workflow
git status
git pull origin main
git add .
git commit -m "Update"
git push origin main
```

### Branch Operations
```bash
git branch <branch-name>        # Create branch
git checkout <branch-name>      # Switch branch
git checkout -b <branch-name>   # Create and switch
git merge <branch-name>         # Merge branch
```

---

*This Q&A guide covers fundamental Git and GitHub concepts. For advanced topics, refer to [Git Documentation](https://git-scm.com/docs) and [GitHub Documentation](https://docs.github.com).*