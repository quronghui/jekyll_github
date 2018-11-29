---
layout: post
title: Windows and GitHub Pages and Jeklly Building owns Bolg
date: 2018-11-14
categories: Blog
tags: windows, GitHub Pages, jeklly, Blog 
---

# By GitHub Pages and Jekyll building Blog
## Install Tools
+ 整个流程参考链接如下，包括博客的模板
+ [Visit Link](https://blog.csdn.net/xudailong_blog/article/details/78762262)
## github
1. Building yourself github account number.
2. Build a New respository.
    + Name : “github_name”.github.io (ep: quronghui.github.io)
3. git clone 选好的模板
4. 上传到你的GitHub
## Github Page
+ GitHub Page 相当于一个服务器
+ Jekyll 运行在 GitHub Page 上

## Jekyll 环境的搭建
### Jekyll Knowledge
1. Jekyll 是一个简单的博客形态的静态站点生产机器
### Jekyll 搭建
1. GitHub Pages + jekyll 的方式
    + 直接参考这个Link 
    + [Jekyll环境的搭建](https://643435675.github.io/2015/02/15/create-my-blog-with-jekyll/)
### Jekyll 搭建中安装包的说明
1. 安装[Ruby](http://www.runoob.com/ruby/ruby-tutorial.html)
    + Ruby 是一种开源的面向对象程序设计的服务器端脚本语言
    + 没找到在Blog中担当的角色
2. 安装RubyGems
    + 用于对 Ruby 组件进行打包的 Ruby 打包系统
    + 也就是 Ruby 的管理系统
    + 用Rubygem 安装Jekyll,所有的依赖包都会被安装
3. 用RubyGems安装Jekyll
4. cd到博客文件夹，开启服务器
5. 访问 http://localhost:4000/
6. 提交代码到远程GitHub上
+ [jekyll 中文说明文档](https://www.jekyll.com.cn/docs/posts/)
### Jekyll 语法
1. jekyll serve
    + => 一个开发服务器将会运行在 http://localhost:4000/
    + 始终需要重新更新

+ 看到头信息