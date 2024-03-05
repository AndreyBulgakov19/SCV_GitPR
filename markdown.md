## Инструкция по работе с Git


## Авторизация в Git. Только при первом подключении:

git config --global user.name "user_name"
git config --global user.email "user_email"


## Создание репозитория:

git init


## Добавление  файла:

git add <имя файла>


## Создание коммита:
git commit -m "Message"


## Просмотр изменений:
git log


## Переключение между коммитами:

git checkout ***первые 4 символа коммита***



## Работа с ветвлением:

### Просмотр списка ветвлений:

git branch


### Создание нового ветвления:

git branch "branch_name"


### Переключение между ветвлениями:

git checkout branch_name



### Удаление ветвления:

git merge branch_name


### Дерево коммитов с ветвлением:

git log --graph


-------------------------------------