# Помощь с GIT

### Создание репозитория
```sh
git init
```

## Проверка текста

Просмотр статуса
```sh
git status
```

log в полном виде
```sh
git log
```

log в кратком виде
```sh
git log --oneline
```

log в кратком виде и с ветками
```sh
git log --oneline --graph
```

Зафиксировать изменения
```sh
git commit -m "message text"
```

Добавить
```sh
git add <имя файла>
```

## Работа с ветками

Создание ветки
```sh
git branch <имя ветки>
```

Отображение всех веток
```sh
git branch
```

Удаление ветки
```sh
git branch -d <имя ветки>
```


Перемещение по веткам
```sh
git checkout <имя ветки>
```