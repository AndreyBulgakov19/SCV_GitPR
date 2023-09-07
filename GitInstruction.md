![logo](git_logo.jpg)
# Working with Git and GitHub
## 1. Check Git installation
Complete **git version** command in terminal.
If installed the message will appear. Else, the error message will appear.
## 2. If Git is not installed
Download the latest Git version from [site](https://git-scm.com/downloads). Set the default settings.
## 3. Git setup
Introduce yourself during the first launch.
Complete two commands:
``````
git config --global user.name "Your name"
git config --global user.email "Your email"
``````
## 4. Repo initialization
To initialize a git repo choose an existing folder or create a new one. Open the folder with VSCode. Create a new terminal and apply the following command:
```
git init
```
## 5. Saving changes in repo
To save the modifications in files complete the following command to track these files in Git:
```
git add <name of the file>
```
and the next comand to apply the changes:
```
git commit -m "Comments"
```
The second variant is to use the joint command:
```
git commit -am "Comments"
```
## 6. Commit logs
To view the history of commits use the command:
```
git log
```
## 7. Moving between commits
To move between the commits complete the command **git log** to view the hash-code of a desired commit. Next complete the command:
```
git checkout <hash-code of a desired commit>
```
## 8. Ignoring files
Create a ***.gitignore*** file to make Git ignore any files or folders in the repo. Insert the names of such files or folders to this file.
## 9. Branching
Use the following commands to create a branch:
``````
git branch <new branch name>
``````
**master** is a default name for the main branch.
Use the following command to view the branches list in the repo:
```
git branch
```
## 10. Merging branches, resolving conflicts
To merge the chosen branch with current branch use the command:
```
git merge <name of the chosen branch>
```
If the same parts of the file were modified in both branches the conflict may occure. The user may be involved to resolve the conflict. VSCode offers several actions. One of the variants should be chosen to resolve the conflict or do the merge manualy.
After resolving the conflict the merge commit must be completed.
## 11. Deleting branches
To delete a branch switch to another branch using command:
```
git switch <name of the branch>
```
and
```
git branch -d <name of the branch>
```
to delete the desired branch.
## 12. Working with remote repositories
1. Create a GitHub account;
2. Create a local repository;
3. Create a remote repository;
4. Connect a remote repository with local.

Add the remote repo to the project:
```
git remote add <name of the repo> <repo net url>
```
To get and merge the changes from a remote repo the following command is used:
```
git pull
```
## 13. Working with someone's project remote repository
1. Find the repository of a project on GitHub.
2. Click "Fork" to add version of a project to your own account.
3. On the project page click "Code", than copy the https link.
4. In VSCode complete the following command to clone the remote repo to the local computer:
```
git clone <repo https link>
``` 
5. Create and go to the new branch:
```
git checkout -b <name of the new branch>
```
6. Perform any manipulations with the information in the project.
7. Commit the changes.
8. Push the changes to the remote repo in your account on GitHub using the command below:
```
git push --set-upstream origin
```
9. Go to the project page and click the green button "Compare & Pull request" to make a pull request to the owner of the project.
 