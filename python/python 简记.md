在 UNIX 上，当某程序在控制台中被引用时，该文件的头两个字节先被读入。

如果这两个字节是 ASCII 字符 #！， shell 就会认为该文件将要由解释器执行，切该文件的首行指定了要使用哪个解释器。

该行称为 shebang（shell 执行）行

    #！/usr/bin/python3.6

或

    #!/usr/bin/env python3.6
> 第二种形式适应性更好，使用在 shell 当前环境中发现的第一个 python 解释器。
