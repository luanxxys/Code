# Use Markdown

1. ### 标题
	> 此处为三级标题
	
		标志：#
		最多六级标题，###### 六级标题
	###### 六级标题效果
	
1. ### 有序列表、无序列表

    + #### 无序列表
            标志：
                -  +  *
    + #### 有序列表
            标志：
                a. 随便写数字
                b. 首项写数字，其它后续项符号表示
            
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
            eg：
                <font color=#099ff size=12 face="黑体">黑体</font>

		<font face="微软雅黑">微软雅黑</font>
		<font face="STCAIYUN">华文彩云</font>
		<font color="gray" size="5">gray</font>
		<font color="#099ff" size="12" face="黑体">黑体</font>
		
		> 暂未成功


1. ### 文字、代码引用

    + #### \> 标志
    
        > 单层引用，效果并不是很出众嘛
        >> 双层应用
        
    + #### Tab 键
    
        	阴影效果

    + #### \` 标志
        	eg：
            	` cout << "Hello,MarkDown !"; `   

        ` cout << "Hello,MarkDown !" ;`

    + #### ``` 标志
        	整段代码引用
        	eg：
				```javascript
				// All the code you will ever need
				var hw = "Hello World!"
				alert(hw);
				```

		```javascript
		// All the code you will ever need
		var hw = "Hello World!"
		alert(hw);
		```

    + ##### \ 标志
            输出普通字符 \ ` * _ {} [] () # + - . !
                eg：
                    \( \* Hello \* \)\[] 
		\( \* Hello \* \)\[]

1. #### 引用图片
		！\[]\()
	
    + 引用网页图片：
	
            eg:
            	![Mou icon](http://mouapp.com/Mou_128.png)        

        ![Mou icon](http://mouapp.com/Mou_128.png)

    + 引用本地图片：
                    
            使用相对路径
            	eg：
                	![test](./test.jpg)

        ![test](./test.jpg)

            控制图片大小 + 加标注
        <center>
        <img src="./test.jpg" width="25%" height="25%" />

        德牧
        </center>

1. #### 链接
    	[]()
    	eg:
			[Markdown](https://github.com/riku/Markdown-Syntax-CN)
        
    [Markdown](https://github.com/riku/Markdown-Syntax-CN)

1. #### 表格

Tables | Are | Here
-----|:-----:|-----:
It's | a | test
--- |:---:|---:
默认左对齐 | 居中 | 右对齐

1. ### 分割线
    	(三个以上） _ _ _ 或 --- 或 ***

    ***


# *问题汇总*

1. 整段代码引用加上行号
