# Advanced usage

- ### Usage

    + ### 数学公式

        可以直接插入TeX公式

            $e^x = \sum_{n=0}^\infty \frac{x^n}{n!} = \lim_{n\rightarrow\infty} (1+x/n)^n$

        渲染效果为

            ex=∑n=0∞xnn!=limn→∞(1+x/n)n

        [Cheat Sheet - LATEX Mathematical Symbols](https://reu.dimacs.rutgers.edu/Symbols.pdf)

    + ### 脚注

    + ### 文献引用

    > [如何用Markdown写论文？](http://www.jianshu.com/p/b0ac7ae98100)

- ### Transfer markdown file into other DOCs

    + Pre-installed

        [Pandoc](https://pandoc.org/installing.html)

        [TeX Live(LaTex)](https://www.tug.org/texlive/)

    + Manual

        [Pandoc demos](http://pandoc.org/demos.html)

        [Pandoc User’s Guide](http://pandoc.org/MANUAL.html)

        常用

        * Standalone HTML file

                pandoc -s MANUAL.txt -o example2.html

        * Word docx

                pandoc -s MANUAL.txt -o example29.docx

        * PDF

                pandoc MANUAL.txt --pdf-engine=xelatex -o example13.pdf

        * HTML slide shows

                pandoc slides.md -o slides.html -t revealjs -s --metadata title="title"

            定制样式：从GitHub上获取 reveal.js，把文件夹放在幻灯片所在目录下即可

                cd project
                git clone https://github.com/hakimel/reveal.js

            除了默认的外观主题以外，reveal.js还提供了多个主题可供选择

                pandoc slides.md -o slides.html -t revealjs -s -V theme=beige --metadata title="title"

            > default：（默认）深灰色背景，白色文字
            >
            > beige：米色背景，深色文字
            >
            > sky：天蓝色背景，白色细文字
            >
            > night：黑色背景，白色粗文字
            >
            > serif：浅色背景，灰色衬线文字
            >
            > simple：白色背景，黑色文字
            >
            > solarized：奶油色背景，深青色文字

        [Markdown HTML 幻灯片](http://notes.11ten.net/pandoc-silde.html)

- ### Reference

    [reveal.js（HTML 演示文稿）中文文档](https://vxhly.github.io/2016/09/reveal-js-cn-document/)

    [Markdown 语法手册 （完整整理版）](http://blog.leanote.com/post/freewalk/Markdown-%E8%AF%AD%E6%B3%95%E6%89%8B%E5%86%8C)
