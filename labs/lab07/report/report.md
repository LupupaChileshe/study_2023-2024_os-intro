---
## Front matter
title: "Лабораторная работа № 7"
subtitle: "Анализ файловой системы Linux. Команды для работы с файлами и каталогами"
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

Ознакомление с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобретение практических навыков по применению команд для работы
с файлами и каталогами, по управлению процессами (и работами), по проверке исполь-
зования диска и обслуживанию файловой системы.

# Выполнение лабораторной работы

1. Выполните все примеры, приведённые в первой части описания лабораторной работы.
2. Выполните следующие действия, зафиксировав в отчёте по лабораторной работе
используемые при этом команды и результаты их выполнения:
- Скопируйте файл /usr/include/sys/io.h в домашний каталог и назовите его equipment. Если файла io.h нет, то используйте любой другой файл в каталоге /usr/include/sys/ вместо него.

![equipment](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:07:08,392742523+03:00.png)

- В домашнем каталоге создайте директорию ~/ski.plases.

![~/ski.plases.](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:07:44,036990078+03:00.png)

- Переместите файл equipment в каталог ~/ski.plases.

![ equipment](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:09:44,797524326+03:00.png)

- Переименуйте файл ~/ski.plases/equipment в ~/ski.plases/equiplist.

![equiplist](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:10:50,916340668+03:00.png)

- Создайте в домашнем каталоге файл abc1 и скопируйте его в каталог ~/ski.plases, назовите его equiplist2.

![abc1](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:11:24,311226633+03:00.png)

- Создайте каталог с именем equipment в каталоге ~/ski.plases.

![ каталоге ~/ski.plases.](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:12:40,888941611+03:00.png)

- Переместите файлы ~/ski.plases/equiplist и equiplist2 в каталог

~/ski.plases/equipment.

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:13:56,717313048+03:00.png)

- Создайте и переместите каталог ~/newdir в каталог ~/ski.plases и назовите его plans.

![plans](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:15:43,552160371+03:00.png)

3. Определите опции команды chmod, необходимые для того, чтобы присвоить перечис-
ленным ниже файлам выделенные права доступа, считая, что в начале таких прав
нет:
3.1. drwxr--r-- ... australia
3.2. drwx--x--x ... play
3.3. -r-xr--r-- ... my_os
3.4. -rw-rw-r-- ... feathers
При необходимости создайте нужные файлы.

![chmod](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:16:24,815247386+03:00.png)

4. Проделайте приведённые ниже упражнения, записывая в отчёт по лабораторной работе используемые при этом команды:
- Просмотрите содержимое файла /etc/password.

![/etc/password](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:16:56,001445640+03:00.png)

- Скопируйте файл ~/feathers в файл ~/file.old.

![ ~/file.old](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:17:59,760925280+03:00.png)

- Переместите файл ~/file.old в каталог ~/play.

![~/play](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:18:12,509906358+03:00.png)

- Скопируйте каталог ~/play в каталог ~/fun.

![fun](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:18:40,909336950+03:00.png)

- Переместите каталог ~/fun в каталог ~/play и назовите его games.

![games](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:19:10,240537049+03:00.png)

- Лишите владельца файла ~/feathers права на чтение.
Что произойдёт, если вы попытаетесь просмотреть файл ~/feathers командой
cat?

![права на чтение](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:19:55,116852621+03:00.png)

- Что произойдёт, если вы попытаетесь скопировать файл ~/feathers?

![cp](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:20:55,657347291+03:00.png)

- Дайте владельцу файла ~/feathers право на чтение.
![право на чтение](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:22:42,628916017+03:00.png)

- Лишите владельца каталога ~/play права на выполнение.
- Перейдите в каталог ~/play. Что произошло?

![Лишите владельца каталога ~/play](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:24:46,062194940+03:00.png)

Дайте владельцу каталога ~/play право на выполнение.

![право на выполнение](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:25:15,733505840+03:00.png)


5. Прочитайте man по командам mount, fsck, mkfs, kill и кратко их охарактеризуйте,
приведя примеры.

![fsck](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:26:05,769031291+03:00.png)

 Проверяет и восстанавливает файловую систему Linux

![mount](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:26:45,577703905+03:00.png)

Команда монтирования в Linux используется для присоединения файловой системы к дереву каталогов в указанной точке монтирования.

![mkfs](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:27:04,966625620+03:00.png)

Команда mkfs в Linux используется для создания файловой системы на устройстве хранения данных, например жестком диске (HDD) или USB-накопителе.

![kill](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab07/report/image/2024-03-23T20:27:17,610407816+03:00.png)

Отправляет сигнал процессу, обычно для его завершения.


# Выводы

Познакомившись с файловой системой Linux, ее структурой, именами и содержимым, я получил четкое представление о том, как Linux организует файлы и каталоги и управляет ими.

# Список литературы{.unnumbered}

::: {#refs}
:::
