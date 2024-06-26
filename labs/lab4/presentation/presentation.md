---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №4.
subtitle: Основы информационной безопасности.
author:
  - Рогожина Н.А.
institute:
  - Российский университет дружбы народов, Москва, Россия

date: 30 марта 2024

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
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Рогожина Надежда Александровна
  * Студентка 2го курса, НКАбд-02-22
  * Компьютерные и информационные науки
  * Российский университет дружбы народов
  * [Github](https://github.com/MikoGreen/study_2023-2024_infosec)

:::
::: {.column width="30%"}

:::
::::::::::::::

# Вводная часть

## Актуальность

- Умение работать в консоли с атрибутами файлов, а также знание основ разграничения доступа в современных системах с открытым кодом на базе OC Linux значительно улучшит и упростит понимание и работу с безопасностью данных.

## Объект и предмет исследования

- Права доступа к каталогам и файлам

## Цели и задачи

- Научиться работать с правами доступа через консоль
- Понимать разницу между доступом владельца, группы, всех пользователей

# Выполнение работы

## Выполнение работы

От имени пользователя guest определите расширенные атрибуты файла `/home/guest/dir1/file1` командой `lsattr /home/guest/dir1/file1` (рис. [-@fig:001]).

![Определение атрибутов файла](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/1.png){#fig:001 width=70%}

## Выполнение работы

2. Установите командой `chmod 600 file1` на файл file1 права, разрешающие чтение и запись для владельца файла (рис. [-@fig:002]).

![Смена доступа к файлу](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/2.png){#fig:002 width=70%}

## Выполнение работы

3. Попробуйте установить на файл /home/guest/dir1/file1 расширенный атрибут a от имени пользователя guest: `chattr +a /home/guest/dir1/file1`. В ответ вы должны получить отказ от выполнения операции (рис. [-@fig:003]).

![Попытка смены атрибутов](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/3.png){#fig:003 width=70%}

## Выполнение работы

4. Зайдите на третью консоль с правами администратора либо повысьте свои права с помощью команды su. Попробуйте установить расширенный атрибут a на файл /home/guest/dir1/file1 от имени суперпользователя: `chattr +a /home/guest/dir1/file1`  (рис. [-@fig:004]).

![Смена атрибутов](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/4.png){#fig:004 width=70%}

## Выполнение работы

5. От пользователя guest проверьте правильность установления атрибута: `lsattr /home/guest/dir1/file1` (рис. [-@fig:005]).

![Проверка](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/5.png){#fig:005 width=70%}

## Выполнение работы

6. Выполните дозапись в файл file1 слова «test» командой `echo "test" /home/guest/dir1/file1`
После этого выполните чтение файла file1 командой `cat /home/guest/dir1/file1`
Убедитесь, что слово test было успешно записано в file1. (рис. [-@fig:006]).

![Дозапись в файл и вывод](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/6.png){#fig:006 width=70%}

## Выполнение работы

7. Попробуйте удалить файл file1 либо стереть имеющуюся в нём информацию командой
`echo "abcd" > /home/guest/dirl/file1`
Попробуйте переименовать файл (рис. [-@fig:007]).

![Попытка переименовать файл и переименования](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/7.png){#fig:007 width=70%}

## Выполнение работы

8. Попробуйте с помощью команды `chmod 000 file1` установить на файл file1 права, например, запрещающие чтение и запись для владельца файла. Удалось ли вам успешно выполнить указан-
ные команды? (рис. [-@fig:008]).

![Попытка смены атрибутов](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/8.png){#fig:008 width=70%}

## Выполнение работы

9. Снимите расширенный атрибут a с файла `/home/guest/dirl/file1` от имени суперпользователя командой `chattr -a /home/guest/dir1/file1`
Повторите операции, которые вам ранее не удавалось выполнить. Ваши наблюдения занесите в отчёт.
(рис. [-@fig:009], рис. [-@fig:010], рис. [-@fig:011], рис. [-@fig:012], рис. [-@fig:013])

![Смена атрибутов от имени root](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/9.png){#fig:009 width=70%}

## Выполнение работы

![Проверка](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/10.png){#fig:010 width=70%}

## Выполнение работы

![Проверка echo](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/11.png){#fig:011 width=70%}

## Выполнение работы

![Проверка echo](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/12.png){#fig:012 width=70%}

## Выполнение работы

![Проверка удаления файла](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/13.png){#fig:013 width=70%}

## Выполнение работы

После удаления, создадим файл заново (рис. [-@fig:014]):

![Проверка](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/14.png){#fig:014 width=70%}

## Выполнение работы

10. Повторите ваши действия по шагам, заменив атрибут «a» атрибутом «i». Удалось ли вам дозаписать информацию в файл? Ваши наблюдения занесите в отчёт (рис. [-@fig:015], рис. [-@fig:016], рис. [-@fig:017], рис. [-@fig:018])

![Проверка](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/15.png){#fig:015 width=70%}

## Выполнение работы

![Проверка](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/16.png){#fig:016 width=70%}

## Выполнение работы

![Проверка](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/17.png){#fig:017 width=70%}

## Выполнение работы

![Проверка](/home/narogozhina/work/study/2023-2024/Информационная безопасность/infosec/labs/lab4/report/image/18.png){#fig:018 width=70%}

# Выводы

В результате выполнения работы мы повысили свои навыки использования интерфейса командой строки (CLI), познакомились на примерах с тем, как используются основные и расширенные атрибуты при разграничении доступа. Имели возможность связать теорию дискреционного разделения доступа (дискреционная политика безопасности) с её реализацией на практике в ОС Linux. Составили наглядные таблицы, поясняющие какие операции возможны при тех или иных установленных правах. Опробовали действие на практике расширенных атрибутов «а» и «i».
