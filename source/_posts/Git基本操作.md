---
title: Git基本操作
toc: true
author: lzaske
tags:
  - 学习笔记
abbrlink: 4788
date: 2023-07-31 17:00:25
cover: https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/202310222040950.jpg
password:
summary:
categories:
---

## git 命令（简单版）

1. 创建仓库  

    ``` git
    git init # 初始化仓库
    git clone 仓库的Http链接
    ```

2. 添加至缓存区  

    ``` git
    git add 文件名称
    # 或者
    git add .  #添加全部名称
    ```

3. 提交信息  

    ``` git
    git commit 
    ```

    * commit 后会进入vim编辑页面 按i进入模式进行备注
    * 编辑完版本信息(备注信息)后按ESC退出插入模式
    * 英文输入状态下在下方命令行输入:wq（强制保存并推出）
4. 上传远程仓库  

    ``` git
    git push 
    git push origin 分支名称
    ```

5. 切换分支  

    ``` git
    git checkout 分支名称
    ```

6. 其他命令  

    ``` git
    git status # 查看仓库当前状态
    git reset  # 回退版本
    git rm     # 将文件从暂存区和工作区移除
    git log    # 查看提交历史
    git log --oneline  # 查看简洁版的提交记录
    git blam<file>     # 以列表形式查看指定文件的历史修改记录

    ```

[git操作]<https://blog.csdn.net/m0_38134431/article/details/86164379>
