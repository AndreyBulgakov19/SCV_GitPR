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

![логотип](logo_git.png)

# Работа с Git

## 1. Проверка наличия установленного Git
В терминале выполнить команду `git--version` Если Git установлен, появится сообщение с информацией о версии программы, иначе будет сообщение об ошибке.
## 2. Установка Git
Загружаем последнюю версию программы с [сайта](https://git-scm.com/downloads). 

 Устанавливаем с настройкам по умолчанию.
## 3. Настройка Git
Установка имени пользователя: `git config --global user.name "<ваше_имя>"`

Установка email: `git config --global user.email "<адрес_почты@email.com>"`



## 4. Инициализация репозитория
В терминале выполнить команду `git--init` для папки проекта

Команда `git status` для проверки является ли папка репозиторием

## 5. Запись изменения в репозитории
Необходимо добавить файлы проекта в будущий commit

```bashq
git add 

git add --all

git add "<имя_файла>"
```

Далее создаем commit. Обязательно указываем комментарий.

`git commit -m "<комментарий>"`

## 6. Просмотр истории изменеий и перемещение между изменениями

Команда `git log` вызывает журнал изменений текущего файла
 
 Выход из режима списка- кнопка Q

 Команда `git diff` показывает отличие текущего файла от уже сохраненного

Возвращают к актуальному состоянию файла следующие команды:
```bash

git checkout master

git switch

```

## 7. Полезные клавиши

`Tab` копирует имя файла

`Стрелка вверх` для быстрого вызова уже применявшихся команд

## 8. Игнорирование файлов
Для того, чтобы исключить из отслеживания в репозитории определенные файлы или папки, необходимо создать файл ***.gitignore*** и записать в него их названия или шаблоны, соответствующие этим файлам или папкам.

## 9. Создание веток в Git
По умолчанию имя основной ветки Git - **master**


Создать ветку можно командой: 

```bash
git branch <имя новой ветки>

```

Список веток в репозитории можно посмотреть с помощью команды:
```bash
git branch
```

## 10. Слияние веток в Git
Осуществить слияние веток можно командой :
```bash
git merge < имя ветки>
```
Слияние веток необходимо осуществлять из главной ветки.

После слияния обязательно осуществить коммит слияния.

## 11. Разрешение конфликтов 

Если между альтернативной веткой (черновиком) и главной веткой (master) обнаружатся различия , при слиянии этих веток возникнет конфликт. Разрешить его можно выбрав нужный вариант( принять текущий вариант, принять оба и тд) из предложенных в поле над выделенными областями. После разрешения конфликта обязательно осуществить коммит слияния. 

## 12. Удаление веток в Git

Для удаления веток необходимо использовать команду:
```bash
git branch -d <имя ветки>
```

Удалять ветку возможно только из ветки master

Если ветка не слита, git отменит удаление. Если необходимо удалить ветку без слияния,для принудительного удаления можно использовать команду:
```bash
git branch -D <имя ветки>
```

## 13. Работа с удаленным репозиторием 
Создание своего удаленного репозитория на GitHub возможно только при наличии аккаунта.
Находим кнопку `+` ,создаем репозитоорий `new repository` , называем репозиторий.

Автоматически можно создать папки README и gitignore

Находим иконку редактировать и работаем в репозитории.

Для выгрузки даннных из удаленного репозитория на локальный используется программа ` git pull` . Это составная команда, помимо выгрузки, команда будет осуществлять merge. 


Находим кноку `code` , копируем адрес , примением команду `git clone <имя файла>` в локальном репозитории 

Для того чтобы начать работу с удаленным репозиторием применяем `cd <имя папки>` Или открыть во встроенном терминале через меню.

Для выгрузки изменений с локального репозитория на удаленный используется команда `git push`. В первый раз `git push- u origin main`

Для работы с чужим удаленным репозиторием используем кнопку `fork` , копируем репозиторий себе на аккаунт и работаем по схеме, описанной выше. Для внесения изменений в чужой репозиторий обязательно создаем новую ветку.

Для предложения своих изменений проекту используем кнопку `pull requests`.








