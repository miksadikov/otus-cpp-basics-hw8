# OTUS C++ Basic курс

## Задание "многопоточный подсчет самых частых слов"

В данном задании нужно переписать однопоточную программу, которая подсчитывает самые частые слова в файлах так,
чтобы она получила выигрыш от использования нескольких потоков.

Стратегия распараллеливания.
У каждого потока имеется свой словарь для подсчета встречаемости слов, после завершения потоков эти словари 
сливаются воедино.

## Инструкция по сборке

Требуется компилятор с поддержкой C++17

Для сборки проекта необходимo выполнить следующие команды
```
mkdir build && cd build
cmake ..
cmake --build .
```

##  Запуск программы

```
topk_words number_of_threads(1..10), topk_words(3..10), [FILES...]
```

number_of_threads - количество потоков, 
topk_words - количество отображаемых слов,
[FILES...] - список обрабатываемых текстовых файлов.

Например:
```
topk_words 5 10 64317-0.txt pg1777.txt
```
