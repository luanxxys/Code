# Python 之排序函数 sort() 和 sorted()

- sort() 是 Python **列表**的一个内置的排序方法，list.sort() 方法排序时直接修改原列表，返回 None；

- sort() 是 Python 内置的一个排序函数，它会从一个迭代器返回一个排好序的新列表。

- 相比于 sort()，sorted() 使用的范围更为广泛，但 sort() 函数不需要复制原有列表，消耗的内存较少，效率也较高。另外，sort() 只是列表的一个方法，只适用于列表，而 sorted() 函数接受一切迭代器，可以方便地针对不同的数据结构进行排序，返回新列表。

## 函数形式

    sorted(iterable[, key][, reverse])

    list.sort(*, key=None, reverse=None)

这两个方法有以下 2 个共同的参数：

- key 是带一个参数的函数，返回一个值用来排序，默认为 None。这个函数只调用一次，所以 fast。

- reverse 表示排序结果是否反转

## sorted()

- 对字典进行排序

        >>> sorted({1: 'D', 2: 'B', 3: 'B', 4: 'E', 5: 'A'})     # 根据字典键排序

            [1, 2, 3, 4, 5]

        >>> sorted({1: 'D', 2: 'B', 3: 'B', 4: 'E', 5: 'A'}.values())    # 根据字典值排序

            ['A', 'B', 'B', 'D', 'E']

- 对多维列表排序

        >>> student_tuples = [('john', 'A', 15),('jane', 'B', 12),('dave', 'B', 10)]
        >>> sorted(student_tuples, key = lambda student: student[0]) # 对姓名排序

            [('dave', 'B', 10), ('jane', 'B', 12), ('john', 'A', 15)]

        >>> sorted(student_tuples, key = lambda student: student[2])  # 年龄排序

            [('dave', 'B', 10), ('jane', 'B', 12), ('john', 'A', 15)]

- 调用 operator 模块中的 itemgetter() 可以实现根据多个参数排序

        >>> sorted(student_tuples, key = itemgetter(2))  # 根据年龄排序

            [('dave', 'B', 10), ('jane', 'B', 12), ('john', 'A', 15)]

        >>> sorted(student_tuples, key = itemgetter(1, 2))  # 根据成绩和年龄排序

            [('john', 'A', 15), ('dave', 'B', 10), ('jane', 'B', 12)]

        >>> sorted(student_tuples, key = itemgetter(1, 2), reverse=True) # 反转排序结果

            [('jane', 'B', 12), ('dave', 'B', 10), ('john', 'A', 15)]

> itemgetter 返回一个函数，实现取元素的功能。比如 `f = itemgetter(2)`，调用 `f(r)` 返回 `r[2]`; `f = itemgetter(2, 5, 3)`，调用 `f(r)` 返回元组 `(r[2], r[5], r[3])`
