---
layout: post
title: "NVM下载、安装和配置教程"
date:   2022-03-21
tags: [NVM,npm,Node,js,node]
comments: true
author: admin
---
# NVM下载、安装和配置教程

本文详细指导如何在Windows系统上下载、安装NVM（Node Version Manager），包括选择版本、配置环境变量、设置镜像源，以及测试和使用Node.js的过程。

## 一、下载

1. 访问NVM的GitHub发布页面，选择适合Windows系统的版本。
2. 下载zip版本的安装包，解压后即可使用。

## 二、安装

1. 双击解压后的exe文件。
2. 选择安装位置，点击next。
3. 选择Node.js的安装位置，点击next。
4. 点击install，完成安装。

## 三、配置环境

1. 右击“我的电脑”，选择属性。
2. 点击高级系统设置，进入环境变量设置。
3. 新建系统变量NVM_HOME，变量值为NVM的安装目录。
4. 新建系统变量NVM_SYMLINK，变量值为Node.js的安装目录。
5. 在Path变量中添加%NVM_SYMLINK%和%NVM_HOME%。

## 四、配置镜像源

1. 打开NVM安装目录下的setting.txt文件。
2. 添加以下两行代码：
   ```
   node_mirror: https://npm.taobao.org/mirrors/node/
   npm_mirror: https://npm.taobao.org/mirrors/npm/
   ```
3. 保存并退出。

## 五、测试安装与使用

1. 打开命令提示符，输入`nvm -v`，显示版本号表示安装成功。
2. 输入`nvm ls`查看已安装的Node.js版本。
3. 输入`nvm list available`查看可安装的所有Node.js版本。
4. 输入`nvm install 版本号`安装指定版本的Node.js。
5. 输入`nvm use 版本号`切换使用的Node.js版本。
6. 输入`node -v`查看当前Node.js版本。
7. 输入`npm -v`查看当前npm版本。

## 六、Node.js配置与使用

1. 在NVM安装目录下创建node_cache和node_global两个文件夹。
2. 打开命令提示符，执行以下命令配置npm：
   ```
   npm config set prefix "D:\Environment\nodejs\node_global"
   npm config set cache "D:\Environment\nodejs\node_cache"
   ```
3. 新建系统变量NODE_PATH，变量值为`D:\Environment\nodejs\node_global\node_modules`。
4. 在Path变量中添加%NODE_PATH%。
5. 配置npm下载源为国内镜像：
   ```
   npm config set registry https://registry.npmmirror.com
   ```
6. 测试安装全局包，如`npm install vue -g`。

通过以上步骤，您可以成功下载、安装和配置NVM，并使用NVM管理多个Node.js版本。

## 下载链接

[NVM下载安装和配置教程](https://pan.quark.cn/s/6318819ecf37)