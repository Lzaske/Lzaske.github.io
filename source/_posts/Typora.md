---
title: Typora使用教程
toc: true
author: Lzaske
cover: 'https://typoraio.cn/img/favicon-128.png'
tags:
  - 软件教程
  - 软件推荐
abbrlink: 64516
date: 2023-03-22 21:34:56
password:
summary:
categories:
---

## Typora使用教程

此教程适用于实验室成员

### 下载

在服务器中（192.168.251.144）找到Typora的安装包
![20230322214012](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20230322214012.png)

### 安装

1. 解压下载后的压缩包
![20230322214217](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20230322214217.png)

2. 双击.exe后缀的安装程序
![20230322214354](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20230322214354.png)

3. 安装目录建议修改到非C盘位置
![20230322214508](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20230322214508.png)

### 激活

1. 将文件夹的app.asar文件复制到Typora的安装文件夹下的resource中
![20230322215744](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20230322215744.png)
复制进去后选择替换
![20230322215817](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20230322215817.png)

2. 密钥在解压的文件中（Key.txt）
![20230322215504](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20230322215504.png)

3. 打开Typora后在弹开的界面输入邮箱和密钥然后点击激活
![20230322215412](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20230322215412.png)

## MarkDown基础

1. 标题级别

    ```Markdown
    # 第一级标题

    ## 第二级标题

    ### 第三级标题

    #### 第四级标题

    ##### 第五级标题

    ###### 第六级标题
    ```

2. 文字格式

    实际上，如果比较熟悉HTML语言的话，这些差不多都是共通的，除了加粗、斜体等少量markdown表达方式可能有些不同。如加粗，除了 **markdown**方式以外，你依然可以使用 <b>HTML</b>方式。以下文字格式包括加粗、斜体、下划线、删除线、颜色、字号、文字背景色。

    ``` MarkDown
    **加粗文字**
    *斜体文字*
    <u>下划线</u>
    ~~删除线~~
    ***加粗斜体文字***
    <font size = 6>6号字</font>
    <font face="楷体">楷体</font>
    <font color=green>绿色</font>
    <table><tr><td bgcolor=Orange>橙色背景色</td></tr></table>
    ```

    效果如下：

    **加粗文字**

    *斜体文字*

    <u>下划线</u>

    ~~删除线~~

    ***加粗斜体文字***

    <font size = 6>6号字</font><table>

    <font face="楷体">楷体</font><table>

    <font color=green>绿色</font>

    <table><tr><td bgcolor=Orange>橙色背景色</td></tr></table>

3. 代码

    * 代码块

        ```markdown
        `我是高亮代码块`
        ```

        效果如下

         `我是高亮代码块`

    * 代码区块（除去\）

        \ ```java

        public class Hello{

        public static void main(String args[]){

        System.out.println("Hello World");

        }

        }

        \ ```

        效果如下:

        ```java
        public class Hello{

        public static void main(String args[]){

        System.out.println("Hello World");

        }

        }
         ```

4. 列表

    ```markdown
    有序号列表（注意后面有空格）：
    1.
    2.
    3.

    无序号列表：

    * 姓名
    * 年龄

    * 入学日期
    * 毕业日期

    * 兴趣
    * 爱好

    下面展示嵌套序号列表：

    * 技能
    * Adobe
        * PS
        * PR
        * AE
    ```

5. 引用区块

    ```markdown
    >引用文字第一行
    >引用文字第二行
    >>引用文字第二层嵌套
    >>>引用文字第三层嵌套
    >
    >引用文字第三行列表
    >
    > 1. 第一项
    > 2. 第二项
    >
    > * 第一项
    > * 第二项
    ```

    效果如下
    >引用文字第一行
    >引用文字第二行
    >>引用文字第二层嵌套
    >>>引用文字第三层嵌套
    >
    >引用文字第三行列表
    >
    > 1. 第一项
    > 2. 第二项
    >
    > * 第一项
    > * 第二项

6. 分隔线

    ```markdown
    ---

    ***
    ```

7. 表格

    ```markdown
    |序号|工程量|备注|
    |---|---|---|
    |1|50|无|
    |2|60|无|
    |3|70|有扣减|
    ```

    效果如下：
  
    |序号|工程量|备注|
    |---|---|---|
    |1|50|无|
    |2|60|无|
    |3|70|有扣减|

8. 链接和图片

    ```markdown
    [百度一下](https://www.baidu.com)

    <https://www.baidu.com>

    ![code](https://figure.pages.dev/img/post1.jpg)
    ```

    效果如下

    [百度一下](https://www.baidu.com)

    <https://www.baidu.com>

    ![code](https://figure.pages.dev/img/post1.jpg)
