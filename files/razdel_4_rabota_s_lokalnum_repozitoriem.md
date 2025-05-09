---
title: Работа с локальным репозиторием
permalink: /files/razdel_4_rabota_s_lokalnum_repozitoriem/
---

На ПК создается главная папка проекта для работы с локальным репозиторием. Существует два способа создания локального репозитория: *клонирование удаленного репозитория* и *инициализация репозитория с нуля*.

### Клонирование удаленного репозитория

1. Создайте главную папку проекта с помощью команды `mkdir <имя_папки>`, например, **Git_proect**.

2. Перейдите в созданную папку с помощью команды `cd <путь_к_папке>`, например, `cd C:/Users/edurnykh/Git_proect`.

3. Скопируйте ссылку удаленного репозитория на GitHub в меню **Code**→**Local** (см. рис. 3 в подразделе [Создание удаленного репозитория на GitHub](/primery/files/razdel_2_registrazia_na_github/)) с адресом https, например, https://github.com/Ekaterinka17/primery.git.
    
4. Склонируйте удаленный репозиторий на ПК с помощью команды `git clone <ссылка_на_удаленный_репозиторий>`, вставив ссылку из шага 3. 

5. Откройте на ПК папку **Git_proect**, в ней будет находиться вторая склонированная папка **primery**. 

   Вторая папка — это наименование проекта/удаленного репозитория на GitHub, т.к. в ней находится Git-репозиторий **.git**. 

6. Перейдите в папку **primery** с помощью команды `cd <имя_папки>`.

   Наименование папки будет соответствовать наименованию удаленного репозитория.

### Инициализация репозитория с нуля

1. Перейдите в главную папку проекта с помощью команды `cd <путь_к_папке>`, например, `cd C:/Users/edurnykh/Git_proect`.
    
2. Создайте папку локального репозитория проекта с помощью команды `mkdir <имя_папки>`, например, `mkdir test`. 
    
3. Перейдите в папку локального репозитория с помощью команды `cd <имя_папки>`.
    
4. Создайте репозиторий в папке с помощью команды `git init .`. Создастся подпапка **.git**. 

5. Перейдите в папку **test** и создайте вручую файл README.md.
    
6. Добавьте файл проекта в индекс с помощью команды `git add README.md`.
    
7. Создайте коммит с помощью команды `git commit -m "первый коммит"`.

8. Переименуйте ветку в *main* с помощью команды `git branch -M main`.

Для связки локального Git-репозитория, например, папка **test**, с удаленным репозиторием на GitHub:

1. Перейдите на GitHub и выполните действия, описанные в подразделе [Создание удаленного репозитория на GitHub](/primery/files/razdel_2_registrazia_na_github/). 

2. Заполните поле **Repository name** имененем локального репозитория, например, **test**, чтобы в будущем избежать путаницы при сопоставлении локальных и удаленных репозиториев.

3. Скопируйте ссылку удаленного репозитория из проекта на GitHub в меню **Code**→**Local** (см. рис. 3 в подразделе [Создание удаленного репозитория на GitHub](/primery/files/razdel_2_registrazia_na_github/)) с адресом https, например, https://github.com/Ekaterinka17/test.git.
    
4. Свяжите локальный репозиторий с удаленным репозиторием с помощью команды `git remote add origin <ссылка_на_удаленный_репозиторий>`, вставив ссылку из шага 3. 
    
5. Отправьте изменения в удаленный репозиторий с помощью команды `git push -u origin main`.

### Команды Git для работы в терминале

Список команд в Git обширен, его можно подробно изучить на просторах интернета. Ниже представлены часто используемые в работе команды:

1. `cd <путь_к_папке>` — переходит в папку по указанному пути **C:/..**.

2. `cd <имя_папки>` — переходит в папку.

3. `mkdir <имя_папки>` — создает новую папку.

1. `git init .` — создает новый репозиторий.

2. `git log` — отображает список существующих коммитов.

3. `git status` — отображает список измененных, добавленных и удаленных файлов.

4. `git branch` — отображает существующие локальные и текущие ветки, с параметром `<-а>` — все ветки.

5. `git branch <vetka>` — создает новую ветку с именем *vetka*.

6. `git checkout <vetka>` — переходит в ветку с именем *vetka*.

7. `git checkout -b <vetka>` — создает и переходит одновременно на ветку с именем *vetka*.

8. `git branch -d <vetka>` — удаляет ветку с именем *vetka*.

9. `git add .` – добавляет указанные файлы в индекс.

10. `git reset` — отменяет действие команды `git add .` на файл.

11. `git commit -m "<сообщение>"` — фиксирует добавленные в индекс изменения с определенным сообщением.

12. `git push -u origin <vetka>` — отправляет изменения в удаленный репозиторий.

13. `git fetch` — отражает информацию о новых ветках.

14. `git pull` — загружает содержимое из удаленного репозитория и обновляет локальный репозиторий этим содержимым.
