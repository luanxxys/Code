# 序列

序列表示索引为非负整数的有序对象集合，包括 字符串、列表、元组.

字符串是字符的序列，列表和元组是任意 Python 对象的序列.

字符串和元组是不可变的，而列表则支持插入、删除和替换元素.

所有序列都支持迭代.

- 适用于所有序列的操作和方法

    项目 | 描述
    ---|---
    s[i]|
    s[i:j]|
    s[i:j:stride]|
    s[1:3, 2:5]| 多维切片
    x in s, x not in s | 成员关系
    for x in s:| 迭代
    len(s)|
    min(s)|
    Max(s)|
    sum(s[, initial])|s 中各项的和
    all(s)| 检查 s 中的所有项是否为 True
    any(s)

- 适用于可变序列的操作

    项目 | 描述
    ---|---
    s[i] = v | 赋值
    s[i:j] = t
    s[i:j:stride] = t|
    del s[i]|
    del s[i:j]|
    del s[i:j:stride]|

- 查看变量类型

```python
type(variable)
```python

    字典 {} dict
    数组 [] array
    元组 () tuple
    列表 [] list
