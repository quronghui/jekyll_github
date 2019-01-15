---
layout: post
title: Computer Programe to GUI
date: 2019-1-10
categories: Electronic
tags: programe software
---

# Computer Programe to GUI

+ 从嵌入式的元件，到计算机的整体架构；
+ [bilibili](https://www.bilibili.com/)  视频学习教程
+ 搜索[计算机科学](https://search.bilibili.com/all?keyword=%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%A7%91%E5%AD%A6&from_source=banner_search)----【计算机科学速成课】

## Programe

1. 早期的冯诺依曼结构

   + ALU + data register + instruction register + instruction adress register  + memory(store instruction and data)
2. 程序的输入方式

   + 插线板 + 开关 + 穿孔纸卡
3. 如何更简单的将程序输入到内存中?

   + 编程语言 + 编译器的方式
   + 抽象成高级语言
4. **抽象一** ：将代码打包成函数 funcation, 库

## Algorithm

1. Algorithm: 解决问题的具体步骤
2. Sorting(排序问题)
   + Array 进行排序：复杂度是 O(n ^ 2)
   + 归并排序：进行分组排序，组内先排序
   + 图搜素

## Data Structures

1. 定义：算法处理的数据在memory中的存储方式

2. 数据的存储方式

   ![data_struct.png]({{ site.url }}/assets/img/computer/data_struct.png)

3. 阿兰图灵的故事

## Software Engineering

1. **抽象一** ： 

   + 硬件：晶体管抽象为逻辑门

   + software：面向对象的编程：函数 -- > 抽象为对象 -- >对象进行不同的分类  

   + ```
     Funcation	Object 				Example :  Obiect Enginer
     			   Funcation 1						Object 1
                    	Funcation 2						 Object2
                	END Object					   End Object
                	
     ```

2. 函数 --->  对象 ：包含了

   + 其他对象
   + 函数
   + 变量

3. 代码：编译之前就只是文字而已

   + IDE  代码编写工具，集成编译工具
   + 文档管理和测试工具

## Integrated Circuit

1. 分立元件 -- 集成元件
2. ( PCB + IC chip )  ---  减小线的连接
3. PCB的工艺（光刻）：放更多的晶体管

## Operate Systems

### Operate System

1. OS :本质上是一个程序
   + 操作硬件的权限
   + 运行和管理其他程序的功能
2. CPU : 硬件的核心，对内存地址的调度
3. 任务：
   + 自动加载需要运行的程序
   + 多任务操作系统：需要对内存地址进行分配；
   + 提供API接口：抽象硬件底层和上层的关系，方便Program

### Storage  &&  Memory

1. Programe 存储方式
   1. Storage : 非易失性存储 -- 硬盘
   2. Memory : 易失性的存储 -- 内存条Memory
2. 存储单位
   1. 1MB=1024KB=1024B*1024=1048576bit
   2. 厂商在制作硬盘的时候，为了计算方便，1KB只有1000Byte，1MB只有1000KB，1G只有1000MB

### Files Systems

1. 文件系统：对文件进行管理和增删
2. 文件格式：文件的本质，知道文件是什么？
3. 文件表示
   + 在最底层的表示：都是0/1数据
   + 上层：各自文件拥有的文件格式。example：.bmp ; .wav
   + 根据文件格式，知道如何去解码
4. 碎片整理
   + 文件的增删改查会导致文件散落在各个块，
   + 碎片整理，将相同的文件类型数据进行调整统一

### Compression

1. 压缩：为了花更小的内存代价，存储更多的数据
2. 无损压缩：相同格式的 位/块 ，只用一位进行表示
3. 时间冗余：利用帧前后的相似性，之存储变化的部分

###  man-machine interaction

1. Input / Output : 对于计算机组件而言，RAM -- CPU 交互
2. 人机交互：早期 -- 人工输入，算盘，齿轮……

### Screen

1. LCD : 像素点进行显示；
2. 显卡：将字符转化为光删图形的设备，通过像素点显示在Screen上；
3. CAD：早期的图形交互工具

### BASIC Interpreter

1. 解释器：运行时进行转换
2. 编译器：提前转换，代码的编译0/1

### GUI （Graphical User Interface）

1. GUI ： 人机交互的界面，从适应机器编程，到更好的服务人类使用；
2. 实现方式：点击实现事件的触发；
3. 2D -->3D 
   + 对三角形进行着色，边缘抗锯齿（模糊处理）
   + 进行旋转，得到3D效果渲染
4. GPU（Graphic Processing Units）
   + 专门的图像处理单元
   + 包含处理2D的网络和纹理
   + 配有专门的RAM
   + 也就是现在的显卡