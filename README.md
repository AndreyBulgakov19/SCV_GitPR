![Logo Git](GitLogo.png)
# Работа с Git и GitHub
## 1. Проверка наличия установленного Git
В терминале выполнить команду `git --version`
Если Git установлен появится сообщение с информацией о версии программы. Иначе будет сообщение об ошибке.
## 2. Установка  Git
Загружаем последнюю версию Git с [https://git-scm.com/]
Устанавливаем с настройками по умолчанию. 
![What'sGit?](2023-08-26_13-41-18.png)
## 3. Настройка Git
При первом использовании Git необходимо представиться. Для этого надо ввести в терминале 2 команды:

```git config --global user.name "Ваше имя английскими буквами"```\
``` git config --global user.email ваша почта@examp.com```

## 4. Инициализация репозитория
Чтобы инициализировать репозиторий нужно ввести команду\
 `git init название папки/.git/` \
 Это необходимо для того, чтобы Git начал свою работу в этом файле
## 5.  Запись изменений в репозиторий
Для фиксации изменений есть несколько команд. Первая команда это: \
`git commit -m""` \
Однако если мы хотим ей воспользоваться, то перед этим надо добавить файл, чтобы Git его смог отслеживать. Добавляем файл по команде:\
 `git add .\НазваниеПапки`\
  Также сушествует команда git commit -am"". Эта команда совмещает в себе и commit и add, перед ее использованием не нужны дополнительные команды. Также хочу отметить, что в `git commit -m""`, так и `git commit -am""` обязательно нужно оставить комментарий изменений.
## 6.  Просмотр истории коммитов
Чтобы посмотреть историю коммитов, нужно воспользоваться командой\
`git log` \
Там мы узнаем номер каждого комиита и с их помощью мы сможем перемещаться между сохранениями.Тажке для просмотра истории коммитов можно воспользоваться командой\
 `git diff` \
 Помимо номеров всех коммитов мы сможем увидеть разницу каждого коммита.
## 7.  Перемещения между сохранениями
Для перемещения используем команду
`git checkout 0000`, где вместо нулей вводим первые четыре цифры/буквы номера нужного нам коммита. Для того, чтобы вернуться к исходной ветке, нужно ввести команду `git checkout master` или `git switch`. Таким образом мы вернемся к основной ветке
## 8. Игнорирование файлов
Для того, чтобы исключить из отслеживания в репозитории определенные файлы или папки необходимо создать файл `.gitignore` и записать в него их названия или шаблоны, соответствующие таким файлам и папкам.

## 9. Создание ветки в Git
Чтобы создать ветку нужно ввести команду 

```
git branch <имя для новой ветки>
```
Список веток в репозитории можно посмотреть с помощью команды:
```
git branch
```
Текущая ветка будет отмечена звездочкой
 `*NameBranch`
 
 ## 10. Слияние веток и разрешение конфликтов
 Для слияния выбранной ветки с текущей нужно выполнить команду \
 `git merge <NameBranch> `\
 Если была изменена одна и та же часть файла в обеих ветках, то может возниикнуть конфликт, который потребует участия пользователя. VisualStudioCod предлагает варианты разрешения конфликта:
 1. Accept current changes
 2. Accept incoming changes
 3. Accept both changes
 4. Compare changes

 Необходимо выбрать нужный вариант.  После разрешения конфликта нужно обязательно создать коммит слияния 

 ## 11. Удаление ветки
 Важно удалять ветки, после того как закончили в них работу и слили с основной веткой. 
Это необходимо для того, чтобы не путаться и не перегружать систему. Для удаления нможно воспользоваться командой: \
 `git branch -d NameBranch`\
 Если же нужно удалить ветку без слияния с основной ветвью, можно воспользоваться командой принудительного удаления\
 `git branch -D NameBranch`\
 **Важно!**\
  При удалении ненужной ветки в самой ветки git выдает ошибку. Нужно переключиться с ветки, которую хотим удалить на другую и после этого ввести команду удаления ветки.

  ## 12. Немного о работе с GitHub
  ![What is GitHub](2023-08-27_21-11-56.png)
  Для работы с GitHub необходимо для начала зарегестрироваться на официальном их сайте [https://github.com/].
Далее создаем локальный репозиторий, 
1. Создать аккаунт на GitHub на официальном их сайте [https://github.com/]
2. Создать локальный репозиторий
3. Создать удаленный репозиторий
4. Связать удаленный репозиторий с локальным
Для того,чтобы свзязать удаленный репозиторий с проектом, необходимо ввести следующие команды:

```
git remote add <namefor repository> <url-adress repository in internet>
```
При первом использовании GitHub понадобиться подтверждение того, что вы действительно можете вносить изменения в данный проект. После определенных команд высветиться окно, где надо будет связать git c аккаунтом на GitHub.

Далее надо переименовать ветку master на имя main  с помощью команды:\

```
git branch -M main
```

Затем надо выполнить последнюю команду для отправления изменений в удаленны репозиторий:
```
git push -u origin main
```
### Репозиторий для **pull request**
* В своём аккаунте на GitHub создать копию репозитория **"NameRepository"** с помощью кнопки **"Fork"**.
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

