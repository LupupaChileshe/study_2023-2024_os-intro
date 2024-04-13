---
## Front matter
title: "Лабораторная работа № 10"
subtitle: "Простейший вариант"
author: "Лупупа Чилеше"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
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
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Познакомиться с операционной системой Linux. Получить практические навыки рабо-
ты с редактором vi, установленным по умолчанию практически во всех дистрибутивах



# Выполнение лабораторной работы

**Задание 1.** Создание нового файла с использованием vi

1. Создайте каталог с именем ~/work/os/lab06.

![~/work/os/lab06](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/report/image/2024-04-13T10:17:36,931693128+03:00.png)

2. Перейдите во вновь созданный каталог.

![cd](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/report/image/2024-04-13T10:17:36,931693128+03:00.png)

3. Вызовите vi и создайте файл hello.sh

 vi hello.sh
 
![ vi hello.sh](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/report/image/2024-04-13T10:21:25,469688709+03:00.png)

4. Нажмите клавишу i и вводите следующий текст.
1 #!/bin/bash
2 HELL=Hello
3 function hello {
4 LOCAL HELLO=World
5 echo $HELLO
6 }
7 echo $HELLO
8 hello

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/report/image/2024-04-13T10:20:45,699215522+03:00.png)

5. Нажмите клавишу Esc для перехода в командный режим после завершения ввода текста.



6. Нажмите : для перехода в режим последней строки и внизу вашего экрана появится приглашение в виде двоеточия.

7. Нажмите w (записать) и q (выйти), а затем нажмите клавишу Enter для сохранения вашего текста и завершения работы.

8. Сделайте файл исполняемым

 1 chmod +x hello.sh
 
**Задание 2**. Редактирование существующего файла

1. Вызовите vi на редактирование файла

 1 vi ~/work/os/lab06/hello.sh

![vi](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/report/image/2024-04-13T10:23:01,613792463+03:00.png) 
 
2. Установите курсор в конец слова HELL второй строки.
3. Перейдите в режим вставки и замените на HELLO. Нажмите Esc для возврата в командный режим.

![HELLO](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/report/image/2024-04-13T10:29:49,896786520+03:00.png)

4. Установите курсор на четвертую строку и сотрите слово LOCAL.
5. Перейдите в режим вставки и наберите следующий текст: local, нажмите Esc для возврата в командный режим.

![local](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/report/image/2024-04-13T10:30:19,342753182+03:00.png)

6. Установите курсор на последней строке файла. Вставьте после неё строку, содержащую следующий текст: echo $HELLO.

![echo $HELLO](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab10/report/image/2024-04-13T10:30:39,661118397+03:00.png)

7. Нажмите Esc для перехода в командный режим.
8. Удалите последнюю строку.
9. Введите команду отмены изменений u для отмены последней команды.
10. Введите символ : для перехода в режим последней строки. Запишите произведённые
изменения и выйдите из vi.

# Выводы

Здесь кратко описываются итоги проделанной работы.

# Список литературы{.unnumbered}

::: {#refs}
:::
