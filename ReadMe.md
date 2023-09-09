# Инструкция по работе с <span style="color:orange"> Git</span>, <span style="color:orange">GitHub</span> и <span style="color:blue"> Microsoft Visual Studio Code</span>.

## Глава 1. Проверка наличия установленного <span style="color:orange"> GIT </span> на вашем ПК. Установка  <span style="color:orange"> GIT </span>. Установка <span style="color:blue"> Microsoft Visual Studio Code</span>

### Для того чтобы проверить наличие установленного или установить GIT на Ваш ПК, требуется выполнить простые действия:

1. Открыть: ___Меню Пуск - Панель управления - Все программы___ и найти там Программу __GIT__

2. В случае наличия программы Git на вашем ПК:

> 1. Запустить программу __GIT__ 
> 2. Ввести команду <span style="color:orange"> _'git --version'_ </span> (запрос версии).
> 3. Получить ответ о текущей версии.
> ![Версия гита](git_version.png)
> 4. Сравнить текущую версию с требуемой, или актуально на сайте разработчика

3. В случае получения ошибки при запросе версии или отсутствия программы __GIT__ на Вашем ПК:

> 1. Открыт сайт разработчик по [данной ссылке](https://git-scm.com/downloads) или скопировав прямую ссылку: _https://git-scm.com/downloads_ и вставив в адресную строку Вашего браузера.
> 2. На странице разработчика программного обеспечения выбрать подходящую для Вас версию программного обеспечения __GIT__, как показано на скриншоте ниже 
> ![Лицевая страница загрузки](download.png)
> 3. При выполнении установки или обновления не выбирать никаких дополнительных параметров (это учебная версия, по этому дополнительные параметры не требуются)
> 4. После установки или обновления __GIT__ запустить командрую строку и ввести команду <span style="color:orange"> _'git --version'_ </span> (запрос версии).

__На этом мы закончили с установкой или обновлением вашей программы __GIT__ до Актуально версии и можем приступать к установке <span style="color:blue"> Microsoft Visual Studio Code</span>__

4. Для установки <span style="color:blue"> Microsoft Visual Studio Code</span> потребуется:
> 1. Перейти на сайт разработчика программного обеспечения по [Ссылке]( https://code.visualstudio.com/Download) или скопировав прямую ссылку  https://code.visualstudio.com/Download и вставив в адресную строку Вашего браузера.
> 2. На странице разработчика программного обеспечения выбрать подходящую для Вас версию программного обеспечения <span style="color:blue"> Microsoft Visual Studio Code</span>, как показано на скриншоте ниже
>![Инсталлер Visual Code](MVSCinstal.png)
> 3. При выполнении установки или обновления не выбирать никаких дополнительных параметров.
> 4. После установки запустите <span style="color:blue"> Microsoft Visual Studio Code</span> и ознакомьтесь с лицевой страницей.
> ![Лицевая страница](MVSChallo.png) 
> 5. Для боле простой и наглядной работы, с при помощи языка разметки __MarkDown__, рекомендуется также установить расширение для <span style="color:blue"> Microsoft Visual Studio Code</span> под названием __Markdown Preview__
>> Для этого вам потребуется:
>> 1. Открыть раздел "Extensions" или "Расширения"
>> 2. В поисковой строке ввести "Markdown Preview"
>> 3. Нажать кнопку Install на указанной ниже (на скриншоте) подпрограмме (расширении)
>> ![Расширение](MVSCmd.png)
>> Что позволит отображать визуальную выходную информацию написанного вами "кода" на языке __Markdown__ 
>> ![Как выглядит](MVSC.png)
>> Для вывода визуальной части потребуется сохранить ваш файл с расширением __.MD__, после чего  по нажатию ПКМ (правой кнопки мыши), вы увидите в контекстном меню __"Markdown Preview Enhanced: Open Preview to the side"__. Данная команда и активирует режим визуализации.

На этом подготовительные мероприятия для работы с __Markdown__ в <span style="color:blue"> Microsoft Visual Studio Code</span> и <span style="color:orange"> Git</span> - завершены. И мы можем перейти к работе с <span style="color:orange"> Git</span>.


## Глава 2. Инициализация программы <span style="color:orange"> Git</span>

Перед началом работы с <span style="color:orange"> Git</span> настоятельно рекомендуется ознакомится с полезными ресурсами:
1. [Git для Новичков. Часть 1](https://habr.com/ru/articles/541258/) и [Git для Новичков. Часть 2](https://habr.com/ru/articles/542616/).
2. [Пользовательский Мануал по Git от разработчиков](https://git-scm.com/docs/user-manual)

После ознакомления с данными ресурсами, мы можем перейти к настройке (инициализации) вашего __GIT__

### Шаг 1. Инициализация пользователя.
Для выполнения любых работ в __GIT__ потребуется проведение первичной авторизации клиента (администратора) ресурса. Для этого выполняются простые команды в терминале Вашего __GIT__
> 1. Установим Имя пользователя. Для этого используем команду: <span style="color:purple"> git config </span> <span style="color:orange"> --global user.name </span> <span style="color:red"> "__ваше_имя__" </span> - где вместо __ваше_имя__ прописывается имя пользователя, допустим __USER__.
>>Так, полученная команда для пользователя __USER__ будет выглядеть следующим образом: git config --global user.name "__USER__"
> 2. Установим Адрес электронной почты.Для этого используем команду: <span style="color:purple"> git config </span> <span style="color:orange"> --global user.email </span> <span style="color:red"> "__адрес_почты@email.com__" </span> - где вместо __адрес_почты@email.com__ прописывается адрес электронной почты пользователя, допустим __USER@gmail.com__.
>>Так, полученная команда для пользователя __USER__ будет выглядеть следующим образом: git config --global user.name "__USER@gmail.com__" 

__<span style="color:red">Внимание!</span>__
1. Ввод "Логина" и электронной почты - являются обязательными для использования ПО __GIT__.
2. При вводе "Логина" и электронной почты, если данные команды выполнены верно, командная строка не вернёт никаких значений или сообщений. Итоговый результат должен выглядеть так:
![Инициализация](userinit.png)
3. Инициализацию пользователя можно также, сразу производить в <span style="color:blue"> Microsoft Visual Studio Code</span> через терминал.

### Шаг 2. Инициализация репозитория.

Для того, чтобы __GIT__ видел файлы и мог выполнять свои функции как программа контроля версий, требуется назначение места (репозитория) где будет находится проект или проекты. Для этого:
> 1. Пропишем команду <span style="color:purple"> git init </span>
>> В ответ получим: __"Initialized empty Git repository in <Адрес репозитория>"__
>> Это означает в указанном месте, находится пустой репозиторий __GIT__.
> 2. Добавим файл, который будет отслеживаться программой __GIT__, для этого пропишем команду <span style="color:purple"> git add </span> __<Имя файла>__
> 3. Добавим свой первый коммит, для этого пропишем команду <span style="color:purple"> git commit -m </span> __"Комментарий"__

### Шаг 3. Запись изменений в репозитории. Отслеживание изменений. Просмотр коммитов. Перемещение между сохраненными файлами

Для выполнения записи и изменения файлов в репозитории, а также отслеживании этих изменений применяются следующие команды:
* <span style="color:purple">git log </span> – вывод на экран истории всех коммитов с их хеш-кодами;
* <span style="color:purple">git checkout </span> – переход от одного коммита к другому;
* <span style="color:purple">git checkout master </span> – вернуться к актуальному состоянию и продолжить работу; 
* <span style="color:purple">git diff </span> – увидеть разницу между текущим файлом и закоммиченным файлом;

__Как производится запись изменений в репозитории?__
> При инициализированом __GIT__ - запись производится автоматически, при ___каждом___ сохранении изменений в файлах.
Для проверки изменений можно использовать команды - __log, chekout__ и __diff__, они позволят отследить все имменения произведенные всеми пользователями с данным файлом, а также какие изменения произошли с файлом между его версиями.

В случае, если пользователь не забывает при изменении версий проставлять комментарии при помощи команды __commit__, также будет выведена информация комментария к версии.

>Пример:
<span style="color:purple">$ git log --pretty=oneline </span>
<span style="color:orange"> 1b11970fd272176da7872f5b9f7a6c2b5c95b4be </span> (<span style="color:blue"> HEAD </span> -> <span style="color:green">master </span>, <span style="color:red"> origin/master, origin/HEAD </span>) 220209 рег. громк. Si4735
<span style="color:orange"> 23cc805326427be3db40bcb5d2829311478d29b1 </span> 220201 косметические исправления в команде tp
<span style="color:orange">f2459c4624ef818e06959ba5fe4c15c1e37d35d4 </span> 220127 Исправил влево-вправо для курсора
<span style="color:orange">93daeff2400033f00e5adbf04fb68cab27e7f9ff </span> 220123 Добавил кнопки TX и RX
<span style="color:orange">509c2f29d919624d3b333fb819a08d94676652bd </span> 220128 Исправил DEL, добавил индикатор РУС-ENG-dig
<span style="color:orange">6c432e5613e0f099ec575833c5aabbc63e681df6 </span> 220115 Исправление режимов под клавиатуру TCA8418
<span style="color:orange">65b292b712292b7ed6e88b7e5e2eadea480a52e9 </span> 220111 Исправил ошибку обработки ~INT для TCA8418
<span style="color:orange">9048b714cbd83d3c3edffb5f8890ef9c935ef027 </span> 220110 Продолжение работы над TCA8418
<span style="color:orange"> 2fb1f10e57de7bc3887574212172bb772c0d8f9f </span> 220109 Начало добавления новой клавиатуры на TCA8418
<span style="color:orange"> 1281f26518378f44ea669a3fd96317a391d7745c </span> 211121 CMSIS в отдельной библиотеке
<span style="color:orange"> 1f920bb4327e43b58b6b3f735a63a21759dab351 </span> 211120 Драйверы HAL в отдельной библиотеке
<span style="color:orange"> ab331d95634e248d9bbe4b291614e798c3ccc56d </span> 220128 Исправил маяки и передачу.
<span style="color:orange"> 7ad03121d46f6ef7c7f992aaff6f033f1d6d3dc8 </span> 211119 Исправил перекос в меню настроек

Где оранжевым выделены номера версий коммитов (изменений файла), а черным комментарии разработчика. 
Далее мы выбираем определенную версию (к которой хотим перейти), допустим версия __"Добавления TX и RX"__, у которой номер коммета __"93daeff2400033f00e5adbf04fb68cab27e7f9ff"__. 
Для этого при помощи команды __chekout__ мы переходим к этой версии. При этом достаточно знать первые 6-8 HEX-символов (символов номера версии):

> <span style="color:purple">$ git checkout 93daef</span>
Note: switching to '93daef'.
>
> You are in 'detached HEAD' state. You can look around, make experimental changes and commit them, and you can discard any commits you make in this state without impacting any branches by switching back to a branch.
>
>If you want to create a new branch to retain commits you create, you may do so (now or later) by using -c with the switch command. Example:
> git switch -c < new-branch-name>
>
> Or undo this operation with:
> git switch -
>
>Turn off this advice by setting config variable advice.detachedHead to false HEAD is now at 93daeff 220123 Добавил кнопки TX и RX
>
> <span style="color:green">microsin@DESKTOP</span> <span style="color:purple">USER</span> <span style="color:orange">/d/asm/radiopager</span> <span style="color:blue">((93daeff...))</span>

#### Работа с ветками. Ветвление, слияние, ошибки.

Из полезных комманд при работе с ветвлением в __GIT__:
* <span style="color:purple">git branch </span> - команда управления ветками проектов; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-branch)
* <span style="color:purple">git checkout </span> – переход от одного коммита к другому;
* <span style="color:purple">git checkout master </span> – вернуться к актуальному состоянию и продолжить работу; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-checkout)
* <span style="color:purple">git diff </span> – увидеть разницу между текущим файлом и закоммиченным файлом; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-diff)
* <span style="color:purple">git-merge </span> - обьединие нескольких пользовательских историй файла в одну; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-merge)
* <span style="color:purple">git remote </span> - удалённое управление некоторыми репозиториями; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-remote)

