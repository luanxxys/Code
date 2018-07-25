# string

- 字符串表示

    让一个字符串扩展到多行: \

        s = "This is a long string\
        that spans two lines"

    字符串保持原貌（忽略了转义字符）：r R

        s = r"This is a long string\
        with a blackslash."

    无需加入续行符、换行符，文本原貌输出

        s = """
        This is an even
        bigger string that
        spans three lines.
        """

    Unicode 字符串： u U

        s = u"hello\u0020world"
    > python3 不必要加

    字符串一旦创建则无法改变，无论对它进行什么操作，总是创建了新的字符串

- 字符串是字符的序列

    索引访问单个字符

        mystr = "my string"
        "my string"[0]    # m
        mystr[0]     # 'm'
        mystr[-2]     # 'n'

    切片访问字符串序列

        mystr[1:4]     # 'y s'
        mystr[3:]     # 'string'
        mystr[-3:]     # 'ing'

    还可以设置切片步长：增加第三个参数

        mystr[：3:-1]     # 'gnirt'
        mystr[1：:2]     # 'ysrn'

    循环遍历整个字符串

        for c in mystr:

    构建另一个序列

        list(mystr)    # 返回 ['m','y' ... 'g']

    字符串拼接

        mystr + 'oid'

    字符串重复

        'ox' * 3

    方法 | 描述
    ---|---
    s.capitalize()| 首字母大写，其余小写
    s.title()| 每个单词的首字母大写
    s.center(width [, pad])|pad 是填充字符
    s.ljust(width [, fill])| 左对齐
    s.rjust(width [, fill])|
    s.find(sub[, start [, end]])| 找出 sub 首次出现的位置
    s.lower()| 转换成小写形式
    s.upper()|
    s.swapcase()| 大小写互换
    s.lstip([chrs])| 删掉 chrs 前面的空格或字符
    s.rstrip([chrs])|
    s.strip([chrs])|
    s.replace(old, new [, maxreplace])|
    s.split(sep [, maxsplite])|sep 作为分隔符对字符串换分，后者参数为最大划分次数

- 字符串对齐、格式化: ljust、 rjust、 center

        print('|', 'hello'.ljust(20),'|', 'world'.ljust(20))
        print('hello'.center(20,'+'))

- 合并字符串

        large_string = ''.join(pieces)    # 空格隔开（符号可选）
