# Use Markdown

1. ### 标题
    > 此处为三级标题

    ##### 最小为六级标题（此即为效果）

        ###### 六级标题

1. ### 列表

    + #### 无序列表

            标志： - + *

    + #### 有序列表

        数字表示（可乱序；首项写数字，其它后续项用符号也可以）

            1.
            1.
            1.
        > 列表嵌套时，**_对齐方式很重要_**

1. ### 字体

    + #### * 斜体 *

        单个 * 或 _

    + #### __粗体__

        两个 * 或 _
        > 同时想要 ** 粗体 ** 和 * 斜体 * 效果时，内层斜体，外层粗体（不加空格）

    + #### ~~ 删除线~~

            ~~ 删除线~~

    + #### 字体、字号、颜色

            <font color=#099ff size=12 face=" 黑体 "> 黑体 </font>

        <font color="red"> 红色 </font>
        <font face="STCAIYUN"> 华文彩云 </font>
        <font color="gray"size="5">gray</font>
        <font color="#099ff"size="12"face=" 黑体 "> 黑体 </font>
        > github 中暂未成功

1. ### 引用

    + #### \>

        > 单层引用，效果并不是很出众嘛
        >> 双层应用

    + #### Tab 键

            阴影效果即如此

    + #### \`

            ` cout <<"Hello, MarkDown !"; `

        ` cout <<"Hello, MarkDown !" ;`

    + #### ```

        整段代码引用

            ```python
            # import module and train/test set
            import numpy as np
            import pandas as pd
            train = pd.read_csv('data/train.csv')
            test = pd.read_csv('data/test.csv')
            # combine the train set and predict set to simplify the step
            full=pd.concat([train,test],ignore_index=True)
            ```

        效果

        ```python
        # import module and train/test set
        import numpy as np
        import pandas as pd
        train = pd.read_csv('data/train.csv')
        test = pd.read_csv('data/test.csv')
        # combine the train set and predict set to simplify the step
        full=pd.concat([train,test],ignore_index=True)
        ```

    + ##### \

        输出普通字符 \ ` * _ {} [] () # + - . !

            \(\* Hello \* \)\[]

        \(\* Hello \* \)\[]

1. #### 链接

    []()

        [Markdown](https://github.com/luanxxys/code/tree/master/markdown)

    [Markdown](https://github.com/luanxxys/code/tree/master/markdown)

1. #### 引用图片

        ！\[]\()

    + 引用网页图片：

            ![shepherd](https://github.com/luanxxys/code/blob/master/markdown/images/show_local_image_demo.jpg)

        ![shepherd](https://github.com/luanxxys/code/blob/master/markdown/images/show_local_image_demo.jpg)

        控制图片大小 + 加标注

            嵌入 HTML 代码, 使用 img 标签
            <img src="images/show_local_image_demo.jpg" width="25%" height="25%" alt="德牧" align=center />

        <img src="images/show_local_image_demo.jpg" width="25%" height="25%" />

    + 引用 github 中上传的图片：两种方式
        > 图片名称不要有空格

        1. 相对于现在位置的相对路径

                ![test_1](../images/test_1.jpg)

        2. 将仓库主目录当作根目录 /

                ![test_1](/images/test_1.jpg)

    + 引用本地图片

        类似于引用 github 仓库中的图片的方法

1. #### EMOJI:smile:

    [EMOJI CHEAT SHEET](https://www.webpagefx.com/tools/emoji-cheat-sheet/)
    [Full Emoji List](https://www.unicode.org/emoji/charts/full-emoji-list.html)

1. #### 表格

        Tables | Are | Here
        -----|:-----:|-----:
        It's | a | test
        --- |:---:|---:
        默认左对齐 | 居中 | 右对齐

    效果

    Tables | Are | Here
    -----|:-----:|-----:
    It's | a | test
    --- |:---:|---:
    默认左对齐 | 居中 | 右对齐

1. #### 分割线

    (三个及其以上） ___ 或 --- 或 ***

    ***

1. #### [Advanced usage](advanced.md)

1. #### 使代码段显示行号

        {% codeblock [lang:python] [title] [url] [link text] [start:#] [mark:#,#-#] [linenos:false] %}

        code snippet

        {% endcodeblock %}

    > lang 语言
    >
    > title 代码块上方的标题
    >
    > url 为本段代码指定一个 url，用于下载或引用
    >
    > link text url 显示的文字
    >
    > 以下三个用于控制行号显示
    >
    > start:# 从第 #行开始显示行号
    >
    > mark:#,#-# 在第 #行，以及第 #-# 行显示行号
    >
    > linenos:false true 所有行都显示行号，false 所有行都不显示行号

# * 问题汇总 *

1. 整段代码引用加上行号 - 未达成
