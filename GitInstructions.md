![Logo](Git-Logo-White_small.png)
![Git_Logo](https://git-scm.com/images/logo@2x.png)

# Working with "Git" Version Control System (VCS)

## _What is VCS and what is it for_
Version control is the organization of structured tracking and management of changes occurring in the program code. VCS are tools that help software (SW) developers manage changes to source code over time. These tools are especially useful for DevOps teams, as they help reduce the time spent on project development and increase the number of successful deployments.

Git is one of the most popular free and open-source VCS tools today. It is also called a category of Distributed VCS (DVCS).

Below is the instruction on how to install and use the Git VCS for any of the uses including SW development.

## 1. Check if "Git" has been already installed

Execute the command ***git --version*** in the terminal. If "Git" is installed then information about the version of the software will be shown, otherwise, the error message will occur.

## 2. Installing "Git"

Download the latest version of "Git" from the [website](https://git-scm.com/downloadsj)
Install using the default settings

You can also download and install the VSCode tool to improve your Git experience (see [VSCode](https://code.visualstudio.com/)).

## 3. Setting up "Git"

At first use Git, you need to introduce yourself. To do so you are going to enter two commands in the terminal:
```Bash
git config --global user.name "Your name using English letters"
git config --global user.email your_email@example.com
```

## 4. Getting a Repository

"Git" repository is obtained in two ways:
1. Turn a current local directory into a Git repository using the ***git init*** command;
2. Clone an existing repository using the ***git clone*** command.

#### 4.1. Initializing a Repository in the current directory

* Make your project directory a current directory: ***cd "G:\Python Learning\GB_lessons>"***;
* Type initialization command: ***git init*** (make sure the directory doesn't already have a Git repository, by checking for hidden <u>```.git```</u> subdirectory).

#### 4.2. Clone an existing repository 

* To make a copy of the existing repository type ***git clone <<u>url</u>>***.

## 5. Recording changes to the repository

To check the current state of the Git repository the ***git status*** command is used. To see the short status information use the ***git status -s*** command, as in the example shown below:
```
PS G:\Python Learning\GB_lessons> git status -s
 M GitInstructions.md
PS G:\Python Learning\GB_lessons>
```

If there are any untracked files in the repository then the ***git add <<u>file name</u>>*** command should be used to start tracking that file. To track all the files in the current directory the ***git add .*** command (_with the dot at the end_) can be used.

If any file has been modified after the last committed changes then to accept new modifications type ***git commit***. This command will open a new file in the editor for your comments related to the current changes. To commit the changes without opening the editor type ***git commit -m "<u>your_comments_on_the_current_changes</u>"***. Adding ***-a*** option will let you skip explicit staging of the file with ***git add*** command.

---
---
> An important note about ***git commit*** and ***git add*** commands:

- Any created or modified files have to be staged by ***git add*** command before the execution of the ***git commit*** command.
---
---

To view the details of changes made before committing them use ***git diff*** command

## 6. Browsing the History of Commits

To show the list of the commits made previously run ***git log*** command. In order to limit the number of committed entities use ***-n*** option, where ***n*** - is the number of last commits to show. Another helpful option is ***-p***, which shows the difference in each displayed commit.

## 7. Transition from one commit to another

To change the current state from one commit to another use the command ***git checkout <<u>commit_hash</u>>***. A git _<<u>commit_hash</u>>_ is a SHA1 hash of the state of the git repository at the time of the commit. This hash code is shown in the output of the ***git log*** command.

## 8. Ignoring the intentionally untracked files

A ***".gitignore"*** file specifies intentionally untracked files which Git will ignore.
Each line in the ***".gitignore"*** file is a file name or a pattern that determines the path and name of files that should be ignored by Git.
The ***".gitignore"*** is affecting the content of the current directory and subdirectories. If the subdirectory has its own ***".gitignore"*** file then this local file will have priority.
The ***".gitignore"*** does not affect files that are already tracked by Git.

## 9. Git Branching

#### 9.1. Creating a new Branch

``` $ git branch <new_branch_name> ``` - creates a new pointer (branch) with the name <u>new_branch_name</u> to the current commit (which is referred to by the pointer called HEAD)

#### 9.2. Switching Branches

To switch to an existing branch run the ***git checkout <<u>branch_name</u>>*** or the ***git switch <<u>branch_name</u>>*** commands

#### 9.3. Checking Branches

Full information on all the observable branches can be obtained by ***git log --all*** command.

A more convenient view of the branches in the terminal window is provided by the following command:
```
git log --oneline --decorate --graph --all
```
This will print out the history of commits, showing where branch pointers are located.

## 10. Merging Branches

#### 10.1. Basic Merging
The command used for merging two branches is given below:
```
git merge <branch_name>
```
During the execution of this command, the branch with the name <u>branch_name</u> is going to be merged with the current (active) branch. If the current branch is "master" then <u>branch_name</u> will be merged with the "master" branch.

#### 10.2. Fast-forward merging

In case there were no activities in the first "current" branch during the time of creation and modification of the second "merging" branch (up to the moment of the merge) then the second branch is going to be simply joined with the first branch.

#### 10.3 Merging Conflicts

Occasionally, the merging process doesn't go well and smoothly. If the same part of the same file in both branches is changed differently then Git won't be able to decide for you which of them is the right one to leave and which of them should be rid of. At this moment the merge conflict emerges.

Below is the example of the ***git merge*** command with conflict:
```
PS G:\Python Learning\GB_lessons> git merge section-about-ignoring-files   
Auto-merging GitInstructions.md
CONFLICT (content): Merge conflict in GitInstructions.md
Automatic merge failed; fix conflicts and then commit the result.
```
In this case, Git pauses the process and gives the control to developer to solve the situation. Below is the result of ***git status*** command in case of merge conflict:
```
PS G:\Python Learning\GB_lessons> git status
On branch master
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   GitInstructions.md
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Git-Logo-White_small.png
```
An additional option is to use ***git mergetool*** command which gives an appropriate visual merge tool. The default tool for merge conflicts is ***opendiff***

When the merge conflict is resolved by the developer (a programmer) ***git commit*** command should be executed to approve and fix the changes, as shown below:
```
PS G:\Python Learning\GB_lessons> git commit -am "Resolving the conflict between master branch and section-about-ignoring-files"
[master 4c02de8] Resolving the conflict between the master branch and section-about-ignoring-files
```

## 11. Removing unnecessary files

After merging branches usually, they become obsolete and should be deleted.

For these purposes, the same ***git branch*** command is used, but with the "-d" option, as shown in the next example:
```
PS G:\Python Learning\GB_lessons> git branch -d section-about-ignoring-files
Deleted branch section-about-ignoring-files (was 7e4011f).
```

The branch we are trying to delete shouldn't be the current (active) branch.

In case if unmerged branch needs to be deleted using "-D" (capital "D") option of ***git branch*** command

## 12. Using the Secure Shell (SSH) protocol
SSH protocol allows to connect and authenticate to GitHub without supplying username and personal access token at each visit. It can also be used for signing commits.

In order to apply ssh protection there are 2 steps:
1. generate a new SSH key on your local machine;
2. add the public key to your account on GitHub.com to enable authentication for Git operations over SSH.

#### 12.1. Generate an SSH key on local user account
- Open a terminal;
- Switch to home directory;
```
cd ~
```
- execute the following command:
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
When you're prompted to "Enter a file in which to save the key", you can press Enter to accept the default file location. At the prompt, type a secure passphrase.

#### 12.2. Adding a new SSH key to your account on GitHub
- Type in terminal:
```
cat ~/.ssh/id_ed25519.pub 
```
- Copy the output to clipboard;
- In the upper-right corner of GitHub account home page, click your profile photo, then click Settings;
- In the "Access" section of the sidebar, click  SSH and GPG keys;
- Click New SSH key or Add SSH key;
- In the "Title" field, add a descriptive label for the new key;
- Select the type of key, either authentication or signing;
- In the "Key" field, paste your public key from clipboard;
- Click Add SSH key.

## 13. installing GitKraken

## 14. Discarding operations made by mistake
- git rebase
- git revolve

## 15. Working with GItHub and execution of ***pull request***


## 16. Additional books and references about 'Git'.


## 17. Some alternative VCSs.