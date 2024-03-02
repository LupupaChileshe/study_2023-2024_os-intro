---
## Front matter
title: "Шаблон отчёта по лабораторной работе"
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


    Изучить идеологию и применение средств контроля версий.
    Освоить умения по работе с git.


# Теоретическое введение

Установка Git служит основополагающим шагом в использовании систем контроля версий для разработки программного обеспечения, позволяя разработчикам отслеживать изменения, сотрудничать и эффективно управлять проектами. Git — это распределенная система контроля версий, то есть она сохраняет полную историю проекта на каждом компьютере разработчика. Эта архитектура гарантирует, что у каждого разработчика есть полная копия истории проекта, что позволяет им работать в автономном режиме и способствует более быстрому и надежному сотрудничеству.
# Выполнение лабораторной работы

Установка git

 dnf install git

![install git](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262352_x.jpg)

Установка gh

 dnf install gh

![nstall gh](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262354_x.jpg)

## Базовая настройка git
 
 Я установил имя и адрес электронной почты репозитория.
 
![git config](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262355_x.jpg)

- Я настроил utf-8 в выводе сообщения git
- Я установил параметр autocrlf
- Я установил параметр SafeCRLF 

![параметр](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262357_x.jpg)

## Создание ssh-ключей

- по алгоритму rsa с ключём размером 4096 бит:

 ssh-keygen -t rsa -b 4096

![rsa 4096](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262358_x.jpg)

- по алгоритму ed25519:

 ssh-keygen -t ed25519

![ ed25519](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262359_x.jpg) 


## Создание ключей pgp

- Генерируем ключ

  gpg --full-generate-key
  
![generate-key](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948741_x.jpg)  

## Настройка автоматических подписей коммитов git

Я использовал введенный адрес электронной почты, скажите Git использовать его при подключении коммитов:

git config --global user.signingkey <PGP Fingerprint>
git config --global commit.gpgsign true
git config --global gpg.program $(which gpg2)

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948742_x.jpg)


## Сознание репозитория курса на основе шаблона

создал шаблон рабочего пространства

  mkdir -p ~/work/study/2022-2023/"Операционные системы"
  cd ~/work/study/2022-2023/"Операционные системы"
  gh repo create study_2022-2023_os-intro --template=yamadharma/course-directory-student-template --public

![шаблон рабочего пространства](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948745_x.jpg)

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948747_x.jpg)

 git clone --recursive git@github.com:<owner>/study_2022-2023_os-intro.git os-intro

![ git clone](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948749_x.jpg)


## Настройка каталога курса

- Зашёл в каталог курса
- Удалил ненужные файлы
- создал необходимые каталоги

![каталога курса](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948751_x.jpg)

- Отправил файлы на сервер

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948752_y.jpg)


# Выводы

Я узнал, как установить git и все необходимые файлы, которые ему нужны для запуска.


