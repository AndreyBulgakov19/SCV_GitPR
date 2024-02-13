# Репозиторий для **pull request**
* В своём аккаунте на GitHub создать копию репозитория **"AndreyBulgakov19/SCV_GitPR"** с помощью кнопки **"Fork"**.
---
* Клонировать копию репозитория на локальный компьютер.
---
* Создать новую ветку.
---
* Добавить файл с инструкцией в новую ветку.

# Подсказки по командной сроке

## Команда смены директории
```sh
cd c:\folder_name
```

## Листинг текущей директории
Windows:
```sh
dir
```
## Инициализация папки
```sh
git init
```
## Добавить к индексации
```sh
git add <имя файла с разрешением>
```
## Зафиксировать изменения
```sh
git commit -m " Message"
```
## Посмотреть в полном виде
```sh
git log
```

## Удаление файла в Windows:
```sh
del <filename> 
```


## Перейти на шаг назад в другую папку
```
sh
cd ..
```

## Создать новую папку такое же название как и в github
```
sh
mkdir [name file]
```

## Выдает информацию о файле (оригинальный )
```sh
git remote show
```
##  Выдает подробную информацию о файле
```sh
git remote show -v
```

 ## Команды для работы работы с удаленными репозиториями
Создаем новый репозиторий на github
Копируем ссылку 
переходим в VS cod

## Команда для клонирования 
``` sh
git clone "ссылка"
```

## Создаем новый файл
``` sh
echo "# trening1" >> README.md
```
 ## Создаем репозиторий
``` sh
git init
```
## Индексируем
``` sh
git add README.md
```
## Создаем комит
``` sh
git commit -m "first commit"
```
## Переименуем ветку мастер в маин
``` sh
git branch -M main
```
## Перенесем изменения в Github
``` sh
git remote add origin https://github.com/TatyanaS-GB/trening1.git
```
## Cлияние
``` sh
git push -u origin main
```
## Показывает все ветки
 git branch –all
##  Посмотреть подробную историю
``` sh
git log --all --graph –oneline

---
* Дополнить инструкцию разделами по работе с удалёнными репозиториями, pull request.

## Это репозиторий для обучения pull request

## Первые шаги

1. Делаем fork репозитория, в которой потом хотим сделать pull request. Ищем кнопку Fork на странице репозитория <https://git@github.com:gulden-geekbrains/version_control.git>
2. Выполняем команду клонирования из своей fork-копии
```sh
git clone git@github.com:*YOURE_GITHUB*/version_control.git
```
3. Создаем новую ветку и вносим необходимые изменения в файл
```sh
git checkout -b updatereadme
vim README.md
git add README.md
git commit -m "Добавили инструкцию как создать pull request"
```
4. Делаем push  
```sh
git push --set-upstream origin updatereadme
```
5. Переходим на свою страницу репозитория. Выбираем ветку **updatereadme** и жмем кнопку **Compare & pull request**

## Заметки

Что бы сделать push от другого пользователя необходимо выполнить команду
```sh
GIT_SSH_COMMAND='ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes' git push git@github.com:gulden-geekbrains/version_control.git
```

вместо *user-private-key* подставьте свой ключ

Можно прописать настройки для подсоединения по ssh
```sh
git config remote.origin.url git@github.com:gitusername/reponame
git config core.sshCommand "ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes"
```
# Как подружить git с github под Windows 10

Вот видео инструкция https://youtu.be/E8cIjbJMEpE


---
* Зафиксировать изменения (коммиты).
---
* Отправить изменения на GitHub.
---
* На сайте GitHub выполнить **Pull request**.
---
