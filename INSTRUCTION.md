# Работа с GIT
## 1. Проверка наличия установленного GIT
В терминале выполнить команду `git --version` Если Git установлен, появится сообщение о версии программы, иначе будет сообщение об ошибке.

## 2. Установка Git
Загружаем последнюю версию Git c сайта https://git-scm.com/downloads Устанавливаем с настройками по умолчанию.

## 3. Настройка GIT
При первом использовании GIT необходимо представиться. Для этого нужно ввестив терминале 2 команды:
```
Bash
git config --global user.name "Ваше имя английскими буквами"
git config --global user.email "Ваша почта"
```
## 4. Инициализация репозитория.
Для работы с файлами необходимо создать папку и файл и  выбрать ее в VS.
Инициализация локального репозитория производится командой ``git init``

 ## 5. Сохранение файла и просмотр состояния GIT
 Сохранение файла производится комбинацией клавиш ctrl+S.
 После сохранения команда ``git status``
 покажет, что файл модифицирован.

 Пример просмотра статуса 
 
 ```
  $ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)   
  (use "git restore <file>..." to discard changes in working directory)
        modified:   insruction.md
 ```
 ``git status`` - показывает текущее состояние файов в репозитории, с помощью команды можно посмотреть готов ли файл для добавления коммита.

## 6. Создание коммитов
1. Необходимо после фиксации состояния ``ctrl+S`` добавить состояния для сохранения коммита
2. Командой `git add "Имя файла"` - добавление файла для коммита
3. команда ``git commit -m`` производится добавление коммита и создается хеш код для последующего возможного восстановления.
4. Командой ``git commit -am`` возможно одновременно добавить файл к коммиту и произвести коммит одновременно.

Пример успешного добавления коммита 
```
$ git commit -a -m "Создание коммитов"
[master 700b3ad] Создание коммитов
 1 file changed, 7 insertions(+)
```

## 7. Просмотр версий коммитов
Командой `git log` можно просматривать зафиксированные коммиты.
Командой `git checkout` 
происходит переход между сохраненными версиями
`git checkout master` - загрузка самой последней версии в дереве master

Примет просмотра хеша с коммитами
```
$ git log
commit 700b3ad795c0f48f6031970a7f86a51e55b223e7 (HEAD -> master)
Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
Date:   Wed Sep 6 22:55:55 2023 +0300

    Создание коммитов

commit d9dc57cb538909cbb80866941ce18f9c8dcd092a
Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
Date:   Wed Sep 6 22:49:56 2023 +0300

    Добавление информации об инициализации и сохранении        

commit f05e571883a495f65c1eb88098a8020b865b856b
Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
Date:   Wed Sep 6 19:28:33 2023 +0300
```
`git switch` - переход между версиями коммитов

## 8. Просмотр изменений 
``git diff`` - команда,  которая показывает разницу между текущем состоянием и сохраненным коммитом

```
$ git diff
diff --git a/insruction.md b/insruction.md
index e6ecf6d..ad44409 100644
--- a/insruction.md
+++ b/insruction.md
@@ -73,3 +73,5 @@ Date:   Wed Sep 6 19:28:33 2023 +0300        
 ```
 `git switch` - переход между версиями коммитов

+## 8. Просмотр изменений 
+``git diff`` - команда,  которая показывает разницу между     
\ No newline at end of file


## 9. Игнорирование файлов

Для того, чтобы исключить из отслеживания в репозитории определенные файлы или папки необходимо создать там файл ***.gitignore*** и записать в него их названия или шаблоны, соответствующие таким файлам или папкам.

## 10. Создание веток в Git
По умолчанию имя основной ветки в Git -
`master`.
Создать ветку можно командой:
```Bash
git branch <Имя новой ветки >
```
Список веток в репозитории можно посмотреть с помощью команды `git branch`

Пример:
```Bash
$ git branch 
* master
  test
  test2
  test3
  test4
```

`git checkout` "Имя ветки"- команда выбора нужной ветки
`git switch` "Имя ветки"- команда для перехода между созданными ветками


## 11. Слияние веток и разрешение конфликтов

Для слияния выбранной ветки с текущей нужно выполнить команду 
```Bash

git merge <Название выбранной ветки >
```
Если была изменена одна и таже часть файла в обеих ветках,   может возникнуть конфликт
Конфликт может быть разрешен посредством терминала или графического интерфейса.

Пример:
```Bash
<<<<<<< HEAD

<<<<<<< HEAD


Возможно что-то добавилось
=======
Пример:
Bash
=======
>>>>>>> test2

<<<<<<< HEAD
=======
```
Пример:
```Bash

>>>>>>> test3
## 12. Тест

Исправленный текст

<<<<<<< HEAD
=======
<<<<<<< HEAD
3. тест тест
=======
>>>>>>> test2
```
После разрешения конфликта необходимо зафиксировать состояние коммитом.


## 12. Удаление веток
Для удаления веток можно спользовать как полную так и сокращенную команду `delete`
Варианты написания: git branch ``--delete``, ``-d``, ``-D``
При написании заклавных букв команда git branch ``-D``, команда будет исполнятся принудительно
Пример:
```Bash
$ git branch --delete resolveConfkikts
Deleted branch resolveConfkikts (was 9fa91a5).

```