__Пример:__ 
> 1. Для создания новой ветки, отличной от основной (ветки Master), потребуется использовать команду <span style="color:purple">git branch "Имя ветки"</span>. Данная команда создаст ответвление от текущей версии.
![Создание веток](branchadd.png)
> * стоит обратить внимание на то, что __GIT__ не понимает русский язык, по этому для выбора имён, лучше всего применять виды написания текстов snake_type или cammel_type, для удобаства чтения. 
> * так же важно то, что __GIT__, никак не отреагирует на создание новой ветки.

> 2. Для проверки, того, создалась ли ветка, нужно использовать команду <span style="color:purple">git branch </span> без ковычек и дополнительных имён. В таком случае мы получем выведенный список всех веток:
![Работа с ветвлением](branch.png)
> И как было сказано ранее - основная ветка будет называться "__master__".

> 3. Для перехода между ветками используем <span style="color:purple">git checkout </span>, <span style="color:purple">git checkout "Имя ветки" </span> или <span style="color:purple">git checkout master </span>. 
> * Первая команда проверит текущую ветку и обозначит что вы находитесь в ней.
> * Вторая команда проведёт вас в указанную ветку.
> * Третья команда проведёт вас из любой ветки в Основную ветку. 
![Прыжки по веткам](branchcheck.png)

