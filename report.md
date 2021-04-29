---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №2"
subtitle: "управление версиями"
author: "Анна Ломакина"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить идеологию и применение средств контроля версий.

# Задание
## 1.Настройка git
1. Создайте учётную запись на https://github.com.
2. Настройте систему контроля версий git, как это описано выше c использованием
сервера репозиториев https://github.com/.
3. Создайте структуру каталога лабораторных работ согласно пункту М.2.
## 2. Подключение репозитория к github
1. Создайте репозиторий на GitHub. Для примера назовём его os-intro.
2. Рабочий каталог будем обозначать как laboratory. Вначале нужно перейти в этот
каталог:
cd laboratory
3. Инициализируем системы git:
git init
4. Создаём заготовку для файла README.md:
echo "# Лабораторные работы" >> README.md
git add README.md
5. Делаем первый коммит и выкладываем на github:
git commit -m "first commit"
git remote add origin git@github.com:<username>/sciproc-intro.git
git push -u origin master
## 3. Первичная конфигурация
1. Добавим файл лицензии:
wget https://creativecommons.org/licenses/by/4.0/legalcode.txt
↪ -O LICENSE
2. Добавим шаблон игнорируемых файлов. Просмотрим список имеющихся шаблонов:
curl -L -s https://www.gitignore.io/api/list
Затем скачаем шаблон, например, для C:
curl -L -s https://www.gitignore.io/api/c >> .gitignore
Можно это же сделать через web-интерфейс на сайте https://www.gitignore.
io/.
3. Добавим новые файлы:
git add .
4. Выполним коммит:
git commit -a
5. Отправим на github:
git push
## 4. Конфигурация git-flow
1. Инициализируем git-flow
git flow init
Префикс для ярлыков установим в v.
2. Проверьте, что Вы на ветке develop:
git branch
3. Создадим релиз с версией 1.0.0
Кулябов Д. С. и др. Операционные системы 21
git flow release start 1.0.0
4. Запишем версию:
echo "1.0.0" >> VERSION
5. Добавим в индекс:
git add .
git commit -am 'chore(main): add version'
5. Зальём релизную ветку в основную ветку
git flow release finish 1.0.0 
5. Отправим данные на github
git push --all
git push --tags
6. Создадим релиз на github.

# Выполнение лабораторной работы
Создаем учётную запись на https://github.com,настраиваем систему контроля версий git,с помощью сервера репозиториев https://github.com/.Создаем структуру каталога лабораторных работ.
- Cоздаем репозиторий labaOS на Github.
- Рабочий каталог будем обозначать как laboratory.Вначале нужно перейти в этот каталог: cd laboratory
- Инициализируем системы git:git init
- Создаем заготовку для файла README.md: echo"# Лабораторные работы">>README.md 

![] (image/1.jpg)

- Делаем первый коммит и выкладываем на github

![](image/1.jpg)


- Добавим шаблон игнорируемых файлов.Просмотрим список имеющихся шаблонов:curl -l -s ,затем скачали шаблон например для C:curl -L -s >> .gitignore.Можно это же сделать через web-интерфейс на сайте

![](image/1.jpg)


- Добавим новые файлы,выполним коммит,отправим на github

![](image/1.jpg)


- Инициализируем git-flow

- Инициализируем git-init

- Префикс для ярлыков - v

- Создаем релиз с версией 1.0.0

 ![](image/2.jpg)


- Отправляем данные на github,cоздаем релиз.

![](image/3.jpg)


# Выводы
Я поняла как работать с репозиториями и Github.