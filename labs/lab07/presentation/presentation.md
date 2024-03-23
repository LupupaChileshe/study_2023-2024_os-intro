---
## Front matter
lang: ru-RU
title: Лабораторная работа № 7
subtitle: Анализ файловой системы Linux. Команды для работы с файлами и каталогами
author:
  - Лупупа Чилеше
institute:
  - Российский университет дружбы народов, Москва, Россия

date: 23 марта 2024

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

# Цели и задачи

Ознакомление с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобретение практических навыков по применению команд для работы
с файлами и каталогами, по управлению процессами (и работами), по проверке исполь-
зования диска и обслуживанию файловой системы.

##  Скопируйте файл /usr/include/sys/io.h в домашний каталог и назовите его equipment. Если файла io.h нет, то используйте любой другой файл в каталоге /usr/include/sys/ вместо него.

![/usr/include/sys/io.h](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/presentation/image/2024-03-23T20:07:08,392742523+03:00.png)

## В домашнем каталоге создайте директорию ~/ski.plases

![~/ski.plases](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/presentation/image/2024-03-23T20:07:44,036990078+03:00.png)

## Переместите файл equipment в каталог ~/ski.plases.

![~/ski.plases](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/presentation/image/2024-03-23T20:09:44,797524326+03:00.png)

## . Переименуйте файл ~/ski.plases/equipment в ~/ski.plases/equiplist.

![equiplist](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/presentation/image/2024-03-23T20:10:50,916340668+03:00.png)


## Создайте в домашнем каталоге файл abc1 и скопируйте его в каталог ~/ski.plases, назовите его equiplist2

![abc1](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/presentation/image/2024-03-23T20:11:24,311226633+03:00.png)

## Создайте каталог с именем equipment в каталоге ~/ski.plases

![equipment](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/presentation/image/2024-03-23T20:12:40,888941611+03:00.png)

## Переместите файлы ~/ski.plases/equiplist и equiplist2 в каталог~/ski.plases/equipment.

![mv](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/presentation/image/2024-03-23T20:13:56,717313048+03:00.png)

## Создайте и переместите каталог ~/newdir в каталог ~/ski.plases и назовите его plans

![newdir](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/presentation/image/2024-03-23T20:15:43,552160371+03:00.png)

## Определите опции команды chmod, необходимые для того, чтобы присвоить перечисленным ниже файлам выделенные права доступа, считая, что в начале таких прав нет:
- drwxr--r-- ... australia
- drwx--x--x ... play
- -r-xr--r-- ... my_os
- -rw-rw-r-- ... feathers

## При необходимости создайте нужные файлы

![chmod](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/presentation/image/2024-03-23T20:16:24,815247386+03:00.png)

## Заключение

Познакомившись с файловой системой Linux, ее структурой, именами и содержимым, я получил четкое представление о том, как Linux организует файлы и каталоги и управляет ими.


