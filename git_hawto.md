# Подсказка по Git

Создание репозитория
```sh
git init
```

Получить информацию от git о его текущем состоянии
```sh
git status
```

Добавить файл(ы) к следующему коммиту, сохранить изменения
```sh 
git add <имя файла с расширением>
```

Создание коммита
```sh
git commit --m "Massage text"
```

Вывод на экран истории всех коммитов с их хеш-кодами
```sh
git log
```

Вывод на экран истории всех коммитов с их сокращёнными хеш-кодами одной строкой
```sh
git log --oneline
```

Перемещение по веткам
```sh
git checkout <имя_ветки>
```

Увидеть разницу между текущим файлом и закоммиченным файлом
```sh
git diff
```

Отображение названий всех веток
```sh
git branch
```

Создать новую ветку
```sh
git branch <имя_ветки>
```

Удалить ветку
```sh
git branch -d <имя_ветки>
```

Слияние веток (нужно выполнять находясь в папке  **main**) 
```sh
git merge <имя_ветки_откуда_переливаем>
```

Отображение всех коммитов и всех веток
```sh
git log --graph
```

Отображение всех веток и всех коммитов c их сокращёнными хеш-кодами, одной строкой
```sh
git log  --oneline --graph
```

Внесение изменений в текст последнего коммита
```sh
git commit --amend -m "New massage text"
```

Клонирование внешнего репозитория на
локальный ПК
```sh
git clone <url-адрес репозитория>
```

Получение изменений и слияние с локальной версией
```sh
git pull
```

Отправляет локальную версию репозитория на внешний репозиторий
```sh
git push
```

# Инструкция pull request

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
