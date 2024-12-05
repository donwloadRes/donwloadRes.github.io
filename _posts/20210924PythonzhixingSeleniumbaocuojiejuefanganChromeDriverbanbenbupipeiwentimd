---
layout: post
title: "Python执行Selenium报错解决方案：ChromeDriver版本不匹配问题"
date:   2022-03-14
tags: [ChromeDriver,Chrome,版本,浏览器,点击]
comments: true
author: admin
---
# Python执行Selenium报错解决方案：ChromeDriver版本不匹配问题

## 简介

本仓库提供了一个资源文件，用于解决在Python执行Selenium时遇到的ChromeDriver版本不匹配问题。具体报错信息为：“This version of ChromeDriver only supports Chrome version 114”。

## 问题描述

在使用Python执行Selenium自动化测试时，可能会遇到以下报错信息：

```
This version of ChromeDriver only supports Chrome version 114
```

该错误通常是由于ChromeDriver的版本与当前系统中安装的Chrome浏览器版本不匹配导致的。

## 解决方案

### 1. 确认Chrome浏览器版本

首先，需要确认当前系统中安装的Chrome浏览器版本。可以通过以下步骤查看：

1. 打开Chrome浏览器。
2. 点击右上角的菜单按钮（三个垂直点）。
3. 选择“帮助” -> “关于Google Chrome”。
4. 在弹出的页面中可以看到当前Chrome浏览器的版本号。

### 2. 下载对应版本的ChromeDriver

根据确认的Chrome浏览器版本，下载相应版本的ChromeDriver。可以从以下地址下载：

- [ChromeDriver下载页面](https://sites.google.com/a/chromium.org/chromedriver/downloads)

### 3. 配置环境变量

将下载的ChromeDriver文件放置在合适的位置，并配置系统环境变量，使其可以在命令行中直接调用。

#### Windows系统

1. 右键点击“此电脑”或“计算机”，选择“属性”。
2. 点击“高级系统设置”。
3. 在“系统属性”窗口中，点击“环境变量”。
4. 在“系统变量”部分，找到并选择“Path”，点击“编辑”。
5. 在“编辑环境变量”窗口中，点击“新建”，添加ChromeDriver的安装路径。
6. 点击“确定”保存设置。

#### macOS/Linux系统

1. 打开终端。
2. 编辑`~/.bash_profile`或`~/.bashrc`文件，添加以下内容：
   ```bash
   export PATH=$PATH:/path/to/chromedriver
   ```
3. 保存文件并执行以下命令使配置生效：
   ```bash
   source ~/.bash_profile
   ```

### 4. 验证配置

在命令行中输入以下命令，验证ChromeDriver是否配置成功：

```bash
chromedriver --version
```

如果显示了ChromeDriver的版本号，说明配置成功。

## 注意事项

- 确保下载的ChromeDriver版本与Chrome浏览器版本完全匹配。
- 如果Chrome浏览器自动更新，可能需要重新下载并配置相应版本的ChromeDriver。

## 参考资料

- [CSDN博客文章](https://blog.csdn.net/xinsuiyunfei/article/details/132456206)

通过以上步骤，您应该能够解决Python执行Selenium时遇到的ChromeDriver版本不匹配问题。

## 下载链接

[Python执行Selenium报错解决方案ChromeDriver版本不匹配问题](https://pan.quark.cn/s/ade3dd5e26be)