﻿**Лабораторная работа №1. Управление файлами и каталогами** 

**Задачи:** 

1. Освоить основные команды для работы с файлами и каталогами (директориями). 
1. Научиться использовать справочную информацию по командам. 

**Подсказки:** 

1. При выполнении работы могут использоваться следующие команды:  cat; cd; chmod, cmp; cp; diff; find; head; less; ln; ls; man; mkdir; mv; nano; patch; rm; split; vi; wc. 
1. Для получения подробного справочного руководства по любой команде можно набрать в «man  название команды», для кратной справки – название_команды --help. 
1. По умолчанию, команды выводят результаты работы в консоль. Для перенаправления стандартного вывода с консоли в файл можно использовать операторы  «>» или «>>». 
1. Команды могут быть собраны в конвейеры с помощью оператора «|». 
1. Для удобства работы можно пользоваться одновременно несколькими консолями. На одной консоли читать справочное руководство, на другой редактировать скрипт и т.п. Переключаться между ними можно нажатием комбинации клавиш Alt+Fn, где Fn — функциональная клавиша (F1 — для первой консоли, F2 - для второй и т.д.). 
1. Для того чтобы было удобнее смотреть результаты выполнения тех команд, которые что-то выводят на экран можно после них вставлять в скрипт паузу (с помощью команды sleep) или ожидать нажатия Enter с помощью команды read. 

**Задание:** 

Создать скрипт (создать текстовый файл с необходимыми командами (добавив в начало #!/bin/sh), сделать его исполняемым). Создать и редактировать скрипт можно в редакторах nano или vi. 

Скрипт должен выполнять следующие действия: 

1. Создать каталог test в домашнем каталоге пользователя. 
1. Создать в нем файл list, содержащий список всех файлов и поддиректориев каталога /etc (включая скрытые) в таком виде, что можно однозначно определить какая из записей является именем файла, а какая — названием директории. 
1. Вывести в конец этого файла два числа. Сначала количество поддиректориев в каталоге /etc, а затем количество скрытых файлов в каталоге /etc. 
1. Создать в каталоге test каталог links. 
1. Создать в каталоге links жесткую ссылку на файл list с именем list_hlink. 
1. Создать в каталоге links символическую ссылку на файл list с именем list_slink. 
1. Вывести на экран количество имен (жестких ссылок) файла list_hlink, количество имен (жестких ссылок) файла list и количество имен (жестких ссылок) файла list_slink. 
1. Дописать в конец файла list_hlink число строк в файле list.  
1. Сравнить содержимое файлов list_hlink и list_slink. Вывести на экран YES, если файлы идентичны. 
1. Переименовать файл list в list1. 
1. Сравнить содержимое файлов list_hlink и list_slink. Вывести на экран YES, если файлы идентичны. 
1. Создать в домашнем каталоге пользователя жесткую ссылку на файл list_link с именем list1. 
1. Создать в домашнем каталоге файл list_conf, содержащий список файлов с расширением .conf, из каталога /etc и всех его подкаталогов. 
1. Создать в домашнем каталоге файл list_d, содержащий список всех подкаталогов каталога /etc, расширение которых .d. 
1. Создать файл list_conf_d, включив в него последовательно содержимое list_conf и list_d. 
1. Создать в каталоге test скрытый каталог sub. 
1. Скопировать в него файл list_conf_d. 
1. Еще раз скопировать туда же этот же файл в режиме автоматического создания резервной копии замещаемых файлов. 
1. Вывести на экран полный список файлов (включая все подкаталоги и их содержимое) каталога test. 
1. Создать в домашнем каталоге файл man.txt, содержащий документацию на команду man. 
21. Разбить файл man.txt на несколько файлов, каждый из которых будет иметь размер не более 1 килобайта. 
21. Создать каталог man.dir. 
21. Переместить одной командой все файлы, полученные в пункте 21 в каталог man.dir. 
21. Собрать файлы в каталоге man.dir обратно в файл с именем man.txt. 
21. Сравнить файлы man.txt в домашней каталоге и в каталоге man.dir и вывести YES, если файлы идентичны. 
21. Добавить в файл man.txt, находящийся в домашнем каталоге несколько строчек с произвольными символами в начало файла и несколько строчек в конце файла. 
21. Одной командой получить разницу между файлами в отдельный файл в стандартном формате для наложения патчей. 
21. Переместить файл с разницей в каталог man.dir. 
21. Наложить патч из файла с разницей на man.txt в каталоге man.dir. 
21. Сравнить файлы man.txt в домашней каталоге и в каталоге man.dir и вывести YES, если файлы идентичны. 

Предъявить скрипт преподавателю и ответить на его вопросы по любым использованным командам и выполняющимся операциям. Перед сдачей лабораторной работы подумать, как объяснить результаты выполнения пунктов 7, 9, 11, 25, 30 
