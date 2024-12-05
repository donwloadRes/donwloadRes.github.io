---
layout: post
title: "Go程序设计语言——Go语言圣经 中文版（高清，非扫描，带目录）"
date:   2024-09-28
tags: [示例,Go,10.7,11.2,3.5]
comments: true
author: admin
---
# Go程序设计语言——Go语言圣经 中文版（高清，非扫描，带目录）

## 资源描述

本书由《C程序设计语言》的作者Kernighan和谷歌公司Go团队主管Alan Donovan联袂撰写，是学习Go语言程序设计的权威指南。本书共13章，涵盖了Go语言的基础知识、基本结构、基本数据类型、复合数据类型、函数、方法、接口、goroutine、通道、共享变量的并发性、包、go工具、测试、反射等内容。

本书内容详实，结构清晰，适合作为计算机相关专业的教材，也可供Go语言爱好者阅读。

## 目录

### 第1章　入门
1.1　hello，world  
1.2　命令行参数  
1.3　找出重复行  
1.4　GIF动画  
1.5　获取一个URL  
1.6　并发获取多个URL  
1.7　一个Web服务器  
1.8　其他内容  

### 第2章　程序结构
2.1　名称  
2.2　声明  
2.3　变量  
2.3.1　短变量声明  
2.3.2　指针  
2.3.3　new函数  
2.3.4　变量的生命周期  
2.4　赋值  
2.4.1　多重赋值  
2.4.2　可赋值性  
2.5　类型声明  
2.6　包和文件  
2.6.1　导入  
2.6.2　包初始化  
2.7　作用域  

### 第3章　基本数据
3.1　整数  
3.2　浮点数  
3.3　复数  
3.4　布尔值  
3.5　字符串  
3.5.1　字符串字面量  
3.5.2　Unicode  
3.5.3　UTF-8  
3.5.4　字符串和字节slice  
3.5.5　字符串和数字的相互转换  
3.6　常量  
3.6.1　常量生成器iota  
3.6.2　无类型常量  

### 第4章　复合数据类型
4.1　数组  
4.2　slice  
4.2.1　append函数  
4.2.2　slice就地修改  
4.3　map  
4.4　结构体  
4.4.1　结构体字面量  
4.4.2　结构体比较  
4.4.3　结构体嵌套和匿名成员  
4.5　JSON  
4.6　文本和HTML模板  

### 第5章　函数
5.1　函数声明  
5.2　递归  
5.3　多返回值  
5.4　错误  
5.4.1　错误处理策略  
5.4.2　文件结束标识  
5.5　函数变量  
5.6　匿名函数  
5.7　变长函数  
5.8　延迟函数调用  
5.9　宕机  
5.10　恢复  

### 第6章　方法
6.1　方法声明  
6.2　指针接收者的方法  
6.3　通过结构体内嵌组成类型  
6.4　方法变量与表达式  
6.5　示例：位向量  
6.6　封装  

### 第7章　接口
7.1　接口即约定  
7.2　接口类型  
7.3　实现接口  
7.4　使用flag.Value来解析参数  
7.5　接口值  
7.6　使用sort.Interface来排序  
7.7　http.Handler接口  
7.8　error接口  
7.9　示例：表达式求值器  
7.10　类型断言  
7.11　使用类型断言来识别错误  
7.12　通过接口类型断言来查询特性  
7.13　类型分支  
7.14　示例：基于标记的XML解析  
7.15　一些建议  

### 第8章　goroutine和通道
8.1　goroutine  
8.2　示例：并发时钟服务器  
8.3　示例：并发回声服务器  
8.4　通道  
8.4.1　无缓冲通道  
8.4.2　管道  
8.4.3　单向通道类型  
8.4.4　缓冲通道  
8.5　并行循环  
8.6　示例：并发的Web爬虫  
8.7　使用select多路复用  
8.8　示例：并发目录遍历  
8.9　取消  
8.10　示例：聊天服务器  

### 第9章　使用共享变量实现并发
9.1　竞态  
9.2　互斥锁：sync.Mutex  
9.3　读写互斥锁：sync.RWMutex  
9.4　内存同步  
9.5　延迟初始化：sync.Once  
9.6　竞态检测器  
9.7　示例：并发非阻塞缓存  
9.8　goroutine与线程  
9.8.1　可增长的栈  
9.8.2　goroutine调度  
9.8.3　GOMAXPROCS  
9.8.4　goroutine没有标识  

### 第10章　包和go工具
10.1　引言  
10.2　导入路径  
10.3　包的声明  
10.4　导入声明  
10.5　空导入  
10.6　包及其命名  
10.7　go工具  
10.7.1　工作空间的组织  
10.7.2　包的下载  
10.7.3　包的构建  
10.7.4　包的文档化  
10.7.5　内部包  
10.7.6　包的查询  

### 第11章　测试
11.1　go test工具  
11.2　Test函数  
11.2.1　随机测试  
11.2.2　测试命令  
11.2.3　白盒测试  
11.2.4　外部测试包  
11.2.5　编写有效测试  
11.2.6　避免脆弱的测试  
11.3　覆盖率  
11.4　Benchmark函数  
11.5　性能剖析  
11.6　Example函数  

### 第12章　反射
12.1　为什么使用反射  
12.2　reflect.Type和reflect.Value  
12.3　Display：一个递归的值显示器  
12.4　示例：编码S表达式  
12.5　使用reflect.Value来设置值  
12.6　示例：解码S表达式  
12.7　访问结构体字段标签  
12.8　显示类型的方法  
12.9　注意事项  

### 第13章　低级编程
13.1　unsafe.Sizeof、Alignof 和Offsetof  
13.2　unsafe.Pointer  
13.3　示例：深度相等  
13.4　使用cgo调用C代码  
13.5　关于安全的注意事项  

## 资源特点
- **高清**：本书为高清版本，阅读体验极佳。
- **非扫描**：内容为可编辑的文本格式，方便读者进行笔记和标注。
- **带目录**：目录结构清晰，方便读者快速定位所需内容。

## 适用人群
- 计算机相关专业的学生和教师
- Go语言爱好者和开发者
- 希望深入学习Go语言的程序员

## 使用建议
建议读者在学习过程中结合实际项目进行练习，以加深对Go语言的理解和掌握。

## 下载链接

[Go程序设计语言Go语言圣经中文版高清非扫描带目录分享](https://pan.quark.cn/s/cb6d83858a1c)