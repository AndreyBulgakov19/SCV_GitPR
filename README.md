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


![Logo](Images\git_logo.png)

# Работа с Git

## 1. Проверка наличия установленного Git
### В терминале выполнить команду 
```bash
git version
```

## 2. Установка Git

### Загружаем последнюю версию программы с [сайта](https://git-scm.com/download/win)
### Устанавливаем с настройками по умолчанию.

## 3. Настройка Git
### первоначальные настройки задаются командами
```bash
git config --global user.name Имя пользователя
```

```bash
git config --global user.email указавается почта польователя
```

```bash
git add <имя файла> - команда добавления файлов в репозиторий
```

## 4. Инициализация репозитория
### Инициализация репозитория выполняется командой
```bash
git init
```

## 5. Запись изменений в репозитории
### добавление файлов в индекс перед фиксацией выполняется командой
```bash
git add .
```
### фиксация изменений в репозитории выполняются командой
```bash
git commit -m "Message"
```
### также можно использовать команду git commit с параметром "-a" без предварительного использования команды "git add"
```bash
git commit -am "Message"
```

## 6. Просмотр истории коммитов
### просмотр истории коммитов выполняется командой
```bash
git log
```

## 7. Перемещение между сохранениями (коммитами)
### просмотр истории коммитов выполнается командой перехода между коммитами
```bash
git checkout <commit hash>
```
название (имя) нужного коммита _**commit hash**_ берется из истории коммитов, которые можно посмотреть командой 
```bash
git log
```

## 8. Игнорирование файлов

### чтобы исключить из отслеживания определенные файлы, необходимо создать файл **.ignorefiles** и имена необходимых файлов и/или папок или маски файлов (типы файлов)

## 9. Создание веток в Git

### по дефолту имя основной ветки - _**master**_

### создание новой ветки выполняется командой 

```bash
git branch <имя новой ветки>
```

### переход в созданную ветку выполняется командой

```bash
git chectout <имя созданной ветки>
```

### также для переход между ветками можно осуществлять командой

```bash
git switch <имя ветки, в которую нужно перейти>
```

### также есть команда создания новой ветки с автоматическим переходом в нее


```bash
git checkout -b branch <имя новой ветки>
```

### просмотр списка веток в репозитории выполняется командой

```bash
git branch
```

### удаление веток осуществляется командой

```bash
git branch -d <имя_ветки>
```
При удалении веток могут быть ситуации:

1. Удалить ветку невозможно, находясь в этой ветке. Нужно перейти в лругую, но лучше в основную, она может называться _**main**_ или _**master**_. Почему? Ответ во второй ситуации
2. При удалении ветки Git обязательно подскажет, что из удалемой ветки информация не была перенесена в основную и соответственно будет потеряна. Тогда делаем слияние веток и именно без лишних движений. В основную ветку сливаем информацию из удаляемой.

Если слив слив информации в любом случае не нужен, то находясь не удаляемой ветки нужно выполнить команду
```bash
git branch -D <имя_ветки>
```

## 10. Работа с удаленным репозиторием

### Создание локального репозитория

В гите создаем новый репозиторий.

### Регистрация на GitHub

 На [сайте](https://github.com/) создаем эккаунт

### Создание удаленного репозитория

На сайте создаем новый репозиторий. Для удобства имя удаленного репозитория указать такое же, как и имя локального репозитория.

### Связка локального репозитория с удаленным

```bash
git remote add origin <https://github.com/SergioBest/SCV_GitPR.git>
```
В данном случае адрес на ГитХабе взят из частного случая для примера.

### отправка локального депозитория в удаленный выполняется командой
```bash
git push -u origin main
```
