---
## Front matter
title: "Отчёт по лабораторной работе №3"
subtitle: "Архитектура компьютера"
author: "Овчинников Антон Григорьевич"

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
Целью работы является освоение процедуры оформления отчетов с помощью легковесного
языка разметки Markdown.

# Задание

Создать отчет

# Теоретическое введение

Чтобы задать для текста полужирное начертание, заключите его в двойные звездочки:
This text is **bold**.
Чтобы задать для текста курсивное начертание, заключите его в одинарные звездочки:
This text is *italic*.
Чтобы задать для текста полужирное и курсивное начертание, заключите его в тройные
звездочки:
This is text is both ***bold and italic***.
Блоки цитирования создаются с помощью символа >:
> The drought had lasted now for ten million years, and the reign of the
terrible lizards had long since ended. Here on the Equator, in the
continent which would one day be known as Africa, the battle for existence
had reached a new climax of ferocity, and the victor was not yet in sight.
In this barren and desiccated land, only the small or the swift or the
fierce could flourish, or even hope to survive.


# Выполнение лабораторной работы
1. Я открыл терминал и перешел в каталог курса, затем обновил локальный репозиторий,скачав изменения из удаленного. (рис. @fig:fig1)

![Результат команды `git pull`](image/1пункт.png){#fig:fig1 width=70%}

2. Я перешел в каталог с шаблоном отчета по лабороторной работе №3. (рис. @fig:fig01)

![Переход в нужный каталог](image/2пункт.png){#fig:fig01 width=70%}

3. Я провел компиляцию шаблона с использованием Makefile. Для этого ввел команду `Make` (рис. @fig:fig001)

![Результат команды `Make`](image/3пункт.png){#fig:fig001 width=70%}

4. Я проверил корректность полученных файлов. (рис. @fig:fig0011)

![Проверка файлов](image/проверкакорректностифайлов.png){#fig:fig0011 width=70%}
 
5. Я удалил полученные файлы с использованием `Makefile` и проверил удаление файлов. (рис. @fig:fig0010)

![Удаление файлов](image/удалениеипроверка.png){#fig:fig0010 width=70%}

6. Я открыл файл report.md и и скомпилировал отчет с использованием Makefile. (рис. @fig:fig111)

![Открытие текстового редактора](image/5image.png){#fig:fig111 width=70%}

# Выполнение заданий для самостоятельной работы

1. Перехожу в каталог с отчетом по второй лабораторной работе. (рис. @fig:fig1111)

![Перемещение между директориями](image/samrabota1.png){#fig:fig1111 width=70%}

2. Открыл файл с шаблоном и заполнил его (рис. @fig:fig0000)

![Заполненный шаблон отчета](image/23.png){#fig:fig0000 width=70%}

3. Компилирую отчет и проверяю, что были созданы файлы. (рис.  @fig:fig0000)

![Компиляция отчета](image/1234.png){#fig:fig00000 width=70%}

4. Загружаю файлы на github. (рис.  @fig:fig000000)

![Добавление файлов на GitHub](image/12345.png){#fig:fig000000 width=70%}

# Выводы

Я освоил процедуры оформления отчетов с помощью легковесного языка разметки Markdown