## 13. Визуализация лог коммитов

`git log --graph` - отображение дерева веток, где будут отображаться как создание новых веток, так и их слияние 

Пример:

```Bash
$ git log --graph
*   commit f86a16fb4a808941ece1b4778a1eccfb481a22de (HEAD -> master)
|\  Merge: 215c3ca 9f01de9
| | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | Date:   Fri Sep 8 20:08:52 2023 +0300
| |
| |     Merge branch 'newvetka'
| |
| * commit 9f01de99d541d39226283d170756e6abc98c85ab
| | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | Date:   Fri Sep 8 20:07:39 2023 +0300
| |
| |     Тест
| |
* | commit 215c3ca24a5c54e21b3cb045c7f9c077f8bd661a
|/  Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
|   Date:   Fri Sep 8 20:01:22 2023 +0300

Пример №2


 commit 15aa0fe6f8edf74c21183d620e8f43c06e217fd6
|\  Merge: 9fa91a5 15f1e47
| | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | Date:   Fri Sep 8 16:25:13 2023 +0300
| |
| |     Merge branch 'createBranches'
| |
| * commit 15f1e4799ab7df68231b18bd083af224a3153947
| | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | Date:   Fri Sep 8 16:18:40 2023 +0300
| |
| |     Зафиксировали 11 пункт, разрешили противоречия
| |
| * commit 799f5014bba90e49c66a59593469c6aa85a3e8b3
| | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | Date:   Fri Sep 8 00:54:59 2023 +0300
| |
| |     Добавили раздел 10 - Создание веток в GIT и команду git branch
| |
* | commit 9fa91a5f5de308f954cb044a4f7793acaef6d7bb
| | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | Date:   Fri Sep 8 15:35:23 2023 +0300
| |
| |     Добавили  11 пункт о слиянии веток
| |
* | commit 36fdb686400f2c07403819024f8b5dbfc134ebc5
|/  Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
|   Date:   Fri Sep 8 15:22:04 2023 +0300
```


## 14. Раздел по созданию 4 тестовых веток

$ git log --graph
*   commit 8b7be6a310f871c2950b195eb0d5222cce609c2e 
```Bash
(HEAD -> master)
|\  Merge: db6b094 41d6cb4
| | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | Date:   Fri Sep 8 21:45:36 2023 +0300
| |
| |     Добавление теста для master
| |
| *   commit 41d6cb4fe12a340d0c368f4ba57793d421d22609 (test)
| |\  Merge: bf510ed 3ecf171
| | | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | | Date:   Fri Sep 8 21:44:23 2023 +0300
| | |
| | |     Добавление тест
| | |
| | *   commit 3ecf17196dcc852c44c93c4397b4cd8a3e42caa0 (test2)
| | |\  Merge: 89429af d9ff127
| | | | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | | | Date:   Fri Sep 8 21:43:12 2023 +0300
| | | |
| | | |     Добавление тест2
| | | |
| | | *   commit d9ff1275d2643ab8c1a0076b3953195f07dde344 (test3)
| | | |\  Merge: dbe3228 8ff85f3
| | | | | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | | | | Date:   Fri Sep 8 21:41:43 2023 +0300
| | | | |
| | | | |     Добавление тест3
| | | | |
| | | | * commit 8ff85f32809d5c9f35ff504ec98cd863eab060f2 (test4)
| | | | | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | | | | Date:   Fri Sep 8 21:36:09 2023 +0300
| | | | |
| | | | |     Добавление тест4
| | | | |
| | | * | commit dbe3228ba57444aa6939935c722ef4474de4493e
| | | |/  Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | | |   Date:   Fri Sep 8 21:37:07 2023 +0300
| | | |
| | | |       Добавление тест3
| | | |
| | * | commit 89429af6b470bfabe066fdf4c0c002a385d6805a
| | | | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | | | Date:   Fri Sep 8 21:38:39 2023 +0300
| | | |
| | | |     Добавление тест2
| | | |
| * | | commit bf510ed75f2238482df79e89032a6714b420ad82
| | | | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | | | Date:   Fri Sep 8 21:39:50 2023 +0300
| | | |
| | | |     Добавление тест
| | | |
| * | | commit 6c91b9bc43038d39156bd3fa0280fa99c3200c56
| |\| | Merge: 72efe2e bc25269
| | | | Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | | | Date:   Fri Sep 8 21:28:11 2023 +0300
| | | |
| | | |     Merge branch 'test2' into test
| | | |
| | * | commit bc25269769be01205a8d162a54efa89f6cf2c7b0
| | |/  Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| | |   Date:   Fri Sep 8 21:23:09 2023 +0300
| | |
| | |       Запись о тесте2
| | |
| * | commit 72efe2e3b515dab5d79b959fad352ca0a935d4d5
| |/  Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
| |   Date:   Fri Sep 8 21:19:47 2023 +0300
| |
| |       Запись о тесте
| |
* | commit db6b094189cfd39299c1303b107636ecf40327eb
|/  Author: Dmitriy Fomin <dmitriytulskiy@gmail.com>
|   Date:   Fri Sep 8 21:12:11 2023 +0300
|
|       Добавлены разделы 12, 13 - удаление веток и визуализации логов
```

