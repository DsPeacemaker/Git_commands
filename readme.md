## В этом файле я опишу все функции терминала для работы с **Git**, которые уже знаю и изучил в достаточной мере.

![Логотип Git](https://www.20i.com/blog/wp-content/uploads/2022/08/git-blog-header.png "Логотип Git")
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
$ git init - инициализация репозитория (Сделать текущую директорию новым репозиторием)

$ git init <name>  - Создать репозиторий в текущей директории с именем <name>

$ git status 

$ git status -s  - Статус в короткой форме

$ git <command> --help  - Откроет информацию по запрашиваемой команде

$ git add file.txt - добавление файла в отслеживаемые 
(--all - добавить все файлы, . - добавить все в текущей директории)

$ git restore <file> - убирает последние изменения файла (убирает файл из статуса modified)
вернуть файл к последней версии, которая была сохранена через git commit или git add

$ git restore <path> - Отменить изменения в указанном месте

$ git commit -m 'Описание изменений' - фиксирование изменений (создание точек возврата)

$ git commit --amend --no-edit - добавь изменения к последнему коммиту без изменения сообщения коммита
--amend работает с последним коммитом HEAD

$ git commit --amend -m "Описание изменений" - исправить коммит с новым описанием

$ git revert <commit>  - Отменить коммит

$ git log - вывод изменений проекта

$ git log <branch-name>  - Посмотреть логи по конкретной ветке

$ git push -u origin main - первая загрузка всех коммитов из локального репозитория в удаленный (origin)
 Ваша ветка может называться master, а не main. Подправьте команду, если это необходимо.

$ git push - передача локальных данных на удаленный сервер (на GitHub)

$ git reset --hard <commit hash> - выбранный коммит станет HEAD и вся разработка пойдет от него

$ git diff - сравнивает последнюю закомиченнубю версию с текущей (измененной версией)

$ git diff --staged - посмотреть изменения в staged файлах

$ git diff <hash 1-го коммита> <HEAD (любой другой хеш)> - сравнение коммитов между собой 
сравнится история изменений между двумя коммитами (разница).

$ git clone <SHH_key> - локальное сохранение удаленного репозитория

$ git status ignore - отобразить файлы .gitignore

$ git branch - активная ветка

$ git branch <название_ветки> - создать новую ветку

$ git branch -a - вывести все известные ветки, и локальные, и удаленные

$ git branch -d <ветка> - удалить ветку, если она является частью main

$ git branch -D <ветка> - удалить ветку, если она не объединена с main

$ git branch -m  - Переименовать ветку

$ git checkout <название_ветки> - перейти на ветку

$ git checkout -b <название_ветки> - создать новую ветку и перейти на неё

$ git diff main HEAD - показать разницу между веткой main и указателем на HEAD

$ git diff HEAD~2 HEAD - показать разницу между коммитом, который был два шага назад, и текущим

$ git merge <branch> - Слить изменения из ветки <branch> в текущую ветку

$ git merge --continue  - Продолжить слияние в случае решения конфликтов

$ git merge --abort  - Отменить merge

$ git push -u origin <ветка> - отправить <ветку> в удаленный репозиторий и связать ветку с удаленной

$ git push <ветка> - отправить допольнительные изменения в <ветку>, которая уже существует в удаленном репозитории

$ git pull - подтянуть изменения текущей ветки из удаленного репозитория

$ git stash -m 'my stash name' - Спрячет все изменения в стеш

$ git stash pop - Достанет последние изменения из стеша, удалив его оттуда. По дефолту 0

$ git stash apply - Достанет последние изменения из стеша, сохранив его. По дефолту 0

$ git stash list - Посмотреть список всех стешей

$ git stash show <stash> - Посмотреть стеш. По дефолту 0

$ git stash drop <stash> - Удалить стеш. По дефолту 0
```
----

### Технические команды **Git**

```
$ ls -a ~/.ssh - проверка на наличие ключей SSH

$ ssh-keygen -t ed25519 -C "почта_аккаунта_с_GitHub" - генерация ключа для GitHub

$ shh -T git@github.com - подключение ключа к аккаунту

$ git remote add origin Ваш_SHH_URL

$ git remote -v - проверка, что подключение прошло успешно

$ Vim <File> - открыть файл в Vim. insert - чтобы изменять файл. :qw - выход

$ git merge --no--ff add <ветка> - отключить fast forward для этого слияния

$ git config [--global] merge.ff false - отключить fast forward ждя всех слияний

$ git config -l - Список текущих настроек

$ git config --global -l  - Список глобальных настроек

$ git config --local -l  - Список локальных настроек репозитория

$ git config --global user.name Name  - Установить имя пользователя в глобальной области

$ git config --global user.email email@example.com - Установить email пользователя в глобальной области

$ git config --unset <var> - Удалить переменную из настроек

$ git config alias.<your-alias> <command>  - Создание алиаса для команды

$ git config alias.st status  - Пример: теперь сможем писать git st вместо git status

$ git config --global core.autocrlf <input|false|true>  - Настройка параметра окончания стро

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

```$ git log --oneline```

```
a9546b7 (HEAD -> master, origin/master) Добавить раздел офрмление сообщений к коммитам
bf63b7e Добавить информацию о статусах файлов в readme
838f373 Добавить описание HEAD в readme
6b3455f Добавить в readme информацию о хеше
3d11a6d еще одни изменения ;)
254f526 Небольшие визуальные изменения
d666812 Добавлено описание в readme.md
```


Она выведет не такой подробный список изменений.

---- 

### HEAD статус

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
Залогиненые файлы, готовые к пушу на сервер. ```modified + git add = staged```

----

### Оформление сообщений к коммитам

В команде разработчиков для эффективного кпд необходимо придерживаться стандартов общения и коммуникации
Например в среде Python разработчиков используют стиль оформления кода PEP-8. Любые другие вариации 
считаются моветоном. Грамотное и подробное описание коммитов так же важно для команды.
Есть несколько принципов для оформления коммитов, но в каждой команде они могут отличаться, это нормально.

1. Информативные заголовки. 
Нужно вложиться в 30-70 символов, чтобы другим разработчикам не приходилост открывать коммит и смотреть
какие конкретно изменения были сделаны.

```
Пофиксить баг №103
Добавить список контактов в footer
```

2. Писать слова в начальной форме.
Чтобы не использовать изменения с помощью склонения, числа, рода и тд
Это делается для автоматизации рутинных процессов.

3. ID Jira.
Если команда использует трекер задач, можно вначале коммита ставить ID задачи в трекере, 
чтобы легче отслеживать статус продукта.

```<ID 101> добавить кнопку "оплатить заказ" на страницу оплаты```

4. Разбивать коммиты на категории: fix, feat, info.

```
fix: Баг рассинхрон корзины на этапе оплаты
feat: Добавить часы в главном меню
info: Добавить описание функций backend
```   

----

### .gitignore

В .gitignore указывают все файлы, которые нужно игнорировать (не отслеживать) 
Например файлы настройки IDE

#### Модификаторы:

#### * - Игнорирует типовые файлы 

```*.jpeg docs/*/temp```

#### ? - соответствует одному символу

#### [...] - соответствует одному символу из списка -> [123], [a-z]

#### / - Игнорирует файлы и категории только в корневой директории

#### ** - игнорирует любое количество каталогов (иерархически) 
``` 
docs/**/temp
**.jpeg 
```

#### ! - инверсия правила
``` *.jpeg
!logo.jpeg 
```
----

Чтобы разрешить конфликт слияния, который возникает, когда главная ветка «уходит» вперёд,можно сделать следующее.
Сначала локально получить новые изменения через git pull, а затем выполнить git merge и разрешить конфликт. 
Далее создать коммит слияния и отправить новые изменения без конфликтов обратно в удалённый репозиторий командой git push.

----

Данный репозиторий будет дополняться по мере изучения возможностей **Git**

В командной разработке стоит придерживаться паттернов разработки например feature branch workflow
Новый функционал -> новая ветка с рабочим названием -> все готово и тесты пройдены? -> мержи в мэйн
! после PL нужно обновить локульную мэйн ветку

*Peace :* *

![Логотип](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/130px-Markdown-mark.svg.png 'Логотип MarkDown')
