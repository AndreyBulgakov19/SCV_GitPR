# Инструкция в Git
## 1. Управление версиями
Что такое «управление версиями» и почему оно должно нас интересовать? Система
управления версиями, или контроля версий, записывает историю изменения файла
или набора файлов, чтобы в будущем была возможность вернуться к конкретной
версии. В книге процесс управления версиями будет рассматриваться на фрагментах
кода, в реальности же эти операции можно проделывать с файлами практически
всех типов.
Графическим дизайнерам и веб-дизайнерам, которым нужно хранить все версии
изображений или компоновок, можно порекомендовать систему контроля версий
(Version Control System, VCS). Она позволяет возвращать в предыдущее состояние как отдельные файлы, так и целый проект, сравнивать сделанные изменения,
смотреть, кто и когда последним редактировал файл, являющийся источником
проблемы, и многое другое. Наличие VCS в общем случае означает, что при сбое
или потере файлов вы можете легко вернуться в рабочее состояние. И это вам
практически ничего не будет стоить.

## 2. Командная строка
Использовать Git можно разными способами. Для этого существуют как инструменты командной строки, так и многочисленные графические пользовательские
интерфейсы с различными возможностями. В этой книге рассматривается только
работа с Git из командной строки. Главным образом потому, что это единственный
способ выполнения всех Git-команд, — в большинстве GUI для простоты реализованы только некоторые варианты функциональности Git. Кроме того, человек,
умеющий работать с Git из командной строки, скорее всего, сможет разобраться, что
делать с GUI-версией, а вот обратное неверно. И если выбор графического клиента
зависит от личных предпочтений, то инструменты командной строки доступны
всем без исключения пользователям.
Предполагается, что вы знаете, как открыть терминал в Mac и приглашение на
ввод командной строки или оболочку **Powershell** в **Windows**. Если вы не понимаете,
о чем идет речь, нужно познакомиться с данными инструментами, чтобы следовать
приводимым в книге примерам и описаниям.

