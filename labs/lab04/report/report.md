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

Получение навыков правильной работы с репозиториями git.


# Задание

1. Установка программного обеспечения
2. Установка Node.js
3. Настройка Node.js 
4. Общепринятые коммиты

# Теоретическое введение

Git — это распределенная система контроля версий, которая произвела революцию в способах управления и совместной работы разработчиков над программными проектами. Это позволяет нескольким людям одновременно работать над одной базой кода, что упрощает отслеживание изменений, управление версиями и совместную работу в распределенной среде. Чтобы эффективно работать с репозиториями Git, необходимо понимать его основные концепции, команды и рабочие процессы. Целью этого теоретического введения является предоставление учащимся фундаментальных знаний, необходимых для уверенной и эффективной навигации по репозиториям Git.

### Основные понятия Git

  __Репозитории__ : сердце любого проекта Git. Репозиторий содержит все файлы, историю, ветки и коммиты, связанные с проектом.
  __Коммиты__ : снимки состояния проекта в определенный момент времени. Каждый коммит уникально идентифицируется и содержит информацию о внесенных изменениях и авторе этих изменений.
    
  __Ветки__ : параллельные версии проекта, которые позволяют разработчикам одновременно работать над различными функциями или исправлениями, не затрагивая основную базу кода.
    
  __Слияния__ : процесс интеграции изменений из одной ветки в другую, обычно в главную ветку.
   
  __Клонирование__ : действие по созданию локальной копии удаленного репозитория для работы.
    
  __Извлечение__ : обновление локального репозитория изменениями из удаленного репозитория.
    
  __Pushing__ : отправка локальных коммитов в удаленный репозиторий.

### Основные команды Git

-    git init: инициализирует новый репозиторий Git.
-    git clone: ​​создает локальную копию удаленного репозитория.
-    git add: добавляет изменения в промежуточную область, подготавливая их к фиксации.
-    git commit: сохраняет изменения в локальном репозитории.
-    git status: показывает статус изменений в рабочем каталоге и промежуточной области.
-    git ветка: перечисляет, создает или удаляет ветки.
-    git checkout: переключает между ветками или коммитами.
-    git merge: объединяет изменения из одной ветки в другую.
-    git pull: извлекает изменения из удаленного репозитория и объединяет их в текущую ветку.
-    git push: отправляет локальные коммиты в удаленный репозиторий.
# Выполнение лабораторной работы

1. Установка программного обеспечения:

   Установка git-flow

  __Enable the copr repository__
     dnf copr enable elegos/gitflow
  __Install gitflow__
     dnf install gitflow

![Enable the copr repository](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T12:57:09,892858139+03:00.png)

![Install gitflow](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:39:40,449621577+03:00.png)

2. Установка Node.js

   На Node.js базируется программное обеспечение для семантического версионирования и общепринятых коммитов.
   
![Node.js](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:40:32,882661839+03:00.png) 
 
  __Комментарий__ :Я установил Node.js с помощью команды ``dnf install nodejs``
  
![pnpm](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:41:01,843453230+03:00.png) 

![pnpm](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:42:24,979214793+03:00.png)

   __Комментарий__ :Я скачал pnpm из интернета
   
3. Настройка Node.js 

   Для работы с Node.js добавим каталог с исполняемыми файлами, устанавливаемыми yarn, в переменную PATH.

![pnpm setup](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:43:06,382703097+03:00.png) 


4. Общепринятые коммиты

  - commitizen:
   Данная программа используется для помощи в форматировании коммитов.
   
![pnpm add -g commitizen](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:43:47,826431510+03:00.png)

  - standard-changelog
  Данная программа используется для помощи в создании логов.
  
![pnpm add -g standard-changelog](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:44:23,957594545+03:00.png) 
  
  - Практический сценарий использования git 
  
   Создание репозитория git

    Подключение репозитория к github

       я создал репозиторий на GitHub. Для примера назовём его git-extended.

![git-extended](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:45:47,552395654+03:00.png)

       Делаем первый коммит и выкладываем на github:
       
