##Bishal Giri
Notes from Git and GitHub for Beginners - Crash Course

What is Git?
Free and open-source version control system
Most programmers used git on a daily basis

What is version control?
Way we (programmers) track our code changes. As our code changes, we can look back to track down bugs or revert to a previous version

Some programmers - Git Kraken, Git Desktop

Directory -> Folder
Terminal -> Interface for Text Commands 
CLI -> Command Line Interface
	cd-> Change directory
Code Editor-> Word Processor for Writing Code 
Repository/repo ->Project, folder/place where the project is kept
GitHub-> Git is the tool that tracks changes in code over time. GitHub is the website where you host all of your git repositories. Being online can help show portfolio and make collaboration easier

Git Commands:
clone-> Bring project locally from Github
add-> Track files and changes in git
commit-> save changes 
push-> when ready, upload to a remote repository, GitHub alternatives(bitbucket, GitLab)
pull->when you want to bring changes, pull down changes

Git status -> shows everything that has been changed and not committed yet
(if there’s a file that hasn’t been added for git to read then it’ll not show up) So,
Git add -> git add . -> tracks all the files or just git add index.html for specific files
Git status again now would show all the changes on the file

Git commit -m “message title” -m “Description” (commit is locally)
Git push -> push it to the repository

Git reset HEAD~1
(unstages and uncommits the changes)
(when made a mistake HEAD is a pointer to the last commit HEAD~1 means go back one commit further)








SSH Keys:

Ssh-keygen -t rsa -b 4097 -C “email.com”
(connect local machine to github account)
(command type strength github email address)
Default file is .ssh/id_rsa
You can add a passphrase or make it empty
–testkey.pub is uploaded on the git repository
testkey is the private key and keep it on the machine
Cat testkey.pub prints out public key
-> copy the key (pbcopy < ~/.testkey.pub copies it into clipboard) 
-> gitub settings -> ssh and gpg keys (new keys) and paste the key



Git push origin master

If there's a folder which is not a git repository
Git init
(initialize git repository)
Git status
(will show untracked file)
Git add .
Git status
(ready to be committed)
Git commit -m “created” -m “description”
Git push origin master 
(shows an error because we created it locally and don't have anywhere to push)
(create a new repo then use git remote add origin git@github.com:......)
Git remote -v 
(shows any remote repository connected to this repo)
Git push origin master
(git push can be used in future but we can use an upstream by 
Git push -u origin master)
(-u ==   - -set-upstream)
(after this we can just use git push)

Review
Write code-> commit changes (commit means add and commit) if we had access to the repo
Locally Write means code-> state changes (git add) -> Commit changes (git commit) -> push changes (git push) -> pull request (maybe)




Git branching
Master -> main or default branch

Feature change
Each individual only keeps track of what changes are made to the branch
Unless merged to the master branches
(can be used to work before merging to the main branch of the code bases)


Inside the repo (local)
Git branch
(shows the branches q to exit)
Git checkout
(switch between branches
Git checkout -b feature 
Feature should be descriptive feature-11-newfile
)

Git branch (shows the branch)
Git branch master
(switch back to master)
Git checkout feature-11-newfile
(go back to the branch)

Git diff feature-11-newfile
(show the difference in code in the branches)
(compare the changes in the codes)
Git merge feature-11-newfile

Git status (shows changes committed  or not)
Git push (tell which branch on github you want to push to) 


Git pull - get the changes in the branch
Git branch (it’ll still show the branch)
Git branch -d feature-11-newfile 
(deletes the file)

Merge conflicts are better off solved within the code editor or the browser

Git log (show log of all commits) (important to have good commit messages)
-you can find hashes off the commits

Git reset *hash*
(unstage everything)
Git reset - - hard *hash*
(Unstage an completely remove)

Forking makes a new branch and copies the review 
 















