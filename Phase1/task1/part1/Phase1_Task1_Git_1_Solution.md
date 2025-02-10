# Challenge 1: Understanding Version Control


## 1.What is version control?

Version control - also known as source control or revision control - is an important software development practice for tracking and managing changes made to code and other files. It is closely related to source code management.



## Why is version control important in software development?

1. make backups
2. keep history
3. view changes
4. Experiment
5. Collaborate

**Create a codebase history:** Version control systems create a complete codebase history, stored in a specialized database, and provide the entire team with a single and secure source of truth.

**Ramp up collaboration:** By tracking every change, version control systems help teams avoid conflict and create opportunities to experiment and innovate.

**Reduce errors:** Using a version control tool allows developers to find errors fast, roll back to a previous version and correct the problem, mitigating the impact of the error.

**Improve code quality:** A version control system encourages developers to follow best practices and write clean code that is easy to access, understand, and maintain.

**Recover in a snap:** With version control, every code change is tracked, restorable, and revertible. A version control system acts as a safety net, preventing accidental code deletions and related developer anxiety.

**Increase coding confidence:** Developers rely on version control systems to synchronize versions so they can resolve conflicts and safely experiment.

**Expand visibility:** Team collaboration and communication improve with version control by providing full visibility to the code documentation and its history.

**Automate tasks:** Efficiency and productivity increase with a version control system by automating testing, analysis, and deployment for fast, consistent results.

# Challenge 2: Types of Version Control Systems (VCS)

## What are the main types of VCS?

**1. Local**

A local version control system is a database situated on your local computer where every file change is stored as a patch. Each patch set contains only the changes made to the file since its last version. To view what the file looked like at any given moment, it’s necessary to aggregate all the relevant patches to the file up to that specific moment.

***The main drawback with this system is that everything is stored locally. If anything were to happen to the local database, all the patches would be lost. Similarly, if anything were to happen to a single version, all the changes made after that version would be lost.***