## 15. Работа с удаленными репозиториями


### 15.1 Создать аккаунт на GitHub


Необходимо зайти на https://github.com, выбрать имя, которое еще не занято, ввести e-mail и пароль.
Затем нажмите большую зелёную кнопку «Sign up for GitHub»

### 15.2 Создать локальный репозиторий

Создаем локальный репозиторий для работы с внешим и инициализируем его.

### 15.3 Создать удаленный репозиторий

1. Для создания удаленного репозитория необходимо нажать "+" на стартовой странице аккаунта.
2. Задаем название для репозитория.
3. Описание репозитория
4. Выбираем публичный или приватный
5. Можно сразу добавить файл Readme.md
6. Нажимаем создать репозиторий


### 15.4 Работа с удаленным репозиторием, совмещение с локальным репозиторием

1. Устанавливаем связь с удаленным репозиторием командой 
`git remote add origin https://github.com/FominDmitriy71/Remote.git

2. Проверяем доступ к удаленному репозиторию командой `git remote -v`
 Пример 
 ```Bash
 $ git remote -v
origin  https://github.com/FominDmitriy71/Remote.git (fetch)
origin  https://github.com/FominDmitriy71/Remote.git (push)
 
 ```

 `git clone "url- адрес репозитория"` - клонирование внешнего рипозитория на локальный ПК

3. Переименовываем ветку "master" на "main" командой `git branch -M main` 

4. Отправляем содержимое локального репозитория в удаленный репозиторий
командой `git push -u origin main`
 
 Пример:
 ```Bash
 $ git push -u origin main
Enumerating objects: 145, done.
Counting objects: 100% (145/145), done.
Delta compression using up to 2 threads
Compressing objects: 100% (138/138), done.
Writing objects: 100% (145/145), 18.48 KiB | 305.00 KiB/s, done.
Total 145 (delta 81), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (81/81), done.
To https://github.com/FominDmitriy71/git_dimon.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
 
 ```


5. `git pull` - получение изменений и слияние с локальной версией

Пример:

```Bash
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 744 bytes | 10.00 KiB/s, done.
From https://github.com/FominDmitriy71/git_dimon
   3bb6d17..15e3725  main       -> origin/main
Updating 3bb6d17..15e3725
Fast-forward
 insruction.md | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

```
### 15.5 Разрешение конфликтов

При зафиксированном состоянии на GITHUB, и одновременно при фиксации на локальном репозитории различный данных на одинаковых строках возникает конфликт.
Конфликт может быть создан командой `git pull`  при подгрузке данных с GITHUB.

Пример:
```Bash

<<<<<<< HEAD


1. Получение конфликта 
=======

1. Тестирование конфликта с изменением
>>>>>>> 2d83b99efee099fc08aaaa0e2bd2242d7db13b9f

```

Принимаем вариант изменения и фиксируем изменение командой commit

При команде `git push` может произойти ошибка, если не обновлен локальный репозиторий.
При актуальном локальном репозитории можем отправить актуальные изменения из локального репозитория на GITHUB

Пример: 
```Bash
$ git push
Enumerating objects: 20, done.
Counting objects: 100% (19/19), done.
Delta compression using up to 2 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 2.23 KiB | 762.00 KiB/s, done.
Total 14 (delta 11), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (11/11), completed with 3 local objects.
To https://github.com/FominDmitriy71/git_dimon.git
   2d83b99..9d66d36  main -> main

```

### 15.6 Работа над проектом с открытым кодом


Копируем необходимый проект с помощью команды `git clone <URL>`

Пример:
```Bash
$ git clone https://github.com/TelegramBots/Telegram.Bot.git Bot
Cloning into 'Bot'...
remote: Enumerating objects: 27091, done.
remote: Counting objects:  93% (885/951)Receiving objects:   0% (1/27remote: Counting objects:  94% (894/951)Receiving objects:   2% (542/remote: Counting objects: 100% (951/951), done.
remote: Compressing objects: 100% (372/372), done.
remote: Total 27091 (delta 607), reused 858 (delta 577), pack-reused Receiving objects: 100% (27091/27091), 30.75 MiB | 887.00 KiB/s, done.

Resolving deltas: 100% (20632/20632), done.
Updating files: 100% (513/513), done.
```
### 15.7 Работа с копированием чужого репозитория


Копирование репозитория для работы в локальной версии необходимо воспользоваться функцией "Fork"

Посмотреть список удаленных репозиториев команда - git remote -v`
Переход на ветку и одновременно ее создать - `git switch -c "name"`
Командой `git push -u origin new` - отправляем информацию в 
удаленный репозиторий, информация отправляется в новой ветке и записываться к основному проекту тоже будет отдельной веткой.
Выполнить Pull request  на основной проект.