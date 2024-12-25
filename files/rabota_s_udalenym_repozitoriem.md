---
title: Работа с удаленным репозиторием
permalink: /files/rabota_s_udalenym_repozitoriem/
---

В рамках проекта все участники процесса клонируют один проект с главной веткой *main*. Однако каждый работает в своей *n-ветке*, созданной отдельно от ветки *main*. После отправки изменений в удаленный репозиторий (команда `git push -u origin <vetka>`) принято подтягивать содержимое *n-ветки* в ветку *main* (см. подраздел [Запрос на принятие изменений (pull request)](#zapros_na_prinyatie_izmenenij_pull_request)), а затем сливать данные изменения (см. подраздел [Запрос на слияние веток (merge pull request)](#zapros_na_sliyanie_vetok_merge_pull_request)). 

Исполнитель по задаче создает **pull request**, а лид — сливает изменения **merge pull request**, проверяя также отсутствие всевозможных конфликтов (см. подразде [Конфликты при слиянии веток](#konflikty_pri_sliyanii_vetok)).

<h3 id="zapros_na_prinyatie_izmenenij_pull_request">Запрос на принятие изменений (pull request)</h3>

Существует два способа запроса на принятие изменений из *n-ветки* в *main*.

**Первый способ**: с помощью желтого уведомления от GitHub.

![текст](images/pull_rekvest.png) 

1. Нажимите кнопку **Compare & pull request**.


   Откроется страница **Open a pull request**.  
   
2. Заполните поле **Add a title** и **Add a description**, нажмите кнопку **Create pull request**.

   ![текст](images/create_pull_request.png) 

**Второй способ**: 

1. Откройте раздел **Pull requests** в панеле навигации на GitHub.
2. Нажмите кнопку **New pull request**.
3. Выберите в поле **base** — *main*, **compare** — ветку, которую хотите мерджить.

    ![текст](images/pull_request.png) 

4. Нажмите кнопку **Create pull request**.

<h3 id="zapros_na_sliyanie_vetok_merge_pull_request">Запрос на слияние веток (merge pull request)</h3>

1. Перейдите в раздел **Pull requests**.
2. Выберите из списка нужный **pull request**.
  
   Откроется cтраница слияния веток. 

   ![текст](images/merge_git.png)

3. Проверьте отсутствие конфликтов (см. подраздел [Конфликты при слиянии веток](#konflikty_pri_sliyanii_vetok)). Если конфликтов нет, нажмите кнопку **Merge pull request**.
4. Подтвердите слияние веток с помощью кнопки **Confirm merdge**.

   Откроется страница с уведомлением о слиянии веток. При необходимости можно заполнить блок с комментарием в нижней части страницы и нажать кнопку **Comment**.

   ![текст](images/create_comment.png)

<h3 id="konflikty_pri_sliyanii_vetok">Конфликты при слиянии веток</h3>
