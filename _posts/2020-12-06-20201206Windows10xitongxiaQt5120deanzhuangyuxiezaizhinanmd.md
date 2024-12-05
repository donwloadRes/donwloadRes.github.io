---
layout: post
title: "Windows 10系统下Qt5120的安装与卸载指南"
date:   2022-05-12
tags: [点击,Qt,安装,卸载,qt]
comments: true
author: admin
---
# Windows 10系统下Qt5.12.0的安装与卸载指南

本资源文件提供了在Windows 10系统下安装和卸载Qt5.12.0的详细步骤。Qt5.12.0是一个跨平台的开发工具包，适用于开发桌面应用程序、移动应用程序和嵌入式系统。以下是安装和卸载的具体步骤。

## 安装步骤

1. **安装包下载**
   - 从Qt社区下载：[Qt社区下载链接](https://download.qt.io/archive/qt/5.12/5.12.10/qt-opensource-windows-x86-5.12.10.exe)
   - 从百度网盘下载：[百度网盘下载链接](链接：百度网盘 请输入提取码)
   - 从Qt官网下载：[Qt官网下载链接](https://www.qt.io/download)

2. **安装提示**
   - 下载好安装包之后，建议断网安装。若联网安装，第二步时需要登录。

3. **软件安装**
   - 双击下载好的安装包，点击“Next”。
   - 清空“Email”和“Password”，点击“skip”。
   - 点击“下一步”，更改安装位置，点击下一步。
   - 选择以下四个组件：
     - MinGW 7.3.0 64-bit：MinGW编译器
     - Sources：Qt源码
     - Qt Creator 4.8.0 CDB Debugger Surpport：用于与CDB调试工具对接
     - MinGW 7.3.0 64-bit：开源的编译器套件
   - 选择“I have read…”，点击“下一步”。
   - 默认，点击“下一步”。
   - 点击“安装”，等待安装完成。

4. **环境配置**
   - 点击“开始”，找到 Windows 系统->此电脑->更多->属性。
   - 点击“高级系统设置”。
   - 点击“环境变量”。
   - 双击“Path”，点击“新建”，把Qt安装目录下的“5.12.0\mingw73_64\bin”添加到环境变量中。
   - 点击“确定”、“确定”、“确定”。

5. **软件测试**
   - 打开Qt Creator，点击“New Project”，选择“Application”，选择“Qt Widgets Application”，点击“Chose”。
   - 更改项目名称和位置，选择编译器，默认，点击“下一步”，默认，点击完成。
   - 双击“mainwindow.ui”，拖拽一个“Push Button”，右击“Push Button”，选择“转到槽”，选择“clicked()”，点击“OK”。
   - 在mainwindow.cpp中添加如下代码：
     ```cpp
     void MainWindow::on_pushButton_clicked()
     {
         qDebug() << "hello qt";
     }
     ```
   - 点击“绿色三角”运行程序，点击“PushButton”，应用程序输出窗口输出“hello qt”，表示程序安装没问题。

## 卸载步骤

1. **软件卸载**
   - 找到Qt安装目录，双击“MaintenanceTool.exe”。
   - 点击“Next”，点击“Skip”。
   - 选择“删除所有组件”，点击“下一步”。
   - 点击“卸载”，等待卸载完成。

通过以上步骤，您可以在Windows 10系统下成功安装和卸载Qt5.12.0。希望本指南对您有所帮助。

## 下载链接

[Windows10系统下Qt5.12.0的安装与卸载指南](https://pan.quark.cn/s/6978b6cfacbc)