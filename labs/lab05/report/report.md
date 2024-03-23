---
## Front matter
title: "Лабораторная работа № 5"
subtitle: "Менеджер паролей pass"
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



# Задание

- Менеджер паролей pass — программа, сделанная в рамках идеологии Unix.
- Также носит название стандартного менеджера паролей для Unix (The standard Unix password manager).

# 

# Выполнение лабораторной работы

Менеджер паролей pass

Установка

    Fedora

       pass

      ``dnf install pass pass-otp``
        
 ![   dnf install pass pass-otp](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228710_x.jpg)

      gopass

       ``dnf install gopass``
            
![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228718_x.jpg)

Настройка

    Ключи GPG

        Просмотр списка ключей:

        gpg --list-secret-keys

![gpg --list-secret-keys](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228721_x.jpg)

        
    Инициализация хранилища

        Инициализируем хранилище:

        pass init <gpg-id or email>

![pass init <gpg-id or email>](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228726_x.jpg) 

    Синхронизация с git

        Создадим структуру git:

        pass git init
        
![pass git init](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228727_x.jpg)

        Также можно задать адрес репозитория на хостинге (репозиторий необходимо предварительно создать):

        pass git remote add origin git@github.com:<git_username>/<git_repo>.git
        
![pass git remote add origin git@github.com:<git_username>/<git_repo>.git](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228729_x.jpg)

        Для синхронизации выполняется следующая команда:

        pass git pull
        pass git push

![pass git pull](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228731_m.jpg)

        Прямые изменения
            Следует заметить, что отслеживаются только изменения, сделанные через сам gopass (или pass).

            Если изменения сделаны непосредственно на файловой системе, необходимо вручную закоммитить и выложить изменения:

            cd ~/.password-store/
            git add .
            git commit -am 'edit manually'
            git push

![.password-store](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228732_x.jpg)

            Проверить статус синхронизации модно командой

            pass git status

![pass git status](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228733_x.jpg)

Настройка интерфейса с броузером

    Для взаимодействия с броузером используется интерфейс native messaging.
    Поэтому кроме плагина к броузеру устанавливается программа, обеспечивающая интерфейс native messaging.

    Плагин browserpass
        Репозиторий: https://github.com/browserpass/browserpass-extension
  
![browserpass-extension](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228737_x.jpg)
        
        Плагин для брoузера
            Плагин для Firefox: https://addons.mozilla.org/en-US/firefox/addon/browserpass-ce/.
            Плагин для Chrome/Chromium: https://chrome.google.com/webstore/detail/browserpass-ce/naepdomgkenhinolocfifgehidddafch.

        Интерфейс для взаимодействия с броузером (native messaging)
            Репозиторий: https://github.com/browserpass/browserpass-native

            Gentoo:

            emerge www-plugins/browserpass

            Fedora

            dnf copr enable maximbaz/browserpass
        
![dnf copr enable maximbaz/browserpass](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228734_x.jpg)
            
            dnf install browserpass

![dnf install browserpass](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228735_x.jpg) 

Сохранение пароля

    Добавить новый пароль

        Выполните:

        pass insert [OPTIONAL DIR]/[FILENAME]
        
![pass insert](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228739_x.jpg)

            OPTIONAL DIR: необязательное имя каталога, определяющее файловую структуру для вашего хранилища паролей;
            FILENAME: имя файла, который будет использоваться для хранения пароля.

        Отобразите пароль для указанного имени файла:

        pass [OPTIONAL DIR]/[FILENAME]
 
![pass](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228740_x.jpg)

        Замените существующий пароль:

        pass generate --in-place FILENAME
        
![pass generate --in-place FILENAME](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228741_x.jpg)

Управление файлами конфигурации

Дополнительное программное обеспечение

    Установите дополнительное программное обеспечение:

    sudo dnf -y install \
         dunst \
         fontawesome-fonts \
         powerline-fonts \
         light \
         fuzzel \
         swaylock \
         kitty \
         waybar swaybg \
         wl-clipboard \
         mpv \
         grim \
         slurp

![программное обеспечение](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228742_x.jpg)

    Установите шрифты:

    sudo dnf copr enable peterwu/iosevka
    
![sudo dnf copr enable peterwu/iosevka](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228744_x.jpg)    
    
    sudo dnf search iosevka
    sudo dnf install iosevka-fonts iosevka-aile-fonts iosevka-curly-fonts iosevka-slab-fonts iosevka-etoile-font iosevka-term-fonts

