# Инструкция по работе с контролем версий в git

## Урок 1
### Начало работы

Для того, чтобы git начал контролировать изменения в ваших файлах, необходимо перейти в папку с проектом и инициализировать git с помощью команды `git init`

### Подготовка репозитория

Для дальнейшей идентификации комитов и связи лучше указать имя и email, это можно сделать командами:
`git config --global user.name "<Name>"`
`git config --global user.email "<email>"`

### Сохранение версии файла

После того, как вы внесли правки в ваш файл, необходимо сохранить изменения в контрое версий. Для этого нужно ввести две команды:

```
git add <filename>
git commit -m "some informative massage for the commit"
```
После этого все изменения в файле будут сохранены в git

> Не забудьте перед добавлением файла в комит предварительно сохранить внесенные изменения (ctrl + s)

### Команды-помощники

* Чтобы узнать версию программы git, введите команду
`git --version`

* Для просмотра всех изменений введите команду:
`git log`

* Для перехода в более раннюю версию файла введите команду
`git checkout <version>` , где `<version>` это первые 4 символа идентификатора коммита. Посмотреть индентификатор можно через предыдущую команду.

* Для возвращения в последнюю версию файла необходимо ввести команду:
`git checkout <branch>` , где `branch` это название ветки, в которой происходит работа.

* Чтобы узнать текущее состояние: новые файлы, файлы с изменениями и пр, необходимо ввести команду:
`git status`

* Чтобы посмотреть разницу между текущей версией файла и последним слепком данного файа в репозитории необходимо ввести команду:
`git diff`

* Для выхода из информационного окна нажмите `q`

### Пример работы в git

`user@ Git_HW_01 % git init`
>hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint:   git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint:   git branch -m <name>
Initialized empty Git repository in /Users/user/Documents/2024/geekbrains/Git_HW_01/.git/

`user@ Git_HW_01 % git status`

>On branch master
No commits yet
Untracked files:
(use "git add <file>..." to include in what will be committed)
git_insrtuction.md
nothing added to commit but untracked files present (use "git add" to track)

`user@ Git_HW_01 % git add git_insrtuction.md`
`user@ Git_HW_01 % git commit -m"First step in git"`

>[master (root-commit) a47b361] First step in git
Committer: Оксана Токарева <user@.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:
git config --global --edit
After doing this, you may fix the identity used for this commit with:
git commit --amend --reset-author
1 file changed, 38 insertions(+)
create mode 100644 git_insrtuction.md

`user@ Git_HW_01 % git status`

>On branch master
nothing to commit, working tree clean

`user@ Git_HW_01 % git log`

>commit a47b36145e0cf7067001246024802340fb6df70d (HEAD -> master)
Author: Оксана Токарева <user@.local>
Date:   Wed Jan 31 23:16:25 2024 +0300
First step in git

`git status` - команда, отображающая блок информации по состоянию репозитория
`git log --graph` - данная команда визуально отображает все текущие ветки в git и сделанные комиты.

## Урок 2

Работа с ветками в git: ветки позволяют вести единовременную работу над одним файлом, отслеживать и сливать изменения.

>При слиянии веток иногда бывают конфликты.

`git branch` - посмотреть все существующие ветки репозитория и ветку, в которой в данный момент ведется работа.
`git branch <branch name>` - создание новой ветки, без моментального перехода на нее.
`git checkout -b <branch name>` - создание новой ветки с моментальным переходом на новую ветку.
`git checkout <branch name>` - переключится на другую ветку репозитория.
`git branch -d <branch name>` - удаление ветки.
`git merge <branch name>` - слить две ветки, нужно производить из ветки, в которую происходит слияние.
Для решения конфликта, возникшего при слиянии веток, необходимо выбрать подходящий вариант, отредактировать файл. Редактор VisualStudio подсвечивает конфликты и предлагает несколько вариантов для редактирования: 
* принять первый вариант, 
* принять второй вариант, 
* принять оба варианта, 
* сравнить два варианта.
После редактирования конфликта в файле, нужно сделать повторный коммит измененного файла: `git add + git commit`.

## Урок 3
### Работа с удаленными репозиториями

Чтобы скопировать данные репозитория на локальный компьютер, необходимо использовать команду `git clone <link to reository>`

Чтобы стянуть все обновления, сделанные другими пользователями, нужно использовать команду `git pull`

Для создания коммита в удаленный репозиторий, нужно использовать следующие 3 команды:
```
git add <filename>
git commit -m"comment"
git push
```