> 4. Для слияния или удаления веток используются команды: <span style="color:purple">git-merge "Имя ветки" </span> и <span style="color:purple">git branch -d "Имя ветки" </span> соотвественно. При применении <span style="color:purple">git-merge "Имя ветки" </span> - вы сольёте названную ветку с текущей. ри применении <span style="color:purple">git branch -d "Имя ветки" </span> - вы удалите названную ветку.
![Слияние удаление](branchrem.png)

### Работа с внешним (удалённым) репозиториями.

Работа с удалённым репозиторием рассматривается на базе платфомы __Github__ 
[Ссылка на ресурс](github.com)
1. Для начала рабыот с удалённым репозиторием, требуется пройти регистрацию на площадке __Github__ для этого потребуется:
> * Электронная почта
> * Придумать пароль
> * Создать никнейм
> * А также подписаться или отписаться от рекламы площадки.
> После этого вас попросят решить простую "капчу". 

2 Для начала работы с внешним (удалённым) репозиторием, его требуется создать.
Для этого нужно выбрать следующие поля меню:
![Ссылка на ресурс](derectoryadd.png)
Далее Вам нужно будет создать репозиторий по в диалоговом окне: 
![Ссылка на ресурс](derectoryadd2.png)
и выбрать тип репозитория:
* Открытый (к такому будут иметь допступ пользователи)
* Приватный (к такому будут иметь допступ только ограниченное число лиц)

