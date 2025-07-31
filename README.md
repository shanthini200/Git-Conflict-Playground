#  Git Conflict Playground

This repository demonstrates how to **intentionally create and resolve a Git merge conflict**, simulating a real-world scenario that developers often face while collaborating on shared codebases.



## 📚 Project Objective

**To showcase:**
- How merge conflicts occur in Git
- How to manually resolve a conflict
- Proper use of Git branches, merges, and commit history
- Best practices for documenting version control workflows


## 🛠️ Tools Used

- Git (Local version control)
- GitHub (Remote repository hosting)
- Markdown (for documentation)



## 👨‍💻 Conflict Scenario

- Created `branch-A` and `branch-B`.
- Both branches edited the same line in `conflict.txt`.
- Merging them caused a conflict.

## 🚀 Step-by-Step Conflict Scenario

###  Initial Setup
1. Created a new GitHub repository: 
   - `git-conflict-playground`

2. Cloned it locally using:
   ```bash
   git clone https://github.com/your-username/git-conflict-playground.git
   cd git-conflict-playground
   ```
3. Added a file conflict.txt with an initial line:
   ```bash
   echo "Initial Line" > conflict.txt
   git add conflict.txt
   git commit -m "Add conflict.txt with initial line"
   ```
4. Creating Two Conflicted Branches:
 
   **Branch A**
   ```bash
   git checkout -b branch-A
   echo "Line from branch A" >> conflict.txt
   git commit -am "Add line from branch A"
   ```
   **Branch B**
   ```bash
   git checkout -b branch-B
   echo "Line from branch B" >> conflict.txt
   git commit -am "Add line from branch B"
   ```
6. Triggering Merge Conflicts
   Back in main:

   ```bash
   git checkout main
   git merge branch-A   # Successful merge
   git merge branch-B   # Conflict occurs here
   ```
7. Conflict in conflict.txt:
   ```
   <<<<<<< HEAD
   Line from branch A
   =======
   Line from branch B
   >>>>>>> branch-B
   ```
8. 🛠️ Conflict Resolution
   Manually resolved the conflict by editing conflict.txt:
   ```
   Line from branch A and B
   ```
   then,
   ```bash
   git add conflict.txt
   git commit -m "Manually resolved conflict between branch A and B"
   ```
9. Pushing To GitHub
   ```bash
   git push origin main
   git push origin branch-A
   git push origin branch-B
   ```
**All branches are now visible on GitHub.**
- **To Mark This As First Version You Can Use Git Tags.**

## >Sample Conflict Section, If Created

![git-conf-res](https://github.com/user-attachments/assets/fe88baf0-3e4e-422a-bfd7-607b3dc27045)

## The Project Demonstrates
- Branching and merging
- How Git handles line-based conflicts
- How to manually resolve and commit conflict changes
- Clean Git history with meaningful commits
- Real-world version control simulation for interviews

## ✅ Key Takeaways

- Practiced resolving real Git merge conflicts
- Used Git branching and merging effectively
- Demonstrated clean documentation and commit history

##  🙌 Author
- Shandhini Parthiban
- 🔗 GitHub: https://github.com/shanthini200



