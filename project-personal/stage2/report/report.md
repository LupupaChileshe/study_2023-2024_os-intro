---
## Front matter
title: "Второй этап индивидуального проекта"
subtitle: "данные о себе"
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

Добавить к сайту данные о себе.

# Задание


    Список добавляемых данных.
        Разместить фотографию владельца сайта.
        Разместить краткое описание владельца сайта (Biography).
        Добавить информацию об интересах (Interests).
        Добавить информацию от образовании (Education).
    Сделать пост по прошедшей неделе.
    Добавить пост на тему по выбору:
        Управление версиями. Git.
        Непрерывная интеграция и непрерывное развертывание (CI/CD).


# Теоретическое введение

Включение личной информации в шаблон сайта Hugo предполагает продуманный подход для обеспечения конфиденциальности и безопасности, особенно при работе с конфиденциальными данными. Hugo, генератор статических сайтов, предлагает гибкость и скорость, что делает его отличным выбором для создания личных веб-сайтов или блогов. Он позволяет легко настраивать систему шаблонов, позволяя пользователям адаптировать внешний вид и функциональность своего сайта к своим потребностям. При добавлении личной информации крайне важно учитывать последствия для конфиденциальности и обеспечивать безопасную обработку данных. Этого можно достичь, используя файлы конфигурации Hugo, такие как config.toml или config.yaml, для определения параметров сайта и личных данных. Эти файлы можно настроить, включив в них ваше имя, контактную информацию, ссылки на социальные сети и любые другие соответствующие личные данные. Также желательно просмотреть документацию Хьюго по шаблонам и конфигурации, чтобы понять, как лучше всего интегрировать личную информацию в дизайн вашего сайта. Помните, что ключом к успешному личному веб-сайту является не только используемая технология, но и продуманная интеграция личной информации, обеспечивающая баланс между персонализацией и конфиденциальностью.

# Выполнение лабораторной работы



## Список добавляемых данных.

1. Разместить фотографию владельца сайта.

![New image](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:41:28,932222987+03:00.png)

![View on blog post](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:41:36,218430514+03:00.png)

__комментарий__ : Я заменил изображение, которое было в  файле author, на свое.

2. Разместить краткое описание владельца сайта (Biography).

![New biography](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:44:00,646444366+03:00.png)

![View of bio on blog post](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:44:19,383735784+03:00.png)

__комментарий__ : Я изменил синтаксис в файле index.md со своей информацией.


3. Добавить информацию об интересах (Interests).

![Interests](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:44:55,104577152+03:00.png) 

![Interests view in blog post](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:45:13,793985838+03:00.png)

__комментарий__ : Я изменил синтаксис в файле index.md, где написано «Interests».

4. Добавить информацию от образовании (Education).

![Education](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:45:31,170640006+03:00.png)

![Education view in blog post](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:45:54,691024846+03:00.png)

__комментарий__ : Я изменил синтаксис в файле index.md, где написано «Education».


## Сделать пост по прошедшей неделе.
 
![Last week's events](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:46:46,822652050+03:00.png)

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:47:08,944009274+03:00.png)
 
## Добавить пост на тему по выбору:
   **Я решил написать о CI/CD**
   
  Управление версиями. Git
        
- Непрерывная интеграция и непрерывное развертывание (CI/CD).

![CI/CD](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:47:26,600536080+03:00.png)

![CI/CD](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:47:31,931244116+03:00.png)

![CI/CD](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/project-personal/stage2/report/image/2024-03-15T20:47:37,163780295+03:00.png)

# Выводы

Я научился загружать свою информацию в сообщение в блоге. Я также понял, что такое CI/CD.

# Список литературы{.unnumbered}

::: {#refs}
:::
