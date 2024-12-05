---
layout: post
title: "Windows环境下Hadoop安装和配置详细步骤（图文）"
date:   2021-08-13
tags: [Hadoop,Windows,配置,HOME,目录]
comments: true
author: admin
---
# Windows环境下Hadoop安装和配置详细步骤（图文）

本文详细介绍了在Windows环境下安装和配置Hadoop的步骤，包括所需的软件下载、环境变量配置、文件修改等内容。通过图文并茂的方式，帮助用户一步步完成Hadoop的安装和配置。

## 主要内容

1. **下载Hadoop**  
   从官方网站下载Hadoop的二进制文件，并解压到指定目录。

2. **修改配置文件**  
   原版的Hadoop不支持Windows系统，需要下载并解压hadooponwindows-master.zip，复制其中的bin和etc文件到Hadoop目录中，替换原有的文件。

3. **配置JAVA_HOME**  
   下载并配置JDK，设置JAVA_HOME环境变量，并检查是否配置成功。

4. **配置HADOOP_HOME**  
   设置HADOOP_HOME环境变量，并将%HADOOP_HOME%\bin添加到系统环境变量path中。

5. **修改hadoop-env.cmd**  
   使用编辑器打开hadoop-env.cmd文件，修改JAVA_HOME的路径为JDK的安装路径。

6. **创建必要的文件夹**  
   在Hadoop目录下创建tmp、data、namenode和datanode文件夹。

7. **修改hdfs-site.xml**  
   打开hdfs-site.xml文件，修改路径为Hadoop目录下的namenode和datanode。

8. **拷贝hadoop.dll**  
   从Hadoop的bin目录下拷贝hadoop.dll到C:\Windows\System32目录中，以避免在Windows平台使用MapReduce测试时报错。

9. **格式化HDFS**  
   以管理员身份打开命令提示符，输入`hdfs namenode -format`命令，格式化HDFS。

10. **启动Hadoop集群**  
    转到Hadoop的sbin目录下，输入`start-all`命令启动Hadoop集群。

11. **验证Hadoop集群**  
    输入`jps`命令查看运行的所有节点，并通过浏览器访问Hadoop的Web界面（http://localhost:50070）和YARN的Web界面（http://localhost:8088）。

12. **上传测试文件**  
    根据core-site.xml的配置，通过命令行上传测试文件到HDFS。

通过以上步骤，您可以在Windows环境下成功安装和配置Hadoop，并进行基本的操作和测试。

## 下载链接

[Windows环境下Hadoop安装和配置详细步骤图文](https://pan.quark.cn/s/006b296dc771)