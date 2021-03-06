---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Lab"
subtitle: ""
summary: "Basics of the interface of user interaction with the Unix system at the command line level"
authors: [Emil Samigullin]
tags: [lab]
categories: [lab]
date: 2022-05-05T22:44:37+03:00
lastmod: 2022-05-05T22:44:37+03:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

# Цель Работы  

**Приобретение практических навыков взаимодействия пользователя с системой посредством командной строки**

# Ход Работы
1. Определили полное имя домашнего каталога.(рис. [-@fig:001])

   ![Определили с помощью команды pwd](images/1.jpg){ #fig:001 width=70% }

2. - Перешли в каталог /tmp .(рис. [-@fig:002])

   ![Переход в каталог /tmp](images/2.1.jpg){ #fig:002 width=70% }
   
   - Вывели  содержимое каталога /tmp с опцией -a.(рис. [-@fig:003])
   
   ![Вывод содержимого с помощью ls -a](images/2.2.1.jpg){ #fig:003 width=70% }
   
   - Вывели содержимое с опцией -l.(рис. [-@fig:004])
   
   ![Вывод содержимого с помощью ls -l](images/2.2.2.jpg){ #fig:004 width=70% }
   
   - Попробовали найти каталог cron в каталоге /var/spool .(рис. [-@fig:005])
   
   ![Нахождение cron](images/2.3.jpg){ #fig:005 width=70% }
   
   - Перешли в домашний каталог и вывели его содержимое.(рис. [-@fig:006])
   
   ![Вывод содержимового дом.катаога](images/2.4.jpg){ #fig:006 width=70% }
   
3. - Создал каталоги newdir и создал в нем каталог morefun и проверил на их наличие.(рис. [-@fig:007])

   ![Cоздание newdir + newdir/morefun](images/3.1.jpg){ #fig:007 width=70% }
   
   - Создал в домашнем каталоге одной командой каталоги letters, memos, misk и после удалил их.(рис. [-@fig:008])
   
   ![Создание и удаление letters, memos, misk](images/3.3.jpg){ #fig:008 width=70% }
   
   - Попробовали удалить каталог newdir с помощью команды rm, но не получилось. Используя опцию -r, получилось удалить.(рис. [-@fig:009])
   
   ![Удаление newdir + newdir/morefun](images/3.5.jpg){ #fig:009 width=70% }
   
4. Посмотрели с помощью команды man ls и узнали о опции -R.(рис. [-@fig:010], [-@fig:011])

   ![Просмотр man](images/4.1.jpg){ #fig:010 width=70% }
   
   ![Вопроизвели команду](images/4.2.jpg){ #fig:011 width=70% }
   
5. Посмотрели с помощью man ls и узнали о опции -t.(рис. [-@fig:012], [-@fig:013])

   ![Посмотрели на man](images/5.1.jpg){ #fig:012 width=70% }
   
   ![Вопроизвели команду](images/5.2.jpg){ #fig:013 width=70% }
   
6. Использовали man для просмотра описания команд: cd, pwd, mkdir, rmdir, rm.(рис. [-@fig:014], [-@fig:015], [-@fig:016], [-@fig:017], [-@fig:018])

   ![Использовали man cd](images/6.1.jpg){ #fig:014 width=70% }
   
   ![Использовали man pwd](images/6.2.jpg){ #fig:015 width=70% }
   
   ![Использовали man mkdir](images/6.3.jpg){ #fig:016 width=70% }
   
   ![Использовали man rmdir](images/6.4.jpg){ #fig:017 width=70% }
   
   ![Использовали man rm](images/6.5.jpg){ #fig:0018 idth=70% }
   
7. Используя информацию с history мы модифицировали и исполнили несколько команд из буфера.(рис. [-@fig:019])

   ![Модифицировали и исполнили](images/7.2.jpg){ #fig:019 width=70% }
   
   
# Вывод

Во время лабораторной работы, мы приобрели навыки взаимодействия пользователя с системой посредством командной строки и познакомились с команды и его опциями.

# Контрольные вопросы.  
1. Командная строка позволяет пользователю взаимодействовать с системой, используя команды.
2. Команда pdf позволяет определить абсолютный путь. Пример: /home/easamigullin
3. При помощи команды ls с опцией -F позволяет узнать тип файлов и их имена в текущем каталоге. Пример: Downloads/
4. При помощи команды ls с опцией -a позволяет увидеть добавочно скрытые файлы. Пример: .ssh
5. При помощи rm можно удалять файлы и каталоги, только с каталогами надо добавить опцию -r. Пример: rm -r newdir
6. При помощи команды history можно вывести информацию о последних выполненных командах.
7. Модернизировать команду можно, используя формат, как
   !<номер команды>:s/<что меняем>/<на что меняем>. Пример: !2:s/a/lFt
8. Чтобы воспользоваться несколькими командами в одной строке, нужно использовать ";" Пример: cd; ls -l
9. Экранирование символов - замена в тексте управляющих символов на соответствующие текстовые подстановки. Если встречаются символы (".","/", "*"), то можно поставить перед ним знак экранирования /. Пример: //
10. Команда ls -l выводит следующую информацию: тип файла - право доступа - число ссылок - владелец, размер - дата последней ревизии - имя файла или каталога.
11. Относительный путь представляет собой путь по отношению к текущему рабочему каталогу пользователя или активных приложений. Используется командой cd. Пример: Относительный: cd ./name_folder
               pwd: /usr/name_folder
Абсолютный: cd /usr/bin/
            pwd: /usr/bin
12. Команда man позволяет получить справочник по той или иной информации.
13. Клавиша Tab служит для автоматического дополнения вводимых команд.
