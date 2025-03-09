# Git and Github Interview Questions and Answers

## 📌 What is Git & Github?
### Git : 
A distributed version control system (VCS) used for tracking changes in source code during software development.It is installed on the local machine.Git keeps track of the files you have edited so, if we want the previous code again we can revert it. once the code is done developer pushes the code into the central repository called Github.

### Github : 
A cloud-based platform that hosts Git repositories, providing features like collaboration, issue tracking, and CI/CD.It store all project source code. Developers can pull the updated code from GitHub to the local machine where git is installed and start their work.

## 📌 Which git Version have you used in your project?
The Git version depends on the project, but commonly used versions are Git 2.x.We can check git version using 
```
git --version
```
## 📌 How will you create a repository on local machine? Explain steps.
### Scenario:
You start a new project and want to use Git.

### 💡 Example:
```
mkdir my_project && cd my_project
git init # Initialize repository
touch test1.txt
git status
git add .
git status
git commit -m "initial commit"
git log --oneline

```
![gitrepo1](https://github.com/user-attachments/assets/6962dd58-8881-4e51-b093-7385f76d1f15)
![gitrepo2](https://github.com/user-attachments/assets/70bdcb38-f104-433c-b856-025951d87de0)


## 📌 Difference between Git and Github ?

![What is Git (2)](https://github.com/user-attachments/assets/09fe20a0-ffad-4312-8a37-cba8ef07f2e2)

## 📌 What is CVCS and DVCS and Explain the difference.
CVCS relies on a central server to store code, whereas DVCS allows every developer to have a complete copy of the project, making it faster and more reliable.

![What is Git](https://github.com/user-attachments/assets/9f71f0b1-5843-4230-b37e-a8d5202cb522)

![What is Git (1)](https://github.com/user-attachments/assets/dc08cc55-562c-4929-bc94-8aa636900c09)


| Feature | CVCS (Centralized Version Control System)	 | DVCS (Distributed Version Control System) |
|  :---: |   :---:    |    :---: |
| ` What is it?	`   | A single central server stores the code, and all users access it.	     | Every developer has a full copy of the project history.    |
| ` Dependency on Server `    | Needs an internet connection to work; if the server goes down, work stops.       | Can work offline because every user has a full copy.      |
| ` Speed `   | Slower because every operation requires server communication.       | Faster since most operations are local.      |
| ` Data Loss Risk `	    | High—if the server crashes, history can be lost.	       | Low—code history is available on every developer’s machine.      |
| ` Examples	`   | SVN (Subversion), Perforce, CVS		       | Git, Mercurial      |

## 📌 Difference between git pull and git fetch ? 

![What is Git (2)](https://github.com/user-attachments/assets/6403d5f0-85f9-4e27-9a4e-90aeb710fcf9)

* **git pull :**
  * fetches and merges remote changes automatically
    
* **git clone :**
    * git fetch only downloads changes without merging them.

|  Command |   git pull  |  git fetch  |
| ------------- | ------------- | ------------- |
| What it does? | Downloads new changes from the remote repository and automatically merges them into your local branch.  | Only downloads new changes from the remote repository but does NOT merge them automatically.  |
|Effect on Local Code| Updates your working directory immediately.	 | Doesn’t affect your working directory until you manually merge.  |
|Use Case |When you want the latest changes and are ready to merge them into your work.	 | When you want to check for updates before merging. |
|Command to Merge After Fetching|Not needed (pull does it automatically).	 | git merge origin/main (to apply fetched changes).  |
|Risk |Can cause conflicts if your local changes conflict with remote updates.	 | Safer since it doesn’t change your working code immediately.  |

## 📌 Difference between git pull and git clone ?
   * **git clone :**
     * copies an entire repository from remote to local for the first time. 
   * **git pull :**
     * updates an existing local repo with new changes from remote.

## 📌 Difference between git pull and git push ?
🔹 **Real-Life Example:**

   * **git pull** → Downloading the latest messages in your WhatsApp group.
  
   * **git push** → Sending a new message to the WhatsApp group.

![What is Git (4)](https://github.com/user-attachments/assets/1d528007-aee2-4ab8-b4d9-b8e67c837826)

 
    
## 📌 Difference between git fork and git clone ? 

🔹 **Real-Life Example:**

   * **git fork** → Copying a Google Doc to your account but keeping the original separate.
     
   * **git clone** → Downloading a PDF from Google Drive to your computer.

## 📌 What is head in git ?

🔹 **HEAD** is the pointer to the latest commit in your current branch.When you commit changes, HEAD moves to the new commit.

## 📌 Explain git workflow or git Architecture? 
    
 🔹 **Git follows three areas:**

  * **Working Directory** → Your local files.
     * This is where you make changes to your files.
     * It contains both tracked (modified/unmodified) and untracked files.
     * Changes here are not yet added to Git.
     * git status → Shows which files are modified in the working directory.
       
  * **Staging Area** → Files ready to be committed (git add).
     * A temporary area where you place changes before committing.
     * Only staged files will be included in the next commit.
     * git add <file> → Moves changes from the working area to the staging area.
       
  * **Repository** → Where committed files are stored permanently (git commit).
     * Stores committed changes permanently in the Git repository.
     * Each commit represents a snapshot of your project.
     * git commit -m "message" → Moves files from staging to the repository.
     * git log → Shows commit history.
     * git log --pretty=oneline
    

       ![What is Git (3)](https://github.com/user-attachments/assets/73677adc-e2d7-493f-b33f-8d292d7c2ffe)

    
  
## 📌 What is git stash?

  * git stash temporarily saves your uncommitted changes without **committing** them.
  * Useful when you need to switch branches but don’t want to lose your work.
    
## 📌  What is staging area?

  * A temporary area where you place changes before committing.
  * git add <file> → Moves changes from the working area to the **staging area.**
  
  
## 📌  What is commit area?

  * Stores permanent snapshots of your code history.
  * You move files from the staging area to the commit area using git commit.
    
🔹 **Example:**
    ```
    git commit -m "Added new feature"
    ```
      
🔹 **Real-Life Example:**
      Submitting final homework after writing and reviewing it.

## 📌 What is git reset and git revert ? Explain the difference?

🔹 **Real-Life Example:**

   * **git reset** → Erasing a sent WhatsApp message.
     
       * Imagine you sent a wrong message and deleted it permanently before anyone saw it.
   * **git revert** → Sending a correction message.
     
       * You sent a wrong message but sent another message to correct it, keeping both messages in chat history.

 ![What is Git (5)](https://github.com/user-attachments/assets/bdcabc65-33ba-4035-8f2f-19a9ff0c8148)

     

## 📌 What is branch in git? Explain branching strategy?



## 📌 what is git conflict?

* A Git conflict happens when two people change the same part of a file.
* To resolve it:

  * Open the conflicted file.
  
  * Choose which version to keep.
  
  * Commit the resolved file.

 🔹 **Example:**
  ```
     git add conflict-file.txt
     git commit -m "Resolved merge conflict"
  ```

🔹 **Real-Life Example:**

    Two people editing the same Google Doc without seeing each other’s changes.


## 📌 What is git log? 

  * **Shows the history of commits.**
    
   **Example:**
     ```
       git log --oneline
     ```
🔹 **Real-Life Example:**

      Checking your browser history.



## 📌 What is git Status?

  * Shows the current state of your repo (staged, unstaged, untracked files).
   
  **Example:**
     ```
       git status
     ```
🔹 **Real-Life Example:**

  Checking your **to-do list** before submitting work.


## 📌 How to ignore unwanted files while adding a files to staging area?

  * Use a .gitignore file to exclude files from Git tracking.

## 📌 What is git merge and rebase?

🔹 **Real-Life Example:**

  * **git merge** → Mixing two paint colors.
  * **git rebase** → Lining up dominoes neatly.

## 📌 What is git cherry pick?
  * Picks a specific commit from another branch.
    
  **Example:**
     ```
       git cherry-pick abc123
     ```


## 📌 How to recover deleted branch?

🔹 **Real-Life Example:**

 * Restoring a **deleted photo** from the recycle bin.


## Scenario:
You accidentally deleted your f1 branch.
```
git reflog  # Find the last commit hash
git checkout -b f1 <commit-hash>
```
![reflog](https://github.com/user-attachments/assets/1fa964fa-f4a9-4317-b495-4013bdafe793)


![thank-you-gif-5](https://github.com/user-attachments/assets/76ca83b3-dbc2-42b9-b57f-851204c2c6f4)




