---
## Front matter
title: "Лабораторная работа №4"
subtitle: "Архитектура Компьютера"
author: "Овчинников Антон Григорьвич"

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
Освоить процедуры компиляции и сборки программ, написанных на ассемблере NASM.

# Задание
Сделать отчет.

# Теоретическое введение

Взаимодействие этих устройств осуществляется через общую шину, к которой они подклю-
чены. Физически шина представляет собой большое количество проводников, соединяющих
устройства друг с другом. В современных компьютерах проводники выполнены в виде элек-
тропроводящих дорожек на материнской (системной) плате.
Основной задачей процессора является обработка информации, а также организация
координации всех узлов компьютера. В состав центрального процессора (ЦП) входят
следующие устройства:
• арифметико-логическое устройство (АЛУ) — выполняет логические и арифметиче-
ские действия, необходимые для обработки информации, хранящейся в памяти;
• устройство управления (УУ) — обеспечивает управление и контроль всех устройств
компьютера;
• регистры — сверхбыстрая оперативная память небольшого объёма, входящая в со-
став процессора, для временного хранения промежуточных результатов выполнения
инструкций; регистры процессора делятся на два типа: регистры общего назначения и
специальные регистры.
Для того, чтобы писать программы на ассемблере, необходимо знать, какие регистры
процессора существуют и как их можно использовать. Большинство команд в программах
написанных на ассемблере используют регистры в качестве операндов. Практически все
команды представляют собой преобразование данных хранящихся в регистрах процессора,
это например пересылка данных между регистрами или между регистрами и памятью, пре-
образование (арифметические или логические операции) данных хранящихся в регистрах.

# Выполнение лабораторной работы

1. Создаю и открываю текстовый файл для дальнейшей работы. (рис. @fig:fig001)

![Создание файла](image/4laba1skrin.png){#fig:fig001 width=70%}

2. Ввожу в файл следующий текст. (рис. @fig:fig010)

![Введенный текст](image/4laba2skrin.png){#fig:fig010 width=70%}

3. Компилирую исходный файл hello.asm в obj.o. (рис. @fig:fig0110)

![Созданные файлы](image/4laba3skrin.png){#fig:fig0110 width=70%}

4. Запускаю на выполнение созданный исполняемый файл. (рис. @fig:fig01010) 

![Выполение нужных для компоновки команд](image/4laba4skrin.png){#fig:fig01010 width=70%}

# Выполнение заданий для самостоятельной работы

1. Создаю копию файла с другим именем и вывожу на экран свою имя и фамилию, после выполняю компоновку файла. (рис. @fig:fig01111)

![Компоновка обьектного файла и его запуск](image/samrabota2.png){#fig:fig01111 width=70%}

2. Копирую файлы hello.asm и lab4.asm в мой локальный репозиторий. (рис. @fig:fig1111)

![Перемещение файлов](image/samrabota4.png){#fig:fig1111 width=70%}

3. Загружаю файлы на github. (рис. @fig:fig00111)

![Проверка файлов](image/samrabota5.png){#fig:fig00111}

# Листинги 

```asm
SECTION .data
	hello:      db "Hello, world!",0xa 
		helloLen:   equ $ - hello
SECTION .text
	global _start 

_start:
        mov eax, 4      
        mov ebx, 1    
        mov ecx, hello
        mov edx, helloLen
        int 0x80        
	
	mov eax, 1
        mov ebx, 0      
        int 0x80  

SECTION .data
	hello:      db "Антон Овчинников",0xa 
		helloLen:   equ $ - hello
SECTION .text
	global _start

_start:
        mov eax, 4      
        mov ebx, 1    
        mov ecx, hello
        mov edx, helloLen
        int 0x80        
	
	mov eax, 1
        mov ebx, 0      
        int 0x80        
```

# Выводы

Я освоил процедуры компиляции и сборки программ, написанных на ассемблере NASM.


