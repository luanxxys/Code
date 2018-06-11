# list set dic tuple 转换

- ## set --> list

        list(seq)

    > 把所有的序列和可迭代的对象转换成一个 list, 元素不变, 排序也不变

- ## list --> set

        set(seq)

    python 中 Set 和 List 的性能差距能有数百倍.

    如果有需要求（集合, 列表等）的并集和交集的时候, 最好使用 Set. set 和 lsit 可以自由转换, 在删除 list 中多个 / 海量重复元素时, 可以先转换成 set, 然后再转回 list 并排序 (set 没有排序). 此种方法不仅方便且效率较高.

- ## list --> dic

    zip 函数和强大的集合操作可以方便的将两个 list 元素一一对应转换为 dict

        names = ['n1','n2','n3']
        values = [1,2,3]
        nvs = zip(names,values)
        nvDict = dict((name,value) for name,value in nvs)

- ## seq --> tuple

        tuple(seq)

        > 可以把所有可迭代的 (iterable) 序列转换成一个 tuple, 元素不变, 排序也不变
