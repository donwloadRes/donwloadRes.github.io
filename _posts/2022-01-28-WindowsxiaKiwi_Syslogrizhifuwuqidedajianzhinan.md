---
layout: post
title: "Windows下Kiwi_Syslog日志服务器的搭建指南"
date:   2021-05-20
tags: [日志,Syslog,点击,Kiwi,安装]
comments: true
author: admin
---
# Windows下Kiwi_Syslog日志服务器的搭建指南

## 简介
本资源文件提供了在Windows操作系统下搭建Kiwi_Syslog日志服务器的详细步骤和配置说明。Kiwi_Syslog是一款功能强大的Syslog服务器软件，适用于网络管理员和IT专业人士，用于集中和简化日志消息管理。

## 安装步骤
1. **下载Kiwi_Syslog服务器软件**  
   从提供的链接下载Kiwi_Syslog服务器软件安装包。

2. **运行安装程序**  
   解压下载的文件，运行`Kiwi_Syslog_Server_9.5.0_setup.exe`安装程序。

3. **安装过程中的选项**  
   - 点击“I Agree”同意许可协议。
   - 选择默认选项，点击“Next”继续。
   - 在某些步骤中，可以选择不安装网页日志获取服务，不影响正常使用。
   - 选择默认路径，点击“Install”进行安装。

4. **安装.NET Framework 3.5**  
   如果安装过程中提示需要安装.NET Framework 3.5，点击安装。如果无法安装，可以在安装完成后手动安装。

5. **完成安装**  
   安装完成后，取消对勾，点击“Finish”结束安装。

## 配置步骤
1. **结束syslogd_service进程**  
   在任务管理器中结束掉`syslogd_service`的进程。

2. **复制注册文件**  
   将“Keygen注册机”文件夹中的`SolarWinds_Licensing_Framework.dll`和`ufmod.dll`复制到软件安装目录“C:\Program Files (x86)\Syslogd”覆盖原文件。

3. **打开Kiwi Syslog Server Console**  
   打开桌面上的Kiwi Syslog Server Console程序。

4. **输入许可证信息**  
   点击上方“Help”>>“Enter license details”，选择第二个选项，点击“Next”。

5. **生成许可证文件**  
   打开“Keygen注册机”文件夹的“keygen.exe”，将ID复制进去，填写用户名和时间，点击“Generate”生成许可证文件。

6. **导入许可证文件**  
   回到软件，点击“导入”，选择生成的许可证文件，完成后点击“Close”关闭弹框。

## 配置日志文件
1. **设置日志文件存放位置**  
   点击左上角的“File”>>“Setup”，选择左侧“Log to file”，设置日志文件的存放位置和格式。

2. **配置计划任务**  
   点击左侧“Schedules”，点击左上角的“新建”进行配置计划任务，设置日志计划频率、临时存储路径和最终日志存储目录。

3. **修改日志编码**  
   点击左侧“Input”>>“UDP”，修改“Date encoding”的值为“Utf-8”，防止部分带有汉字的日志为乱码。

## 发送端设置
1. **防火墙设置**  
   每个品牌的防火墙设置方法不同，具体请查询设备文档。

2. **Windows设置**  
   下载并安装Evtsys，将文件拷贝到“C:\Windows\System32”目录，通过命令提示符启动服务。

## 总结
通过以上步骤，您可以在Windows系统上成功搭建Kiwi_Syslog日志服务器，并配置相关设置以接收、记录和管理来自网络设备的日志信息。

## 下载链接

[Windows下Kiwi_Syslog日志服务器的搭建指南分享](https://pan.quark.cn/s/975ee891825a)