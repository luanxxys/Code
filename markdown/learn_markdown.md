# Use Markdown

1. ### 标题
    > 此处为三级标题

    ##### 最小为六级标题（此为六级标题效果）

        ###### 六级标题

1. ### 有序列表、无序列表

    + #### 无序列表

            标志：  -    +   *

    + #### 有序列表

        a. 随便写数字

            1.
            1.
            1.

        b. 首项写数字，其它后续项符号表示

            -
            1.
            1.
        > 列表嵌套时，**_对齐方式很重要_**

1. ### 字体

    + #### *斜体*

        单个 * 或 _

    + #### __粗体__

        两个 * 或 _
        > 同时想要 **粗体** 和 *斜体* 效果时，内层斜体，外层粗体（不加空格）

    + #### ~~删除线~~

            ~~删除线~~

    + #### 字体、字号、颜色

            eg
                <font color=#099ff size=12 face="黑体">黑体</font>

        <font face="STCAIYUN">华文彩云</font>  
        <font color="gray" size="5">gray</font>
        <font color="#099ff" size="12" face="黑体">黑体</font>

        > 暂未成功

1. ### 文字、代码引用

    + #### \> 标志

        > 单层引用，效果并不是很出众嘛
        >> 双层应用

    + #### Tab 键

            阴影效果即如此

    + #### \` 标志

            eg
                ` cout << "Hello,MarkDown !"; `   

        ` cout << "Hello,MarkDown !" ;`

    + #### ``` 标志

        整段代码引用

            eg
            ``` javascript
            // All the code you will ever need
            var hw = "Hello World!"
            alert(hw);
            ```

        ``` javascript
        // All the code you will ever need
        var hw = "Hello World!"
        alert(hw);
        ```

    + ##### \ 标志

        输出普通字符 \ ` * _ {} [] () # + - . !

            eg
                \( \* Hello \* \)\[]

        \( \* Hello \* \)\[]

1. #### 引用图片

        ！\[]\()

    + 引用网页图片：

            eg
                ![shepherd](https://github.com/luanxxys/code/blob/master/markdown/images/show_local_image_demo.jpg)

        ![shepherd](https://github.com/luanxxys/code/blob/master/markdown/images/show_local_image_demo.jpg)

        控制图片大小 + 加标注

        <center>

        <img src="https://github.com/luanxxys/code/blob/master/markdown/images/show_local_image_demo.jpg" width="25%" height="25%" />

        德牧

        </center>

    + 引用本地图片

        使用绝对路径

            eg
                ![test](/home/luanxxy/github/code/markdown/images/show_local_image_demo.jpg)

    + 引用 github 中上传的图片：两种方式
    > 图片名称不要有空格

        1. 相对于现在位置的相对路径

                ![test_1](../images/test_1.jpg)

        2. 将仓库主目录当作根目录 /

                ![test_1](/images/test_1.jpg)

1. #### 链接

    []()

        eg
            [Markdown](https://github.com/luanxxys/code/tree/master/markdown)

    [Markdown](https://github.com/luanxxys/code/tree/master/markdown)

1. #### 表格

    Tables | Are | Here
    -----|:-----:|-----:
    It's | a | test
    --- |:---:|---:
    默认左对齐 | 居中 | 右对齐

1. #### 分割线

    (三个及其以上） ___ 或 --- 或 ***

    ***

# *问题汇总*

1. 整段代码引用加上行号
