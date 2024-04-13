---
## Front matter
lang: ru-RU
title: Лабораторная работа № 10
subtitle: Простейший шаблон
author:
  - Лупупа Ч.
institute:
  - Российский университет дружбы народов, Москва, Россия
 
date: 13 апраля 2024.

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

Познакомиться с операционной системой Linux. Получить практические навыки рабо-
ты с редактором vi, установленным по умолчанию практически во всех дистрибутивах

## Создание каталога с именем ~/work/os/lab06.

![~/work/os/lab06](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/presentation/image/2024-04-13T10:17:36,931693128+03:00.png)

- используя команду mkdir, я создал файл с именем ~/work/os/lab06.

## перешел в вновь созданный каталог..

![cd](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/presentation/image/2024-04-13T10:18:13,643793520+03:00.png)

- с помощью команды cd я изменил каталог на lab10

## Вызвал vi и создал файл hello.sh.

![hello.sh](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/presentation/image/2024-04-13T10:20:45,699215522+03:00.png)

## Вызовите vi на редактирование файла

  vi ~/work/os/lab06/hello.sh

![vi](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/presentation/image/2024-04-13T10:23:01,613792463+03:00.png)

## Перешел в режим вставки и заменил на HELLO.

![HELLO](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/presentation/image/2024-04-13T10:29:49,896786520+03:00.png)

## Перешел в режим вставки и выделил текст: local

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/presentation/image/2024-04-13T10:30:19,342753182+03:00.png)

## Поместил курсор на последнюю строку файла. После него вставлена ​​строка, содержащая текст: echo $HELLO

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/presentation/image/2024-04-13T10:30:39,661118397+03:00.png)


