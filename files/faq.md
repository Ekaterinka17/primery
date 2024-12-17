---
title: FAQ?
permalink: /files/faq/
---

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

### Действия, которые могут сломать главную ветку (или иную) необратимо

Если случайно сделать только команду `git push -f`, то можно испортить свою главную ветку. 
