---
title: 'Methods'
author: 'RMS83'
---

# Методы

## Методы строк:
* `String.upper()` - Возвращает строку с заглавными буквами
* `String.lower()` - Возвращает строку с малыми буквами
* `String.capitalize()` - Возвращает строку с первым символов в верхнем регистре
* `String.swapcase()` - Меняет регистры у всех символов с верхних на нижние  и наоборот
* `String.title()` - Первые символы каждого слова в верхнем регистре 
* `String.count(sub[, start[, end]])` - Определяет число вхождений подстроки в строке
* `String.find(sub[, start[, end]])` - Возвращает индекс первого найденного вхождения
* `String.rfind(sub[, start[, end]])` - Возвращает индекс первого найденного вхождения при поиске справа
* `String.index(sub[, start[, end]])` - Возвращает индекс первого найденного вхождения (в отличии от find выдает ошибку если False)
* `String.rindex(sub[, start[, end]])` - Возвращает индекс последнего найденного вхождения (в отличии от rfind выдает ошибку если False)
* `String.replace(old, new, count=2)` - Заменяет подстроку old на new по количеству 2
* `String.isalpha()` - Определяет: состоит ли строка целиком из буквенных символов (возвращает True or False)
* `String.isdigit()` - Определяет: состоит ли строка целиком из цифр (возвращает True or False)
* `String.isalnum()` - Определяет: состоит ли строка целиком только из цифр и букв (возвращает True or False)
* `String.islower()` - Определяет: состоит ли строка целиком только строчных букв (возвращает True or False)
* `String.isupper()` - Определяет: состоит ли строка целиком только из заглавных букв (возвращает True or False)
* `String.rjust(width[, fillchar = ‘ ‘])` - Расширяет строку, добавляя символы слева
* `String.ljust(width[, fillchar = ‘ ‘])` - Расширяет строку, добавляя символы справа
* `String.split(sep=None, maxsplit=-1)` - Разбивает строку на подстроки
* `''.join(список)` - Объединяет коллекцию в строку
* `String.strip()` - Удаляет пробелы и переносы строк справа и слева
* `String.rstrip()` - Удаляет пробелы и переносы строк справа
* `String.lstrip()` - Удаляет пробелы и переносы строк слева

## Методы списков:
* `List.append(x)` - Добавляет объект x в конец списка, например [1, 2, 3].append([4, 5]) --> [1, 2, 3, [4, 5]]
* `List.extend(x)` - Добавляет элементы x в конец списка, например [1, 2, 3].extend([4, 5]) --> [1, 2, 3, 4, 5]
* `del List[x]` - Удаляет из списка элемент с индексом x
* `List.insert(x)` - Вставляет заданное значение в список
* `List.index(x)` - Возвращает индекс первого вхождения заданного значения
* `List.reverse(x)` - Меняет порядок следования элементов на противоположный
* `List.count(x)` - Возвращает количество равных заданному значению элементов
* `List.clear(x)` - Удаляет все элементы из списка
* `List.remove(x)` - Удаляет первое вхождение заданного значения

## Методы множеств:
* `Set.add(X)` - Добавляет элемент 'X' в множество
* `Set.update([x1, x2, x3])` - Добавляет итерируемый объект (в данном случае элементы списка) в множество 
* `Set.discard(X)` - Удаляет элемент 'X' из множества (не выдает ошибку при отсутствии X)
* `Set.remove(X)` - Удаляет элемент 'X' из множества (выдает ошибку при отсутствии X)
* `Set.pop()` - Удаляет произвольный элемент из множества (выдает ошибку при пустом множестве)
* `Set.clear()` - Очищает множество
* `Set.copy()` - Создает копию множества
* `SetA.isdisjoint(SetB)` - True - Если множества не содержат общих элементов, иначе — False
* `SetA.issubset(SetB)` - True - Если множество A является подмножеством B, иначе — False
* `SetB.issuperset(SetA)` - True - Если множество A полностью входит в множество B, иначе — False

### Замороженные множества (frozenset):
* `frozenset([1, 2, 3, 4, 5, 6])` - замороженное множество - порядок элементов определен (может стать key для словаря)
```Python
print(*frozenset([1, 2, 3, 4, 5, 6])) # -> 1, 2, 3, 4, 5, 6
```

## Операции с множествами:
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
