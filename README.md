# Git and Github Interview Questions and Answers

## 1. What is Git & Github?
### Git : 
A distributed version control system (VCS) used for tracking changes in source code during software development.It is installed on the local machine.Git keeps track of the files you have edited so, if we want the previous code again we can revert it. once the code is done developer pushes the code into the central repository called Github.

### Github : 
A cloud-based platform that hosts Git repositories, providing features like collaboration, issue tracking, and CI/CD.It store all project source code. Developers can pull the updated code from GitHub to the local machine where git is installed and start their work.

## 2. Which git Version have you used in your project?
The Git version depends on the project, but commonly used versions are Git 2.x.We can check git version using 
```
git --version
```
## 3. How will you create a repository on local machine? Explain steps.
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


## Difference between Git and Github ?

![What is Git (2)](https://github.com/user-attachments/assets/09fe20a0-ffad-4312-8a37-cba8ef07f2e2)

## What is CVCS and DVCS and Explain the difference.
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

## Difference between git pull and git fetch ? 
## Difference between git pull and git clone 
## Difference between git pull and git push ?
## Difference between git fork and git clone ? 

## What is head in git ?.
## Explain git workflow or git Architecture? 
## What is git stash?
## What is staging area?
## What is commit area?
## What is git reset and git revert ? Explain the difference?
## What is branch in git? Explain branching strategy?
## what is git conflict?
## What is git log? 
## What is git Status?
## How to ignore unwanted files while adding a files to staging area?
## What is git merge and rebase?
## What is git cherry pick?
## How to recover deleted branch?
## Scenario:
You accidentally deleted your f1 branch.
```
git reflog  # Find the last commit hash
git checkout -b f1 <commit-hash>
```
![reflog](https://github.com/user-attachments/assets/1fa964fa-f4a9-4317-b495-4013bdafe793)

