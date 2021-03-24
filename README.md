# Название семестровой работы

![Build status](https://github.com/Algorithms-and-Data-Structures-2021/semester-work-template/actions/workflows/cmake.yml/badge.svg)

_Краткое описание семестрового проекта._

## Команда "название команды"

| ФИО участника | Вклад (%) |
| :---          |   ---:    |
| Участник №1   | 50        |
| Участник №2   | 25        |
| Участник №3   | 25        |

_Девиз: "Наши цели ясны. Задачи определены. За работу, товарищи!"_

## Структура проекта

_Описание основных частей семестрового проекта._

Проект состоит из следующих частей:
- [`benchmarks`](benchmarks) - контрольные тесты производительности структуры данных (операции добавления, удаления, поиска и пр.);
- [`examples`](examples) - примеры работы со структурой данных (желательно предоставить решение какой-либо задачи);
- [`dataset`](dataset) - набор данных для запуска контрольных тестов;
- [`tests`](tests) - модульные и IO тесты.

## Требования

_В этом разделе задаются требования к программному и аппаратному обеспечению для успешного запуска проекта._

1. С++ компилятор c поддержкой стандарта C++17 (например, _GNU GCC 8.x.x_ и выше).
2. Система автоматизации сборки _CMake_ (версия _3.5.x_ и выше).
3. Интерпретатор Python (версия _3.7.x_ и выше).
4. Рекомендуемый объем оперативной памяти - не менее 4 ГБ.
5. Свободное дисковое пространство объемом ~ 1 ГБ (набор данных для контрольных тестов).

## Как собрать и запустить проект?

_Инструкция сборки проекта, генерации тестовых данных, запуска контрольных тестов и примеров работы._

_Постарайтесь написать инструкцию так, чтобы незнакомый с проектом человек смог самостоятельно всё запустить._

**Пример (Windows)**

Склонируйте проект к себе на компьютер через [Git Bash](https://gitforwindows.org/) (либо используйте встроенные средства среды разработки):
```shell
git clone https://github.com/Algorithms-and-Data-Structures-2021/semester-work-template.git
```

Сборка *CMake* проекта в терминале (из папки проекта):
```shell
cd <project-dir>
mkdir -p build && cd build && cmake .. && cmake --build .
```

Генерация тестового набора данных в формате [comma-seperated values (CSV)](https://en.wikipedia.org/wiki/Comma-separated_values):
```shell
cd dataset && python generate_csv_bench_dataset [args ...] --out remove_bench_dataset.csv
```

Возможные аргументы:
- `--samples` - кол-во генерируемых элементов;
- `--out` - название выходного файла;
- и т.д.

Запуск контрольных тестов:


## Источники

_Список использованных при реализации структуры данных источников._

_**Это не плагиат, это уважение чужого труда и помощь своим сокурсникам более подробно разобраться в теме.**_
