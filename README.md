# devops

					GIT_All Concepts
Version Control System (VCS) is a software that helps software developers to work together and maintain a complete history of their work.

**Listed below are the functions of a VCS −**
•	Allows developers to work simultaneously.

•	Does not allow overwriting each other’s changes.

•	Maintains a history of every version.

**Advantages of Git**
•	Free and open source

•	Fast and small

•	Easier branching

•	Implicit backup
 
**GIT ARCHITECHTURE:**

![image](https://github.com/user-attachments/assets/d848cede-de92-4a48-8573-06fecdd1a03f)

 
**Local Workspace:** this is the space local workspace where it contains all the files, folders and can do all the changes and work on it. Once we do all the changes and sure of having the changes in centralized repository (github) we start with the command git add

Command: git add <file name1> <file name 2> 

 git add . 
 
git add *

git add –A 

git add –a

git add -u  Add all changes to tracked files only and This command stages modifications and deletions, but not new files


**Staging/Index:**  Once the changes are done and sure with the changes, we save the data in staging or index. We assign a commit id for reference here in staging.

Command: git commit –m “message for reference”

git commit --amend  Changing the Last Commit Message

git commit --amend -m "New commit msg"  Amend the Last Commit Msg with a New Msg (without opening an editor)

git rebase -i HEAD~N  Changing an Older Commit Message

Local Repository: the files here in Local Repository are ready to push github. 

Command: git push

**Remote Repository/ Centralised repository:** this is the centralized repository(github) where all your code is stored and can be accessed to all the developers and others in the organization.

**Git Revert vs Git Reset:** These are the commands that are used to 

Git Revert: Git revert is used to revert back a commit which is pushed into the github. This is used in a scenario where we need to undo the changes in the github repository. 

Command: git revert <the commit id to be reverted>
 
**Git reset:** Git reset is also a command which is used to revert back the changes, the difference is git revert will leave the footprint (ie., it will leave a commit id for each and every commit) where as git reset doesn’t give any commit id.

![image](https://github.com/user-attachments/assets/25b12a94-a8b9-4d62-a151-bef019ccba83)

Git reset --soft: using the bellow command we can bring back the committed data in back to staging

Git reset --mixed: using the bellow command we can bring back the committed data back to local working directory

Git reset --hard: using the bellow command we can bring back the committed data and delete it.

Considering below example and need to bring back cid1

**Git Cherry pick:**

To get a specified commit id of some other branch we can use git cherry-pick

command: git cherry-pick <commit-id> (from the target branch)

**Git Stash:** when you want to record the current state of the working directory and the index, but want to go back to a clean working directory. The command saves your local modifications away and reverts the working directory to match the initial 
**Commands: **
git stash save (to save the current changes)

Git stash list (to see the information of saved data)

Git stash pop (to bring back the workspace)

Git shash drop (to delete the workspace)

**GIT Interview Question:**

**What is GIT ?**
  
Git is a version control system used for tracking changes in computer files. It is generally used for source code management in software development.

•Git is used to tracking changes in the source code

•The distributed version control tool is used for source code management

•It allows multiple developers to work together

•It supports non-linear development through its thousands of parallel branches

* **What is difference between GIT &Github?**
  
Git is a version control system that allows developers to track changes in their code. GitHub is a web-based hosting service for git repositories. In simple terms, you can use git without Github, but you cannot use GitHub without Git.

* **Why we use GIT?**
  
Git is used to tracking changes in the source code, enabling multiple developers to work together on non-linear development

* **What is SCM &VCS?**
  
VCS are sometimes known as SCM (Source Code Management) tools or RCS (Revision Control System)

* What are the process of pushing the code to GithubRepository ?
  
* **Why do we commit?**
  
The "commit" command is used to save your changes to the local repository.

* **Difference between github and SVN**
  
GitHub is a distributed version control platform. SVN is a centralized version control platform.

* **What are the commands of GIT to push the code?**
  
git push -u origin master

* **What is branching in git?**
  
A branch in Git is simply a lightweight movable pointer to one of these commits. The default branch name in Git is master .

* **Different types of branching in GIT?**
  
Feature Branches, Release Branches, Hotfix Branches, Main/Branch or Master/Branch

* **What is merge conflict in git?**
  
A merge conflict is an event that takes place when Git is unable to automatically resolve differences in code between two commits.

* **How you can resolve merge conflict?**
  
. Accept the local version. To accept all changes on a file from the local version, run: git checkout --ours <file name> ...

. Accept the remote version. ...

. Review changes individually.

**Git commands**
Path: C:\Users\kalkumar\projects\olio-ELK\Prod\68 Logstash\versa 

git stash

git checkout kalva-dev

git checkout -b kalva_dev

git status

git add.

git commit -m

git fetch origin

git rebase origin/dev

git push origin HEAD: refs/for/dev

---------------------------------------------
git clone ssh URL

cd Olio-ELK

git checkout kalva_dev

git status

git add .

git status

git commit -m "ELK versa_raw_tcp_logs.conf"

git push origin HEAD:refs/for/kalva_dev

------------------------

git fetch origin

git stash

git rebase origin/master

git rebase --abort

git stash apply

git add .

git commit -m "sample"

git push origin HEAD:refs/for/kalva_dev

git cherry-pick <commit-hash> will apply the changes made in an existing commit to another branch, while
recording a new commit. Essentially, you can copy commits from branch to branch.

Recover from git stash

git stash apply

git stash list

git stash pop

git stash clear  Removes the last stash

git stash drop stash@{n}  Remove the specific stash

**remove untracked files**

git clean -i

git clean -f

git pull --rebase

git config --global alias.up 'pull --rebase --autostash'

git reset --hard origin/master
