---
## Front matter
title: "Отчёт по лабораторной работе"
subtitle: "Лаб 7"
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

Освоить на практике применение режима однократного гаммирования1

# Задание

Нужно подобрать ключ, чтобы получить сообщение «С Новым Годом, друзья!». Требуется разработать приложение, позволяющее шифровать и дешифровать данные в режиме однократного гаммирования. Приложение должно:

1. Определить вид шифротекста при известном ключе и известном открытом тексте.
2. Определить ключ, с помощью которого шифротекст может быть преобразован в некоторый фрагмент текста, представляющий собой один из возможных вариантов прочтения открытого текста.

# Выполнение лабораторной работы

Здесь мы представляем открытый текст на шестнадцатеричном представлении (рис. [-@fig:001]).

![шестнадцатеричное представление](image/img01.png){#fig:001 width=70%}

Здесь генераваный ключ шифроврания случайным образом (рис. [-@fig:002]).

![Random Key](image/img02.png){#fig:002 width=70%}

Здесь мы представляем открытый текст двойчном представлении (рис. [-@fig:003]).

![Двойчное представление](image/img03.png){#fig:003 width=70%}

Функция xor_16bit_strings() реализирует операция сложение по модулю 2 чтобы шифровать текст. (рис. [-@fig:004]).

![Зашифрованный текст](image/img04.png){#fig:004 width=70%}

Здесь у нас дешифрованный текст в двойчном представлении. (рис. [-@fig:005]).

![Дешифрованный текст в двойчом представлении](image/img05.png){#fig:005 width=70%}

Здесь Мы получили сообщение после дешифрования (рис. [-@fig:006]).

![дешифрованный текст](image/img06.png){#fig:006 width=70%}

Мы исползуем другой ключ для дешифрования (рис. [-@fig:007]).

![Новый Ключ](image/img07.png){#fig:007 width=70%}

Здесь мы получили неправилное сообщение исползуя другой ключ для дешифрования (рис. [-@fig:008]).

![Неправилное сообщение](image/img08.png){#fig:008 width=70%}

# Выводы

В ходе этой лабораторной работы мы изучили хороший метод криптографии для отправки сообщений, которые могут быть поняты только теми, у кого есть ключ дешифрования.