__Подготовительные работы завершены, теперь можно вернуться в GIT__

По завершению создания репозитория, последней процедурой будет интеграция вашего локального репозиртория в гитхаб. Для этого потребуется прописать несколько команд, которые автоматически будут сгенерированны в окне репозитория на гитхабе.

>Пример: 
> git remote add origin "ссылка на репозиторий в гитхабе"
> git branch -M main
> git push -u origin main

> __Важно, что после инициализации всех этих команд, ваша основная ветка будет не MASTER, а MAIN.__

Поссле ведения данных команд, ваш локлаьный __GIT__ репозиторий будет автоматически перенесен в гитхаб, а также произойдёт аутентификация пользователя в модальном окне. В конце всех мероприятий мы получем следующие строки в командной строке (терминале):
![Ссылка на ресурс](github.png)

__Приступим к работе с удалённым репозиторием:__

Для работы с удалённым репозиторием нам понадобсят команды:
* <span style="color:purple"> git status </span> - проверка сосотояния программы;
* <span style="color:purple"> git commit -m </span> __"Комментарий"__ - запись комментария к выбранной версии файла;
* <span style="color:purple">git log </span> – вывод на экран истории всех коммитов с их хеш-кодами;
* <span style="color:purple">git checkout </span> – переход от одного коммита к другому;
* <span style="color:purple">git checkout master </span> – вернуться к актуальному состоянию и продолжить работу; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-checkout)
* <span style="color:purple">git branch </span> - команда управления ветками проектов; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-branch)
* <span style="color:purple">git-merge </span> - обьединие нескольких пользовательских историй файла в одну; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-merge)
* <span style="color:purple">git remote </span> - удалённое управление некоторыми репозиториями; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-remote)
* <span style="color:purple">git fetch </span> - загрузка обьектов и ссылок из другого репозитория; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-fetch)
* <span style="color:purple">git push </span> - обновление удаленных ссылок вместе со связанными объектами. Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-push)



#### Перечень полезных команд.

* <span style="color:purple"> git status </span> - проверка сосотояния программы;
* <span style="color:purple"> git config </span> <span style="color:orange"> --global user.name </span> <span style="color:red"> "__ваше_имя__" </span> - инициализация пользователя;
* <span style="color:purple"> git config </span> <span style="color:orange"> --global user.email </span> <span style="color:red"> "__адрес_почты@email.com__" </span> - инициализация электронной почты пользователя;
* <span style="color:purple"> git init </span> - инициализация репозитория;
* <span style="color:purple"> git add </span> - добавление в репозиторий файла;
* <span style="color:purple"> git commit -m </span> __"Комментарий"__ - запись комментария к выбранной версии файла;
* <span style="color:purple">git log </span> – вывод на экран истории всех коммитов с их хеш-кодами;
* <span style="color:purple">git checkout </span> – переход от одного коммита к другому;
* <span style="color:purple">git checkout master </span> – вернуться к актуальному состоянию и продолжить работу; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-checkout)
* <span style="color:purple">git diff </span> – увидеть разницу между текущим файлом и закоммиченным файлом; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-diff)
* <span style="color:purple">git clear </span> - очищает командную строку;
* <span style="color:purple">git help </span> - справка по всем командам;
* <span style="color:purple">git branch </span> - команда управления ветками проектов; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-branch)
* <span style="color:purple">git-merge </span> - обьединие нескольких пользовательских историй файла в одну; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-merge)
* <span style="color:purple">git remote </span> - удалённое управление некоторыми репозиториями; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-remote)
* <span style="color:purple">git fetch </span> - загрузка обьектов и ссылок из другого репозитория; Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-fetch)
* <span style="color:purple">git push </span> - обновление удаленных ссылок вместе со связанными объектами. Полное описание можно найти по [Ссылке на справку разработчиков](https://git-scm.com/docs/git-push)

<<<<<<<Head 

тут конфликт

=======

тут вторая половина конфликта

>>>>>>>