## 3. Установка в Windows
Установка Git в операционной системе Windows также осуществляется разными
способами. Официальный вариант системы доступен на сайте Git. Достаточно
зайти на [страницу](http://git-scm.com/download/win), и загрузка начнется автоматически. Обратите внимание, что этот проект называется Git для Windows (или
msysGit) и отличается от Git; дополнительная информация находится на [сайте](http://msysgit.github.io/).
Другой простой способ — это установка GitHub для Windows. Пакет установки
включает в себя версию как с командной строкой, так и с GUI. Он хорошо работает
с оболочкой Powershell и обеспечивает надежное кэширование учетных данных и
работоспособные настройки CRLF. Подробно мы рассмотрим эти вещи чуть позже,
пока же достаточно сказать, что они вам потребуются. Загрузить эту версию можно
с [сайта](http://windows.github.com).
Некоторые пользователи предпочитают установку Git из исходного кода, потому
что это позволяет получить самую новую версию. Немного отстают установщики
бинарных пакетов, хотя в последние годы развитие Git понемногу стирает эту
разницу.
Для установки Git из исходного кода вам потребуются следующие библиотеки, от
которых зависит эта система: curl, zlib, openssl, expat и libiconv. В системах с
инструментом yum (таких как Fedora) или apt-get (как системы семейства Debian)
для установки всех зависимостей можно воспользоваться следующими командами:

+ yum install curl-devel expat-devel gettext-devel \
 openssl-devel zlib-devel
+ apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \libz-dev libssl-dev

При наличии всех нужных зависимостей архив tar с последней версией можно найти в нескольких местах. Например, загрузить с сайта [Kernel.org](https://www.kernel.org/pub/software/scm/git) или с зеркала сайта [GitHub](https://github.com/git/git/releases). Как правило, последнюю версию проще найти на странице GitHub, но и на сайте kernel.org есть подписи версий, позволяющие проверить, что именно вы загружаете.

Затем остаются процедуры компиляции и установки:
+ tar -zxf git-1.9.1.tar.gz
+ cd git-1.9.1
+ make configure
+ ./configure --prefix=/usr
Первая настройка Git  31
+ make all doc info
+ sudo make install install-doc install-html install-info
После этого обновления можно загружать через саму систему Git:
+ git clone git://git.kernel.org/pub/scm/git/git.git

## 4. Первая настройка Git

Теперь, когда на вашей машине установлена система **Git**, нужно настроить ее
окружение. На каждом компьютере эта процедура проводится только один раз;
при обновлениях все настройки сохраняются. Впрочем, вы можете изменить их
в любой момент, снова воспользовавшись указанными командами.
Система **Git** поставляется с инструментом _**git config**_, позволяющим получать
и устанавливать переменные конфигурации, которые задают все аспекты внешнего
вида и работы **Git**. Эти переменные хранятся в разных местах.
+ Файл _**/etc/gitconfig**_ содержит значения, действующие для всех пользователей
системы и всех их репозиториев. Указав параметр --system при запуске git
config, вы добьетесь чтения и записи для этого конкретного файла.
+ Файл _**~/.gitconfig**_ или _**~/.config/git/config**_ связан с конкретным пользователем. Чтение и запись для этого файла инициируются передачей параметра
_**--global**_.
+ Параметры конфигурационного файла в папке Git _**(то есть .git/config)**_ репозитория, с которым вы работаете в данный момент, действуют только на конкретный репозиторий. 

Настройки каждого следующего уровня переопределяют настройки предыдущего, то есть конфигурация из .git/config перекроет конфигурацию из /etc/gitconfig. В системах семейства Windows Git ищет файл .gitconfig в папке $HOME _**(в большинстве случаев она вложена в папку C:\Users\$USER)**_. Кроме того, ищется файл _**/etc/gitconfig**_, но уже относительно корневого каталога MSys, расположение
которого вы сами выбираете при установке Git.

## 5. Ваш идентификатор

При установке **Git** первым делом следует указать имя пользователя и адрес
электронной почты. Это важно, так как данную информацию **Git** будет включать
в каждую фиксируемую вами версию, и она обязательно включается во все создаваемые вами коммиты (зафиксированные данные):

+ git config --global user.name "Name"
+ git config --global user.email name@example.com

Передача параметра --global позволяет сделать эти настройки всего один раз,
так как в этом случае Git будет использовать данную информацию для всех ваших
действий в системе. Если для конкретного проекта требуется указать другое имя
или адрес электронной почты, войдите в папку с проектом и выполните эту команду
без параметра _**--global**_.
Многие GUI-инструменты помогают выполнять эти действия при своем первом запуске

## 6. Инициализация репозитория в существующей папке

Чтобы начать слежение за существующим проектом, перейдите в папку этого проекта и введите команду _**git init**_. В результате в существующей папке появится еще одна папка с именем .git и всеми
нужными вам файлами репозитория — это будет основа вашего Git-репозитория.
Пока контроль ваших файлов отсутствует. 
Чтобы начать управление версиями существующих файлов (в противовес пустому каталогу), укажите файлы, за которыми должна следить система, и выполните
первую фиксацию изменений. Для этого потребуется несколько команд git add,
добавляющих файлы, за которыми вы хотите следить, а затем команда git commit:

+ git add *.c
+ git add LICENSE
+ git commit -m 'первоначальная версия проекта'

Чуть позже мы подробно рассмотрим, что делают эти команды. А пока у вас есть репозиторий Git с добавленными туда файлами и первой зафиксированной версией.

## 7. Проверка состояния файлов

Основным инструментом определения состояния файлов является команда
git status. Непосредственно после клонирования она дает примерно такой результат:
+ *git status*

*On branch master
nothing to commit, working directory clean*

Это означает, что в рабочей папке отсутствуют отслеживаемые и измененные файлы. Кроме того, система Git не обнаружила неотслеживаемых файлов, в противном
случае они были бы перечислены в выводимых командой данных. Наконец, команда
сообщает имя ветки, на которой вы в данный момент находитесь, и информирует
о совпадении состояний этой ветки и аналогичной ветки на сервере. Пока мы
будем работать только с веткой master, предлагаемой по умолчанию, тем более
что на данном этапе эта информация не имеет особого значения. Ветки и ссылки
подробно обсуждаются в главе 3.
Предположим, вы добавили в проект простой файл README. Если до этого момента
он не существовал, команда git status покажет данный неотслеживаемый файл
примерно так:

+ echo 'My Project' > README
+ git status

*On branch master*

*Untracked files:*

 *(use "git add <file>..." to include in what will be committed)*

*README*

*nothing added to commit but untracked files present (use "git add" to track)*

Понять, что новый файл README является неотслеживаемым, можно по заголовку
*Untracked files* в выводимых командой status данных. Указанное состояние,
по сути, означает, что Git видит файл, отсутствующий в предыдущем снимке состояния (в коммите); без явного указания с вашей стороны Git не будет добавлять
этот файл в число коммитов. Подобный подход гарантирует, что в репозитории не
сможет случайно появиться сгенерированный бинарный файл или другие файлы,
которые вы не собирались туда добавлять. Однако файл *README* туда добавить
нужно, поэтому давайте сделаем его отслеживаемым.

## 8. Фиксация изменений

Теперь, когда область индексирования настроена нужным вам образом, можно
зафиксировать внесенные туда изменения. Помните, что все, оставленное неиндексированным, в том числе любые созданные или измененные файлы, для которых
после редактирования не была выполнена команда _**git add**_, в текущий коммит не
войдет. Все эти файлы останутся на вашем диске как измененные. Впрочем, в рассматриваемом сейчас примере мы будем считать, что последний запуск команды
_**git status**_ показал все файлы как проиндексированные и все готово к фиксации
изменений. Проще всего осуществить фиксацию командой git commit:

+ git commit

Эта команда открывает выбранный вами текстовый редактор. (Редактор устанавливается переменной окружения оболочки $EDITOR — обычно это vim или emacs, хотя вы можете выбрать и другой вариант, воспользовавшись командой _**git config --global core.editor**_.)
В редакторе вы увидите следующий текст (в данном случае для примера взят редактор Vim):
+ Please enter the commit message for your changes. Lines starting
+ with '#' will be ignored, and an empty message aborts the commit.
+ On branch master
+ Changes to be committed:
+ new file: README
+ modified: benchmarks.rb
+ «.git/COMMIT_EDITMSG» 9L, 283C

Как видите, по умолчанию сообщение фиксации представляет собой превращенный
в комментарий результат работы команды git status с пустой строкой сверху. Этот
комментарий можно удалить, напечатав вместо него свой вариант, или оставить в
качестве напоминания о том, что именно вы фиксируете. Если вам требуется более
подробная информация об изменениях, можно добавить к команде git commit параметр -v. В результате в редакторе появится список изменений, включаемых в новые
фиксируемые данные. При выходе из редактора Git создает коммит с указанным
сообщением (удаляя комментарии и список изменений).
Сообщение фиксации можно задать и в команде commit, поставив перед ним флаг -m,
как в следующем примере:
+ git commit -m "Story 182: Fix benchmarks for speed"
[master 463dc4f] Story 182: Fix benchmarks for speed
 2 files changed, 2 insertions(+)
 create mode 100644 README

Итак, вы только что создали первую версию изменений! Надеемся, вы обратили
внимание, что версия предоставила вам ряд данных о себе: зафиксированная вами
ветка _**(master)**_, контрольная сумма _**SHA-1**_ версии _**(463dc4f)**_, количество подвергшихся изменениям файлов и статистика добавленных и удаленных строк.

## 9. Просмотр истории версий

После сохранения нескольких версий файлов или клонирования уже имеющего
содержимое репозитория вы, скорее всего, захотите взглянуть на то, что было сделано ранее. Базовым и самым мощным инструментом в данном случае является
команда _**git log**_.

## 10. Добавление удаленных репозиториев

Чтобы добавить репозиторий под коротким именем, которое упростит дальнейшие обращения к
нему, используйте команду 

+ _**git remote add [сокращенное имя] [url]**_.

## 11. Отправка данных в удаленный репозиторий

Чтобы поделиться результатами своего труда, их нужно отправить в репозиторий.
Это делается простой командой _**git push [имя удаленного сервера] [ветка]**_. Для
отправки ветки master на сервер origin (еще раз напоминаем, что в процессе клонирования эти имена присваиваются автоматически) следует написать:

+ git push origin main

Команда сработает только при условии, что клонирование осуществлялось с сервера, где у вас есть доступ на запись, и за это время никто не отправлял туда свои
данные. Если вы выполнили клонирование одновременно с другим пользователем
и он уже отправил результаты своей работы на сервер, ваша попытка отправки
данных окончится неудачей. Вам сначала нужно скачать все добавленное этим
пользователем и встроить это в свои данные, и только после этого появится возможность воспользоваться командой **push**.

## 12. Репозиторий для **pull request**
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
