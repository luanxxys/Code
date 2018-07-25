# file operation

- 打开文件

        input = open('/tmp/test', 'w')

    模式参数

        'r'    # 以文本模式读取文件，默认值
        'rb'    # 以二进制模式读取文件
        'w'    # 创建文件，并以文本模式写文件
        'wb'

- 写入文件

        # 写入文本到文本文件
        open('file.txt', 'w').write(all_content)

        # 写入数据到二进制文件
        open('abinfile', 'wb').write(all_content)

    给文件对象指定名称

        file_object = open('file.txt', 'w')
        file_object.write(all_content)
        file_object.close()

    将数据写入字符串列表，而不是一个大字符串中

        file_object.writelines(list_strings)
        open('abinfile', 'wb').writelines(list_strings)

    > 'w' 或 'wb' 打开一个文件写入数据时，文件原有的数据将被删除。若想把新数据添加到原有数据后面，使用参数 'a'（或 'ab'）

- 读取文件

    一次性读取全部内容并放置到一个字符串中

        # 文本文件中的所有文件
        all_content = open('file.txt').read()

        # 二进制文件中的所有数据
        all_content = open('file', 'rb').read()

    防止无用文件对象占用内存，给打开的文件对象指定名字

        file_object = open('file.txt')
        try:
             all_content = file_object.read()
        finally:
             file_object.close()

    逐行读取文本文件内容，并放到字符串列表

        # 每行文本末尾都含有 '/n'
        list_lines = file_object.readlines()

        # 另末尾不包含 '/n'
        for line in file_object:
             line = line.rstrip('/n')
             process line

        # 或者替换成下句，以去除末尾空白符（不止 '/n'）
        line = line.rstrip()

- 搜索和替换文件中的文本

        file_object.write(exist_file.read().replace(stest,rtest))

- 示例

    ```python
    date = []
    f = open("text.md", 'r/w')
    # 写入时默认不换行
    g = f.read()/.write('\n')
    rows = g.split('\n')
    for row in rows:
        split_row = row.split(',')
        date.append(split_row)
    # 取第 i+1 列
    data_row = []
    for row in g:
        data_row.append(row[i])
    f.close()
    ```
