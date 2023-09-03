# Репозиторий для **pull request**
## 1. В своём аккаунте на GitHub создать копию репозитория

 **"AndreyBulgakov19/SCV_GitPR"** с помощью кнопки **"Fork"**.
## 2. Клонировать копию репозитория на локальный компьютер.

1. Копируем ссылку из необходимого нам репозитория GitHub.
2. Используем команду:
```
**git clone** + *скопированную ссылку*
```
## 3. Создать новую ветку.

Создаем новую ветку в локальном репозитории и переключиться на неё командой:
```
checkout -b <название ветки>
```
## 4. Добавить файл с инструкцией в новую ветку.

Создаем новый файл например **README.md** если его нет. 
## 5. Дополнить инструкцию разделами по работе с удалёнными репозиториями, pull request.

Вносим изменения в файл
## 6. Зафиксировать изменения (коммиты).

Делаем комит (git add и git commit) или используем команду:
```
git commit -am "***Коментарий***"
```
## 7. Отправить изменения на GitHub.

```
git push
```
## 8. На сайте GitHub выполнить **Pull request**.

![Пример](Example.png)
1. В GitHub появляется кнопка **Compare & pull request**
2. Добавить описание.