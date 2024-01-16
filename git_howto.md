![Логотип git](https://git-scm.com/images/logos/downloads/Git-Logo-1788C.png)
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

## Создание локальной копии удаленного репозитория:
[документация](https://git-scm.com/docs/git-clone "clone")
```pwsh
git clone <url-адрес репозитория>
```

## Выкачать все изменения из удаленного репозитория в локальный:
[документация](https://git-scm.com/docs/git-pull "pull")
```pwsh
git pull
```

## Отправить изменения в удаленный репозиторий из локального:
[документация](https://git-scm.com/docs/git-push "push")
```pwsh
git push
```

## Отправить в удалённый репозиторий новую ветку:
```pwsh
git push --set-upstream origin <имя_ветки>
```

![GitHub](https://github.githubassets.com/assets/GitHub-Mark-ea2971cee799.png)
## Команды на Github

### Создать в своём аккаунте новый репозиторий копированием чужого:
[документация](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo "fork")
```pwsh
fork
```

### Создать запрос на включение сделанных изменений:
[документация](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request "pull request")
```pwsh
pull request
```