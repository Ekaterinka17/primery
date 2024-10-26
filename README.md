# Руководство по Git

## Что такое Git?
Git – это инструмент, который позволяет сразу нескольким людям сохранять и отслеживать изменения в файлах проекта. С помощью данного инструмента технический писатель может анализировать и откатывать изменения в файлах .md, либо сливать свои доработки в репозиторий.

Git относится к распределенным системам контроля версий, который имеет репозиторий не только на сервере, но и локально на компьютерах. 

Для понимания важных терминов в настоящей инструкции дадим им трактовку:

- **Репозиторий** представляет собой хранилище данных, в котором находятся файлы конфигурации репозитория, файлы журналов, хранящие операции, выполняемые над репозиторием, индекс, описывающий расположение файлов, и хранилище этих файлов.
- **Локальный репозиторий** — это хранилице данных, расположенное в папках на компьютере.
- **Удаленный репозиторий (сервер)** — это хранилище данных, расположенное в интернете.
- **Коммит (commit)** — зафиксированное состояние проекта в определенный момент времени (контрольная точка, снимок) или конкретная версия репозитория.
- **Индекс** — пространство, в котором живут изменения перед становлением коммитом.
- **Ветка** — альтернативная реальность кода, история которого начинается от конкретного коммита.
- **Main** – главная ветка, "золотая" ветка, содержащая эталонный код. Ее также называют origin main.
- **Мердж** — слияние (объединение) истории двух веток.

Для работы с удаленным репозиторием используются сервисы:

