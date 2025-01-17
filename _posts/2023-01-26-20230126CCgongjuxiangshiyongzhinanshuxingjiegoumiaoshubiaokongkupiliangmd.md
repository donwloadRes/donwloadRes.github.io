---
layout: post
title: "CC工具箱使用指南属性结构描述表空库批量"
date:   2020-01-29
tags: [属性,CC,工具箱,表空库,数据库]
comments: true
author: admin
---
# CC工具箱使用指南：属性结构描述表空库(批量)

## 简介

本资源文件提供了CC工具箱的使用指南，特别是针对“属性结构描述表空库(批量)”功能的详细说明。随着县级国土空间总体规划数据库规范的下发，建立标准空库是一项马上就要着手的工作。国空的数据库体量很大，单是要素类就有100多个，手动建库是不可能的，工具自动建库就是一个很合理的选择。

数据库标准里有每个要素类和表格的【属性结构描述表】，里面规定了要素类、表的名称、别名、字段等属性，只要提取出来就可以用来建库。此工具就以这个标准的【属性结构描述表】来进行批量建空库。

## 工具参数介绍

### 1. 选择属性结构描述表（Excel）

将数据库标准里的属性结构表提取出来，转成Excel格式。这部分工作可以网上搜一下PDF转其它格式数据的方法。但是这张表还缺少一个属性，就是要素类的类型【点、线、面】，甚至没法知道他是要素类还是表。因此需要在表头上增加一个文字，其它需要注意的点如下图所示：

- 上面4个有空的列，都必须填满，不能有空值，特别是字段类型和字段长度，经常有人会漏掉。

这里放出一个模板文件，可供下载，最好在这个Excel的基础上去修改，可以避免很多错误。

### 2. 选择输出GDB数据库的文件路径

选择1个文件夹，生成的GDB数据库会放在这里。

### 3. 选择坐标系

手动选择坐标系，根据你的具体项目来确定。

## 工具执行结果

以三调用地为例，工具如果正常执行的话，提示框信息如下：

生成结果如下：

打开一个要素查看一下，字段、坐标系都没问题。

## 工具箱下载链接

CC工具箱完全免费无套路，可到下方的百度网盘链接直接下载工具。如果对工具使用仍有不理解的地方、无法解决的错误、改进的意见，可以加下面的交流群导游号入群进行反馈，同时欢迎关注本人公众号。

---

通过本指南，您可以轻松掌握CC工具箱的使用方法，特别是针对“属性结构描述表空库(批量)”功能的操作步骤。希望本资源对您的工作有所帮助。

## 下载链接

[CC工具箱使用指南属性结构描述表空库批量](https://pan.quark.cn/s/63c52a4e1358)