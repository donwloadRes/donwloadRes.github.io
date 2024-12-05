---
layout: post
title: "SpringBoot  Vue 学生选课管理系统"
date:   2021-06-15
tags: [选课,bash,学生,查询,com]
comments: true
author: admin
---
# SpringBoot + Vue 学生选课管理系统

## 项目介绍

这是一个采用前后端分离开发的学生选课管理系统。前端使用 Vue 框架进行开发，后端则采用 SpringBoot 和 Mybatis 技术栈。该系统主要包含三个角色：管理员（admin）、教师（teacher）和学生（student），每个角色都有其特定的功能和权限。

## 功能模块

### 管理员（admin）

- **教师管理**：实现对教师信息的增删改查。
- **学生管理**：实现对学生信息的增删改查。
- **课程管理**：实现对课程信息的增删改查。
- **教师业务控制**：全方位控制教师业务，如课程开设、学生选课等。
- **学生业务控制**：全方位控制学生业务，如选课、退课、成绩查询等。

### 教师（teacher）

- **课程查询**：查询自己开设的课程。
- **学生信息查询**：查询选择自己课程的学生信息。
- **成绩录入**：对学生成绩进行录入。

### 学生（student）

- **选课与退课**：实现选课和退课的功能。
- **成绩查询**：查询自己的成绩。

## 技术栈

- **前端**：Vue
- **后端**：SpringBoot + Mybatis

## 安装与运行

### 前端

1. 克隆仓库到本地：
   ```bash
   git clone https://github.com/your-repo/springboot-vue-course-selection.git
   ```
2. 进入前端目录：
   ```bash
   cd springboot-vue-course-selection/frontend
   ```
3. 安装依赖：
   ```bash
   npm install
   ```
4. 运行前端项目：
   ```bash
   npm run serve
   ```

### 后端

1. 进入后端目录：
   ```bash
   cd springboot-vue-course-selection/backend
   ```
2. 使用 Maven 安装依赖并运行项目：
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

## 贡献

欢迎任何形式的贡献，包括但不限于代码提交、问题反馈、功能建议等。请参考 [CONTRIBUTING.md](CONTRIBUTING.md) 了解更多详情。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。

## 联系我们

如有任何问题或建议，请通过以下方式联系我们：

- 邮箱：[your-email@example.com](mailto:your-email@example.com)
- 项目地址：[GitHub](https://github.com/your-repo/springboot-vue-course-selection)

感谢您的关注和支持！

## 下载链接

[SpringBootVue学生选课管理系统](https://pan.quark.cn/s/90d1b775d373)