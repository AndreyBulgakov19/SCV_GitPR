![Logo](Git-Logo-2Color.png)
# Работа с GIT
## 1. Проверка наличия установленного Git
В терминале выполнить комманду `git --version`. Если Git установлен, появиться сообщение с информацией о версии программы, иначе будут сообщение об ошибке.

 ## 2. Установка Git
  Загружаем последнюю версию Git с [сайта](https://git-scm.com/downloads)
  Устанавливаем с настройками по умолчанию.

## 3. Настройка Git
При первом использовании git необходимо представиться. Для этого в терминале нужно ввести 2 комманды:
```Bash
git config --global user.name "Ваше имя английсими буквами"
git config --global user.email ваша почта@example/com
```
## 4.Инициализация репозитория
В терминале переходим в папки, в которых хотим создать репозиторий. Выполняем команду:
```
git init
```
В исходной папке появиться скрытая папка ***.git***

Чтобы посмотреть какой статус работы на данный момент, используем команду:
```
git status
```
Таким образом мы видим какие файлы изменены и чтобы добавить их в состаяние staged , мы вводим:
```
git add
```

Далее создаем новый комментарий:

```
git commit -m"text"
```
Команда для просмотра истории комментариев в ветке:

```
git log
```
Чтобы посмотреть на изменения, которые были произведены между файлами, используеться комманда:
```
git diff
```

## 5. Запись изменений в репозиторий
## 6. Просмотр истории коммитов
## 7. Перемещение между сохранениями
 Для этого используеться комманда:
 ```Bash
git checkout
 ```
 Для начала воспользуемся коммандой ***git log*** далее переключаемся на момент, когда был выполнени коммит ***git checkout <хэш коммита>***

## 8. Игнорирование файлов
Для того чтобы исключить из отслеживания в репозитории определенные файлы или папки, необходимо создать файл .***gitignore*** и записать в него их названия или шаблоны, соответствующие таким файлам или папкам.

## 9. Создание веток
По умолчанию имя основной ветки в git - ***master***
Создать ветку можно командой:
```Bash
git branch< имя новой ветки>
```
Список веток в репозитории можно посмотреть с помощью комманды:
```Bash
gitbranch
```
Текущая ветка будет омечена звездочкой: **\**master***
## 10. Слияние веток,разрешение конфликтов
Для слияния выбранной ветки с текущей нужно выполнить комманду:
```Bash
git merge < название выбранной ветки>
```
Если была изменена одна и та же часть файла в обеих ветках, то может возникунуть конфликт, который потребует участия пользователя. Vscode предлагает варианты разрешения.
Чтобы разрешить конфликт нужно выбрать один из вариантов. Выполнить коммит слияния:
```Bash
git merge <название ветки которую хотим слить>
```
## 10. Удаление веток
После этого необходимо удалить ветку с конфликтующим вариантом, для этого используем комманду:
```Bash
git branch -d <название ветки необходимую удалить>
```
***ВАЖНО*** производить выполнение этой программы с сторонней ветки или с ветки *master*

## 11. Работа с GITHUB
1. Cоздали аккаунт на Github.com
2. Создать локальный репозиторий
3. "Подружить" ваш локальный и удаленный репозиторий. Github при создании нового репозитория подскажет как это сделать.
4. Отправить (push) ваш локальный репозиторий в удаленный (на Github), при этом вам, возможно, еужно будет авторизоваться на удаленном репозитории.
5. провести изменения "с другого компьютера".
6. Выкачать (pull) актуальное состояние из удаленного репозитория.

## 12. Работа с удаленными репозиториями

1. Создать аккаунт на Github
2. Создать локальный репозиторий
3. Создать удаленный репозиторий
4. Связать удаленный репозиторий с локальным

Добавить удаленный репозиторий к проекту:
```Bash
git remote add <имя для репозитория> <url - адрес репозитория в сети>
```
Для получения и слияния изменений из удаленного репозитория используется команда `git pull`
Отправить изменения локального репозитория в удаленный: `git push`

```C#
while(cjunt < 0)
{
count++;
}
```
Отправить изменения локального репозитория в удаленный: `git push`
## 13. Pull request
1. Делаем *fork* репозитория
2. Делаем *clone* своей версии репозитория
3. Создаем новую ветку и в нее вносим свои изменения
4. Фиксируем изменения (делаем коммиты)
5. Отправляем свою версию в свой GitHub
6. На сайте GitHub нажимаем кнопку pull request

