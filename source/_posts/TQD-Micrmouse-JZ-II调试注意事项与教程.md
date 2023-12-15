---
title: TQD-Micrmouse-JZ-II调试注意事项与教程
toc: true
author: Yue Tao
tags:
  - 学习笔记
abbrlink: 41255
date: 2023-08-25 10:16:18
img: 
coverImg: 
cover: http://www.qcmcu.com/uploadfile/2020/0831/20200831014234887.jpg
password:
summary:
categories:
---

## 介绍

实验室现有除自制电脑鼠以外，还有从天津启诚伟业科技有限公司购入的三只
TQD-Micrmouse-JZ-II 精致智能鼠。

* 底层代码加密 可调整部分少
* 对赛道要求高 赛道的洁净程度要高
* 一套代码对应一套鼠
* <label style="color: #FF0000;">电源接口无反接设计 </label>

## 调试

1. 调试前准备

     电脑环境要求：

    * keil  
    * MATLAB Runtime 9.6(对应MATLAB R2019a)

       若安装了其他版本，只需在官网下载[MATLAB Runtime 9.6](https://ww2.mathworks.cn/products/compiler/matlab-runtime.html?s_tid=pi_mwas_mcr_pi_R2020a_win64)版本的安装即可不需要卸载MATLAB
    * 红外计算软件: TQD-Micromouse-JZII V2022 Ir calc
    * 上位机软件: TQD-Micromouse-JZII V2022 Analysis
    * 程序烧录软件: flash_loader_demonstrator

    赛道和其他要求：

    * 赛道尽可能的干净，挡板无翘起的情况
    * 电脑鼠轮胎要干净
    * 电池要固定稳，电池线要原理轮胎的齿轮
    * 检查电机插口是否松动

2. 调试

    * 脉冲的测试
    * 红外值与陀螺仪的调试
    * 红外计算软件、上位机软件、烧录软件的使用

3. FAQ

  > Q1：在运行过程中突然停止是什么情况？
  > A1: 左右轮电机脉冲误差过，原因1.电机插线松了，按一按 2.电池的线刮到了轮胎或者电池没有固定稳，重新固定电池。
  > Q2: 为什么晚上跑的好好的白天就不行了
  > A2: 白天因为自然光影响了场地光的环境，拉上窗帘或者挑距离窗户的远端作为起点
