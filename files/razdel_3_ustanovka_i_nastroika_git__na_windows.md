---
title: Установка и настройка Git на Windows (совместно с VS Code)
permalink: /files/razdel_3_ustanovka_i_nastroika_git__na_windows/
---

Чтобы работать с Git через приложение Git bash:

1. Скачайте программу Git по [ссылке](https://git-scm.com/downloads/win).

2. Установите Git по [инструкции](https://tproger.ru/articles/ustanovka-git-na-windows).

Чтобы работать с Git и терминалом Git bash через приложение VS Code:

1. Скачайте программу VS Code по [ссылке](https://code.visualstudio.com/). Установка стандартная.

2. Руководствуйтесь инструкцией [Интерфейс VS Code для работы с Git](https://ekaterinka17.github.io/mkdocs-example/).


### Настройки Git
Чтобы Git понимал, кто вносит изменения в удаленный репозиторий, необходима настройка (на уровне пользователя). Без нее Git работать не будет (см. подраздел [FAQ](/primery/files/razdel_8_faq/)).

Настройка имени пользователя может осуществляться как *для всех репозиториев на компьютере*, так и *для одного конкретного репозитория*. 

Выполните глобальную настройку для всех репозиториев на ПК:

1. Откройте терминал Git bash.
2. Введите команду `git config --global user.name "<ваше_имя>"`.
3. Введите команду `git config --global user.email "<адрес_почты@email.com>"`. 
