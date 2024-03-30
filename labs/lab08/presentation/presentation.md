---
## Front matter
lang: ru-RU
title: Лабораторная работа № 8
subtitle: Простейший шаблон
author:
  - Чилеше Л.
institute:
  - Российский университет дружбы народов, Москва, Россия

date: 30 марта 2024

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

Ознакомление с инструментами поиска файлов и фильтрации текстовых данных.
Приобретение практических навыков: по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.

## Запишите в файл file.txt названия файлов, содержащихся в каталоге /etc. Допишите в этот же файл названия файлов, содержащихся в вашем домашнем каталоге

![file.txt ](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T20:20:36,658167622+03:00.png)


## Выведите имена всех файлов из file.txt, имеющих расширение .conf, после чего запишите их в новый текстовой файл conf.txt.

![.conf](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T20:25:51,410057347+03:00.png)

##  запишите их в новый текстовой файл conf.txt.

![conf.txt](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T20:26:22,617140052+03:00.png)

##. Определите, какие файлы в вашем домашнем каталоге имеют имена, начинавшиеся с символа c? Предложите несколько вариантов, как это сделать.

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T20:27:58,408749596+03:00.png)

## Выведите на экран (по странично) имена файлов из каталога /etc, начинающиеся с символа h.

![начинающиеся с символа h](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T20:45:15,660566604+03:00.png)

## Запустите в фоновом режиме процесс, который будет записывать в файл ~/logfile файлы, имена которых начинаются с log.

![~/logfile](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T20:47:43,195507059+03:00.png)

## Определите идентификатор процесса gedit, используя команду ps, конвейер и фильтр grep. Как ещё можно определить идентификатор процесса?

![ps](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T20:51:56,403056964+03:00.png)


## Прочтите справку (man) команды kill, после чего используйте её для завершения процесса gedit.

![kill](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T21:03:51,779799484+03:00.png)



## Выполните команды df и du, предварительно получив более подробную информацию об этих командах, с помощью команды man.

![df](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T21:04:54,097589208+03:00.png)

## du

![du](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T21:06:21,400967652+03:00.png)

## Воспользовавшись справкой команды find, выведите имена всех директорий, имеющихся в вашем домашнем каталоге.

![find](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab08/presentation/image/2024-03-30T22:00:14,653076578+03:00.png)


