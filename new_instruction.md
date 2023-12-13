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

Это репозиторий для обучения pull request
Первые шаги

    Делаем fork репозитория, в которой потом хотим сделать pull request. Ищем кнопку Fork на странице репозитория https://git@github.com:gulden-geekbrains/version_control.git
    Выполняем команду клонирования из своей fork-копии

git clone git@github.com:*YOURE_GITHUB*/version_control.git

    Создаем новую ветку и вносим необходимые изменения в файл

git checkout -b updatereadme
vim README.md
git add README.md
git commit -m "Добавили инструкцию как создать pull request"

    Делаем push

git push --set-upstream origin updatereadme

    Переходим на свою страницу репозитория. Выбираем ветку updatereadme и жмем кнопку Compare & pull request

Заметки

Что бы сделать push от другого пользователя необходимо выполнить команду

GIT_SSH_COMMAND='ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes' git push git@github.com:gulden-geekbrains/version_control.git

вместо user-private-key подставьте свой ключ

Можно прописать настройки для подсоединения по ssh

git config remote.origin.url git@github.com:gitusername/reponame
git config core.sshCommand "ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes"