![alt text](https://miro.medium.com/v2/resize:fit:640/format:webp/1*rmrT25EfoeqgulhBpZ9FuQ.png)

Examples of Local VCS: **SCCS**, **RCS**

**2. Centralized**

With centralized version control systems, you have a single “central” copy of your project on a self-hosted server and commit your changes to this central copy. You pull the files that you need, but you never have a full copy of your project locally. Some of the most common version control systems are centralized, including Subversion (SVN) and Perforce.

***This structure facilitates seamless collaboration among developers or a team. However, a significant drawback is that everything is stored on the centralized server. If something were to happen to that server, users wouldn’t be able to save their versioned changes, pull files, or collaborate. Similar to Local Version Control, if the central database were to become corrupted without proper backups, the entire project history could be lost, except for individual snapshots stored on users’ local machines.***


![alt text](https://miro.medium.com/v2/resize:fit:640/format:webp/1*XE_yTRkZkDqNpCM5BamoYw.png)

Examples of Centralized VCS: **CVS**, **Perforce**, **Subversion**

**3. Distibuted (DVCS)**

With distributed version control systems (DVCS), you don't rely on a central server to store all the versions of a project’s files. Instead, you clone a copy of a repository locally so that you have the full history of the project. 

![alt text](https://miro.medium.com/v2/resize:fit:640/format:webp/1*OV6nRDFioFpQtpE4f1D67w.png)

**Bazaar, Mercurial, Git, and Darcs**

## What is the difference between Centralized and Distributed VCS?

 Centralized and distributed version control systems differ primarily in how they store and manage project history. In a **centralized VCS**, such as Subversion (SVN) or Perforce, a single central server hosts the project's version history, and developers pull or push changes to this server without having a full local copy of the repository. This setup facilitates collaboration but creates a dependency on the central server—if it crashes or becomes corrupted without backups, project history may be lost. In contrast, a **distributed VCS (DVCS)**, like Git or Mercurial, allows each developer to clone the entire repository, including its full history, enabling offline work and reducing reliance on a single server. This makes distributed systems more resilient, as any local copy can restore the project if needed, while also improving performance by handling most operations locally.

## Name an example of each type.

Examples of Local VCS: **SCCS**, **RCS**

Examples of Centralized VCS: **CVS**, **Perforce**, **Subversion**

Examples of Local DVCS: **Bazaar, Mercurial, Git, and Darcs**


# Challenge 3: Git Ecosystem & Hosting Services

## What are some well-known Git hosting services?

Some well-known Git hosting services include:

1. **GitHub** – One of the most popular platforms for hosting Git repositories, widely used for open-source and private projects.
2. **GitLab** – A full DevOps platform with CI/CD, issue tracking, and built-in security features.
3. **Bitbucket** – A Git repository hosting service by Atlassian, commonly used by teams using Jira and Trello.
4. **SourceForge** – An older platform for hosting open-source projects with Git and SVN support.
5. **AWS CodeCommit** – A fully managed Git repository service provided by Amazon Web Services.
6. **Azure DevOps (formerly VSTS)** – Microsoft's platform with Git repository hosting, CI/CD pipelines, and project management tools.
7. **Gitea** – A lightweight, self-hosted Git service that is easy to deploy.
8. **Gogs** – A self-hosted Git service similar to Gitea but designed to be even more minimalistic.

## What is Gitea, and how does it compare to GitHub?



Github is a central service, all your data is on Github's servers on their machines. The big benefit of Gitea (and Gitlab) is you can **selfhost** it on your own servers (for free!), so you have total control of your data (important for certain industries), and you are not affected by Github outages etc.
Downside is you have to take care of server administration yourself. Gitlab – and recently also Gitea – offer paid managed instances: your data on your servers, but administration by them.

Gitea is free (in both senses). Gitlab has a gratis but feature-reduced community edition and a full enterprise edition (both closed-source). But I think even the community one has still more features than Gitea.
And compared to Github: Gitea has become noticably better over the last few years, but there is still a big difference in both features and polish to Github. I don't think Gitea at the moment has any features that Github does not (because it started out as a free Github clone. The devs often copy any new things that GH adds, but they will probably always lag a bit behind). The only big advantage is the selfhosting and the zero cost; if you don't want to trust them with sensitive data and/or don't want to pay for enterprise, Gitea can be an adequat replacement.

Github offers a large number of integrations with third party services (e.g., TravisCI, Jenkins, Sentry), while Gitea provides few such integrations by default

# Challenge 4: Local vs. Remote Git

![alt text](https://miro.medium.com/v2/resize:fit:640/format:webp/1*CGEmZKsnb3dC-nBkBneSNQ.png)

Local Repository:
A local repository is a copy of the entire project’s history and codebase that resides on a developer’s machine. When a developer initializes a local repository, Git sets up the necessary infrastructure to track changes, branches, and commits within the project.
A remote repository serves as a central hub where developers can collaborate and share their work with others. It enables team members to synchronize their changes and provides backup and visibility for the project. 

## What is meant by origin and upstream in Git?

$
# Challenge 5: Understanding Commits

## What does committing in Git do?

git commit creates a commit, which is like a snapshot of your repository. These commits are snapshots of your entire repository at specific times. You should make new commits often, based around logical units of change. Over time, commits should tell a story of the history of your repository and how it came to be the way that it currently is. Commits include lots of metadata in addition to the contents and message, like the author, timestamp, and more.


## How is it different from saving a file?

Great question! While **saving a file** and **committing in Git** may seem similar because both preserve changes, they operate at different levels and serve different purposes. Here’s the key difference:

### **1. Saving a File (Regular Save)**
- When you save a file in an editor, it simply updates that file on your local system.
- The old version is overwritten unless you manually create a backup.
- There is no built-in history of changes unless you use something like "Save As" with different filenames.

### **2. Git Commit (Version Control)**
- A **commit** in Git is like taking a "snapshot" of your project at a specific point in time.
- Each commit records **what changed, when, and by whom**.
- Commits are stored in Git’s history, meaning you can **revert to previous versions** if needed.
- Each commit has a unique **hash ID**, allowing you to track changes over time.


| Feature | Saving a File | Git Commit |
|---------|-------------|-----------|
| Purpose | Updates file on disk | Records a version in Git history |
| Tracks changes? | No | Yes |
| Can revert easily? | No | Yes |
| Requires a message? | No | Yes (commit message) |
| Scope | Single file | Entire project (staged changes) |

In short: **Saving a file updates its contents, while a Git commit permanently records a version of the project in version control.** 🚀


# Challenge 6: Branching in Git

## What is a Git branch?

🔹 A Git branch is a copy of your code where you can make changes without affecting the main version.
🔹 You can create multiple branches to work on different features or fixes simultaneously.
🔹 Once your work is done, you merge it back into the main branch.

## How do branches help in team collaboration?

✔ Parallel Work – Everyone works on different tasks without blocking each other.
✔ Code Isolation – Prevents incomplete or buggy code from breaking the main project.
✔ Safe Merging – Ensures tested, reviewed, and approved code gets into main.
✔ Effortless Experimentation – Try new ideas without risks.
✔ Efficient Bug Fixing – Hotfix branches allow quick bug resolution without disrupting ongoing work.

## What is the difference between main, dev, and feature branches?

1. **`main` branch** (or `master`) – The stable production-ready code.  
2. **`dev` branch** – The main development branch where new features are integrated.  
3. **`feature` branches** – Individual branches where new features are developed.
   


### **🛠 Summary: Differences at a Glance**

| Branch | Purpose | Who Works Here? | When to Merge? |  
|--------|---------|----------------|----------------|  
| `main` | Production-ready, stable branch | Only after testing | After full testing & approval |  
| `dev` | Development & testing before production | All developers merge features here | When a new release is ready |  
| `feature-*` | Work-in-progress new features | Individual developers | After the feature is completed & tested |  

---

## Challenge 7: Merge Conflicts



## What happens when changes collide in Git?
## How do developers resolve merge conflicts?

# Challenge 8: Forking in Git

## What does forking a repository mean?
## How does it differ from cloning?

# Challenge 9: When to Commit?
## When should you commit your changes?

## How frequent should commits be?


# Challenge 10: Common Git Commands

**git init:** (create the local repository)

**git clone:** When running git clone, what actually happens in the background is:

   * git init
    
  *  git remote add origin ${URL}
    
  *  git pull

----------------------------------------------------------------
**git add:** The git add command adds a change in the working directory to the staging area. 

**git commit:** The git commit command captures a snapshot of the project's currently staged changes.

----------------------------------------------------------------

**git push:** git push is most commonly used to publish an upload local changes to a central repository. 

**git pull:** The git pull command is used to fetch and download content from a remote repository and immediately update the local repository to match that content. 

-------------------------------------------------------------------
**git branch:** Git branches are effectively a pointer to a snapshot of your changes. 

**git checkout:** The git checkout command lets you navigate between the branches created by git branch

**git merge:** Git merge will combine multiple sequences of commits into one unified history. In the most frequent use cases, git merge is used to combine two branches. 






