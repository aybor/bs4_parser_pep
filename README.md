# Парсер документации PEP
## Описание
Программа для парсинга документации со страницы https://peps.python.org/

Режимы работы:
 - Вывод информации о релизах Python (режим "whats-new")
 - Режим вывода статусов версий Python (режим "latest-versions")
 - Вывод сводной информации о статусах всех PEP (режим "pep")
 - Загрузка документации к последней версии Python (режим "download")

Текстовая информация с результатами может быть:
 - Выведена в терминал напрямую
 - Выведена в терминал в виде таблицы
 - Сохранена в виде файла .txt

## Установка

1. Клонировать репозиторий
```
git clone https://github.com/aybor/bs4_parser_pep.git
```
<br>

2. Установить зависимости
```
pip install -r requirements.txt
```
<br>

## Использование
В проекте есть встроенная подсказка по использованию аргументов командной строки:
```
python main.py -h
```
Результат:
```
usage: main.py [-h] [-c] [-o {pretty,file}]
               {whats-new,latest-versions,download,pep}

Парсер документации Python

positional arguments:
  {whats-new,latest-versions,download,pep}
                        Режимы работы парсера

optional arguments:
  -h, --help            show this help message and exit
  -c, --clear-cache     Очистка кеша
  -o {pretty,file}, --output {pretty,file}
                        Дополнительные способы вывода данных
```

* аргумент `-с` очищает кеш, при этом работа парсера занимает порядка 5 минут
* аргумент `-o` используется при необзодимости вывода в терминал в виде таблицы (`pretty`) либо в файл (`file`)
