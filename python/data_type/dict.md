# dict

> 关联数组，或散列表
>
> Python 解释器中最完善的数据类型

创建

    prices = {"name" : "goods",
        "shares" : 100,
        "price" : 33.33
    }

创建空字典

    prices = {}
    prices = dict()

获得字典关键字列表

    # list() 将可迭代的对象转换成一个列表 []
    syms = list(prices)

> tuple() 将可迭代的对象转换成一个元组 ()

项目 | 描述
---|---
len(m)| 项的数量
m[k]| 返回 m 中 键 k 的值
m[k] = x | 添加或修改对象
del m[k]|
m.clear()|
m.keys()| 返回键值组成的一个序列
m.values()| 返回 m 中所有值的一个序列
m.items()| 返回由 (key, value) 对组成的一个序列
m.update(b)| 将 b 中所有对象【(key, value)对】添加到 m 中
