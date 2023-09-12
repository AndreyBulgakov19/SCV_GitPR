# Table of Contents
* [What is Git?](#what-is-git)
* [Repositories and Branches](#repositories-and-branches)
* [Main Commands](#main-commands)
* [Remote Repository](#remote-repository)

## What is Git?
Git is a distributed version control system that tracks changes in any set of computer files. Git was created by Linus Torvalds during the Linux development. Git saves only the difference between files and not the entire files, allowing Git to save a considerable amount of memory.

## Repositories
To start a new local Git repository, follow the instructions below:
1. Create a directory to contain the project.
2. Go into the new directory.
3. Open the console.
4. Type `git init` and execute the command (this will also create the _master_ branch).

### Creating a Repository by Cloning
You can create a new local repository by cloning an already existing one from the remote server.
Please note that Git supports several URL syntaxes. For more information, visit the official Git manual on [Git Clone](https://git-scm.com/docs/git-clone).

To copy a repository from a remote server:
1. Run the console.
2. Use `git clone {URL}` and then execute the command.

> **N.B.!** Don't forget to use the `cd` command to change the directory of the repository folder.

## Branches
Use the `git branch` command with the branch name to create a new branch in your project.
Alternatively, use the `git checkout` command with the `-b` option and specify the branch name as well as the commit to create your branch from.
To switch between branches, use the `git checkout` command with the branch name.

### Common Options with Branch
- `git branch`: List all of the branches in your repository. This is synonymous with `git branch --list`.
- `git branch <name>`: Create a new branch called `<name>`. This does not check out the new branch.
- `git branch -d <branch>`: Delete the specified branch. This is a “safe” option to delete a branch with unmerged content.
- `git checkout <name>`: Switches to the branch with the name that follows `checkout`.
- `git merge <name>`: This command will merge the current branch into the master branch.

**N.B.!** If the two branches you're trying to merge both changed the same part of the same file, Git won't be able to figure out which version to use. When such a situation occurs, it stops right before the merge commit so that you can resolve the conflicts manually.

## Main Commands
- `git init`: Create an empty Git repository or reinitialize an existing one.
- `git add`: This command updates the index using the current content found in the working tree, to prepare the content staged for the next commit.
- `git commit`: Create a new commit containing the current contents of the index and the given log message describing the changes.
- `git commit -m <comment>`: Use `-m` to add a message or comment to commit for better understanding of the log.
- `git diff`: Show changes between commits, commit, and working tree.
- `git log`: Show commit logs. For better visualization, use the command `git log --graph`.
- `git checkout`: Switch branches.
- `git status`: Show the working tree status.
- `git cherry-pick`: Apply the changes introduced by some existing commits.
- `git reset`: Reset the master branch to the specified state.
- `git revert`: Revert some existing commits.
- `git rm`: Remove files from the working tree and from the index.
- `git pull`: Fetch from and integrate with another repository or a local branch.
- `git push`: Update remote refs along with associated objects.

# Remote Repository
In this section, we will explore the Git's possibility to work with remote repositories on platform Github 

## GitHub
To create a remote repository using GitHub, follow the instructions below:
1. Create a GitHub account or sign in.
2. Create a local repository.
3. Synchronize your local repository with the remote one. GitHub has its own detailed instructions.
![Monosnap Screenshot](https://monosnap.com/image/4oK79Og7dTGyzcca8DhVXP3XvkkxG8)
4. Use the `pull` command to add your local repository to your GitHub repository (for the first time, you will need to authorize your account).
5. After this, you can `push` your changes into the remote repository and `pull` changes from the remote repository to the local one.

## Pull Request
If you're working with someone else's project on GitHub, you won't be able to push your changes directly (unless you have been given permission by the project owner). Instead, you will need to create a pull request. You can create your pull request by following the instructions below:
1. Make a repository fork.
2. Clone your repository version.
3. Create a new branch and make your edits.
4. Commit changes.
5. Push the local repository to your GitHub repo.
6. On GitHub, click the "Pull Request" button.