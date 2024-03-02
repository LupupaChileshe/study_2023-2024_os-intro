---
## Front matter
lang: ru-RU
title: Лабораторная работа № 2
subtitle: git
author:
  - Чилеше Л.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 01 января 1970

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

- Изучить идеологию и применение средств контроля версий.
-  Освоить умения по работе с git.

## Установка git

![ git](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262352_x.jpg)


## Установка gh

 dnf install gh

![install gh](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262354_x.jpg)

# Базовая настройка git

## Установка имени и адреса электронной почты владельца репозитория

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/presentation/image/photo_5987624490609262355_x.jpg)

## Настроим utf-8 в выводе сообщений git

![utf-8 ](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/presentation/image/photo_5987624490609262357_x.jpg)

# Создание ssh-ключей

## по алгоритму rsa с ключём размером 4096 бит:

 ssh-keygen -t rsa -b 4096

![rsa 4096](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262358_x.jpg)

## по алгоритму ed25519:

 ssh-keygen -t ed25519
 
![ed25519](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5987624490609262359_x.jpg)


# Настройка автоматических подписей коммитов git

## использование введенного адреса электронной почты для указания Git

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948742_x.jpg)

# Сознание репозитория курса на основе шаблона

![репозитория курса](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948749_x.jpg)


## Настройка каталога курса

![каталога курса](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948751_x.jpg)

## Загрузка файлов на сервер

git add .
git commit -am 'feat(main): make course structure'
git push


![git push](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab02/report/image/photo_5989876290422948752_y.jpg)



