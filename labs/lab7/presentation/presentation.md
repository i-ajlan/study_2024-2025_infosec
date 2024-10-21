---
## Front matter
lang: ru-RU
title: Презентация Лаб 7
subtitle: Лаб 7
author:
  - Аристид Ж. Л.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 19 октобря 2024

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
  - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}

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
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- Аристид Жан Л. А.
- Студент
- Российский университет дружбы народов

:::
::::::::::::::

# Вводная часть

## Объект и предмет исследования

- Криптография
- Однократное гаммирование
- Сложение по моделю 2

## Цели и задачи

-Освоить на практике применение режима однократного гаммирования1

# Определение

- Гаммирование представляет собой наложение (снятие) на открытые (зашифрованные) данные последовательности элементов других данных, полученной с помощью некоторого криптографического алгоритма, для получения зашифрованных (открытых) данных.

# Этапы алгоритмы криптографии

- Представить Открытый тектс на двойчном представлении
- Генеровать ключ шифрования случайном образом
- Сложение по модулью 2

## Итоговый слайд

- В ходе этой лабораторной работы мы изучили хороший метод криптографии для отправки сообщений, которые могут быть поняты только теми, у кого есть ключ дешифрования.
