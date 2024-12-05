---
layout: post
title: "解决MATLAB2020B找不到VS2019 C++编译器问题"
date:   2020-05-26
tags: [编译器,MATLAB,VS2019,C++,mex]
comments: true
author: admin
---
# 解决MATLAB2020B找不到VS2019 C++编译器问题

## 简介
本仓库提供了一个资源文件，用于解决MATLAB 2020B在配置深度学习环境时找不到VS2019 C++编译器的问题。该问题通常出现在尝试运行`mex -setup`命令时，MATLAB无法识别已安装的VS2019编译器。

## 问题描述
在配置MATLAB 2020B的深度学习环境过程中，用户可能会遇到找不到VS2019 C++编译器的问题。具体表现为在MATLAB中运行`mex -setup`命令时，系统提示找不到已安装的编译器。

## 解决方案
本仓库提供的资源文件包含了一个替换的`mexopts`文件夹，用户可以将其替换到MATLAB的安装目录中。替换后，再次运行`mex -setup C++`命令，即可成功使用VS2019进行编译。

## 使用方法
1. 下载本仓库中的资源文件。
2. 找到MATLAB的安装目录（例如：`E:\matlab\matlab2020b\bin\win64`）。
3. 将下载的`mexopts`文件夹替换到上述目录中。
4. 在MATLAB命令行中运行`mex -setup C++`，系统将成功识别并使用VS2019编译器。

## 注意事项
- 请确保MATLAB和VS2019均已正确安装。
- 替换文件夹前，建议备份原有的`mexopts`文件夹，以便出现问题时可以恢复。

## 参考资料
该解决方案参考了CSDN博客文章《解决MATLAB2020B关于找不到vs2019C++编译器问题》，详细步骤和原理可参考该文章。

## 贡献
如果您有更好的解决方案或发现任何问题，欢迎提交Issue或Pull Request。

## 许可证
本仓库内容遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[解决MATLAB2020B找不到VS2019C编译器问题](https://pan.quark.cn/s/e9ace1ac7030)