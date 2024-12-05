---
layout: post
title: "Oracle XE 下载与安装指南"
date:   2020-04-05
tags: [Oracle,安装,XE,下载,数据库]
comments: true
author: admin
---
# Oracle XE 下载与安装指南

本仓库提供了一个关于Oracle XE（Express Edition）数据库的下载与安装指南。Oracle XE是一个轻量级的、免费的数据库版本，适用于开发、部署和发布。以下是详细的下载与安装步骤。

## 下载Oracle XE

1. **下载链接**：
   - 访问提供的下载链接，获取Oracle XE的安装文件。

2. **提取码**：
   - 下载链接可能需要提取码，请确保输入正确的提取码以完成下载。

## 安装Oracle XE

1. **安装步骤**：
   - 运行下载的安装文件，按照提示进行安装。
   - 在安装过程中，设置管理员口令（建议使用sys或root）。

2. **安装完成**：
   - 安装完成后，会出现一个界面，点击“完成”按钮关闭此界面。
   - 如果勾选了“在浏览器中打开页面”选项，安装完成后会在浏览器中打开一个页面。

3. **登录验证**：
   - 在用户名处输入sys，在口令处输入刚才设置的口令。
   - 输入无误后点击“登录”按钮，登录成功后会出现相应的页面。

## 验证安装

1. **启动SQL命令行**：
   - 安装完成后，在开始菜单中找到Oracle Database 11g Express Edition，并运行SQL命令行。

2. **连接数据库**：
   - 输入命令：`conn sys as sysdba`，看到“已连接”提示即表示安装成功。
   - 可以尝试执行简单的SQL查询，如：`select 1 from dual;`。

## 环境配置

1. **环境变量设置**：
   - 右击“我的电脑”，点击“属性”，选择“高级系统设置”，弹出系统属性对话框。
   - 选择“环境变量”，新建以下变量：
     - `ORACLE_HOME`：Oracle数据库安装路径
     - `TNS_HOME`：Oracle监听配置路径
     - `NLS_LANG`：设置统一编码格式（如：AMERICAN_AMERICA.ZHS16GBK）
     - `PATH`：将Oracle的bin目录配置进去

2. **监听配置**：
   - 使用编辑器打开tnsnames.ora文件，编辑SERVICE_NAME、HOST和PORT为相应的配置。

## 注意事项

- Oracle XE虽然功能强大，但数据库大小限制在4GB之内，适用于中小型项目。
- 如果需要更强大的功能，可以考虑升级到Oracle Standard或Enterprise Edition。

通过以上步骤，您可以顺利完成Oracle XE的下载与安装，并进行基本的环境配置。希望本指南对您有所帮助！

## 下载链接

[OracleXE下载与安装指南](https://pan.quark.cn/s/3743d6f05fcc)