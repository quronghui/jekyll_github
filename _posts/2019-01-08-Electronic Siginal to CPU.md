---
layout: post
title: Electronic Signal to CPU
date: 2019-1-8
categories: Electronic
tags: ALU RAM CPU
---

# Electronic Signal to CPU

+ 从嵌入式的元件，到计算机的整体架构；
+ [bilibili](https://www.bilibili.com/)  视频学习教程
+ 搜索[计算机科学](https://search.bilibili.com/all?keyword=%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%A7%91%E5%AD%A6&from_source=banner_search)----【计算机科学速成课】

[TOC]



## Electronical Signal

1. 继电器里面的虫子 -- Bug

2. 继电器 -- 真空管 -- 晶体管 ？

   + 让电路的开闭，以更快的速度跳变；
   + 半导体材料的研发对计算机的发展起到了作用---硅
   + 这个地方称之为--硅谷

3. 逻辑门 and or not

   + XOR 电路的设计

     ![xor.png]({{ site.url }}/assets/img/computer/xor.png)

4. **抽象一** ：逻辑门首次将电信号首次抽象为0/1数据

## Data

+ 用二进制编码，表示照片，电影，数据

1. byte -- bits
2. 32 bit and 64bit difference
   + 当首位的 0 1 表示正负时，32bit 的就不够用了
   + 计算机目前采用的是64bit
3. **抽象二** ：ALU 算术逻辑单元
   + 将逻辑门封装成半加器和全加器，用于输入输出的级联；
   +  half adder : 用于保存相加结果
   + full adder : 用于保存进位
   + **抽象三**： 将所有的half and full 封装在一起 ----> 芯片
4. Arithmetic & Logic Unit (ALU)
   + 抽象为芯片后，有四个标志位
   + Overflow bit  --  溢出flag
   + Zero bit  --  input  A = B
   + Negative bit  --  input  A < B
5. 到这里就明白了，计算机在没有卡轮情况下，是如何进行计算的。

## Data Memory -- RAM

1. 运用ALU进行数据存储

   ![memory.png]({{ site.url }}/assets/img/computer/memory.png)

   1. 锁存的意思：锁住了一个值

   ![memory1.png]({{ site.url }}/assets/img/computer/memory1.png)

   2. **抽象一**：为了引出 Read / Write control bit

      + When write emable = 1 ,  Data input value influence Dataoutput value

      + But when write emable = 1, Data input value can't influence Dataoutput value; so this is latch.

        ![memory2.png]({{ site.url }}/assets/img/computer/memory2.png)

2. **抽象二**：256 位存储器，存储一位数据

   1. 并排放置的锁存器，需要大量的输入总线，输出总线，控制总线

   2. 抽象为矩阵：用行和列表示输入总线，输出总线；

   3. 加上：1条数据线，1条 Read control 线，1条 Write control 线

   4. example ：  2^8(16*16)--> 16+16+3 = 35条线，

      ![memory3.png]({{ site.url }}/assets/img/computer/memory3.png)

3. **抽象三**: 将256位数据存储单元，封装位一个整体

   1. 一位数据，256位的存储单元表示

      ![memory4.png]({{ site.url }}/assets/img/computer/memory4.png)

   2. 存储8位数据

      ![memory5.png]({{ site.url }}/assets/img/computer/memory5.png)

4. 数据的存储，就是矩阵的层层嵌套，难的在于如何一层层的抽象

## CPU

1. 概念：

   + ALU : Input Binary to conculation;
   + 内存：
     + 寄存器：存运行数据，和操作数
     + RAM：存数据和程序
   + CPU = ALU + 内存
     + CPU -- 执行programs 
     + program -- 由操作数组成
     + 操作数 -- 由指令组成 instruction

2. **CPU的过程**：取指 --> 解码 --> 执行

   1. 这一过程：**时钟周期**

   2. 完成这一过程需要：

      + 4个寄存器；1个RAM；
      + 2个CPU寄存器：指令地址寄存器(存指令的adress); 指令寄存器(存指令)
      + 内存RAM中的Data 存着 -- 指令：前四位--操作码；后四位--内存地址（数据来源）

      ![CPU1.png]({{ site.url }}/assets/img/computer/CPU1.png)

3. **抽象一**: 将CPU的过程抽象，由时钟进行控制CPU的过程

   ![CPU2.png]({{ site.url }}/assets/img/computer/CPU2.png)

4. 超高的时钟频率

5. Instruction and Programs
   1. **CPU is powerful is that it is programmable**
   2. 指令：Jump and HALT(停止指令)
   3. **抽象一**：可变指令长度（32bits and 64bits）

6. 高级CPU的设计

   1. CPU chip  --- RAM  : Data交互，通过Bus总线 ;
   2. CPU chip 增加 Cache : 为了适应高时钟频率，更快传递Data;
   3. 串行执行[CPU过程] -- 并行执行；
   4. 流水线进行操作