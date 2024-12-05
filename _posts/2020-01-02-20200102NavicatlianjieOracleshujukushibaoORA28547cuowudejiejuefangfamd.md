---
layout: post
title: "Navicat连接Oracle数据库时报ORA28547错误的解决方法"
date:   2022-10-02
tags: [Oracle,Navicat,数据库,ORA,28547]
comments: true
author: admin
---
# Navicat连接Oracle数据库时报ORA-28547错误的解决方法

## 简介
本资源文件提供了一个解决Navicat连接Oracle数据库时报ORA-28547错误的有效方法。该错误通常是由于Navicat自带的oci.dll文件不支持Oracle 11g版本，需要下载对应支持的版本并进行配置。

## 解决步骤

### 1. 查询Oracle版本
首先，使用IDEA或其他工具连接到Oracle数据库，执行以下SQL查询版本：
```sql
select * from v$version;
```

### 2. 下载Oracle对应oci.dll文件
从Oracle官网下载对应版本的Instant Client，可能需要注册Oracle账号。下载后解压文件。

### 3. 修改oci配置
将下载的Instant Client文件夹中的所有文件覆盖到Navicat的OCI环境目录下。

### 4. 修改Navicat配置
打开Navicat，依次点击“工具” -> “选项” -> “环境”，在OCI环境选项中选择新解压出来的oci.dll文件。

### 5. 重启Navicat并连接Oracle
完成配置后，重启Navicat并尝试连接Oracle数据库。

## 总结
通过以上步骤，可以有效解决Navicat连接Oracle数据库时报ORA-28547错误的问题。确保OCI版本与Oracle服务器版本匹配是关键。

## 下载链接

[Navicat连接Oracle数据库时报ORA-28547错误的解决方法](https://pan.quark.cn/s/a68aacec7fe3)