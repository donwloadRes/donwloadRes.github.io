---
layout: post
title: "PLSQLDeveloper登录时没有可选数据库和数据库连接问题解决办法"
date:   2023-02-23
tags: [数据库,Developer,Oracle,Instant,Client]
comments: true
author: admin
---
# PLSQLDeveloper登录时没有可选数据库和数据库连接问题解决办法

在使用PL/SQL Developer时，用户可能会遇到无法看到可选数据库或数据库连接选项的问题，这可能是因为配置不当所引起。以下是一套详细的解决步骤，帮助您顺利解决这一常见问题，确保您能够正常连接到Oracle数据库。

### 问题现象

- 登录PL/SQL Developer时，界面中缺乏数据库选项。
- 无法选择“连接为...”进行数据库登录。

### 解决策略

#### 第一步：配置Instant Client

1. **下载并解压Instant Client**: 获取适用于您的Oracle版本的Instant Client压缩包，例如`instantclient_11_2`，并解压至非中文目录。
   
2. **设置PLSQL Developer配置**：
   - 不登录，点击取消。
   - 进入`Tools` > `Preferences`，在`Oracle` -> `Connection`下，指定Instant Client的路径，确保`OCI Library`设置为您解压后的`oci.dll`完整路径。
   
3. **环境确认**：确保Oracle的相关服务已启动，并检查是否有端口冲突。

#### 第二步：处理数据库连接问题

1. **复制tnsnames.ora**：找到Oracle的tnsnames.ora文件（通常位于Oracle安装的网络\admin目录），将其复制到Instant Client的安装目录下。

2. **配置PLSQL Developer启动脚本**（可选，适用于特定情况）：
   - 创建一个批处理文件（`.bat`），设定环境变量指向Instant Client目录，并启动PL/SQL Developer。例如：
     ```batch
     set path=<Your_InstantClient_Path>
     set ORACLE_HOME=<Your_InstantClient_Path>
     set TNS_ADMIN=<Your_InstantClient_Path>
     set NLS_LANG=SIMPLIFIED CHINESE_CHINA.ZHS16GBK
     start plsqldev.exe
     ```
   - 通过此脚本启动软件以正确加载连接信息。

#### 第三步：检查和服务调整

- 确认数据库监听器(`lsnrctl status`)工作正常。
- 如果遇到特定的错误代码，如ORA-12514，需检查服务名称配置是否正确。

### 结论

面对PL/SQL Developer无法展示数据库选项的问题，通过正确配置 Instant Client 和 tnsnames.ora 文件，以及适当的环境变量设置，您可以解决这一登录障碍，恢复数据库的正常连接。记得每次更改配置后重启PL/SQL Developer以使变更生效。希望这份指南能助您快速排除困扰，高效使用数据库管理工具。

## 下载链接

[PLSQLDeveloper登录时没有可选数据库和数据库连接问题解决办法](https://pan.quark.cn/s/97fbfabcdb9b)