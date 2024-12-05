---
layout: post
title: "精通Odoo开发和使用"
date:   2022-10-16
tags: [模块,Odoo,视图,数据库,会计科目]
comments: true
author: admin
---
# 精通Odoo开发和使用

## 资源文件描述

本资源文件详细介绍了Odoo的开发和使用，涵盖了从基础到高级的多个方面。内容包括Odoo的历史、ERP简介、Odoo框架的介绍、安装和配置、模块的创建和管理、以及Odoo开发的基础知识。以下是资源文件的主要内容概述：

### 1. ERP简介
- Odoo历史
- ERPⅡ或商业智能化
  - 什么是商业智能

### 2. Odoo框架简介
- Python模块分析
- Python2还是Python3

### 3. Odoo的安装和配置
- PostgreSQL数据库
- Ubuntu14.04下可能缺失的软件包
- 网页显示node.js方面
- 其他问题
- 通过命令行运行时的配置
  - –xmlrpc-port=8888
  - –addons-path=addons
  - 数据库的一些配置
  - –save
- 将安装环境封装起来
- 文档编译

### 4. 初入Odoo
- 管理数据库
- 登录界面
- Administrator首选项
- 导入一个翻译
- 新的Demo用户
- 模块管理
- 修改公司信息
- 打开技术特性支持之后
- 进销存和财务系统的抽象讨论
  - 以采购部门为例
- 安装和配置模块

### 5. 创建自己的模块
- 快速生成模块骨架
  - Python模块的init文件
  - 作为Odoo模块的说明文件
- 安装自定义模块
  - 模块文件夹管理
- 一个简单的演示模块
  - controllers
  - views
  - models
  - security
  - 美化网页
- 加分项: 通过pgadmin3来查看数据库
  - 安装
  - 连接服务器
  - 图形化查询

### 6. Odoo开发基础: 请假模块第一谈
- 纯理论讨论
- 定义模型
- 加入菜单
  - act_window的属性
  - menuitem的属性
- 视图优化
  - 修改tree视图
  - 修改form视图
- 完整的views.xml
- 给模块加个图标

### 7. Odoo开发基础: 工作计划模块第一谈
- 数据访问权限管理
  - access rule
  - record rule

### 8. 扩展现有模块－继承机制
- 给模块增加field
- 修改已有的field
- 重载原模型的方法
  - 什么是Recordset
  - Odoo里面的domain语法
  - recordset的search方法
- 视图xml文件的继承式修改
  - 视图元素添加
  - 原视图元素属性修改
- 多态继承
- 修改其他数据文件
  - 删除记录
  - 更新数据
- 委托继承

### 9. 理解模型内的数据文件
- 理解外部id
- 使用外部id
- 导出或导入数据文件
- 快捷输入标签
- 用field标签设置值
  - eval语法
  - ref属性
  - One2many和Many2many的eval赋值

### 10. Odoo开发基础: 请假模块第二谈
- 本例涉及到的数据库表格简介
- 工作流概念入门
  - 定义工作流对象
  - 创建节点
  - 创建连接

### 11. Odoo模型层详解
- _name
- 各个表头属性
- name字段
- 具体模型的数据
- 模型间的关系
- 工作流

### 12. Odoo视图层详解

### 13. 附录
- Odoo里老的API
- PostgreSQL数据库命令行操作
  - 命令行数据库备份
- 反向代理 (reverse proxy)
  - 安装ngnix软件
  - 强制https连接
  - nginx优化
  - 轮询机制
- 跟踪项目源码初始化进程
  - base模块
  - web模块
  - web_kanban模块
- 配置会计科目
  - 配置会计科目类型
  - 配置会计科目
- 分录
- 新建业务伙伴
  - 新建业务伙伴标签
  - 新建客户
- 创建新的产品
- 设置会计年度
- 向供应商下单
- 会计学入门
  - 财务报表
  - 原始凭证
  - 账户
  - 分类帐
  - 会计科目表
  - 报告期间
- 参考资料

本资源文件适合所有对Odoo开发感兴趣的读者，无论是初学者还是有经验的开发者，都能从中获得有价值的信息和指导。

## 下载链接

[精通Odoo开发和使用分享](https://pan.quark.cn/s/82dbf26d962c)