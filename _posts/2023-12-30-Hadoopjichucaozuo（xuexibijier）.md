---
layout: post
title: "Hadoop基础操作（学习笔记二）"
date:   2021-09-23
tags: [hdfs,Hadoop,dfs,email,log]
comments: true
author: admin
---
# Hadoop基础操作（学习笔记二）

欢迎来到Hadoop基础操作的学习笔记第二部分。本笔记详细介绍了Hadoop集群的基本管理和操作步骤，适合初学者快速上手。以下是本文档涵盖的主要内容：

## 一、Hadoop集群基本信息查看

- **监控服务**: 通过访问`http://master:50070/`，您可以监控HDFS的状态。
- **资源信息**: 查看集群计算资源，在浏览器中输入`http://master:8088/cluster/nodes`。
- **文件系统浏览**: 使用`http://master:50070/nn_browserdfscontent.jsp`查看HDFS根目录。

## 二、HDFS文件操作

### 上传文件到HDFS
假设您有一个名为'email_log.txt'的文件，通过以下命令将其上传：
```sh
hdfs dfs -put /home/email_log.txt /user/test/example
```
文件会被切分成128MB块，并且每个块会有三个副本，分布存储于不同数据节点上。

### 下载与删除文件
- 下载文件: `hdfs dfs -copyToLocal /user/test/example/email_log.txt /local/path/`
- 删除文件或目录: `hdfs dfs -rm -r /user/test/example/email_log.txt`

## 三、运行MapReduce任务

以统计'email_log.txt'中的用户登录次数为例，首先确认Hadoop的示例jar路径，然后运行：
```sh
hadoop jar /path/to/hadoop-mapreduce-examples-2.x.jar wordcount /user/test/example/email_log.txt /user/root/output
```
完成后，结果位于`/user/root/output`，包括`_SUCCESS`标志文件和实际输出文件`part-r-00000`。

## 四、集群任务管理
- **监控与管理任务**: 访问`http://master:8088/cluster/apps`来查看和管理任务。
- **中断任务**: 选择任务并终止其运行。

## 五、常用HDFS Shell命令
- **创建目录**: `hdfs dfs -mkdir /new_directory`
- **上传文件**: `hdfs dfs -put localfile /hdfs/path`
- **下载文件**: `hdfs dfs -get /hdfs/path localfile`
- **删除文件**: `hdfs dfs -rm /path/to/file`

这篇笔记为你提供了实用的Hadoop操作指导，帮助你在实践中更好地理解和运用Hadoop。记得理论结合实践，不断提升你的大数据处理技能。

## 下载链接

[Hadoop基础操作学习笔记二分享](https://pan.quark.cn/s/aa9177b0f12f)