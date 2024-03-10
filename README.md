![Logo](git_logo.png)

# Инструкция по использованию Git

## 1 Установка Git
Сначала убедитесь, что Git установлен на вашем компьютере. Если нет, вы можете скачать его с официального сайта Git.
Установите Git, следуя инструкциям для вашей операционной системы.

## 2 Настройка Git
Откройте терминал (командную строку) на вашем компьютере.
Настройте ваше имя пользователя: 
*git config --global user.name "Ваше Имя"*
*git config --global user.email "ваша@почта.com"*
## 3 Инициализация репозитория
Создайте новый каталог для вашего проекта:
*mkdir my_project
cd my_project*
Инициализируйте новый Git-репозиторий:
*git init*
## 4 Добавление файлов в игнорирование
Чтобы игнорировать какие либо файлы нужно создать папку .gitignore 
и добавлять туда те файлы которые не хоти отслеживать.
## 5 Простмотр истории коммитов
Чтобы просмотреть историю коммитов нужно прописать в терминале git log
## 6 Перемещение между сохраненными коммитами
Чтобы просмотреть историю коммитов нужно
и перемещаться нужно прописать git checkout и hash коммита
## 7 Конфликт 
Чтобы просмотреть историю коммитов нужно conflict2
## 8 Добавление файлов
Команда *git add* используется для добавления изменений 
в индекс (промежуточную зону) перед фиксацией (коммитом).
*git add имя_файла*
## 9 Фиксирование изменений
Команда *git commit* фиксирует изменения, 
добавленные в индекс, и создает новый коммит.
*git commit -m "Описание изменений"*
## 10 Клонирование удаленного репозитория
Команда *git clone* используется для клонирования (создания копии) 
удаленного репозитория.
*git clone URL_репозитория*
## 11 Отправка изменений
Команда *git push* используется для отправки локальных изменений на 
удаленный репозиторий.
*git push origin имя_ветки*
## 12 Получение изменений
Команда *git pull* используется для получения изменений из удаленного 
репозитория и объединения их с локальными изменениями.
*git pull origin имя_ветки*