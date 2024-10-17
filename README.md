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
- **Master branch** – главная ветка, "золотая" ветка, содержащая эталонный код. Ее также называют origin master.

Для работы с удаленным репозиторием используются сервисы:

* [GitHub](https://github.com/) — используется для работы с различными open-source проектами, для создания портфолио.
* [GitLab](https://about.gitlab.com/) — используется компаниями для хранения приватного контента.
* [Bitbucket](https://bitbucket.org/) — аналог GitLab, специализирующийся на корпоративных пользователях.

Большой разницы между GitHub и GitLab нет, но предположим, что мы хотим работать над одним open-source проектом в открытом доступе. Поэтому для работы с удаленным репозиторием будем использовать GitHub.

## Регистрация на GitHub

### Создание аккаунта на GitHub
1. Переходим по ссылке https://github.com/. 
2. Регистрируем свою учетную запись. В поле для ввода почты вводим адрес своей почты и нажимаем кнопку **Sign up for GitHub**.

![text](/images/registrazia_github.png)

3. В открывшемся окошке снова подтверждаем свою почту с прошлого шага и нажимаем кнопку **Continue**.
4. В открывшемся окошке придумываем пароль.
5. В открывшемся окошке в поле ввода печатаем имя нашего профиля — оно будет использоваться в интерфейсе, в коммитах и комментариях. Так нас будет видеть любой пользователь GitHub, поэтому придумываем что-нибудь приличное и жмем кнопку **Continue**.
6. Дальше GitHub спросит, нужна ли нам рассылка об обновлениях. Устанавливаем ч\б, если да; иначе - жмем кнопку **Continue**.
7. Проверимся на капчу.
8. Получаем письмо с кодом на почту и вводим его на следующей странице.
9. В открывшемся окошке вводим свои учетные данные. Нажимаем кнопку **Sign in**.
10. В открывшемся окошке регистрируем аккаунт для себя, поэтому выбираем "Student". Второй пункт — выбираем "Just me". Дальше GitHub спросит вас об интересах — зачем вы регистрируете аккаунт. Можем выбрать себе пару пунктов, а можем пропустить, нажав кнопку **Continue**.
11. Выбираем бесплатный тариф "Free" (публичные (public) репозитории будут доступны любому желающему, приватные (private) — только нам и еще 3-м соавторам).
12. Профиль на GitHub создан.

### Создание удаленного репозитория на GitHub

1. Для создания репозитория нажимаем кнопку **Create repository**.

![text](/images/create_repository.png)

2. Откроется страница создания репозитория *Create a new repository*.

![text](/images/create_a_new_repository.png)

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

![text](/images/straniza_git_proect.png)

## Установка Git на Windows (совместно с VS Code)
Предполагается единная установка для всех. Описать установку Git c VS Code, показать открытие терминала в VS.

## Настройки Git
Конфигурационные настройки, без которых Git не будет работать.

## Работа с локальным репозиторием
Основные команды от создания локального репозитория до пуша в удаленный репозиторий.

## Работа с удаленным репозиторием
слияние веток, проверка изменений, написание комментариев

## Сценарии работы с Git
Описать частые кейсы по процессу работы в Git

## FAQ
распространенные вопросы по ошибкам, м.б что то еще
