# Phase 1, Task 1, Git Practice

## Challenge 1: Set Up a Private Git Repository  
**Goal:**  
- Learn how to create and configure a private repository on a Git hosting platform.  

**Challenge:**  
- Create a private repository on **GitHub/GitLab**.  
- Explore the different settings available when creating a repository.  

**Hints:**  
- public vs private?  
- description, license, README

---

## Challenge 2: Generate and Add an SSH Key  
**Goal:**  
- Understand SSH authentication and set up secure access to remote repositories.  

**Challenge:**  
- Generate an **SSH key** (`ssh-keygen`).  
- Add the SSH key to your **GitHub/GitLab** account.  
- Verify that SSH authentication works (`ssh -T git@github.com`).  
- Where are SSH keys stored on your machine?
- What is the advantage of using SSH over HTTPS for Git authentication?  

---

## Challenge 3: Clone the Repository  
**Goal:**  
- Learn how to clone a repository using SSH.  

**Challenge:**  
- Clone your private repository using SSH (`git clone git@github.com:username/repo.git`).  
- Compare **SSH cloning** vs. **HTTPS cloning**.  
- Check which remote URL type you are using?

---

## Challenge 4: Add a Collaborator  
**Goal:**  
- Learn how to share a repository and control access.  

**Challenge:**  
- Invite a collaborator to your private repository.  
- Review different permission levels available for collaborators.  
- What are the available roles in **GitHub/GitLab** (e.g., read, write, admin)? 


---

## Challenge 5: Stage, Commit, and Push Changes  
**Goal:**  
- Learn how to track changes and push them to a remote repository.  

**Challenge:**  
- Create a new file (`README.md`) and add some content.  
- Use `git add` to stage the file.  
- Commit the change with a **clear message** (`git commit -m "Add README"`).  
- Push the changes to the **remote repository**.  
- What happens if you try to push without committing first?  
- Use `git log` to view commit history.
- What are the most popular options for `git log`?
- What is Head? What other information is available in the log?

---

## Challenge 6: Create a .gitignore File  
**Goal:**  
- Understand how to prevent tracking of unnecessary files.  

**Challenge:**  
- Create a **.gitignore** file and add common patterns (e.g., ignoring `.log` files).  
- Add some files that follow the pattern specified in the .gitignore (e.g something.log file)
- Try to add an ignored file and see what happens.
- What are `node_modules/`, `__pycache__/`, or `.env` files?  

**Hints:**  
- Use `git status` to check ignored files.

---

## Challenge 7: Modify a File and Commit Again  
**Goal:**  
- Understand how to track modifications in Git.  

**Challenge:**  
- Edit `README.md`, stage, and commit the changes.  
- Use `git status` before and after staging.  
- What’s the difference between **unstaged** and **staged** changes?  

**Hints:**  
- Use `git diff`

---

## Challenge 8: Create a File Online and Pull Changes Locally  
**Goal:**  
- Learn how to sync changes between local and remote repositories.  

**Challenge:**  
- Add a new file using **GitHub/GitLab’s web interface**.  
- What is `git fetch` and how is it different from `pull`?
- Fetch changes and check repo's state.
- Pull repo on your local machine and check repo's state.


**Hints:**  
- What happens if you **don’t pull before making local changes**?  

---

## Challenge 9: Undoing Changes (Reverting & Resetting)  
**Goal:**  
- Learn how to undo commits and changes safely.  

**Challenge:**  
- Modify a file, stage it, then **unstage** it.  
- Commit a change and undo the commit using `reset`.
- Commit a change and then **revert** it before pushing.  

---

## Challenge 10: Viewing and Navigating Git History  
**Goal:**  
- Understand how to inspect past commits and changes.  

**Challenge:**  
- Use `git log` to view commit history.  
- Use `git show <commit-hash>` to inspect a specific commit.  
- Use `git diff` to compare different commits.  

**Hints:**  
- What do `HEAD`, `HEAD~1`, and `HEAD~2` mean in Git?  