---
layout: post
title: "PHPMySQL学生成绩管理系统"
date:   2023-04-28
tags: [成绩,学生,课程,数据库,教师]
comments: true
author: admin
---
# PHP+MySQL学生成绩管理系统

## 项目描述

本项目是一个基于PHP和MySQL的学生成绩管理系统，旨在为学校提供一个高效、便捷的管理工具。系统分为三个主要模块：学生模块、教师模块和管理员模块。每个模块都有其特定的功能，以满足不同用户的需求。

### 管理员模块
- **学生和教师信息管理**：管理员可以对学生和教师的信息进行增删改操作。
- **课程信息管理**：管理员可以发布、修改和删除课程信息，以便学生进行选课。
- **成绩审核与存档**：管理员可以审核教师提交的学生成绩，并打印成绩存档。
- **成绩查询**：管理员可以按课号查询每个课程的学生成绩统计，也可以按学号查看学生的成绩情况，方便进行教学总结。

### 教师模块
- **个人信息修改**：教师可以修改自己的个人信息。
- **课程与学生管理**：教师可以查看自己所教的课程及选择该课程的学生，并为学生录入平时成绩和考试成绩。系统会根据课程比例自动计算总分，并提交给管理员审核。
- **成绩查询**：教师可以查询自己所教课程的成绩情况。

### 学生模块
- **个人信息修改**：学生可以修改自己的个人信息。
- **选课与退课**：学生可以根据学年进行选课和退课操作。
- **成绩与学分查询**：学生可以查询已取得的学分、课程成绩以及学分绩，并打印各门课成绩的统计报表。

## 技术栈

- **前端**：HTML, CSS, JavaScript, jQuery, Bootstrap
- **后端**：
  - 控制器：SpringMVC
  - 依赖注入：Spring
  - ORM：MyBatis
- **数据库**：MySQL

## 安装与配置

1. **下载项目**：由于项目中含有大量图片，下载时间可能会比较久。
2. **数据库配置**：
   - 新建数据库 `bookstore`。
   - 导入 `bookstore.sql` 文件。
3. **修改数据库配置**：
   - 在 `resource` 文件夹下找到 `db.properties` 文件。
   - 将数据库账号和密码修改成自己MySQL数据库的账号密码。

## 访问地址

- **首页地址**：`http://localhost:8080/index.do`
- **后台管理地址**：`http://localhost:8080/backLoginPage.do`

## 注意事项

- 项目中包含大量图片，下载时间可能较长。
- 请确保数据库配置正确，以便系统正常运行。

通过本系统，学校可以更高效地管理学生成绩，教师和学生也可以更方便地进行相关操作。希望本项目能为您的教学管理工作带来便利。

## 下载链接

[PHPMySQL学生成绩管理系统](https://pan.quark.cn/s/47cc87c5bb0a)