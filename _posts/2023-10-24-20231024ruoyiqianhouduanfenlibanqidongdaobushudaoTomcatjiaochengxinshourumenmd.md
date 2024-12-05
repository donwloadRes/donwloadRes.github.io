---
layout: post
title: "若依前后端分离版启动到部署到Tomcat 教程新手入门"
date:   2022-10-15
tags: [Tomcat,部署,Vue,若依,war]
comments: true
author: admin
---
# 若依前后端分离版启动到部署到Tomcat 教程（新手入门）

欢迎来到若依(RuoYi)前后端分离版的部署指南，专为初次接触项目部署的小白定制。本教程将一步步引导您完成若依Vue项目的本地运行至最终部署到Tomcat服务器的过程，确保即使是初学者也能顺利完成。

## 步骤概述

### 1. **项目获取**
- 访问若依官方Gitee仓库([https://gitee.com/y_project/RuoYi-Vue](https://gitee.com/y_project/RuoYi-Vue))下载最新代码。
- 使用IDEA或其他编辑器，通过Git克隆项目到本地。

### 2. **前端运行**
- 进入Vue项目目录，执行`npm install`安装依赖。
- 继续使用`npm run serve`启动前端服务，确认前端界面正确展示。

### 3. **后台配置与启动**
- 创建MySQL数据库`ry-vue`，导入项目提供的SQL脚本。
- 在`ruoyi-admin`模块下，调整数据库连接配置，如URL、用户名和密码。
- 设置Redis，作为缓存服务器，默认端口6379，保证其正常运行。
- 修改后端配置文件，确保所有环境配置符合本地开发或部署需求。
- 使用Maven的`package`命令生成后台 `.jar` 或者转换成 `.war` 格式用于Tomcat。

### 4. **部署到Tomcat**
- 确保Tomcat服务器已安装，并配置好JDK环境。
- 对于`.war`包，需在`ruoyi-admin`的`pom.xml`指定打包类型为`war`，去除内置Tomcat插件。
- 构建后，将生成的`.war`文件放到Tomcat的`webapps`目录下。
- 重启Tomcat服务器，通过浏览器访问确认后端服务已启动。

### 5. **前端部署**
- 修改Vue项目的`config/index.js`里的`publicPath`为您的部署路径。
- 执行`npm run build`生成生产环境的静态文件。
- 将生成的`dist`文件夹内容部署到Tomcat的相应目录下，通常是创建新的目录，并将此目录映射为应用上下文路径。
- 注意处理可能的404错误，可能需要在Tomcat的`webapps`下创建`WEB-INF`文件夹，并配置特定的XML文件。

### 6. **解决刷新404问题**
- 部署过程中，确保解决SPA单页应用刷新导致的404问题，可能需要在Tomcat配置或使用特定的HTML错误页面策略。

### 结束语
按照上述步骤，即使是对部署工作完全陌生的新手，也可以成功地将若依前后端分离项目部署到本地或服务器上的Tomcat环境中。实践是最好的老师，动手试试吧！

## 下载链接

[若依前后端分离版启动到部署到Tomcat教程新手入门](https://pan.quark.cn/s/3b91756c9d2e)