# 理解 Python 中的 `if __name__ == '__main__'`

`if __name__ == '__main__'` 简单的理解就是： 如果模块是被直接运行的，则代码块被运行，如果模块是被导入的，则代码块不被运行。

- ### 程序入口

    Python 属于脚本语言，不像编译型语言那样先将程序编译成二进制再运行，而是动态地逐行解释运行。也就是从脚本第一行开始运行，没有统一的入口。

    一个 Python 源码文件除了可以被直接运行外，还可以作为模块（也就是库）被导入。不管是导入还是直接运行，最顶层的代码都会被运行（Python 用缩进来区分代码层次）。而实际上在导入的时候，有一部分代码我们是不希望被运行的。

    `if __name__ == '__main__'` 就相当于是 Python 模拟的程序入口。Python 本身并没有规定这么写，这只是一种编码习惯。由于模块之间相互引用，不同模块可能都有这样的定义，而入口程序只能有一个。到底哪个入口程序被选中，这取决于 ``__name__`` 的值。

- ### `__name__`

    `__name__` 是内置变量，用于表示当前模块的名字，同时还能反映一个包的结构。

- ### example
    > [from: Adam Rosenfield](https://stackoverflow.com/questions/419163/what-does-if-name-main-do/419189#419189)

    ```python
    # file one.py
    def func():
        print("func() in one.py")

    print("top-level in one.py")

    if __name__ == "__main__":
        print("one.py is being run directly")
    else:
        print("one.py is being imported into another module")

    # file two.py
    import one

    print("top-level in two.py")
    one.func()

    if __name__ == "__main__":
        print("two.py is being run directly")
    else:
        print("two.py is being imported into another module")
    ```

    $ python one.py

        top-level in one.py
        one.py is being run directly

    $ python two.py

        top-level in one.py
        one.py is being imported into another module
        top-level in two.py
        func() in one.py
        two.py is being run directly

    > Thus, when module one gets loaded, its `__name__` equals "one" instead of `__main__`


对导入的模块来说，模块中的函数是调用时才执行的，但是语句会立刻执行（没有缩进的那些语句，如变量赋值语句, print, if else ...）

- [Reference:http://blog.konghy.cn/2017/04/24/python-entry-program/](http://blog.konghy.cn/2017/04/24/python-entry-program/)
