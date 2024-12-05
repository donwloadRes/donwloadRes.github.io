---
layout: post
title: "在Linux中安装Pentaho Server 9.1并使用MySQL作为存储库"
date:   2020-08-03
tags: [MySQL,pentaho,配置文件,安装包,安装]
comments: true
author: admin
---
# 在Linux中安装Pentaho Server 9.1并使用MySQL作为存储库

本文详细介绍了如何在Linux系统中安装Pentaho Server 9.1，并将其配置为使用MySQL作为存储库。通过本文的步骤，您可以顺利完成Pentaho Server的安装和配置，确保其正常运行。

## 一、本文环境

- 应用名称：CentOS Linux
- 应用版本：7.99.15.71.8
- Pentaho Server CE：9.1.0.0-324
- MySQL：已安装并配置
- JDK：已安装并配置

## 二、准备工作

1. **下载pentaho-server-ce-9.1.0.0-324安装包**
   - 开源仓库渠道：[下载链接](https://sourceforge.net/projects/pentaho/files/Pentaho%209.1/server/)
   - 百度网盘渠道：[下载链接](https://pan.baidu.com/s/1UB91ACgdG3bUBSP5keRa3w) 提取码：y2ql

2. **安装JDK（省略）**
3. **安装MySQL（省略）**

## 三、安装Pentaho Server

1. **创建目录**
   - 在`/opt`目录下创建`software`和`module`两个目录，分别用于存放软件安装包和软件具体安装路径。

2. **上传安装包**
   - 将`pentaho-server-ce-9.1.0.0-324.zip`安装包上传至`/opt/software/`目录下。

3. **解压安装包**
   - 使用`unzip`命令解压安装包。如果系统中没有`unzip`命令，可以通过`yum install -y unzip zip`命令安装。

4. **移动解压后的目录**
   - 将解压后的`pentaho-server`目录移动至`/opt/module/`目录下。

5. **切换存储库为MySQL并修改配置文件**
   - 修改MySQL脚本中的默认密码以及字符集编码为UTF-8，密码自定义。
   - 登录MySQL并运行相关SQL脚本。
   - 修改`pentaho-solutions/system/quartz/quartz.properties`配置文件。
   - 修改`pentaho-solutions/system/applicationContext-spring-security-jdbc.properties`配置文件。
   - 修改`pentaho-solutions/system/simple-jndi/jdbc.properties`配置文件。
   - 修改`pentaho-solutions/system/applicationContext-spring-security-hibernate.properties`配置文件。
   - 修改`pentaho-solutions/system/hibernate/hibernate-settings.xml`配置文件。
   - 修改`pentaho-solutions/system/hibernate/mysql5.hibernate.cfg.xml`配置文件。
   - 替换审计日志文件的默认版本为MySQL对应的配置文件。
   - 将Jackrabbit的配置文件`repository.xml`的仓库信息配置为MySQL。

6. **下载MySQL的JDBC连接驱动**
   - 下载MySQL的JDBC连接驱动，并将其上传到`/opt/software`目录中，然后将其复制到`pentaho-server/tomcat/lib`目录中。

## 四、总结

通过以上步骤，您已经成功在Linux系统中安装并配置了Pentaho Server 9.1，并将其与MySQL数据库集成。希望本文对您有所帮助。

## 下载链接

[在Linux中安装PentahoServer9.1并使用MySQL作为存储库分享](https://pan.quark.cn/s/ece89b9795b1)