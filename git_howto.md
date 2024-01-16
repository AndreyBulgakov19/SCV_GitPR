![Логотип git](logo.png)
# Справка по GIT

## Создание репозитория:
[документация](https://git-scm.com/docs/git-init "init")
```pwsh
git init
```

## Добавление в раздел проиндексированных файлов:
[документация](https://git-scm.com/docs/git-add "add")
```pwsh
git add
```

## Создаёт снимок текущего состояния изменений:
[документация](https://git-scm.com/docs/git-commit "commit")
```pwsh
git commit -m "Message text"
```

## Просмотр истории коммитов:
[документация](https://git-scm.com/docs/git-log "log")
```pwsh
git log
```

### Сокращённая история коммитов:
```pwsh
git log --oneline
```

### История с графическим представлением:
```pwsh
git log --graph
```

### Можно комбинировать оба способа:
```pwsh
git log --oneline --graph
```

## Перемещение по веткам:
[документация](https://git-scm.com/docs/git-checkout "checkout")
```pwsh
git checkout <имя_ветки>
```

## Отображение всех веток:
[документация](https://git-scm.com/docs/git-branch "branch")
```pwsh
git branch
```

### Создание новой ветки:
```pwsh
git branch <имя_ветки>
```

### Удаление ветки:
```pwsh
git branch -d <имя_ветки>
```

## Показывает изменения, отображает различия:
```pwsh
git diff
```

## Слияние одной ветки с другой:
[документация](https://git-scm.com/docs/git-merge "merge")
```pwsh
git merge
```