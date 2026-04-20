# 🚀 Git Branching, Merging & Conflict Resolution Lab

## 📌 Overview

This repository demonstrates hands-on practice of core Git concepts including branching, merging, and conflict resolution. The goal of this lab was to understand how Git manages parallel development and handles merge conflicts in real-world scenarios.

---

## 🧠 Concepts Covered

* Git initialization and commits
* Creating and switching branches
* Parallel development using branches
* Merging branches into main
* Handling and resolving merge conflicts
* Understanding Git commit graph

---

## 🛠️ Steps Performed

### 1️⃣ Initial Setup

* Initialized a Git repository
* Created a base file (`file.txt`)
* Performed initial commit

### 2️⃣ Branch Creation

* Created a new branch (`feature`) from `master`
* Switched to the feature branch

### 3️⃣ Parallel Changes

* Added changes in `feature` branch
* Switched back to `master` and made different changes

### 4️⃣ Merge Operation

* Merged `feature` branch into `master`
* Encountered a merge conflict due to changes in the same file

### 5️⃣ Conflict Resolution

* Manually resolved conflict markers:

  ```
  <<<<<<< HEAD
  =======
  >>>>>>> feature
  ```
* Finalized merge with a commit

---

## 📊 Git Graph Insight

The commit graph clearly demonstrates:

* Branch divergence (parallel work)
* Independent commits in both branches
* Merge commit after conflict resolution

---

## 💡 Key Learnings

* Git branches are lightweight pointers, not copies of code
* Changes remain isolated within branches until merged
* Merge conflicts occur when the same lines are modified in multiple branches
* Conflict resolution requires manual decision-making
* Git Graph helps visualize project history effectively

---

## 📂 Project Structure

```
git-branching-lab/
 ├── file.txt
 └── README.md
```

---

## 🚀 How to Run This Lab

```bash
git init
echo "hello" > file.txt
git add .
git commit -m "Initial commit"

git checkout -b feature
echo "feature change" >> file.txt
git add .
git commit -m "Feature update"

git checkout master
echo "main change" >> file.txt
git add .
git commit -m "Main update"

git merge feature
```

---

## 🔥 Outcome

Successfully demonstrated:

* Real-world Git workflow
* Conflict detection and resolution
* Visual understanding of branching using Git Graph

---

## 📎 Author

**Mohit Verma**
Aspiring Cloud & DevOps Engineer 🚀

---

