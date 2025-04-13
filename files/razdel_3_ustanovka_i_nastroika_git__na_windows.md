---
title: Установка и настройка Git на Windows
permalink: /files/razdel_3_ustanovka_i_nastroika_git__na_windows/
---

Чтобы работать с Git через приложение Git Bash:

1. Скачайте программу Git по [ссылке git-scm.com/downloads/win](https://git-scm.com/downloads/win).

2. Установите Git по [инструкции](https://tproger.ru/articles/ustanovka-git-na-windows).

Чтобы работать с Git и терминалом Git Bash через приложение VS Code:

1. Скачайте программу VS Code по [ссылке code.visualstudio.com](https://code.visualstudio.com/).

2. Руководствуйтесь [инструкцией](https://ekaterinka17.github.io/mkdocs-example/).


### Настройки Git
Чтобы Git понимал, кто вносит изменения в удаленный репозиторий, необходима настройка на уровне пользователя. Без нее Git работать не будет (см. подраздел [Вопросы и ответы](/primery/files/razdel_8_faq/)).

Настройка имени пользователя может осуществляться как *для всех репозиториев на компьютере*, так и *для одного конкретного репозитория*. 

Выполните глобальную настройку для всех репозиториев на ПК:

1. Откройте терминал Git Bash.
2. Выполните команду `git config --global user.name "<ваше_имя>"`.
3. Выполните команду `git config --global user.email "<адрес_почты@email.com>"`. 
