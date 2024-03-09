---
title: vscode使用ssh连接云服务器
toc: true
cover: https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/10001.jpg
abbrlink: 64003
date: 2024-03-09 04:41:08
author: lzaske
password:
summary:
tags:
    - 软件教程
categories:
---
## Vscode连接服务器

Vsccode作为使用率兼容性很高的编程软件，在日常使用中需要操作远程服务器时我们除了可以使用专门的SSH连接工具以外，还可以使用Vscode中的插件实现SSH连接，可以极大的提升开发效率。但是vscode的SSH连接如果使用密码连接的话需要频繁的输入密码，且当密码比较复杂的时候，频繁输入密码更是一个极为痛苦的操作，因此，除了密码连接我们还可以使用SSH公钥连接的方式，只需要在配置文件中配置好，后续就可以免密码登录（不是自己的电脑为了安全起见最好还是使用密码链接），不需要再反复的输入我们复杂的密码了。

1. 安装拓展Remote-SSH
![Remto-SSH](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20240309093526.png)

2. 远程点击资源管理器，并输入ssh username@IP地址
![20240309094913](https://lzaske-tuchuang.oss-cn-beijing.aliyuncs.com/Blog/20240309094913.png)

3. 密码连接的方式，只需要根据提示选择系统并输入密码即可。

## 使用公钥的方式进行连接

1. 生成公钥
    安装Git，如果没有安装百度安装一下，安装完成后打开CMD或者Git-bash输入以下命令

    ```bash
    ssh-keygen -t rsa -C "自己的邮箱"
    ```

    回车运行命令系统会自动生成密钥文件 默认储存位置在 C:\User\用户名（Administrator）\.ssh文件夹中的id_rsa.pub

2. 公钥上传至服务器
    将id_ras.pub重命名为authorized_keys上传至服务器的/root/.ssh文件夹下(没有则创建，可以先使用密码模式登录去上传文件或者使用其他SSH连接工具)

3. 配置VScode远程文件
    系应该vscode的ssh的config文件，添加或修改成如下：

    ```config
    Host 服务器名称（自定义）或者直接使用IP地址
        HostName 服务器IP地址
        User 用户名
        PerferredAuthentications publickey
        IdentityFile "本机公钥存放路径"
    ```

## 可能会出现的问题

1. 文件权限问题

    ```bash
    chmod 700 /root
    chmod 700 /root/.ssh 
    chmod 644 /root/.ssh/authorized_keys
    ```

2. 服务器端SSH配置问题
    编辑/etc/ssh/sshd_coonfig文件
    找到对应配置取消前面#号注释 并修改为下面设置

    ```bash
    # 开启秘钥登录
    PubkeyAuthentication yes
    AuthorizedKeysFile  .ssh/authorized_keys .ssh/authorized_keys2
    # 将RSAAuthentication注释
    # RSAAuthentication no
   ```

    执行命令重启

    ```bash
    service sshd restart
    ```
