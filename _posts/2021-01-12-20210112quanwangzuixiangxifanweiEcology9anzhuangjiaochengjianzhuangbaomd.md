---
layout: post
title: "全网最详细泛微Ecology9安装教程及安装包"
date:   2020-02-05
tags: [安装,泛微,Ecology9,JDK,Resin]
comments: true
author: admin
---
# 全网最详细泛微Ecology9安装教程及安装包

本仓库提供了一个详细的泛微Ecology9安装教程及安装包，帮助用户顺利完成泛微Ecology9的安装和配置。以下是安装步骤的简要概述：

## 安装步骤

1. **选择安装路径**  
   选择合适的安装路径，确保有足够的磁盘空间。

2. **选择JDK安装的目录**  
   配置JDK的安装目录，确保JDK版本符合要求。

3. **端口检测与修改**  
   检测端口是否被占用，如果被占用，需要修改端口。

4. **下载并安装Resin**  
   下载完成后，打开安装目录下的Resin文件夹，点击`Install/Change`开始安装Resin。

5. **新建数据库**  
   使用SQL Server Management Studio或Navicat新建数据库。

6. **初始化数据库**  
   打开浏览器，输入`http://127.0.0.1:8085`，填写验证码、数据库名称等信息，点击初始化数据库。

7. **处理JDK相关问题**  
   如果使用JDK 1.8，可能会出现报错，需要修改`java.security`文件中的相关配置。

8. **检查SQL Server配置**  
   确保SQL Server设置了固定端口1433，并检查防火墙是否放行了1433端口。

9. **初始化完成**  
   初始化完成后，可以在数据库中看到生成的表。

10. **重启Resin服务**  
    重启Resin服务后，登录泛微OA，sysadmin密码存放在表HrmResourceManager中。

11. **上传License文件**  
    如果是第一次登录，需要上传License文件，License文件可以从公司系统的License授权文件中申请后下载。

12. **登录成功**  
    上传完License后，登录成功。

## 注意事项

- 确保所有步骤按照教程操作，避免遗漏。
- 如果遇到问题，可以参考教程中的常见问题解答部分。
- 安装过程中，确保网络连接稳定，避免因网络问题导致安装失败。

通过本教程，您将能够顺利完成泛微Ecology9的安装和配置，开始使用泛微OA系统。

## 下载链接

[全网最详细泛微Ecology9安装教程及安装包](https://pan.quark.cn/s/a772d5f13f1a)