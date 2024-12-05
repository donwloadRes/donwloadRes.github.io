---
layout: post
title: "JavaWeb图书项目2.0：Vue axios Servlet Lombok JDBC MySQL"
date:   2020-10-08
tags: [图书,信息,数据库,用户,项目]
comments: true
author: admin
---
# JavaWeb图书项目2.0：Vue axios Servlet Lombok JDBC MySQL

## 项目简介

本项目是一个基于JavaWeb的简单图书管理系统，采用Vue、axios、Servlet、Lombok、JDBC和MySQL等技术实现。项目旨在提供一个基础的图书管理功能，包括用户登录、注册、信息修改、图书信息管理、图书类型统计等功能。

## 功能列表

1. **用户登录**：
   - 用户输入用户名和密码进行登录，登录成功后信息保存到session中，并跳转到首页。

2. **用户注册**：
   - 用户输入相关信息（包括验证码）进行注册，注册成功后跳转到登录页面。

3. **用户信息修改**：
   - 用户可以修改昵称和密码。

4. **图书信息页面**：
   - 展示所有图书信息，支持数据分页显示、分页展示、模糊查询以及只显示用户自己的图书。

5. **新增图书信息**：
   - 用户可以新增一条图书信息，包括选择图书类型、输入书名和简介，信息插入数据库后返回图书信息页面。

6. **删除图书信息**：
   - 用户只能删除自己的图书，删除成功后返回图书信息页面。

7. **修改图书信息**：
   - 用户可以修改图书信息，原有的信息会进行回显，修改成功后返回图书信息页面。

8. **图书类型分类统计**：
   - 按照图书类型进行统计，数量为0的类型也会显示为0。

## 技术栈

- **前端**：Vue、axios
- **后端**：Servlet、Lombok
- **数据库**：MySQL
- **数据访问**：JDBC

## 项目结构

- `src/`：包含项目的源代码。
- `web/`：包含前端页面和静态资源。
- `lib/`：包含项目依赖的第三方库。
- `conf/`：包含数据库配置文件。

## 运行环境

- JDK 1.8 或更高版本
- Tomcat 9.0 或更高版本
- MySQL 5.7 或更高版本

## 安装与运行

1. **克隆项目**：
   ```bash
   git clone https://github.com/yourusername/JavaWebBookProject.git
   ```

2. **导入数据库**：
   - 在MySQL中创建一个新的数据库，并将项目中的SQL文件导入到该数据库中。

3. **配置数据库连接**：
   - 修改`conf/db.properties`文件中的数据库连接信息，确保与本地数据库配置一致。

4. **部署项目**：
   - 将项目打包成WAR文件，并部署到Tomcat服务器中。

5. **启动Tomcat**：
   - 启动Tomcat服务器，访问`http://localhost:8080/JavaWebBookProject`即可进入系统。

## 注意事项

- 项目中的用户密码存储为明文，请在实际使用中进行加密处理。
- 项目中的验证码功能较为简单，建议在实际使用中增加验证码的复杂度。

## 贡献

欢迎大家提交Issue和Pull Request，共同完善这个项目。

## 许可证

本项目采用MIT许可证，详情请参阅`LICENSE`文件。

## 下载链接

[JavaWeb图书项目2.0VueaxiosServletLombokJDBCMySQL](https://pan.quark.cn/s/cf38b9cc0a04)