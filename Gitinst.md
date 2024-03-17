![Logo](Git-Logo-White.png)

1. **Установка Git**:
   - Убедитесь, что **Git** установлен на вашем компьютере. Если нет, вы можете скачать его с [официального сайта Git](https://git-scm.com/downloads).
   - После установки, откройте терминал и убедитесь, что Git доступен, выполнив команду:
     ```bash
     git --version
     ```

2. **Настройка Git**:
   - Настройте свое имя пользователя и адрес электронной почты:
     ```bash
     git config --global user.name "Ваше имя"
     git config --global user.email "ваша_почта@example.com"
     ```

3. **Создание репозитория**:
   - Перейдите в папку, где вы хотите создать репозиторий.
   - Инициализируйте новый репозиторий:
     ```bash
     git init
     ```

4. **Добавление файлов в репозиторий**:
   - Создайте или скопируйте файлы в папку репозитория.
   - Добавьте файлы в индекс:
     ```bash
     git add имя_файла
     ```

5. **Создание коммита**:
   - Создайте коммит с описанием изменений:
     ```bash
     git commit -m "Описание изменений"
     ```

6. **Создание удаленного репозитория на GitHub**:
   - Зайдите на [GitHub](https://github.com/) и создайте новый репозиторий.
   - Скопируйте URL удаленного репозитория.

7. **Связывание локального и удаленного репозиториев**:
   - Добавьте удаленный репозиторий:
     ```bash
     git remote add origin URL_удаленного_репозитория
     ```
   - Отправьте изменения на GitHub:
     ```bash
     git push -u origin master
     ```

8. **Работа с ветками**:
   - Создайте новую ветку:
     ```bash
     git branch имя_ветки
     ```
   - Переключитесь на ветку:
     ```bash
     git checkout имя_ветки
     ```

9. **Обновление репозитория**:
   - Получите последние изменения с GitHub:
     ```bash
     git pull origin master
     ```

10. **Дополнительные команды**:
    - `git status`: Показывает состояние репозитория.
    - `git log`: Показывает историю коммитов.
    - `git diff`: Показывает различия между файлами.


 GitHub - chadbraunduin/markdown.bash: A Markdown interpreter using only .... https://github.com/chadbraunduin/markdown.bash/.
 markdown - Formatting GitHub commit messages from shell - Stack Overflow. https://stackoverflow.com/questions/29037274/formatting-github-commit-messages-from-shell.
 Highlight Bash, shell code in Markdown Readme.md files. https://www.thecodebuzz.com/highlight-bash-shell-code-in-markdown-readme-md-wiki-files/.
 Getting started with writing and formatting on GitHub. https://docs.github.com/articles/markdown-basics.) https://ru.wikipedia.org/wiki/Markdown.

