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

* Created a new branch (`feature`) from `main`
* Switched to the feature branch

### 3️⃣ Parallel Changes

* Added changes in `feature` branch
* Switched back to `main` and made different changes

### 4️⃣ Merge Operation

* Merged `feature` branch into `main`
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
 ├── README.md
 └── screenshots/
      ├── git-graph.png
      ├── conflict.png
      └── merge-result.png
```

---

## 🚀 How to Run This Lab

Follow the steps below to reproduce the branching, merging, and conflict resolution workflow.

---

### 🔹 Step 1: Initialize Repository

```bash
git init
echo "hello" > file.txt
git add .
git commit -m "first"
```

👉 This creates the base project.

---

### 🔹 Step 2: Create Feature Branch

```bash
git checkout -b feature
echo "feature change" >> file.txt
git add .
git commit -m "Feature work"
```

👉 Work is done in the `feature` branch.

---

### 🔹 Step 3: Switch to Main Branch

```bash
git checkout master
echo "main change" >> file.txt
git add .
git commit -m "Main edit"
```

👉 Now a different change is made in the main branch.

---

### ⚠️ Why Conflict Occurs

👉 Both `feature` and `master` branches modified the **same file (`file.txt`)** after branching.
👉 When Git tries to merge, it cannot automatically decide which change to keep.

---

### 🔹 Step 4: Merge Branches

```bash
git merge feature
```

👉 This will trigger a **merge conflict**.

---

### 🔹 Step 5: Resolve Conflict

Open `file.txt` and you will see:

```text
<<<<<<< HEAD
main change
=======
feature change
>>>>>>> feature
```

👉 Manually resolve it by keeping the desired content:

```text
hello
main edit
feature edit
```

---

### 🔹 Step 6: Finalize Merge

```bash
git add .
git commit -m "Resolved merge conflict"
```

👉 This completes the merge process.

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

