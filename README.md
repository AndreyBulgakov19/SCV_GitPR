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
![logo](Git-Logo-White.png)

# Работа с Git
## 1. Проверка наличие установленного Git
В Терминале выполнить команду  `git --version` если git установлен появится версия программ или сообщение об ошибке если не установлен

## 2. Установка Git
Загружаем последнюю версию Git с 
[сайта](https://git-scm.com/downloads)
Устанавливаем с настройками по умолчанию 

## 3. Настройка Git
При первом использовании Git необходимо представится. Для этого в терминале нужно ввести две команды:
```bash
git config --global user.name «Ваше имя английскими буквами» 
git config --global user.email ваша почта@example.com
```

## 4. Инициализация репозитория
в терминале переход
им к папке в которой хотим создать репазиторий.Выпоняем команды
```
git init
```
в исходной папке появится скрытая папка ***.git***

## 5. Запись изменений в репазиторий
При создании каждой новой записи в исходном файле перед тем как она попадет в репазиторий ее необходимо зафиксировать командой:
```
 1. git add команда для фиксации одного файла
 2. git add . команда для фиксации всех файлов
```
Псле создания фиксации файла в индексе, его необходимо сохранить в репозитории при это обязательно нужно указать коментарий или название к сохранению.
Существует несколько команд:
```
 1. git commit -m "коментарий к записи" выполняется после фиксации индексе
 2. git commit -am "коментарий к записи" комбенированная команда, которая выполняет одновременно фиксацию в индексе и кометарий,после чего сохроняет файл в репозитории
```
## 6. Просмотр истории коммитов
Чтобы посмотреть историю коммитов,так же существует несколько команд:
 ```
  1. git log стандартная команда для просмотра истории коммитов с более детальной инфомацией о них
  2. git log --oneline команда которая вызывает историю коммитов с краткой информацией о них
  3. git diff команда которая показывает изменения или удаления в истории коммитов
 ```
## 7. Перемещени между сохранениями
Иногда нам необходимо отредактировать какой то отдельно взятый коммит,для нам нужно вызвать историю где у каждого сохранения есть свой уникальный номер,как показанно на скриншёте
![screenshot](screenshot.PNG)
Псле этого копируем первые четыре или пять символов уникального номера коммита
где после команды:
```
 git chekcout 9c8cc3 вставляем первые несколько символов уникального номера коммита
```
После этого git открывает нам указанный коммит где мы можем вносить свои изменения.

## 8. Игнорирование файлов
Для того чтобы исключить изотслеживания в репозитории файлы,расширения или папки,необходимо создать там файл ***.gitignore*** и записать в него их названия (расширения,файлы,папки).

## 9. Создание веток
По умолчанию имя основной ветки в Git - `master`
Создать ветку можно командой:
```
git branch <имя новой ветки>
```
Список веток в репозитории можно посмотреть с помощью команды
```
git branch
```
Текущая ветка будет отмечена **\*master**
 
## 10. Слияние и разрешение конфликтов у веток
Для слияния выбранной ветки с текущей нужно выполнить команду:
```
git merge <имя выбранной ветки>
```
Если была изменена одна и та же часть файла в одной и тойже ветке,то при слиянии веток может возникнуть конфликт,который потребует участия пользователя. VSCode предлагает выбрать варианты разрешения
 * Принять текущее изменение
 * Принять входящее изменение
 * Сравнить оба изменения
 * Обьединить оба изменения

После выбранного решения сразу необходимо выполнить слияние, находясь в исходной ветке (master)

## 11. Удаление веток
Для токо чтобы удалить выбранную ветку так же существует несколько команд:
```
 1. git branch -d <имя ветки>
 2. git branch -D <имя ветки> удаление ветки принудительно
```
 # Рабата с удаленными репозиториями 

## 1. Github это сервис который позволяет работать с удаленными репозиториями и групповыми проэктами.

## 2. Для того чтобы загрузить свой проект в Github,нужно создать в нем учетную запись.

## 3. Создать локальный репозиторий

## 4. Создать удаленный репозиторий
   После регистрации своего аккаунта на `Github` создаем свой новый локальный репозиторий и дать ему имя, а так же настроить некоторые функции.
## 5. Связать локальный и удаленный репозиторий
 * На сайте Github появятся команды которые делаются по порядку и связывают репозитории 
```
git remote add <имя для репозитория> <url-адрес репозитория в сети>
```
 * Для получения и слияния изменений из удаленного репозитория используется команда:
```
git pull
```
 * Отправить изменения из локального репозитория в удаленный:
```
git push
```
# 6. Работа с чужими репозиториями в Github у которых есть свободный доступ
 * После того как мы нашли нужный нам репозиторий, нам нужно колонировать его в свой репозиторий на свой аккаут. Сначал в нутри сайта мы ищем кнопку ***```Fork```***
 * В новом окне откроется нужный нам репозиторий и информация в нем. Теперь чтобы открыть новый репозиторий в локальном нам нужно нажать на кнопку ***```code```*** и скопировать адрес данного репозитория.
 * В локальном репозитории в корневой папке создаем команду:
 ```
 git clone <адрес скопированного репозитория> <можно дать новое имя>
 ```
 * Навав работу в новом репозитории (сколонированном) необходимо создать новую ветку (черновик) и переключится на неё используя команду:
```
git checkout -b <имя новой ветки>
```
 * После внесения новых изменений в новую ветку нам необходимо отправить их в удаленный репозиторий исрользуя команду:
```
git push
```
 * Так же важно учесть перед отправкой изменений в локальный репозиторий место нахождения своей ветки
(имя ветки) так как по умалчанию на Github используется ветка ***```main```***
 * Чтобы в Github появилась ветка(черновик) используется команда:
 ```
 git push --set-upstream origin <имя ветки>
 ```
 * Переходим в удаленный репозиторий Github и нажимаем зеленую нопку ***```Pull request```***
 если копка не появилась значит нужно переключится на добавленную новую ветку(черновик) во вклатке
 ***Pull request*** нажимаем на зеленую кнопку ***New Pull request*** и переключаемся на нужную ветку.
  * Необходимо подчеркнуть,если мы в локальном репозитории после внесенных изменений,перешли на ветку ***```main```*** то в Github удаленном репозитории зеленая кнопка ***```Pull request```*** появляется сразу.
  
  ***END***