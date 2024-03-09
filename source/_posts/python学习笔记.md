---
title: python学习笔记
toc: true
author: lzaske
tags:
  - 学习笔记
  - Python
abbrlink: 54473
date: 2023-06-08 21:16:34
cover:
password:
summary:
categories:
---
## 第一节 Python的基础语法

1. 标识符
    * 第一个字符必须是字母或者下划线_
    * 其他部分由字母、数字和下划线组成
    * 区分大小写
2. 保留字

    ```python
    # 保留字=关键字
    import keyword
    keyword.kwlist
    ['False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
    ```

3. 注释  
    * python中单行注释以#开头
    * 多行注释可以用多个#，还有'''和"""

    ```python
    #!/usr/bin/python3

    # 第一个注释

    # 第二个注释

    '''
    第三注释
    第四注释
    '''

    """
    第五注释
    第六注释
    """
    print ("Hello, Python!")
    ```

4. 行与缩进
    * 使用缩进来表示代码块，不需要使用大括号
    * 缩进的空格数是可变的，但是同一个代码块的语句必须包含相同的缩进数，例如

* 整数 int
* 浮点数 float 无单双精度之分
* /除法结果为float //结果为整形
* python3 与 python2不同
* 进制数转换 转换为二进制bin() 十进制转换int() 十六进制转换hex() bool类型转换bool()
* bool类型 0为假 非0为真
* 字符串str

    ``` python
    bin ()
    ```
