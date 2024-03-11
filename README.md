# Работа с Git
## 1. Проверка наличия установленного Git
В терминале выполнитиь команду 
```
git --version
```
 Если Git установлен появится сообщение с информацией о версии программы, иначе будет сообщение об ошибке.

## 2. Установка Git
Загружаем последнюю версию программы с [сайта](https://git-scm/downloads)
Устанавливаем с настройками по умолчанию.

## 3. Настройка Git
Вводим в терминале следующие команды:
```
git config --global user.name "ваше имя"
git config --global user.email "ваша почта"
```
## 4. Инициализация репозитория
* Создаём папку в любом удобном месте
* Выбиракм её в Visual Studio (кнопка Open Folder)
* Вводим в терминале команду `git init`
* __Готово!__

## 5. Запись изменений в репозиторий
За это отвечают команды `git add <название документа>` + `git commit -m "заметка об изменениях в данном коммите"`.
Либо же, в некоторых случаях, можно совместить это в команде `git commit -am "заметка об изменении" `.

## 6. Просмотр истории коммитов
__Вся подробная информация о каждом коммите(кто вносил изменения в файл, в какой денб недели и в какое время) показывается с помощью команды__
```
1. git log
2. git diff
```
## 7. Перемещение между сохранениями(коммитами)
Вводим команду `git checkout <первые 5 символов коммита, который вам нужен>`
Пример: 
```
__git checkout 3c53vg__
```

## 8. Игнорирование файлов
Для того, чтобы исключить из отслеживания в репозитории определённые файлы или папки необходимо создать файл 
***.gitignore*** и записать в него их названия или шаблоны, соответствующие таким файлам или папкам.

## 9. Создание веток в Git
По умолчанию имя основной ветки в Git -
 **master**. 
 Создать ветку можно командой:
 ```
git branch <имя новой ветки>
 ```

### 9.1. Слияние веток и разрешение конфликтов
Для слияния текущей ветки с какой-либо другой используется команда 
```bash
git merge < имя ветки >
```
*В результате выполнения этой команды в текущей ветке появится новый коммит*

**Конфликты слияния** происходят при слиянии ветвей, имеющих конкурирующие фиксации, и Git требуется ваша помощь, чтобы принять решение относительно того, какие изменения следует включить в окончательное слияние.
Чтобы разрешить конфликт слияния, необходимо ***вручную*** отредактировать конфликтующий файл и выбрать изменения, которые необходимо сохранить в окончательном слиянии.

 ### 9.2. Удаление веток
Команда для удаления локальной ветки в Git:
```bash
git branch -d < имя ветки, которую нужно удалить > 
```
`-d` это сокращённое значение команды `--delete`.

_Также стоит помнить, что невозможно удалить ветку, в которой вы сейчас находитесь и которую просматриваете. Если вы попытаетесь это сделать, вы получите сообщение об ошибке, так что перед удалением ветки обязательно нужно переключиться на другую ветку, которую вы **НЕ** хотите удалять(с помощью команды `git checkout`)._

 Ещё может быть так, что ветка, которую собираются удалить, содержит неотправленные изменения и коммиты, тогда флаг `-d` не даст удалить данную ветку, потому что коммиты не видны другим веткам, а Git защищает от случайной потери данных коммитов.

 Тогда нужно будет использовать `-D`. Например, вот так:
 ```
git branch -D <имя ветки>
 ``` 
 *Эта команда принудительно удаляет ветку, но с ней стоит быть аккуратным, тк тогда не последует запроса от программы с просьбой подтвердить наши действия(действительно ли мы хотим удалить данную ветку или же нет).*
 
## 10. ***Работа с удалёнными репозиториями***

1. Создать аккаунт на GitHub
2. Создать локальный репозиторий
3. Создать удалённый репозиторий
4. Связать локальный репозиторий с удалённым

Получить изменения из удалённого репозитория и выполнить слияние с локальной версией:
```bash
git pull
```
Отправить локальную версию репозитория на внешний: `git push`

Получить список связанных репозиториев `git remote`

## 10.1. Репозиторий для **pull request**
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