![](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228746_x.jpg)

Установка

    Установка бинарного файла. Скрипт определяет архитектуру процессора и операционную систему и скачивает необходимый файл:

        с помощью wget:

        sh -c "$(wget -qO- chezmoi.io/get)"

![sh -c "$(wget -qO- chezmoi.io/get)"](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228748_x.jpg)

Создание собственного репозитория с помощью утилит

    Будем использовать утилиты командной строки для работы с github.

    Создадим свой репозиторий для конфигурационных файлов на основе шаблона:

    gh repo create dotfiles --template="yamadharma/dotfiles-template" --private
    
![gh repo create dotfiles --template="yamadharma/dotfiles-template" --private](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228751_x.jpg)    

Подключение репозитория к своей системе

    Инициализируйте chezmoi с вашим репозиторием dotfiles:

    chezmoi init git@github.com:<username>/dotfiles.git

![chezmoi init git@github.com:<username>/dotfiles.git](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228752_x.jpg)    

    Проверьте, какие изменения внесёт chezmoi в домашний каталог, запустив:

    chezmoi diff
    
![chezmoi diff](/home/lchileshe/work/study/2023-2024/Операционные системы/os-intr/labs/lab05/report/image/photo_6030412634144228753_x.jpg)    

    Если вас устраивают изменения, внесённые chezmoi, запустите:

    chezmoi apply -v

Использование chezmoi на нескольких машинах

    На второй машине инициализируйте chezmoi с вашим репозиторием dotfiles:

    chezmoi init https://github.com/<username>/dotfiles.git

    Или через ssh:

    chezmoi init git@github.com:<username>/dotfiles.git

    Проверьте, какие изменения внесёт chezmoi в домашний каталог, запустив:

    chezmoi diff

    Если вас устраивают изменения, внесённые chezmoi, запустите:

    chezmoi apply -v

    Если вас не устраивают изменения в файле, отредактируйте его с помощью:

    chezmoi edit file_name

    Также можно вызвать инструмент слияния, чтобы объединить изменения между текущим содержимым файла, файлом в вашей рабочей копии и измененным содержимым файла:

    chezmoi merge file_name

    При существующем каталоге chezmoi можно получить и применить последние изменения из вашего репозитория:

    chezmoi update -v

Настройка новой машины с помощью одной команды

    Можно установить свои dotfiles на новый компьютер с помощью одной команды:

    chezmoi init --apply https://github.com/<username>/dotfiles.git

    Через ssh:

    chezmoi init --apply git@github.com:<username>/dotfiles.git

Ежедневные операции c chezmoi

    Извлеките последние изменения из репозитория и примените их

        Можно извлечь изменения из репозитория и применить их одной командой:

        chezmoi update

        Это запускается git pull --autostash --rebase в вашем исходном каталоге, а затем chezmoi apply.

    Извлеките последние изменения из своего репозитория и посмотрите, что изменится, фактически не применяя изменения

        Выполните:

        chezmoi git pull -- --autostash --rebase && chezmoi diff

        Это запускается git pull --autostash --rebase в вашем исходном каталоге, а chezmoi diff затем показывает разницу между целевым состоянием, вычисленным из вашего исходного каталога, и фактическим состоянием.

        Если вы довольны изменениями, вы можете применить их:

        chezmoi apply

    Автоматически фиксируйте и отправляйте изменения в репозиторий
        Можно автоматически фиксировать и отправлять изменения в исходный каталог в репозиторий.
        Эта функция отключена по умолчанию.

        Чтобы включить её, добавьте в файл конфигурации ~/.config/chezmoi/chezmoi.toml следующее:

        [git]
            autoCommit = true
            autoPush = true

        Всякий раз, когда в исходный каталог вносятся изменения, chezmoi фиксирует изменения с помощью автоматически сгенерированного сообщения фиксации и отправляет их в ваш репозиторий.
        Будьте осторожны при использовании autoPush. Если ваш репозиторий dotfiles является общедоступным, и вы случайно добавили секрет в виде обычного текста, этот секрет будет отправлен в ваш общедоступный репозиторий.

# Выводы

Здесь кратко описываются итоги проделанной работы.

# Список литературы{.unnumbered}

::: {#refs}
:::
