# PEP 8 -- Style Guide for Python Code
> Record the error that is easy to appear in the Python coding specification

垂直隐式缩进；悬挂缩进

禁止使用通配符导入

    通配符导入 (from <module> import *) 应该避免

括号里边避免空格

索引操作中的冒号当作操作符处理前后要有同样的空格

关键字参数和默认值参数的前后不要加空格

如果注释是断句，首字母应该大写

注释块内的段落用仅包含单个 '#' 的行分割

首尾有下划线的情况:

    _single_leading_underscore:(单前置下划线): 弱内部使用标志。 例如 "from M import" 不会导入以下划线开头的对象。

    single_trailing_underscore_(单后置下划线): 用于避免与 Python 关键词的冲突。

    __double_leading_underscore(双前置下划线): 当用于命名类属性，会触发名字重整。 (在类 FooBar 中，__boo 变成 _FooBar__boo)。

    __double_leading_and_trailing_underscore__(双前后下划线)：用户名字空间的魔法对象或属性。例如:__init__ , __import__ or __file__，不要自己发明这样的名字。

捕获异常时尽量指明具体异常，而不是空 "except:" 子句

    空 "except:" 子句 (相当于 except Exception) 会捕捉 SystemExit 和 KeyboardInterrupt 异常，难以用 Control-C 中断程序，并可掩盖其他问题。如果 你捕捉信号错误之外所有的异常，使用 "except Exception"

空 "except:" 子句适用的情况两种情况：

    a. 打印出或记录了 `traceback`，至少让用户将知道已发生错误。
    b. 代码需要做一些清理工作，并用 `raise` 转发了异常。这样 `try...finally` 可以捕捉到它。

- ### Reference

    [PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/)

    [python 代码风格指南：pep8 中文翻译](https://my.oschina.net/u/1433482/blog/464444)
