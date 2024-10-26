---
## Front matter
title: "Отчёт по лабораторной работе"
subtitle: "Лаб 8"
author: "Аристид Жан Лоэнс Аристобуль"

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
mainfont: Calibri
romanfont: Calibri
sansfont: Calibri
monofont: Calibri
mathfont: Calibri
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Освоить на практике применение режима однократного гаммирования на примере кодирования различных исходных текстов одним ключом

# Задание

Два текста кодируются одним ключом (однократное гаммирование).
Требуется не зная ключа и не стремясь его определить, прочитать оба текста. Необходимо разработать приложение, позволяющее шифровать и дешифровать тексты P1 и P2 в режиме однократного гаммирования. Приложение должно определить вид шифротекстов C1 и C2 обоих текстов P1 и P2 при известном ключе ; Необходимо определить и выразить аналитически способ, при котором злоумышленник может прочитать оба текста, не зная ключа и не стремясь его определить

# Выполнение лабораторной работы

Здесь мы представляем открытые тексты P1 и P2 на шестнадцатеричном представлении (рис. [-@fig:001]).

![шестнадцатеричное представление](image/img01.png){#fig:001 width=70%}

Здесь генераваный ключ шифроврания случайным образом (рис. [-@fig:002]).

![Random Key](image/img02.png){#fig:002 width=70%}

Здесь мы представляем открытыe тексты в двойчном представлении (рис. [-@fig:003]).

![Двойчное представление](image/img03.png){#fig:003 width=70%}

Функция xor_16bit_strings() реализирует операция сложение по модулю 2 чтобы шифровать тексты. (рис. [-@fig:004]).

![Зашифрованный текст](image/img04.png){#fig:004 width=70%}

Здесь у нас дешифрованные тексты в двойчном представлении. (рис. [-@fig:005]).

![Дешифрованный текст в двойчом представлении](image/img05.png){#fig:005 width=70%}

Здесь Мы получили сообщение после дешифрования (рис. [-@fig:006]).

![дешифрованный текст](image/img06.png){#fig:006 width=70%}

Мы исползуем другой метод без знания ключа что дешифровать. (рис. [-@fig:007]).

![Новый Ключ](image/img07.png){#fig:007 width=70%}

# Выводы

В ходе этой лабораторной работы мы изучили хороший метод криптографии для отправки сообщений, которые могут быть поняты только теми, у кого есть ключ дешифрования.
