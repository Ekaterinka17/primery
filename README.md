# Руководство по Git

## Что такое Git?
Git – это инструмент, который позволяет сразу нескольким людям сохранять и отслеживать изменения в файлах проекта. С помощью данного инструмента техический писатель может анализировать и откатывать изменения в файлах .md, либо сливать свои доработки в репозиторий.

Git относится к распределенным системам контроля версий, который имеет репозиторий не только на сервере, но и локально на компьютерах. 

Для понимания важных терминов в настоящей инструкции дадим им трактовку:

- **Репозиторий** представляет собой хранилище данных, в котором находятся файлы конфигурации репозитория, файлы журналов, хранящие операции, выполняемые над репозиторием, индекс, описывающий расположение файлов, и хранилище этих файлов.
- **Локальный репозиторий** — это хранилице данных, расположенное в папках на компьютере.
- **Удаленный репозиторий (сервер)** — это хранилище данных, расположенное в интернете.
- **Коммит (commit)** — зафиксированное состояние проекта в определенный момент времени (контрольная точка, снимок) или конкретная версия репозитория.
- **Ветка** — альтернативная реальность кода, история которого начинается от конкретного коммита.
- **Main** – главная ветка, "золотая" ветка, содержащая эталонный код. Ее также называют origin main.

Для работы с удаленным репозиторием используются сервисы:

