# git
Git


**Основы git**

**Системы контроля версий (СКВ, VCS, Version Control Systems)** позволяют разработчикам сохранять все изменения, внесенные в код. СКВ также позволяют нескольким разработчикам работать над одним проектом и сохранять внесенные изменения независимо друг от друга.

**Git** — это инструмент, позволяющий реализовать распределенную систему контроля версий.

С помощью git можно откатить свой проект до более старой версии, сравнивать, анализировать или сливать свои изменения в репозиторий.

**Репозиторием** называют хранилище кода и историю его изменений. Git работает локально и все ваши репозитории хранятся в определенных папках на жестком диске.

**Коммиты** - Каждая точка сохранения называется коммит (commit). У каждого commit есть hash (уникальный id) и комментарий. Из таких commit-ов собирается ветка. Ветка — это история изменений. У каждой ветки есть свое название.

**Ветвления** - Ветки имеют свою собственную историю и изолированные друг от друга изменения до тех пор, пока вы не решаете слить изменения вместе.

**Установка и настройка репозитория**

Установка git из репозитория:
```
sudo apt-get install git
```
Настройка git для корректного отображения автора коммитов:
```
git config --global user.name "My Name"
git config --global user.email myEmail@example.com
```
Инициализация репозитория:
```
git init
```
Просмотр текущего статуса:
```
git status
```
**Работа с git**

Чтобы добавить файлы для отслеживания используется команда:
```
git add имя_файла
```
После этого изменения файла начнут отслеживаться и его можно закоммитить:
```
git commit -m "some useful comment here"
```
Перед каждым коммитом необходимо проиндексировать файлы, которые будут закоммичены. Это можно сделать с помощью:
```
git add
```
либо добавив ключ:
```
git commit -a
```
Последний коммит в ветке обозначается как HEAD. Это сделано для упрощенного доступа к нему.

**Работа с git: отмена изменений**

До выполнения индексации:
```
git checkout имя файла
```
После индексации:
```
git reset HEAD имя файла
```
Откат изменений коммита осуществляется с помощью revert:
```
git revert HEAD --no-edit
```
Вместо HEAD можно указать любой id коммита из истории. Просмотр истории:
```
git log
```
**Работа с ветками**

Создание веток:
```
git checkout -b имя_ветки
git checkout master
```
Слияние веток:
```
git merge develop
```
**Клонирование репозитория**

Клонировать репозиторий с сервера можно с помощью команды:
```
git clone https://github.com/netology-code/sysadm-homeworks.git
```
Репозиторий будет помещен в директорию ./имя_репозитория 

Просмотр удаленных репозиториев:
```
git remote
```
В ответ мы увидим имена всех существующих удаленных репозиториев (по умолчанию обычно origin):
```
git remote show origin
```
**Добавление удаленного репозитория**
Добавление удаленного репозитория:
```
git remote add origin https://github.com/netology-code/sysadm-homeworks.git
```
Отправка изменения в удаленный репозиторий:
```
git push origin master
```
Для того чтобы скачать себе последние изменения из репозитория:
```
git pull
```
**.gitignore** - В любой директории внутри репозитория можно создать файл .gitignore В него можно добавить правила игнорирования некоторых файлов. Например, локальный кеш, тестовые конфигурации и прочее.

**Github** — сервис онлайн-хостинга репозиториев, обладающий всеми функциями всего, что поддерживает Git и даже больше. Также GitHub может похвастаться контролем доступа, багтрекингом, управлением задачами и вики для каждого проекта. Кроме GitHub есть другие сервисы, которые используют Git, — например, Bitbucket и GitLab. Вы можете разместить Git- репозиторий на любом из них.






