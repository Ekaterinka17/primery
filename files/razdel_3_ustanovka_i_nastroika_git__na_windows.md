---
title: Установка и настройка Git на Windows (совместно с VS Code)
permalink: /files/razdel_3_ustanovka_i_nastroika_git__na_windows/
---

В рамках настоящей инструкции предполагается работа с Git толька на ОС Windows.

1. Работать с Git будем через приложение Git bash. Скачайте программу Git по [ссылке](https://git-scm.com/downloads/win) и установите
по [инструкции](https://tproger.ru/articles/ustanovka-git-na-windows). Для удобства работы с файлами .md будем запускать терминал Git bash из редактора кода Visual Studio Code (читать инструкцию [Интерфейс VS Code для работы с Git](/primery/files/razdel_8_interfeis_vs_code_dla_raboty_s_git/)).

2. Скачайте программу Visual Studio Code по [ссылке](https://code.visualstudio.com/). Установка стандартная.

### Настройки Git
Чтобы Git понимал, кто вносит изменения в удаленный репозиторий, необходима настройка (на уровне пользователя). Без нее Git работать не будет (см. подраздел [FAQ](/primery/files/razdel_7_faq/)).

Настройка имени пользователя может осуществляться как *для всех репозиториев на компьютере*, так и *для одного конкретного репозитория*. 

Выполните глобальную настройку для всех репозиториев на ПК:

1. Откройте терминал Git bash.
2. Введите команду `git config --global user.name "<ваше_имя>"`.
3. Введите команду `git config --global user.email "<адрес_почты@email.com>"`. 
