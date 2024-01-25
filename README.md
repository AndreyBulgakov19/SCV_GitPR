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

## Инструкция по работе с гит

**Создание репозитория**:
```sh
git init
```
Статус гита:
``````sh
git status
``````
Добавить файлы к следующему коммиту:
```sh
git add
```
Добавить комментарий к коммиту:
```sh
git commit -m "Message text"
```
Просмотр коммитов
>(журнал изменений)
```sh
git log
```
Сокращенный просмотр изменений:
```sh
git log --oneline
```

Просмотр ветки:
````sh
git branch
``````
Обьединить ветки:
```sh
git merge
```
Создание новой ветки:
````sh
git branch <имя_ветки>
````
Удаление ветки:
````sh
git branch -d <имя_ветки>
```````
Просмотр веток в графе:
``````sh
git log --oneline --graph
``````
Объединение веток:
``````sh
git merge
``````

Очистить терминал:
``````sh
clear
``````
Разница между файлами:
``````sh
git diff
``````
Копирование внешнего репозитория:
``````sh
git clone
``````
Скачать всё из тек. репо:
``````sh
git pull
``````
Отправить свою версию на сервер:
``````sh
git push
``````