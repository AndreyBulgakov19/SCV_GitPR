# Это репозиторий для обучения pull request

## Первые шаги

1. Делаем fork репозитория, в которой потом хотим сделать pull request. Ищем кнопку Fork на странице репозитория <https://git@github.com:gulden-geekbrains/version_control.git>

2. Выполняем команду клонирования из своей fork-копии

```sh
git clone https://github.com/Nikolaevch1/version_control.git
```
3. Создаем новую ветку и вносим необходимые изменения в файл
```sh
touch README.md
git add README.md
git commit -m "Создали репозиторий"
vim README.md
git add README.md
git commit -m "Добавили инструкцию как создать pull request"
```
4. Делаем push  
```sh
git push --set-upstream origin main
```
5. Переходим на свою страницу репозитория. Выбираем ветку **updatereadme** и жмем кнопку **Compare & pull request**

## Заметки
###Удаление ветки на удаленном репозиории
```sh
git push origin --delete nameBranch
```

Что бы сделать push от другого пользователя необходимо выполнить команду
```sh
GIT_SSH_COMMAND='ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes' git push git@github.com:gulden-geekbrains/version_control.git
```

вместо *user-private-key* подставьте свой ключ

Можно прописать настройки для подсоединения по ssh
```sh
git config remote.origin.url git@github.com:gitusername/reponame
git config core.sshCommand "ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes"
```






# Подсказака по GIT

>git init

```sh
git init - инициализация репозитория
``` 

## git add
```sh
git add "имя файла" -добавить директорию и все файлы в ней находящиеся в список отслеживаемых
```
## git commit
```sh
git commit - создание комита
(Откроется редактор комита
- Для создания комита необходимо нажать i
- Для выхода нажать Esc; написать команду :wq  (w- для записи; q- для выхода ))

git commit -m 'commit message' - добавить сообщение комита

git commit -a (это две команды git add name.file / git commit ) 
```
``````sh
git commit -am ‘message' - добавление комита и принятие изменений
``````
```sh
git restore name.file - отменнее изменений до комита
```
## *git log* & *git log --oneline*

```sh
git log  - Просмотр истории комитов

git reflog  - Просмотр истории действий

git reset  - Сброс текущего состояния истории

git revert - Отмена последствий комита

git restore - Сброс состояния файла на указанное

git log --oneline - Компактный вывод истории комитов
```

>*touch images/.gitkeep -создание скрытых системных файлов для определения пустых папок репозиторием*

```sh
git checkout <name branch>- переключение по комитам 
```



![Часть в квадратных скобках - это так называемый альтернативный текст, который важен по следующим причинам:Для доступности. Программы чтения с экрана читают именно его. Например, для тех, кто плохо видит.Этот текст будет отображаться вместо изображения, если файл изображения не может быть загружен.Он обеспечивает контекст и описание изображения для поисковых систем, помогая им с поиском.](/images/images_one.jpg)
![avatar](https://itsfoss.com/content/images/2023/02/adding-images-markdown.png)

## Отображение всех веток 
```sh
git brach
```
## Перемещение по веткам
```sh
git checkout 'имя_ветки'
```
## Создание новой ветви
```sh
git brach "name_branch"
```
## Удаление ветки
```sh
git branche -d  <имя ветки>
```



## Объеденение ветвей
```sh
git merge <name_branch>
```
###### *находиться на ветви master*

# Изменение адреса репозитория

```sh
git remote set-url origin git://new.url.here
```