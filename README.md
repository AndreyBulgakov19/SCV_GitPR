# Работа с Git.


## 1. Установка Git.
Загружаем последнюю версию программы Git с [сайта](https://git-scm.com/downloads). Устанавливаем с настройками по умолчаению.  

## 2. Проверка наличия установленного Git.
В терминале выполнить команду __*git --version*__. Если Git установлен появится сообщение с информацией о версии программы, иначе будет сообщение об ошибке.

## 3. Настройка Git.
Настройка системы Git предполагает указание **_имени пользователя и e-mail_**, которые используются для подписи коммитов и отправки изменений в удалённый репозиторий.   
В Git существует три места, где хранятся настройки:
    
    * на уровне системы;
    * на уровне пользователя;
    * на уровне проекта (репозитория).

 Для настройки Git на том или ином уровне можно изменить конфигурационные файлы или воспользоваться специальными командами. Наиболее удобный и безопасный способ — использование команд.

 ## 4. Инициализация репозитория Git.
Файл Git начинает работать ~~сразу при запуске~~ _**только**_ после того как мы инициализируем программу- создание, активация, подготовка к работе, определение параметров. Данную команду можно и проще прописывать как `git init`, т.е. не нужно писать слово *initialization*.

## 5. Запись изменений в репозитории Git.
Итак, ~~можно~~ **нельзя** просто взять и написать команды сохранив их. Для изменения файла нужно сохранять все изменения, а также лучше записать,что изменилось. Существуют команды которые помогают сохранить правки в файле:

    1. git add [первая буква файла и далее tab], и уже после (на следующей строке) fit commit -m "краткое описание изменений";
    2. git commit -a -m "краткое описание изменений" 
Можно проверить записано ли изменение в файл. Для проверки используем команду **git status**. Если название и изменение файла указано красным, то изменения не сохранены.

## 6. Просмотр истории коммитов в Git.
Есть некая функция, позволяющая просматреть все изменения в файле. Для этого нам необходимо ввести один из вариантов команд:

    1. git log;
    2. git log --oneline;
    3. git log --graphs.
Первая(1.) команда отображает очень длиным списком, когда другие команды: вторая(2.) и третья(3.) показывают изменения супер коротко.

## 7. Перемещение между сохранениями (коммитами) в Git.
Для перемещения между коммитами нам понадобятся одна из команд из п. 6, которая выведит все изменения и команда:

**git checkout [цифры и буквы изменений в начале появившегося желтого текста, которых достаточно ввести не меньше 5]**. 

После чего наш файл вернется в изменения, которые произошли на определенный момент с начала, а последующие перестанут отображаться. Ну и конечно же, для продолжения работы с файлом с самого последнего изменения нам необходимо вернуться в команду с этими изменениями. С помощью команды **git checkout _master_** (или какое-либо др. название) мы перейдем в самое последнее изменение файла.

## 8. Добавление изображений в Git.

В Git можно добавлять не только текст, но и картинки.

Для начала нам необходимо загрузить нужное нам изображение в папку в которой работаем. После этого нам нужна следующая команда:
    
    ![картинка](имя_файла.расширение).

**Пример:**
![картинка](Petya_and_wolf.jpg)


## 9. Gitignore в Git.
Команда **.gitignore** используется для игнорирования git(ом) файлов, которые мы укажем. Это очень полезно, тк значительно уменьшает объем файла всего проекта.
Для использования функции игнорированя, нам необходимо создать файл `.gitignore` и внести туда нзвания файлов, который нужно игнорировать.

## 10. Ветки в Git.
 Ветки (*от англ. branch*)-это своего рода разделение (далее ответвление) главного файла, то есть всего проекта, который должен получиться. Ответвление дает возможность работать каждой команде и/или каждому человеку в команде выполнять свою, определенную, функцию общего проекта. Команда для создания ветки **git branch branch_name**.

 ## 11. Слияние веток и разрешение конфликтов в Git.
 Слияние веток- что же это такое?
Все просто! 

    Слияние веток- эта функция необходимая для того, чтобы "кусочки" работы над общим проектом "влить" соединить с главной веткой. Таким образом мы создадим конечный (полный) файл проекта.
Команда для слияния: **git merge branch_name**. 

### `Важно!` ### 
    Через команду git merge branch_name происходит слияние какой-то ветки в выбранную, отмеченую знаком (*) . Сливаем в главную.

**Но!**

Все не так просто, как кажется на первый взгяд.
Прислиянии веток могут возникнуть так называемые *конфликты*- это когда то или иное изменение не совпадает с информацией в другой ветке. Приведем пример:

_допустим у одной ветки на определенной строке прописано слово **А**, когда у другой **В**._

При слиянии эти веток возникнит конфликт, тк строка со словом **А** не ровна строке **В**. У нас появится следующее:

    <<<<<<< HEAD
    А
    =======
    >>>>>>> В
    
Она означает, что Git предлагает нам выбрать, какой из вариантов нам оставить, для того чтобы нам было проще ориентироваться сначала мы можем, нажав на *сравнить изменения*, выяснить что конкретно создало конфликт. Далее нам необходимо принять решение, что нам необходимо оставить, для этого git предлогает выбрать измененя с помощью следущих команд:

* Принято текущее изменение ( в нашем примере выше- это строка <<<<<<< HEAD А);
* Принять входящее изменение (в нашем примере выше- это строка >>>>>>> В);
* Принять оба изменения.

`Запомним`

    Git не может самостоятельно разрешить конфликт. Для решения нам необходимо ему помочь. Нужно выбрать с помощью пунктов, которые нам предлагает git, принять решение.

## 12. Удаление веток.
После слияния веток в единую мы можем удалить ненужные ветки через команду: 
    
    git branch -d branche_to_delete.

`Будь внимателен!`

**При удалении ветки могу возникнуть ошибки:**

* Удаление активной ветки. Если вы находитесь на определённой ветке и пытаетесь её удалить, Git не позволит вам это сделать, потому что вы работаете с этой веткой в данный момент.

* Удаление ветки с незагруженными изменениями. Если у вас есть незавершенные изменения в локальной ветке и вы пытаетесь её удалить, Git предупредит вас, чтобы вы не потеряли свою работу.

* Удаление ветки без сохранения копии. Ветка может содержать ценную информацию, и случайное удаление может нанести урон проекту.
    
**Небольшой лайфхак для избежания ошибок при удалении веток.**

    Перед удалением веток лучше себя перепроверить запустив команды
    
    * git status 
    * git branch



# Локальные и удаленные репозитории Git.

## 1. Локальные и удаленные репозитории Git.

С репозиториями можно работать двумя способами:
* локально;
* удаленно.

Для использования локального репозитория необходима его инициализация на своём компьютере. 

Работает это так:

1. Мы берем уже имеющуюся или создаем папку на своем компьютере; 
2. Открывам VS Code c Git_ом и внутри указанной папки команду _git init_;
3. Вносим какие-то изменения;
4. Commit_m изменения;

**Локальные репозитории.**
На компьютере все происходит локально только в папке, которую мы указали. 
За ее пределы ничего не выходит.

**Удаленный репозиторий**- это не тот, который удалили (переместили в корзину). 
В данном случае удаленный- это сделанный где-то на другом компьютере/ в другой папке.

Удаленный нам нужен для того, чтобы передать репозиторий одного человека другому не используя такие средства как:
сохранение файла на флешку и передачу его лично, ожидая, когда другой человек внесет свои изменения и вернет нам флешку и т.д.

## 2. Git и GitHub.

Итак.

	1. Git — это программа, которая устанавливается на компьютер, где локально выполняет указанные вами команды.
	2. GitHub — это сервис компании Microsoft, который позволяет интегрироваться с программой Git и настроить удалённую работу с вашим репозиторием.

Таким образом, можено работать локально или хранить свой репозиторий на GitHub,
используя команды, входящие в программу Git.

`Важно!`

**Git и GitHub — разные вещи.**

При работе с одним репозиторием нескольким людям, необходимо, чтобы доступ к нему был у всех.
Для этого удобно пользоваться GitHub_ом .

## 3. Работа с сайтом GitHub.

Первое, что нам нужно сделать- это перейти на сайт [github.com](https://github.com) и пройти регистрацию.

Мы можем как создать свой репозиторий, так и взять готовый на этом сайте.

Для работы с готовым репозиторием, нам необходимо его клонировать через команду:

**git clone ссылка_на_готовый_репозиторий**

Через поиск находим нужного нам автора и проект. Переходим к проекту и нажимаем кнопку `CODE`.

Во вкладке HTTP отобразится ссылка. Копируем и вставляем ее в наш терминал через команду клонирования. Ждем загрузку. Далее через команду git status можно увидеть, что этот репозиторий горит красным. Для сохранения нам нужно использовать команду: 

**cd наименование_папки_нашего_репозитория**.

## 4. Pull и push.

После того, как сконнектим наши репозитории.
Можно добавлять изменения как в локальном репозитории так и удаленном.

`Важно`

    Перед добавлением изменений локально и удаленно нужно обязательно commit_ить изменения.

Команда **git pull** (_от англ. потянуть, выдернуть_) предназначена для того, чтобы в наш локальный репозиторий подтянулись изменения, сделанные в удаленном.

Команда **git push** (_от англ. толчок, продвинуть_) рпедназначена для того, чтобы мы с локального репозитория отправили "вытолкнули" в удаленный репозиторий.

`Запомним!`

    git pull- подтягиваем в локальный репозиторий данные удаленного;

    git push- выталкиваем из локального репозитория в удаленный.

## 5. Копирование репозитория через кнопку `Fork`.

Чтобы работать с чужим репозиторием, лучше скопировать его и работать с копией.
Для копирования репозитория нам нужно использовать кнопку `Fork` _(от англ. вилка)_. Происходит своего рода ответвление.

Кнопку искать долго не нужно. Она находится непосредственно там же, где и определенный удаленный репозиторий. Справа чуть выше.

Клонирование репозитория на наш локальный компьютер производим командой из _пункта 3. Работа с сайтом GitHub._

    **git clone ссылка_на_готовый_репозиторий**.

## 6. Pull requests.
Слияние локальной и удаленной ветки происходит с помощью команды  
### Pull requests 
Она находится сверху в строке над репозиторием
Code-**Pullrequests**-Actions-Projects-Wiki-Security-Insights-Settings.