![git commit ](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:46:58,585498352+03:00.png)

    
   - Конфигурация общепринятых коммитов
   
     Конфигурация для пакетов Node.js
   
![ Конфигурация для пакетов](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:47:47,497036306+03:00.png)




Необходимо заполнить несколько параметров пакета.

    Название пакета.
    Лицензия пакета. Список лицензий для npm: https://spdx.org/licenses/. Предлагается выбирать лицензию CC-BY-4.0.

Сконфигурим формат коммитов. Для этого добавим в файл package.json команду для формирования коммитов:

"config": {
    "commitizen": {
        "path": "cz-conventional-changelog"
    }
}

Таким образом, файл package.json приобретает вид:

{
    "name": "git-extended",
    "version": "1.0.0",
    "description": "Git repo for educational purposes",
    "main": "index.js",
    "repository": "git@github.com:username/git-extended.git",
    "author": "Name Surname <username@gmail.com>",
    "license": "CC-BY-4.0",
    "config": {
        "commitizen": {
            "path": "cz-conventional-changelog"
        }
    }    
}

  - Добавим новые файлы:

     git add .

  - Выполним коммит:

     git cz

![заполнение параметров пакета.](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:49:06,733744923+03:00.png)


 - Конфигурация git-flow

    Инициализируем git-flow
    
![git flow init](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:50:14,579768439+03:00.png) 

 - Проверьте, что Вы на ветке develop:
 
![git branch](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:50:56,682805337+03:00.png) 

 - Загрузите весь репозиторий в хранилище

![git push --all](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:52:17,545621419+03:00.png)

 - Установите внешнюю ветку как вышестоящую для этой ветки: 
 
![git branch --set-upstream-to=origin/develop develop](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:54:36,157991851+03:00.png) 

 - Создадим релиз с версией 1.0.0
 
![git flow release start 1.0.0](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:55:00,782400922+03:00.png) 

 - Создадим журнал изменений

![standard-changelog --first-release](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:56:00,008526998+03:00.png)

 - Добавим журнал изменений в индекс
 
![git add](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:56:47,801774007+03:00.png) 

 - Зальём релизную ветку в основную ветку
 
![git flow release finish 1.0.0](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-08T23:58:28,855476346+03:00.png) 

 - Отправим данные на github

   git push --all

![git push --all](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:00:17,054387778+03:00.png)

   git push --tags
   
![git push --tags](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:00:49,716430975+03:00.png) 

 - Создадим релиз на github. Для этого будем использовать утилиты работы с github
 
![gh release create v1.0.0 -F CHANGELOG.md](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:01:50,714270274+03:00.png)

#### Работа с репозиторием git

      Разработка новой функциональности

        Создадим ветку для новой функциональности

![git flow feature start feature_branch](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:03:13,975629423+03:00.png) 


 - Далее, продолжаем работу c git как обычно.

 - По окончании разработки новой функциональности следующим шагом следует объединить ветку feature_branch c develop

![git flow feature finish feature_branch](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:06:26,727877703+03:00.png)


#### Создание релиза git-flow

     Создадим релиз с версией 1.2.3:
    
![git flow release start 1.2.3](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:07:01,876579230+03:00.png)

 - Создадим журнал изменений
 
![standard-changelog](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:08:14,476558797+03:00.png) 

 - Добавим журнал изменений в индекс

![git add CHANGELOG.md](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:08:58,910483624+03:00.png)

 - Зальём релизную ветку в основную ветку
 
![git flow release finish 1.2.3](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:10:15,259143688+03:00.png) 

 - Отправим данные на github

  git push --all

![  git push --all](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:10:36,194539122+03:00.png) 

  git push --tags
  
![git push --tags](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T00:10:58,355938969+03:00.png) 
  
 - Создадим релиз на github с комментарием из журнала изменений
 
![gh release create v1.2.3 -F CHANGELOG.md](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/report/image/2024-03-09T02:07:17,840611374+03:00.png) 


# Выводы

Я получил навыки корректной работы с git-репозиториями.

# Список литературы{.unnumbered}

::: {#refs}
:::