* [GitHub](https://github.com/) — используется для работы с различными open-source проектами, для создания портфолио.
* [GitLab](https://about.gitlab.com/) — используется компаниями для хранения приватного контента.
* [Bitbucket](https://bitbucket.org/) — аналог GitLab, специализирующийся на корпоративных пользователях.

Большой разницы между GitHub и GitLab нет, но предположим, что мы хотим работать над одним open-source проектом в открытом доступе. Поэтому для работы с удаленным репозиторием будем использовать GitHub.

## Регистрация на GitHub

### Создание аккаунта на GitHub
1. Переходим по [ссылке](https://github.com/). 
2. Регистрируем свою учетную запись. В поле для ввода почты вводим адрес своей почты и нажимаем кнопку **Sign up for GitHub**.

<p align="center">
  <img src="/images/registrazia_github.png" />
</p>


3. В открывшемся окошке снова подтверждаем свою почту с прошлого шага и нажимаем кнопку **Continue**.
4. В открывшемся окошке придумываем пароль.
5. В открывшемся окошке в поле ввода печатаем имя нашего профиля — оно будет использоваться в интерфейсе, в коммитах и комментариях. Так нас будет видеть любой пользователь GitHub, поэтому придумываем что-нибудь приличное и жмем кнопку **Continue**.
6. Дальше GitHub спросит, нужна ли нам рассылка об обновлениях. Устанавливаем ч\б, если да; иначе - жмем кнопку **Continue**.
7. Проверимся на капчу.
8. Получаем письмо с кодом на почту и вводим его на следующей странице.
9. В открывшемся окошке вводим свои учетные данные. Нажимаем кнопку **Sign in**.
10. В открывшемся окошке регистрируем аккаунт для себя, поэтому выбираем *Student*. Второй пункт — выбираем *Just me*. Дальше GitHub спросит вас об интересах — зачем вы регистрируете аккаунт. Можем выбрать себе пару пунктов, а можем пропустить, нажав кнопку **Continue**.
11. Выбираем бесплатный тариф *Free* (публичные (public) репозитории будут доступны любому желающему, приватные (private) — только нам и еще 3-м соавторам).
12. Профиль на GitHub создан.

### Создание удаленного репозитория на GitHub

1. Для создания репозитория нажимаем кнопку **Create repository**.

<p align="center">
  <img src="/images/create_repository.png" />
</p>

2. Откроется страница создания репозитория *Create a new repository*.

<p align="center">
  <img src="/images/create_a_new_repository.png" />
</p>

3. На странице отображаются:
   - Поля:
     - **Owner** - владелец, заполняется автоматически.
     - **Repository name** – имя репозитория, которое будет отображаться на странице аккаунта. 
     - **Description** – описание репозитория, заполнять необязательно.
   - Радиобаттоны:
     - **Public** - открытый тип репозитория, доступный всем пользователям GitHub.
     - **Private** - закрытый тип репозитория, доступный только вам и людям, которым вы предоставите доступ.
   - последние три поля предлагают нам добавить *README файл*, *.gitignore файл* и выбрать *лицензию* для нашего проекта. Ставим только ч\б напротив *README файла*, с которым будем работать.

4. Жмем кнопку **Create repository**.
5. Откроется страница созданного репозитория.

<p align="center">
  <img src="/images/straniza_git_proect.png" />
</p>

## Установка Git на Windows (совместно с VS Code)
В рамках настоящей инструкции предполагается работа с Git толька на ОС Windows.

1. Работать с Git будем через приложение Git bash. Скачиваем программу Git по [ссылке](https://git-scm.com/downloads/win) и установливаем
по [инструкции](https://tproger.ru/articles/ustanovka-git-na-windows). Для удобства работы с файлами .md будем запускать терминал Git bash из редактора кода Visual Studio Code.

1. Скачиваем программу Visual Studio Code по [ссылке](https://code.visualstudio.com/). Установка стандартная, запускаем установщик.

### Интерфейс VS Code для работы с Git
Для работы с локальным репозиторием можно использовать родную командную оболочку Windows — PowerShell или установленную — Git Bash. Однако работать проще, если видишь весь проект целиком. Поэтому в рамках настоящей инструкции рассмотрим работу с Git в приложении VS Code.

Так или иначе, нам понадобится терминал. Откроем его в VS Code c помощью верхнего меню **Terminal**→**New Terminal**.

По умолчанию открывается терминал *PowerShell*. Переключимся на терминал *Git Bash* во избежание проблем распознавания синтаксиса команд. Для этого нажимаем на значок стрелочки, показанный на рисунке ниже, и выбираем пункт **Git Bash**.

<p align="center">
  <img src="/images/terminal_bash.png" />
</p>

Терминал *Git Bash* открыт.

<p align="center">
  <img src="/images/terminal_git_bash.png" />
</p>

Описание команд, выполняемых в терминале *Git Bash*, для работы с локальным репозиторием см. в подразделе **Работа с локальным репозиторием**. В настоящем подразделе (ниже) показаны альтернативные команды, которые можно выполнять с помощью функционала VS Code.

Для работы с ветками в VS Code предусмотрена панель в левом нижнем углу приложения. В зеленой рамке со стрелочками отображается значок синхронизации. При нажатии на значок и подтверждении операции загружаются изменения из одноименной ветки удаленного репозитория (аналог команды `git pull` в терминале Git Bash).

<p align="center">
  <img src="/images/vetka_git.png" />
</p>

В зеленой рамке с текстом *test_primery1* отображается наименование ветки, в которой работает технический писатель в настоящий момент, находясь в локальном репозитории. При нажатии на данное наименование в строке поиска отобразятся команды для создания новой ветки (1) и перехода к другой существующей ветке (2).

<p align="center">
  <img src="/images/reserch_vetki.png" />
</p>

Для создания новой ветки от текущей локальной ветки выбираем команду *Create new branch* и вводим наименование ветки, но для создания ветки не от текущей — выбираем команду *Create new branch from* и вводим наименование ветки (аналог команды `git checkout -b <имя ветки>`). 

Для перехода к другой существующей ветке выбираем нужную из списка на рисунке выше (аналог команды `git checkout <имя ветки>`). 

Для работы с индексом и коммитами в VS Code предусмотрен раздел **Source Control** (1), после открытия которого отображаются вкладки *Source Control* (2) и *Source Control Graph* (3).

<p align="center">
  <img src="/images/commit_vs.png" />
</p>

На вкладке *Source Control* отображаются файлы с изменениями, которые можно добавить в индекс и закоммитить. Для этого заполняем поле коментарием (1) и нажимаем кнопку **Commit** (2) (описанные действия аналоги комманд `git add .` и `git commit -m "коммит"` в терминале Git Bash).

<p align="center">
  <img src="/images/commit_git.png" />
</p>

После создания коммита на вкладке отобразится кнопка **Sync Changes**, предназначенная для отправки файлов в удаленный репозиторий (аналог команды `git push` в терминале Git Bash).

На вкладке *Source Control Graph* можно отслеживать на каком коммите находится удаленная и локальная ветки.
- Синее выделение показывает коммит в локальном репозитории.
- Фиолетовое выделение показывает коммит в удаленном репозитории.
- Оранжевое выделение показывает главную ветку, старт создания проекта. Или выделяет главную ветку "не main", если относительно нее были созданы новые ветки. 

<p align="center">
  <img src="/images/graf_source.png" />
</p> 

С помощью данного графа можно отслеживать и просматривать изменения в файлах. Для этого выбираем нужный коммит в графе, после чего открывается файл с изменениями. К примеру в коммите "обновление РП2" красным выделены удаленные элементы в файле, а зеленым - добавленные.

<p align="center">
  <img src="/images/izmenenia_commit.png" />
</p>

### Настройки Git
Чтобы Git понимал, кто вносит изменения в удаленный репозиторий, необходима настройка (на уровне пользователя). Без нее Git работать не будет (см. подраздел **FAQ**).

Настройка имени пользователя может осуществляться как *для всех репозиториев на компьютере*, так и *для одного конкретного репозитория*. Выполним глобальную настройку для всех репозиториев на компьютере.

Для этого:

1. Открываем терминал Git bash.
2. Вводим команду `git config --global user.name "<ваше_имя>"`. Нажимаем **Enter**.
3. Вводим команду `git config --global user.email "<адрес_почты@email.com>"`. Нажимаем **Enter**.

## Работа с локальным репозиторием
Основные команды от создания локального репозитория до пуша в удаленный репозиторий.

## Работа с удаленным репозиторием
слияние веток, проверка изменений, написание комментариев

## Сценарии работы с Git
Описать частые кейсы по процессу работы в Git

## FAQ

### Ошибка директории

После перехода в локальный репозиторий `cd C:/Users/edurnykh/Git_proect` выполнил команду `git status`, `git log`, в консоли отобразилась ошибка:
   
```fatal: not a git repository (or any on the parent directories): .git```

<u>Решение</u>: вернуться в папку репозитория командой `cd programm` (папка *programm* лежит в папке *Git_proect*).

### Не задано имя пользователя

Выполнил команду `git commit -m "первый коммит"`, в консоли отобразилось сообщение с ошибкой (пример):
   
```
Commit failed - exit code 128 received, with output: '*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'User@DESKTOP-CA2F2PA.(none)')'

```

<u>Решение</u>: настроить имя пользователя и email (см. подраздел **Настройки Git**).