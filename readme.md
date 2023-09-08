## В этом файле я опишу все функции терминала для работы с **Git**,
которые уже знаю и изучил в достаточной мере.
---

### Команды терминала

```
$ pwd - активный каталог

$ cd ~ - домашний каталог

$ ls - файлы и папки активного каталога

$ touch имя_файла.расширение - создать файл (touch ../../file.txt)

$ mkdir имя_директории - создать новую папку (-p создать многоуровневый каталог)

$ cp file.txt ~/my_dir - копировать файл из активной папки в выбранную директорию

$ mv file.txt ~/my_dir - переместить файл 

$ cat text.txt - открыть файл (прочитать)

$ rmdir - удалить папку

$ rm - удалить файл

$ rm -r - удалить папку и все файлы в ней

$ clip < ~/text.txt - копирование содержимого файла в буфер обмена
```
-----

### Команды Git

```
$ git init - инициализация отслеживания VCS

$ git status - отслеживание проекта

$ git add file.txt - добавление файла в отслеживаемые 
(--all - добавить все файлы, . - текущую папку)

$ git commit -m 'Описание изменений' - фиксирование изменений (создание точек возврата)

$ git log - вывод изменений проекта

$ git push - передача локальных данных на удаленный сервер (на GitHub)
```
----

### Технические команды **Git**

```
$ ls -a ~/.ssh - проверка на наличие ключей SSH

$ ssh-keygen -t ed25519 -C "почта_аккаунта_с_GitHub" - генерация ключа для GitHub

$ shh -T git@github.com - подключение ключа к аккаунту

$ git remote add origin Ваш_SHH_URL

$ git remote -v - проверка, что подключение прошло успешно
```
----

### Хеш или протокол шифрования SHA-1

С помoщью команды git log можно проследить за изменениями файлов в проекте
```
$ git log
commit 3d11a6d24c6ab0fc88c12ed00d2010703e1a7222 (HEAD -> master, origin/master)
Author: Name <***mail.ru>
Date:   Fri Sep 8 14:46:22 2023 +0300
```
Каждому коммиту присваивается уникальный ID, с помощью алгоритма шифрования SHA-1
это сделано для удобства перехода к разным версиям файлов и отслеживаением измненений проекта

В данном случае хеш выглядит так **3d11a6d24c6ab0fc88c12ed00d2010703e1a7222**

Если в проекте уже сделано множество изменений для удобства их вывода можно использовать команду:

```$ git log --online```

Она выведет не такой подробный список изменений.

---- 

##### HEAD статус

Когда мы используем команду ```$ git log```, то можно увидеть надпись после последнего коммита
```
(HEAD -> master, origin/master)
```
Данная запись является указателем на текующую ветку, которая является указателем на последний коммит.

----

### Статусы файлов

Во время работы с git важно различать статусы файлов, для корректной работы с ними.
С помощью команды ```$ git status``` можно узнать какие файлы есть в проекте и в каком они состоянии

#### Untracked 

Неотслеживаемые git`ом файлы, но находящиеся в папке проекта.

#### Tracked 

Это все файлы, которые были добавлены командой  ```git add```, готовые для коммита

#### Modified

Это измененные файлы, но не готовые к коммиту.

#### Staged

Закоммиченные файлы, готовые к пушу на сервер.

----

Данный репозиторий будет дополняться по мере изучения возможностей **Git**

**Peace :* **