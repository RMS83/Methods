---
title: 'Methods'
author: 'RMS83'
---

# Методы

## Методы строк:
* `String.upper()` - Возвращает строку с заглавными буквами
* `String.lower()` - Возвращает строку с малыми буквами
* `String.count(sub[, start[, end]])` - Определяет число вхождений подстроки в строке
* `String.find(sub[, start[, end]])` - Возвращает индекс первого найденного вхождения
* `String.rfind(sub[, start[, end]])` - Возвращает индекс первого найденного вхождения при поиске справа
* `String.index(sub[, start[, end]])` - Возвращает индекс первого найденного вхождения
* `String.replace(old, new, count=2)` - Заменяет подстроку old на new по количеству 2
* `String.isalpha()` - Определяет: состоит ли строка целиком из буквенных символов
* `String.isdigit()` - Определяет: состоит ли строка целиком из цифр
* `String.rjust(width[, fillchar = ‘ ‘])` - Расширяет строку, добавляя символы слева
* `String.ljust(width[, fillchar = ‘ ‘])` - Расширяет строку, добавляя символы справа
* `String.split(sep=None, maxsplit=-1)` - Разбивает строку на подстроки
* `''.join(список)` - Объединяет коллекцию в строку
* `String.strip()` - Удаляет пробелы и переносы строк справа и слева
* `String.rstrip()` - Удаляет пробелы и переносы строк справа
* `String.lstrip()` - Удаляет пробелы и переносы строк слева

## Операции (методы) с множествами:
![setDiagram&](/img/setDiagram&.png)
* ` & `, `setA.intersection(setB)` - Пересечение множест (получение только общих значений):
```Python
setA = {1, 2, 3, 4}
setB = {3, 4, 5, 6, 7}
print(setA & setB) # -> {3, 4}
print(setA.intersection(setB)) # -> {3, 4}
```
* `setA &= setB`, `setA.intersection_update(setB)` - Cоздает новое множество setA:
```Python
setA = {1, 2, 3, 4}
setB = {3, 4, 5, 6, 7}
setA &= setB # или setA.intersection_update(setB)
print(setA) # -> {3, 4}
```
![setDiagram.union](/img/setDiagram.union.png)
* ` | `, `setA.union(setB)` - Объединение множеств (получить объединенные множества с уникальными значениями):
```Python
setA = {1, 2, 3, 4}
setB = {3, 4, 5, 6, 7}
print(setA | setB) # -> {1, 2, 3, 4, 5, 6, 7}
print(setA.union(setB)) # -> {1, 2, 3, 4, 5, 6, 7}
```
* `setA |= setB` - Cоздает новое объединенное множество setA:
```Python
setA = {1, 2, 3, 4}
setB = {3, 4, 5, 6, 7}
setA |= setB
print(setA) # -> {1, 2, 3, 4, 5, 6, 7}
```
![setDiagram-](/img/setDiagram-.png)
* ` - ` `setA.difference(setB)` - вычитание множеств (вычесть пересекающиеся знаения множеств):
```Python
setA = {1, 2, 3, 4}
setB = {3, 4, 5, 6, 7}
print(setA - setB) # -> {1, 2}
print(setA.subtracting(setB)) # -> {1, 2}
```
* `setA -= setB`, `setA.difference_update(setB)` - Cоздает новое множество setA:
```Python
setA = {1, 2, 3, 4}
setB = {3, 4, 5, 6, 7}
setA -= setB # или setA.difference_update(setB)
print(setA) # -> {1, 2}
```
![setDiagram^](/img/setDiagram^.png)
* ` ^ `, `setA.symmetric_difference(setB)` - Cимметричная разность (соединить множества за исключением общего элемента):
```Python
setA = {1, 2, 3, 4}
setB = {3, 4, 5, 6, 7}
print(setA ^ setB) # -> {1, 2, 5, 6, 7}
print(setA.symmetric_difference(setB)) # -> {1, 2, 5, 6, 7}
```
* `setA ^= setA`, `setA.symmetric_difference_update(setB)` - Cоздает новое множество setA:
```Python
setA = {1, 2, 3, 4}
setB = {3, 4, 5, 6, 7}
setA ^= setB # или setA.symmetric_difference_update(setB)
print(setA) # -> {1, 2, 5, 6, 7}
```
* `setA == setB ` - Сравнение множеств происходит по кол-ву элементов и их значениям:
```Python
setA = {1, 2, 3, 4}
setB = {3, 4, 1, 2}
print(setA == setB) # -> True
```
Но если в множестве A есть элемент не входящий в множество B то:
```Python
setA = {1, 2, 24}
setB = {3, 4, 1, 2}
print(setA == setB) # -> False
print(setA > setB) # -> False
print(setA < setB) # -> False
print(setA != setB) # -> True
```
