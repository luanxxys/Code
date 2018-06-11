# set

用于包含一组无序对象，无法通过数字索引; 放入集合中的元素序是不可变的.

基本功能包括关系测试和消除重复元素. 集合对象还支持 union(联合), intersection(交), difference(差) 和 sysmmetric difference(对称差集) 等数学运算.

支持 `x in set`, `len(set)`, 和 `for x in set`. 作为一个无序的集合，set  不记录元素位置或者插入点. 因此，set 不支持 `indexing`, `slicing`, 或其它类序列（`sequence-like`）的操作.

## 创建

    s = set([3, 5, 7])    # 数值集合
    t = set("hello")    # 唯一字符集合

        >>> t
        set(['h', 'e', 'l', 'o'])

## 标准操作

    a = t | s    # 并集
    b = t & s    # 交集
    c = t - s    # 差集
    d = t ^ s    # 对称差集

## 基本操作

集合类型的方法和描述

项目 | 描述
---|---
len(s)|
s.copy()|s 的一个浅复制
s.issubset(t)|s <= t, 测试是否 s 中的每一个元素都在 t 中
s.issuperset(t) | s >= t, 测试是否 t 中的每一个元素都在 s 中
s.difference(t)| 差集
s.intersection(t)| 交集
s.union(t)| 并集
s.symmetric_difference(t)| 对称差集

可变集合的方法

项目 | 描述
---|---
s.add('x')|
s.update([10,37,42])|添加多项
s.remove('H')|
s.diffence_update(t)| 删除同时存在在 t 中的所有项
s.intersection_update(t)| 交集，并放在 s 中
s.discard(item)| 删除
s.remove(item)| 删除并可报异常
s.pop()| 返回任意元素并删除, 如果为空则引发 KeyError
s.clear()|删除所有元素
