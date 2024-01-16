# Инструкция по работе с GIT
## Инициализация репозитория
```sh
git init
```
## Текущее состояние
```sh
git status
```
## Добавляем изменения
```sh
git add <filename>
```
## Фиксируем изменения
```sh
git commit -m 'message'
```
## Удаляем незафиксированные изменения
```sh
git restore <filename>
```
## Лог действий
```sh
git log
```
## Лог действий в облегченном формате
```sh
git log --oneline
```
## Лог действий в облегченном формате
```sh
git log --oneline --graph
```
## Переключение на определенный коммит
```sh
git checkout <hash>
```
## Перемещение по веткам
```sh
git checkout <branch>
```
## Возврат к актуальному состоянию
```sh
git checkout master
```
## Сравнение изменений
```sh
git diff e9bed3b 6190e53
```
## Показать ветки
```sh
git branch
```
## Создать ветку
```sh
git branch <branch_name>
```
## Слить ветку
```sh
git merge <branch_name>
```