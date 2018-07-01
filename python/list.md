# list

**任意对象** 组成的序列, 有序, 可变.

    一组有序项目的集合
    可变的数据类型【可进行增删改查】
    列表中可以包含任何数据类型, 也可包含另一个列表【可任意组合嵌套】
    列表是以方括号“ []”包围的数据集合, 不同成员以“ ,”分隔
    列表可通过序号访问其中成员

## 相关操作

### 声明/创建

    l = []
    l = [1, 'a', [2,3] ]
    l = list('hello')
    l = '1,2,3,4,5'.split(',')

> 内建函数 list(a_sequence) 可以将一个序列转为列表

### 速查表

op|function|mark
---|---|---
增加元素||
|l.append(item)|
|l.insert(i, item)|
|l3 = l1 + l2|l1不变, 二者返回新的列表, 当列表很长时, 会消耗大量内存
|l.extend(t)| 追加新列表 t 到 列表 l 末尾
删除元素||
|l.remove(item) | 按 item 的值进行删除
|del l1[0:2] | 按 item 的索引或切片删除
|del l | 删除列表
|a = l.pop([i])| 返回位置 i 的值, 并删除它; 若未指定索引, pop 返回列表最后一项
修改元素||
|l[0] = 0|对指定索引进行赋值操作
|l[0:2] = [7,8,9]|
|l[:] = [] |清空
切片和索引||
|l[-1]|
|l[i:j:k]|i 不指定默认 0, j 不指定默认序列尾, k 不指定默认 1
排序||
|l.sort()|原地排(在原 list 上排序, 不返回排序后的 list), 默认升序
|sorted(l)|不改变原 list , 返回排序后的 list
|l.reverse()|l反序
|reversed(l)|返回一个iterator, `l[::-1]` 可以达到一样的效果, 但是这个是返回一个新的列表
查找和统计||
|1 not in l|False
|l.index(item)|
|l.count(item)|item 出现次数
遍历列表||
|for i in l:|
|for index,value in enumerate(l):|需要索引位置
清空列表|l1 = [], l1[:] = [], del l1[:]|
复制列表|l2 = l1[:]|
列表长度|len(l)|
重复|l*3|

### 列表解析

Python 的强大特性之一是其对 list 的解析, 它提供一种紧凑的方法, 可以通过对 list 中的每个元素应用一个函数, 从而将一个 list 映射为另一个 list.

    列表解析, 又叫列表推导式( list comprehension)

    列表解析比 for 更精简, 运行更快, 特别是对于较大的数据集合

    列表解析可以替代绝大多数需要用到 map 和 filter 的场合

列表推导式提供了一个创建链表的简单途径, 无需使用 map(),  filter() 以及 lambda . 以定义方式得到列表通常要比使用构造函数创建这些列表更清晰. 每一个列表推导式包括在一个 for 语句之后的表达式, 零或多个 for 或 if 语句. 返回值是由 for 或 if 子句之后的表达式得到的元素组成的列表. 如果想要得到一个元组, 必须要加上括号.

#### 基本列表解析

- 基本

        [x for x in range(5)]   # [0, 1, 2, 3, 4]

- 多个值的

        [ '%s = %s' for (k, v) in a_map.items()]

- 两次循环

        [x+y for x in l1 for y in l2]

- 调用函数

        [ func(x) for x in l1]  # 等价于 map

> 列表解析不会改变原有列表的值，会创建新的 list

#### 条件列表解析

    [ x for x in range(100) if x%2 == 0 ]

#### 嵌套列表解析

    mat = [ [1, 2, 3],[4, 5, 6], [7, 8, 9]]

交换行列

    [ [row[i] for row in mat] for i in (0,1,2)] #[[1, 4, 7], [2, 5, 8], [3, 6, 9]]

[reference](http://lib.csdn.net/article/python/64627)
