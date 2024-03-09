---
## Front matter
lang: ru-RU
title: ЛАБОРАТОРНАЯ РАБОТА 4
subtitle: Продвинутое использование git.
author:
  - Чилеше Л.
institute:
  - Российский университет дружбы народов, Москва, Россия

date: 09 марта 2024.

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


## Цели и задачи

 - Получение навыков правильной работы с репозиториями git.
 
# Установка программного обеспечения

## Установка git-flow (dnf copr enable elegos/gitflow)

- Установка из коллекции репозиториев Copr 

   Enable the copr repository
   ``dnf copr enable elegos/gitflow``

![gitflow](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T12:57:09,892858139+03:00.png)

## Install gitflow

  ``dnf install gitflow``

![gitflow](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:39:40,449621577+03:00.png) 

# Установка Node.js

## На Node.js базируется программное обеспечение для семантического версионирования и общепринятых коммитов.

![Node.js](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:40:32,882661839+03:00.png)


## установка apt-get install pnpm из Интернета

``apt-get install pnpm``

![apt-get install pnpm](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:41:01,843453230+03:00.png)

## apt-get install pnpm

![apt-get install pnpm](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:42:24,979214793+03:00.png)

# Настройка Node.js


## Для работы с Node.js добавим каталог с исполняемыми файлами, устанавливаемыми yarn, в переменную PATH.

![Настройка Node.j](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:43:06,382703097+03:00.png)

# Общепринятые коммиты

## commitizen

 - Данная программа используется для помощи в форматировании коммитов.

![commitizen](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:43:47,826431510+03:00.png)

## standard-changelog

- Данная программа используется для помощи в создании логов.

![pnpm add -g standard-changelog](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:44:23,957594545+03:00.png)

## Создание репозитория git

- Подключение репозитория к github

![git clone](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:45:47,552395654+03:00.png)

## Делаем первый коммит и выкладываем на github

![first commit](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:46:58,585498352+03:00.png)


## Конфигурация для пакетов Node.js

![pnpm init](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:47:47,497036306+03:00.png)

## Сконфигурим формат коммитов. Для этого добавим в файл package.json команду для формирования коммитов

![Конфигурация](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:49:06,733744923+03:00.png)


## Загрузите весь репозиторий в хранилище

![git push --all](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab04/presentation/image/2024-03-08T23:52:17,545621419+03:00.png)


## Заключение

- Я получил навыки корректной работы с git-репозиториями


