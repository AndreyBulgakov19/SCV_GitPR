# Репозиторий для **pull request**
* В своём аккаунте на GitHub создать копию репозитория **"AndreyBulgakov19/SCV_GitPR"** с помощью кнопки **"Fork"**.
---
* Клонировать копию репозитория на локальный компьютер.
---
* Создать новую ветку.
---
* Добавить файл с инструкцией в новую ветку.
---
* Дополнить инструкцию разделами по работе с удалёнными репозиториями, pull request.
---
* Зафиксировать изменения (коммиты).
---
* Отправить изменения на GitHub.
---
* На сайте GitHub выполнить **Pull request**.
---
![logo](1color-lightbg@2x.png)
# Work with git
## 1. Check if git is installed
In terminal enter the command: 
```Bash 
  git --version
```
If **git** is installed then git version text will appear, if it's not installed than error massage will appear

## 2. Git instalation
[Download](https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-Git) the latest git version. Install **git** with default settings

## 3. Git setup
For the first time using **git** you have to introduse yourself:
```Bash
  git config --global user.name "<Your_name>" use english latters 
  git config --global user.email "<email_adress@email.com>"
```

## 4. Initialization of the repository
To start working with **git** you have to enter 
```Bash
  git init
```
in **terminal** (it will create **.git** folder in your main folder)

## 5. Writing the change to the repository 
While working, you sould save your progress, for this you have to enter
```Bash
  git add + <folder_name> 
  git commit -m "<changes description>"
```

## 6. View commit history
To view your commits history and **commit codes** you have to enter
```Bash
  git log
```
## 7. Moving between saves
To moving between your saves (*commits*) you have to enter 
```Bash
  git checkout commit_code <---- more functions than just (swich)
or
  git switch commit_code <---- only (swich) function
 ```
**commit code** - watch 6th paragraph

## 8. How to ignore file
 To exclude tracking files in the repository, you need to create a **folder** called **.gitignore** in the repository and write there the file names or patterns corresponding to such files. **My example**:

* Create a `.gitignore`  
* ![screen](screen.jpg)

* Unload your picture in repozitory:

* ![screen](screen3.jpg) 

* ![screen](screen2.jpg) <---- In **VS CODE**

## 9 Creating branches in **git**
Default branch name in **git** is - `master`

To create new branch you need to enter a command:

```Bash
  git branch <new branch_name>
```
## 10. Merging branches and resolving conflicts
To merge the **selected branch** with the current one enter the command:
```Bash
  git merge <selected_branch_name>
```
If the same part of the file was changed in **both branches**, then when they are merged, a conflict may arise that requires **user** participation.

 * ![alt](palapa.jpg)

 The solution to the conflict is shown in the **picture above**.
 
 Here are all the possible solutions:
 1. Accept current change (master branch)
 2. Accept incoming change (selected brunch)
 3. Accept both changes (both variants on a screen and you may fix both by your hands)
 4. Compare changes (shows you a screen with difference between two branches watch on (**picture below**))

* ![url-adress](https://learn.microsoft.com/en-us/visualstudio/version-control/media/vs-2022/git-compare-branches.png?view=vs-2022#lightbox)
This solutions from **VS CODE**

## 10. Deleting branches
If you don't need specific **branch** any more than you may delite it by using command:
```Bash
  git branch -d <branch_name_you_wanna_delite>
```
* You can't delite **current** branch! Because you are on this branch 
* You can't delite **merged** branch! Because **unmerged branch** include **commits** that are not reachable from any of your branches.

# ***Work with remote repisitory***

## Create an account on GitHub 
To create an account on **GitHub** go [link](https://github.com/) and register. 

## Create a lockal repository
1. Create a directory to contain the project.
2. Go into the new directory.
3. Type
 ```Bash
    git init
 ``` 
 
4. Write some **code**.
5. Type 
```Bash
   git add
``` 
to add the files (see the typical use page).
6. Type
 ```bash
    git commit
 ```
  with comment of changes.
  * ![screen](screen1.jpg)
  * ![screen](screen2.png)
  

## Create a remote repository
* Go to **GitHub** and click on "+" than "create a new rep."
* Than name you rep. 
* Click on "Create repository"
* ![screen](smt1.jpg)
* ![screen](smt2.jpg)
* ![screen](smt3.jpg)
## LInk a lockal repository and remote
With the help of the URL, we will link the repository. To link a repository, execute the following command.

* ![screen](smt4.png)

The URL adres you may find on a pictire above.
To check whether we linked our repository or not, execute the
 ```BASH
 git remote
 ``` 
 command. You have to see this:
* ![screen](https://www.toolsqa.com/gallery/Git/6.Local%20Repository%20Remote%20repository%20-%20Git%20Remote%20command%20to%20check%20if%20repository%20is%20connected%20with%20Origin.png)

Use a command to view the same result along with the URL as shown below. 
```bash
git remote -v
``` 

* ![screen](https://www.toolsqa.com/gallery/Git/7.Local%20Repository%20Remote%20repository%20-%20Git%20Remote%20command%20to%20show%20link%20remote%20repository.png)

 Also you may use some commands like 
 ```bash
 git push

 git pull
 ```

**Git push** - is pushing your data from locak repository to remote on **GitHub**

**Git pull** - is pulling your data from remote repository on **GitHub** to local

And one more thing: Don't forget to change a name of your main branch (it has to be **main** instead **master**)