* [GitHub](https://github.com/) — для работы с различными open-source проектами или создания портфолио.
* [GitLab](https://about.gitlab.com/) — для хранения приватного контента.
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
6. Дальше GitHub спросит, нужна ли нам рассылка об обновлениях. Устанавливаем чекбокс, если да; иначе - жмем кнопку **Continue**.
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
   - последние три поля предлагают нам добавить *README файл*, *.gitignore файл* и выбрать *лицензию* для нашего проекта. Ставим только чекбокс напротив *README файла*, с которым будем работать.

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

Описание команд, выполняемых в терминале *Git Bash*, для работы с локальным репозиторием см. в подразделе **Команды Git для работы в терминале**. В настоящем подразделе (ниже) показаны альтернативные команды, которые можно выполнять с помощью функционала VS Code.

Для работы с ветками в VS Code предусмотрена панель в левом нижнем углу приложения. В зеленой рамке со стрелочками отображается значок синхронизации. При нажатии на значок и подтверждении операции загружаются изменения из одноименной ветки удаленного репозитория (аналог команды `git pull` в терминале Git Bash).

<p align="center">
  <img src="/images/vetka_git.png" />
</p>

В зеленой рамке с текстом *test_primery1* отображается наименование ветки, в которой работает технический писатель в настоящий момент, находясь в локальном репозитории. 

При нажатии на данное наименование в строке поиска отобразятся команды для создания новой ветки (1) и команды для перехода к другой существующей ветке (2).

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

Настройка имени пользователя может осуществляться как *для всех репозиториев на компьютере*, так и *для одного конкретного репозитория*. Выполним глобальную настройку для всех репозиториев на ПК.

Для этого:

1. Открываем терминал Git bash.
2. Вводим команду `git config --global user.name "<ваше_имя>"`. Нажимаем **Enter**.
3. Вводим команду `git config --global user.email "<адрес_почты@email.com>"`. Нажимаем **Enter**.

## Работа с локальным репозиторием
Для работы с локальным репозиторием на ПК должна быть создана соответствующая папка. Существует два способа создания локального репозитория: *клонирование удаленного репозитория* и *инициализация репозитория с нуля*.

### Клонирование удаленного репозитория

Для клонирования удаленного репозитория создадим главную папку проекта, чтобы знать, где все хранится. В моем случае это папка **Git_proect**.

Далее выполним последовательно команды через терминал Git Bash:

- `cd <путь_к_папке>` — переход в папку по указанному пути **C:/..** (у каждого он свой, например, у меня это `cd C:/Users/edurnykh/Git_proect`), слэши обязательно с наклоном вправо.
- `git clone <ссылка_на_удаленный_репозиторий>` — происходит клонирование удаленного репозитория на ПК. Ссылку берем на GitHub в меню **Code**→**Local** (см. рис. 4 настоящей инструкции) с адресом https, например, https://github.com/Ekaterinka17/primery.git.

Откроем на ПК папку **Git_proect** и увидим в ней вторую склонированную папку **primery**. Вторая папка — это наименование проекта/удаленного репозитория на GitHub, т.к. в ней находится Git-репозиторий **.git**. Перейдем в папку **primery** с помощью команды:

- `cd <имя_папки>` — у каждого она своя, например, у меня это `cd primery`.

Теперь можно работать с проектом, добавлять и изменять файлы.

### Инициализация репозитория с нуля

Для инициализации репозитория с нуля превратим обычную папку в Git-репозиторий. 

Выполним последовательно команды через терминал Git Bash:
- `cd <путь_к_папке>` — переход в папку по указанному пути **C:/..** (у каждого он свой, например, у меня это `cd C:/Users/edurnykh/test_git`), слэши обязательно с наклоном вправо.
- `mkdir <имя_папки>` — создает новую папку (например, у меня `mkdir test`).
- `cd <имя_папки>` — переходим в папку (например, у меня это `cd test`).
- `git init .` — создает репозиторий в папке, откуда она была вызвана (например, у меня создается репозиторий **.git** в папке **test**). Переходим в папку **test** и создаем вручую файл README.md.
- `git add README.md` — добавляем файл проекта в индекс.
- `git commit -m "первый коммит"` — создаем первый комментарий.
- `git branch -M main`  — переименовываем ветку в *main*.

Если папка уже существует и нужно ее сделать Git-репозиторием, выполняем те же действия, зайдя в нужную папку. Через терминал переходим в нее с помощью команды `cd <имя_папки>` и инициализируем репозиторий с помощью команды `git init .`.

Далее связываем наш локальный Git-репозиторий (папка **test**) с удаленным репозиторием на GitHub. Для этого переходим на GitHub и выполняем действия, описанные в подразделе **Создание удаленного репозитория на GitHub** настоящей инструкции. Поле **Repository name** можно заполнять любым наименованием, но автор рекомендует использовать имя локального репозитория — **test**, чтобы в будущем избежать путаницы при сопоставлении локальных и удаленных репозиториев.

Выполним последовательно команды через терминал Git Bash:
- `git remote add origin <ссылка_на_удаленный_репозиторий>` — связывает локальный репозиторий с удаленным репозиторием. Ссылку удаленного репозитория берем в проекте **test** на GitHub, см. меню **Code**→**Local**, например, https://github.com/Ekaterinka17/test.git.
- `git push -u origin main` — отправляем изменения в удаленный репозиторий.


### Команды Git для работы в терминале

Список команд в Git обширен, его можно подробно изучить на просторах интернета. Здесь представлены самые распространенные и часто используемые в работе команды:

1. `git init .` — создает новый репозиторий.

2. `git log` — отображает список существующих коммитов.

3. `git status` — отображает список измененных, добавленных и удаленных файлов.

4. `git branch` — отображает существующие локальные и текущие ветки (с параметром `<-а>` — вообще все).

5. `git branch <vetka>` — создает новую ветку с имененем *vetka*.

6. `git checkout <vetka>` — переходит в ветку с имененем *vetka*.

7. `git checkout -b <vetka>` — создает и переходит (одновременно) на ветку с имененем *vetka*.

8. `git branch -d <vetka>` — удаляет ветку с имененем *vetka*.

9. `git add .` – добавляет указанные файлы в индекс (обязательно перед последующим коммитом).

10. `git reset` — отменяет действие команды `git add .` на файл.

11. `git commit -m "<сообщение>"` — фиксирует добавленные в индекс изменения с определенным сообщением.

12. `git push -u origin <vetka>` — отправляет изменения в удаленный репозиторий.

13. `git fetch` — отражает информацию о новых ветках.

14. `git pull` — загружает содержимое из удаленного репозитория и обновляет локальный репозиторий этим содержимым.


## Работа с удаленным репозиторием

В рамках проекта все участники процесса клонируют один проект с главной веткой *main*. Однако каждый работает в своей *n-ветке*, созданной отдельно от ветки *main*. После отправки изменений в удаленный репозиторий (команда `git push`) принято подтягивать содержимое *n-ветки* в ветку *main* (см. подраздел **Запрос на принятие изменений (pull request)**), а затем сливать данные изменения (см. подраздел **запрос на слияние веток (merge pull request)**). 

Иполнитель по задаче создает **pull request**, а лид — сливает изменения **merge pull request**, проверяя также отсутствие всевозможных конфликтов (см. подраздел **Конфликты при слиянии веток**).

### Запрос на принятие изменений (pull request)

Существует два способа запроса на принятие изменений из *n-ветки* в *main*.

**Первый способ**: с помощью желтого уведомления от GitHub.

<p align="center">
  <img src="/images/pull_rekvest.png" />
</p>

1. Нажимаем кнопку **Compare & pull request**.
2. Откроется страница **Open a pull request**.  Заполняем поле **Add a title** и **Add a description**, нажимаем кнопку **Create pull request**.

<p align="center">
  <img src="/images/create_pull_request.png" />
</p>

3. **Pull request** создан.

**Второй способ**: 

1. Открываем раздел **Pull requests** в панеле навигации на Github.
2. Нажимаем кнопку **New pull request**.
3. Выбираем в поле **base** — *main*, **compare** — ветку, которую хотите мерджить.

<p align="center">
  <img src="/images/pull_request.png" />
</p>

4. Нажимаем кнопку **Create pull request**.

### Запрос на слияние веток (merge pull request)

1. Заходим в раздел **Pull requests**.
2. Выбираем из списка нужный **pull request**.
3. Откроется cтраница слияния веток. 

<p align="center">
  <img src="/images/merge_git.png" />
</p>

4. Проверяем отсутствие конфликтов (см. подраздел **Конфликты при слиянии веток**). Если конфликтов нет, нажимаем кнопку **Merge pull request**.
5. Подтверждаем слияние веток с помощью кнопки **Confirm merdge**.
6. Откроется страница с уведомлением о слиянии веток. При необходимости можно заполнить блок с комментарием в нижней части страницы и нажать кнопку **Comment**.

<p align="center">
  <img src="/images/create_comment.png" />
</p>

### Конфликты при слиянии веток


## Сценарии работы с Git

### Добавление новой инструкции в удаленный репозиторий

1. Клонируем репозиторий с помощью команды `git clone` (все необходимые действия см. в подразделе **Клонирование удаленного репозитория**).
2. Переходим в папку с репозиторием с помощью команды `cd <имя_папки>`.
3. Проверяем статус репозитория с помощью команды `git status`.
4. Создаем ветку для работы над инструкцией с помощью команды `git checkout -b <название_ветки>`. Корректность наименования веток обсуждается с отделом, исходя иp общих правил.
5. Создаем .md файл в папке с репозиторием из шага 2.
6. Пишем инструкцию и сохраняем файл.
7. Повторно проверяем статус репозитория с помощью команды `git status`.
8. Добавляем изменения в индекс с помощью команды `git add .`.
9. Поверяем добавление изменений в индекс с помощью команды `git status`.
10. Коммитим изменения из индекса с помощью команды `git commit -m "первый коммит"`. Корректность наименования коммитов обсуждается с отделом, исходя иp общих правил.
11. Публикуем локальную ветку с изменениями в удаленный репозиторий с помощью команды `git push -u origin <название_ветки>`. Название ветки должно совпадать с названием из шага 4.

### Правка инструкции по другому проекту в новой ветке

1. Переходим в папку, где лежит репозиторий по другому проекту с помощью команды `cd <путь_к_папке>`.
2. Переходим в папку с репозиторием с помощью команды `cd <имя_папки>`.
3. Подтягиваем изменения с удаленного репозитория с помощью команды `git pull`.
4. Проверяем статус репозитория с помощью команды `git status`.
5. Создаем ветку для работы над инструкцией с помощью команды `git checkout -b <название_ветки>`. Корректность наименования веток обсуждается с отделом, исходя из общих правил.
6. Открываем и вносим правки в .md файл с инструкцией.
7. Добавляем изменения в индекс с помощью команды `git add .`.
8. Поверяем добавление изменений в индекс с помощью команды `git status`.
9. Коммитим изменения из индекса с помощью команды `git commit -m "правки по задаче CR-1012"`. Корректность наименования коммитов обсуждается с отделом, исходя из общих правил.
10. Публикуем локальную ветку с изменениями в удаленный репозиторий с помощью команды `git push -u origin <название_ветки>`. Название ветки должно совпадать с названием из шага 5.

### Правка инструкции с коллегой в одной ветке

1. Переходим в папку с репозиторием с помощью команды `cd <имя_папки>`.
2. Переходим в рабочую ветку задачи с помощью команды `git checkout <название_ветки>`.
3. Подтягиваем изменения с удаленного репозитория с помощью команды `git pull`.
4. Проверяем статус репозитория с помощью команды `git status`.
5. Открываем и вносим правки в .md файл с инструкцией.
6. Добавляем изменения в индекс с помощью команды `git add .`.
7. Поверяем добавление изменений в индекс с помощью команды `git status`.
8. Коммитим изменения из индекса с помощью команды `git commit -m "правки по задаче CR-1012"`. Корректность наименования коммитов обсуждается с отделом, исходя из общих правил.
9. Подтягиваем новые изменения из удаленной ветки с помощью команды `git pull`, т.к. знаем, что параллельно в этой ветке работает коллега.
10. Публикуем локальную ветку с изменениями в удаленный репозиторий с помощью команды `git push -u origin <название_ветки>`. Название ветки должно совпадать с названием из шага 2.

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

### Действие, которое может сломать главную ветку (или иную) необратимо

Если случайно сделать только команду `git push -f`, то можно испортить свою главную ветку. 