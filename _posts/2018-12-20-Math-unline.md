---
layout: post
title: 数值分析--非线性方程求解
date: 2018-12-21
categories: Math
tags: Newton 
---

+ 邮箱： 	hustmath2018@163.com -- math2018
+ [typora使用操作](https://blog.csdn.net/WeiDelight/article/details/81011921)
# 非线性方程求解

+ 考试内容
  + 迭代法的两个计算
  + 牛顿法 Newton - Raphson Method 
  + 牛顿法改进


## Schedule

|Dateline|start time|end time|Learning|
|:-:|:-:|:-:|:-:|
|2018/12/21|10：15|||

## 非线性根转化问题

1. 将 f(x) = 0 的方程，转化为关于 x = g（x）的方程。
   + f(x)=0  的点称为根
   + x = g(x) 不动点
2. 迭代法：不断通过 x 进行逼近

![unline]({{ site.url }}/assets/math/unline.png)

## 迭代法的两个计算

1. 是否收敛，且判断收敛速度

   ![unline1]({{ site.url }}/assets/math/unline1.png)

2. 为达到精度误差，需要迭代的次数

   ![unline2]({{ site.url }}/assets/math/unline2.png)

## 局部收敛的收敛速度

1. 对误差进行收敛速度的评判

   ![unline3]({{ site.url }}/assets/math/unline3.png)

## 牛顿法 Newton - Raphson Method 

1. 将非线性方程线性化，Taylor展开 

2. 求解：f(x)的一个构造； 如何取初值（才能收敛）

   ![unline4]({{ site.url }}/assets/math/unline4.png)

## Newton 改进

1. 初值 x 偏离太大时，如何选取x的值

   ![unline5]({{ site.url }}/assets/math/unline5.png)

2. m重根的收敛

   ![unline6]({{ site.url }}/assets/math/unline6.png)