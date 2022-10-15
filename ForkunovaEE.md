**ИНСТРУКЦИЯ**

# **1. Проверка работает ли**

что бы проверить работает ли терминал,
заходим в "терминал" далее " создать терминал" 
и набираем *git --version*
если выдало строку, например,

PS D:\29 09> git version

git version 2.37.3.windows.1

PS D:\29 09> 

значит все ок.

# **2. идентификация**

Далее надо идентифитироваться в git:

*git config --global user.name "Elena Forkunova"*
и все запоминается
и email вводим:

*git config --global user.email "forkelena@****.ru"*

Как проверить мои данные, которые я ввела? 

вводим:
*git config --global user.name*
и выдается имя пользователя, например:

PS D:\29 09> git config --global user.name                       
Elena Forkunova
PS D:\29 09> 

# **3. СОЗДАЕМ репозиторий**

Для того что бы инициализировать (СОЗДАТЬ) репозиторий, вводим:

*git init*

получаем:
PS D:\29 09> git init
Reinitialized existing Git repository in D:/29 09/.git/
PS D:\29 09>
  
и на компе появляется папка внутри 2909 с названием .git
это и есть доказательство работы.
Если нужно удалить репозиторий, то удаляем папку.

# **4. ЧТО ты знаешь?**
а ты занешь, что то расскажет
 о репозитории - команда *git status*
на какой ветке мы стоим, есть ли комиты, и про файлы есть или нет, отслеживается или нет.

# **5. Очищение**

ЧТО БЫ ОЧИСТИТЬ ВСЕ КОМАНДЫ, КОТОРЫЕ БЫЛИ - ввести *clear* и все исчезнет.

# **6. Я слежу за тобой**

изначально все файлы неотслеживаемые 

правой кнопкой мыши по полю "проводник" и создаем новый файл, например,
readme.md (это расширение маркдаун)
это файл должен быть зеленый или должна появиться метка *U* - это значит неотслеживаемый.

**ДОБАВИТЬ ФАЙЛ В ОТСЛЕЖИВАЕМЫЙ** *git add* и нажимаем табуляцию и выбираем нужный файл

и файл помечается буквой *А* и он отслеживается!
проверим:

PS D:\GIT\29 09> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   readme.md

далее внесем опять изменения и **СОХРАНЯЕМ ctrl+s**

# **7. КОММИТ - как много в этом слове**

Каждое свое действие желательно коммитить, прдварительно сохранив.

После того как изменили файл, добавляем комментарий и добавляем файл в отслеживаемый, **вводим команду 2 в1:**
 *git commit -a -m "Добавила подзаголовок"*

# **8. вы прекрасны**

  убедиться в этом поможет команда *git log* , которая показывает все коммиты, которые мы сделали.

# **9. Основные команды Git**

git diff – увидеть разницу между текущим файлом и закоммиченным файлом
git branch <название ветки>_ - создать новую ветку
git branch - посмотреть список веток в репозитории
git branch -d <название ветки> – удалить ветку
git checkout <название ветки> – переход к другой ветке
git checkout -b <название ветки> - создать ветку и перейти на нее

# **10.Слияние веток**

Если нужно применить изменения из дополнительной ветки, их нужно внести в master. Перейдем в master и выполним команду:

git merge <дополнительная ветка> :

Если над общими участками какого-либо файла успели поработать несколько человек, с этим нужно разбираться вручную. При возникновении ошибок Git помечает общие части файлов из разных веток и сообщает о конфликте.

  ## **11. РАБОТА С GITHUB**

1. Создать аккаунт на github.com
2. создать локальный репозиторий
3. подружить мой локальныйи удаленный репозиторий, github при создании подскажет, как это сделать
4. отправить (push) мой локальный репозиторий в удаленный на github, при необходимости авторизоваться
5. перенести изменения "с другого компьютера"
6. выкачать (pull) актуальное сосотояние из удаленного репозитория.

## **12. Работа с форк**

1. Переходим по ссылке https://github.com/KruglovDA/0610.git
2. Жмем на кнопку Fork (в списке наших репозиториев появился fork)
3. Клонируем к себе в папку
4. Открывает папку в VS
5. выполняем git branch FIO
6. выполняем git checkout FIO
7. Добавляем свой файл с названием FIO.MD
8. Выполняем Коммит
9. выполняем git push (если git ругается, выполняем команду из подсказки)
10. на github выполняем pull request