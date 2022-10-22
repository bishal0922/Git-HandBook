## **Guide to GIT**
##### [Bishal Giri](https://www.bishalgiri.com)
---
### Notes from Git and GitHub for Beginners - Crash Course
[Lecture Link YT](https://www.youtube.com/watch?v=RGOj5yH7evk "Click to go to the lecture")


* **What is Git?**
Free and open-source version control system. Most programmers used git on a daily basis.

* **What is version control?**
It is the way we (programmers) track our code changes. As our code changes, we can look back to track down bugs or revert to a previous version. Some programs - Git Kraken, Git Desktop

### Some important terms:
* **Directory** : Folder
* **Terminal** : Interface for Text Commands 
* **CLI** :  Command Line Interface
* **Code** Editor:  Word Processor for Writing Code 
* **Repository/repo** : Project, folder/place where the project is kept
* **GitHub**:  Git is the tool that tracks changes in code over time. GitHub is the website where you host all of your git repositories. Being online can help show portfolio and make collaboration easier

### Git Commands (git ____ ):
* **clone**:  Bring project locally from Github
* **add**:  Track files and changes in git
* **commit**:  save changes 
* **push**:  when ready, upload to a remote repository, GitHub alternatives(bitbucket, GitLab)
* **pull**: when you want to bring changes, pull down changes

**Git status** :  shows everything that has been changed and not committed yet.
(if there’s a file that hasn’t been added for git to read then it’ll not show up). So,
Git add :

```git add . ```

tracks all the files or just git add index.html for specific files
Git status again now would show all the changes on the file

```git commit -m “message title” -m “Description”``` (commit is locally)

```git push ```
 push it to the repository

```git reset HEAD~1```
(unstages and uncommits the changes)
(when made a mistake HEAD is a pointer to the last commit HEAD~1 means go back one commit further)

---
### SSH Keys:

```Ssh-keygen -t rsa -b 4097 -C “email.com” ```

connect local machine to github account
(command type strength github email address).

Default file is .ssh/id_rsa. You can add a passphrase or make it empty.

```–testkey.pub``` is uploaded on the git repository.

```testkey``` is the private key and keep it on the machine
Cat testkey.pub prints out public key
* copy the key 
  ```pbcopy < ~/.testkey.pub``` copies it into clipboard
* gitub settings : ssh and gpg keys (new keys) and paste the key



```git push origin master```

--- 

If there's a folder which is not a git repository
1. ```git init:``` initialize git repository
2. ```git status``` : shows all the files that are not tracked
3. ```git add .``` : tracks all the files
4. ```git status``` : shows all the files that are tracked ready to be committed
5. ```git commit -m “created” -m “description”``` : commits the changes
6. ```git push origin master ``` : pushes the changes to the repository (would shows an error because we created it locally and don't have anywhere to push). So, create a new repo then use ```git remote add origin git@github.com:......``` to connect the local repo to the remote repo. Then, ```git push origin master``` to push the changes to the remote repo.)
7. ```git remote -v ``` (shows any remote repository connected to this repo)
8. ```git push origin master``` pushes the changes to the remote repo (git push can be used in future but we can use an upstream by 
9. ```git push -u origin master``` this will push the changes and set the upstream to the remote repo so that we don't have to use origin master in future. "-u ==   - -set-upstream" (after this we can just use git push)

---
### Review

* **Write code**: commit changes commit means add and commit if we had access to the repo
* **Locally Write** means code: state changes git add
* **Commit changes** git commit
* **Push changes** git push 
* **Pull request** (maybe)


---

**Git branching Master** : main or default branch

> Feature change: 
``` git checkout -b feature-branch-name``` creates a new branch and switches to it. Each individual only keeps track of what changes are made to the branch unless merged to the master branches.
(can be used to work before merging to the main branch of the code bases)

---
### Merge Branches
Inside the repo (local)

```git branch``` : shows all the branches

```git checkout master``` : switches to master branch
    
```git merge feature-branch-name``` : merges the feature branch to the master branch
    
```git branch -d feature-branch-name``` : deletes the feature branch
    
```git push origin master``` : pushes the changes to the remote repo
  
```git merge feature-branch-name``` : merges the feature branch to the master branch

```git branch -d feature-branch-name``` : deletes the feature branch
(shows the branches q to exit)

```git checkout``` : switch between branches

```git checkout -b feature ``` : Feature should be descriptive feature-11-newfile

```git branch master``` : switch back to master

```git checkout feature-11-newfile```: go back to the branch

```git diff feature-11-newfile```: show the difference in code in the branches (compare the changes in the codes)

```git merge feature-11-newfile```: merge into the master branch

```git status```: shows changes committed  or not

```git push```: tell which branch on github you want to push to 


```git pull```: get the changes in the branch

```git branch```: it’ll still show the branch

```git branch -d feature-11-newfile ```: deletes the file

**Merge conflicts** are better off solved within the code editor or the browser

```git log```: show log of all commits (important to have good commit messages). You can find hashes off the commits

```git reset *hash*```: unstage everything

```git reset --hard *hash*```: Unstage an completely remove

**Forking** makes a new branch and copies the review 

---
### The End 















