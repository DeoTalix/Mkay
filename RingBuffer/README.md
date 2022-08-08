# Сортировка с минимальным процессорным временем

__Задание:__
На языке Python 2.7 реализовать минимум по 2 класса реализовывающих циклический буфер FIFO. Объяснить плюсы и минусы каждой реализации.

__Решение:__
Кольцевой буфер, использующий `collections.deque` в качестве структуры данных и кольцевой буфер, использующий `list`.

Плюсы:
- простая реализация
- операции добавления и удаления из очереди $O(1)$
- операции добавления и удаления из очереди потоко-безопасны, так как являются атомарными.

Минусы:
- на практике блокировку многопоточности все же приходится включать для проверки переполненности массива

Тесты находятся в файле RingBuffer/tests.py
```
python2 -m unittest tests
```

---

Чтобы запустить тесты выполните:
```
python run.py
```