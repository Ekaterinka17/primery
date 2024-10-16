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

### Создание аккаунта
1. Переходим по ссылке https://github.com/. 
2. Регистрируем свою учетную запись. В поле для ввода почты вводим адрес своей почты и нажимаем на кнопку **Sign up for GitHub**.

![text](/images/registrazia_github.png)

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
