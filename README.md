# Название семестровой работы

![Build status](https://github.com/Algorithms-and-Data-Structures-2021/semester-work-template/actions/workflows/cmake.yml/badge.svg)

_Краткое описание семестрового проекта. Следует отразить информацию по следующим пунктам:_
- _Какая структура данных реализуется?_ 
- _Что она из себя представляет (сбалансированное дерево, линейный список и пр.)?_
- _Где и как она используется (приложения)?_
- _Какие операции над ней можно выполнять (поиск, удаление, добавление, вставка и пр.)?_
- _Какова теоретическая сложность операций (поиск за `O(log(n))`, вставка за `O(n^2)` и т.д.)?_

## Команда "название команды"

_Заполните таблицу с указанием вклада каждого из участников в проект._

| ФИО участника | Вклад (%) | Прозвище     |
| :---          |   ---:    |  ---:        |
| Участник №1   | 50        |  _босс_        |
| Участник №2   | 30        |  _потрошитель памяти_ |
| Участник №3   | 20        |  _самозванец_  |

_Девиз команды (проекта): "Наши цели ясны. Задачи определены. За работу, товарищи!"_

## Структура проекта

_Описание основных частей семестрового проекта._

Проект состоит из следующих частей:
- [`benchmarks`](benchmarks) - контрольные тесты производительности структуры данных (операции добавления, удаления, поиска и пр.);
- [`examples`](examples) - примеры работы со структурой данных (желательно предоставить решение какой-либо задачи);
- [`dataset`](dataset) - набор данных для запуска контрольных тестов;
- [`tests`](tests) - модульные и IO тесты.

## Требования (prerequisites)

_В этом разделе задаются требования к программному и аппаратному обеспечению._

### Пример
1. С++ компилятор c поддержкой стандарта C++17 (например, _GNU GCC 8.x.x_ и выше).
2. Система автоматизации сборки _CMake_ (версия _3.5.x_ и выше).
3. Интерпретатор _Python_ (версия _3.7.x_ и выше).
4. Рекомендуемый объем оперативной памяти - не менее 4 ГБ.
5. Свободное дисковое пространство объемом ~ 1 ГБ (набор данных для контрольных тестов).

## Сборка и запуск

_Инструкция по сборке проекта, генерации тестовых данных, запуска контрольных тестов и примеров работы._

_Постарайтесь написать инструкцию так, чтобы незнакомый с проектом человек смог самостоятельно всё запустить._

### Пример (Windows)

#### Сборка проекта

Склонируйте проект к себе на компьютер через [Git for Windows](https://gitforwindows.org/) (либо используйте встроенные средства среды разработки):
```shell
git clone https://github.com/Algorithms-and-Data-Structures-2021/semester-work-template.git
```

Сборка проекта осуществляется средствами [*CMake*](https://cmake.org/). Используйте встроенные возможности среды разработки (IDE) либо произведите ручную сборку через терминал:
```shell
# переход в папку с проектом
cd C:\Users\AlgoDude\Projects\semester-work-template

# создание папки для файлов сборки (чтобы не засорять папку с проектом) 
mkdir -p build && cd build 

# сборка проекта
cmake .. -DCMAKE_BUILD_TYPE=RelWithDebInfo && cmake --config RelWithDebInfo --build . 
```

#### Генерация тестовых данных

_Подробно опишите формат хранения (JSON, XML, CSV, YAML и пр.) и процесс генерации тестовых данных._

Генерация тестового набора данных в формате [comma-seperated values (CSV)](https://en.wikipedia.org/wiki/Comma-separated_values):
```shell
cd dataset && python generate_csv_bench_dataset [args ...] --out remove_bench_dataset.csv
```

Возможные аргументы генератора данных:
- `--samples` - кол-во генерируемых элементов;
- `--out` - название выходного файла;
- и т.д.

Тестовые данные представлены в CSV формате, каждая строка в файле формирует сущность с полями `id`, `full_name`, и пр.:
```csv
id, full_name
0, "Ramil Safin"
1, "Bulat Abbyasov"
2, "Artur Shafikov"
...
```

#### Контрольные тесты (benchmarks)

_Опишите, как запустить контрольные тесты, что они из себя представляют, какие метрики замеряют (время работы, потребление памяти и пр.)._

Для запуска контрольных тестов необходимо предварительно сгенерировать или скачать готовый набор тестовых данных.

**Примечание**. Можете указать здесь ссылку на _zip_-архив с набором данных. Подготовленные наборы данных должны находиться в папке семестровой работы на Google Drive.

## Источники

_Список использованных при реализации структуры данных источников._

_**Это не плагиат, это уважение чужого труда и помощь своим сокурсникам более подробно разобраться в теме.**_

### Пример
1. [Википедия](https://ru.wikipedia.org/wiki/%D0%A1%D1%82%D1%80%D1%83%D0%BA%D1%82%D1%83%D1%80%D0%B0_%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85)
2. [YouTube](https://www.youtube.com/results?search_query=data+structures)
