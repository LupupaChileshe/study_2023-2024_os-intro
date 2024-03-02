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
Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.


# Теоретическое введение

Fedora Sway — это инновационный мозаичный оконный менеджер, работающий по протоколу отображения Wayland и предлагающий высокоэффективную и удобную альтернативу традиционным средам рабочего стола. Он предназначен для повышения производительности и оптимизации рабочих процессов, позволяя пользователям управлять своими приложениями в виде логической сетки, которой можно манипулировать с помощью сочетаний клавиш, что сводит к минимуму необходимость взаимодействия с мышью. Sway полностью совместим с конфигурацией оконного менеджера i3, что упрощает переход для пользователей, знакомых с i3. Эта совместимость распространяется на большинство функций i3, а также на некоторые дополнительные возможности, отвечающие потребностям композиторов Wayland, таких как Sway.

# Выполнение лабораторной работы

После установки
    • Войдите в ОС под заданной вами при установке учётной записью. 
    • Нажмите комбинацию Win+Enter для запуска терминала. 
    • Переключитесь на роль супер-пользователя:
           sudo -i
           
Я обновил все пакеты
 dnf -y update
 
 ![ dnf -y update](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142641_y.jpg)
 
![dnf -y update](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142642_y.jpg)

Повышение комфорта работы

    Программы для удобства работы в консоли:

    dnf -y install tmux mc
    
![dnf -y install tmux mc](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142644_y.jpg)   

![dnf -y install tmux mc](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142645_y.jpg)

## Автоматическое обновление
    • При необходимости можно использовать автоматическое обновление. 
    • Установка программного обеспечения:
dnf install dnf-automatic

![dnf install dnf-automatic](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/image_2024-03-01_20-08-36.jpg)

![dnf install dnf-automatic](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142652_y.jpg)

Задаёте необходимую конфигурацию в файле /etc/dnf/automatic.conf. 
    • Запустите таймер:

![таймер](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142653_x.jpg)

Отключение SELinux
    • В данном курсе мы не будем рассматривать работу с системой безопасности SELinux. 
    • Поэтому отключим его. 
    • В файле /etc/selinux/config замените значение
    
SELINUX=enforcing
на значение
SELINUX=permissive

    • Перегрузите виртуальную машину:
reboot

![SELINUX=permissive](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142654_x.jpg)

Установка драйверов для VirtualBox
    • Войдите в ОС под заданной вами при установке учётной записью. 
    • Нажмите комбинацию Win+Enter для запуска терминала. 
    • Запустите терминальный мультиплексор tmux:
tmux
    • Переключитесь на роль супер-пользователя:
sudo -i
    • Установите средства разработки:
dnf -y group install "Development Tools"

![dnf -y group install "Development Tools"](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142656_x.jpg)

![dnf -y group install "Development Tools"](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142657_x.jpg)

Установите пакет DKMS:

dnf -y install dkms

![dnf -y install dkms](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142658_x.jpg)

![dnf -y install dkms](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142660_x.jpg)
    
В меню виртуальной машины подключите образ диска дополнений гостевой ОС. 
    • Подмонтируйте диск:
    
mount /dev/sr0 /media

![mount /dev/sr0 /media](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142661_x.jpg)

Установите драйвера:

/media/VBoxLinuxAdditions.run

![/media/VBoxLinuxAdditions.run](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142662_x.jpg)

Настройка раскладки клавиатуры
    • Войдите в ОС под заданной вами при установке учётной записью. 
    • Нажмите комбинацию Win+Enter для запуска терминала. 
    • Запустите терминальный мультиплексор tmux:
    
tmux

Создайте конфигурационный файл ~/.config/sway/config.d/95-system-keyboard-config.conf:

touch ~/.config/sway/config.d/95-system-keyboard-config.conf

![95-system-keyboard-config.conf](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142663_x.jpg)

Отредактируйте конфигурационный файл ~/.config/sway/config.d/95-system-keyboard-config.conf:

exec_always /usr/libexec/sway-systemd/locale1-xkb-config --oneshot

![exec_always](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142664_x.jpg)

Переключитесь на роль супер-пользователя:

sudo -i

    • Отредактируйте конфигурационный файл /etc/X11/xorg.conf.d/00-keyboard.conf:
Section "InputClass"
        Identifier "system-keyboard"
        MatchIsKeyboard "on"
        Option "XkbLayout" "us,ru"
        Option "XkbVariant" ",winkeys"
        Option "XkbOptions" "grp:rctrl_toggle,compose:ralt,terminate:ctrl_alt_bksp"
EndSection

![00-keyboard.conf](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142666_x.jpg)

Установка имени пользователя и названия хоста
    • Если при установке виртуальной машины вы задали имя пользователя или имя хоста, не удовлетворяющее соглашению об именовании, то вам необходимо исправить это. 
    • Запустите виртуальную машину и залогиньтесь. 
    • Нажмите комбинацию Win+Enter для запуска терминала. 
    • Запустите терминальный мультиплексор tmux:
    
tmux

    • Переключитесь на роль супер-пользователя:
    
sudo -i

Установите имя хоста (вместо username укажите ваш логин в дисплейном классе):

hostnamectl set-hostname username

    • Проверьте, что имя хоста установлено верно:
    
hostnamectl

![hostnamectl](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142668_x.jpg)

Я уже создал имя пользователя при установке Fedora, поэтому создал только имя хоста.

Работа с языком разметки Markdown
    • Средство pandoc для работы с языком разметки Markdown. 
    • Установка с помощью менеджера пакетов:
    
dnf -y install pandoc

![ pandoc](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142703_x.jpg)

![pandoc](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142704_x.jpg)

![pandoc](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142706_x.jpg)

![pandoc](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142708_x.jpg)

После загрузки pandoc с github я переместил его в каталог bin.

texlive

    • Установим дистрибутив TeXlive:
    
dnf -y install texlive-scheme-full

![texlive](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142720_x.jpg)

![texlive](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab01/report/image/photo_5985773956705142721_x.jpg)


# Выводы

Я научился устанавливать Fedora Sway, а также скачивать все необходимые пакеты.

# Список литературы{.unnumbered}

::: {#refs}
:::
