---
layout: post
title: 数值分析--数值微分
date: 2018-12-19
categories: Math
tags: Euler Runge-Kutta
---

+ 邮箱： 	hustmath2018@163.com -- math2018
+ [typora使用操作](https://blog.csdn.net/WeiDelight/article/details/81011921)
# 数值微分

+ 考试内容
  + Netwon-Cotes 构造n次代数精度
  + 正交多项式族求Gussion


## Schedule

|Dateline|start time|end time|Learning|
|:-:|:-:|:-:|:-:|
|2018/12/19|17：00|||



## 欧拉方法：显 / 隐

1. 微分相当于求导

2. 显式 / 隐式

   ![euler]({{ site.url }}/assets/math/euler.png)

## 改进欧拉

1. 采用中间值的方法：增加处初值，提高精度；

   ![euler1]({{ site.url }}/assets/math/euler1.png)

## Runge-Kutta(龙格-库塔)

1. 对两点斜率进行加权平均

   ![euler2]({{ site.url }}/assets/math/euler2.png)

## 4阶Runge-Kutta

1. 构造4阶的K

   ![euler3]({{ site.url }}/assets/math/euler3.png)





