---
layout: post
title: Internet with Date Exchange
date: 2019-1-14
categories: Electronic
tags: LAN WAN Wide Web
---

# Internet with Date Exchange

+ [bilibili](https://www.bilibili.com/)  视频学习教程
+ 搜索[计算机科学](https://search.bilibili.com/all?keyword=%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%A7%91%E5%AD%A6&from_source=banner_search)----【计算机科学速成课】
+ Internet : 主旨在于数据的交换，访问

##  Date Exchange

1. Local Area Internet ( LAN )

   + Ethernet（以太网） and WiFi

   + MAC Adress(Media Access Control ):  Differentiating computer devices

2. 数据交换中的冲突问题

   + 指数退让时间的设置
   + **交换机**分成不同块的LAN

3. 数据交换方式

   + 电路交换 ：User之间线路直连
   + 报文交换：知道下一站的目的地址；通过**路由**实现多条线路的传输
   + 分组交换：防止大报文阻塞电路，分成不同数据包进行传输。

## LAN TO Internet

1. **LAN**(Local Area Internet ) :Ethernet（以太网） and WiFi 
2. WAN : 区域网，也就是**路由**构建的;
3. More Big WAN : 多个路由连接到**网关**
4. Internet :最大的WAN
5. Server : 提供数据和服务的源头

## Data Format

1. 数据包的传输，符合IP协议，限制数据包的格式。*（类似于文件系统，方便更好的读取文件）*
2. IP 协议
   + IP Header : 目的地址 + 元数据
   + **功能**：把数据包送到正确的Computer
3. UDP协议
   + 正确的Computer中的程序：request port
   + Header : IP Header + port + 校验和
   + 功能：把数据送到正确的程序
4. TCP协议
   + 增加了 ACK 确认机制
   + Header :  IP Header + port + 校验和 + 序列号 ……
   + **序列号**：接收者按着序列号便能还原数据
5. **这就是为什么叫做 TCP/IP 协议**

## Access Network

1.  通过 IP Adress + Port
   + 需要记住不同网址的IP
2. 互联网
   + 域名系统DNS：将域名和IP Adress 进行一一对应
   + Files Storage: 树形存储
     + 一级：.com  ;  .edu;  .baidu
     + 二级：google.com
     + 子域名：image.google.com

## Session 

+ 会话过程：Data 按照一定的[Data Format](#Data Format)，以一定的[交换方式](#Date Exchange)，从LAN一步步的访问到[Internet](#LAN TO Internet) 的过程，最终获得Server的这个过程

1. 数据链路层：

   + 物理层的数据交换；电信号（光缆）和无线信号（WIFI）

   + 电信号（光缆）和 Electronic Siginal 区别？
   + LAN 中数据的交换

2. 网络层：

   + 报文交换和路由交换（WAN）
   + LAN 到WAN的数据交换

3. 传输层

   + UDP/TCP
   + 负责计算机点到点的传输
   + 具备修复路由的功能

4. 会话层

   + 使用TCP/UDP创建连接。传递信息，关掉连接
   + 整个流程：用户发送请求，服务器查找网页对应的DNS，返回网页，提供服务……

## World Wide Wed

1. **万维网** ： 在[互联网](#LAN TO iNTERNET)之上
   + 基本单位：单个页面
   + 超链接：实现不同页面的切换（不用再通过 Files System 进行搜索）
2. **超文本**
   + 为了实现每一个网页有一个唯一的地址
   + **统一资源定位符** : URL
3. **HTML**
   + 超文本标记语言
   + 也是一种格式，可以制作网页