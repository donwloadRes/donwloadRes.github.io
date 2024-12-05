---
layout: post
title: "在VSCode中配置CC开发环境使用MinGW"
date:   2021-10-06
tags: [VSCode,MinGW,C++,配置,文件夹]
comments: true
author: admin
---
# 在VSCode中配置C/C++开发环境（使用MinGW）

## 简介

本资源文件详细介绍了如何在VSCode中配置C/C++开发环境，使用MinGW作为编译器。通过本教程，您可以避免常见的配置错误，确保环境配置一次成功。

## 主要步骤

### 第一步：下载并安装MinGW编译器

1. 访问MinGW的官方下载页面，选择合适的版本进行下载。
2. 下载完成后，解压安装包并记住解压路径。
3. 将解压后的文件夹移动到您希望安装的位置（例如：D:\mingw-w64）。

### 第二步：配置环境变量

1. 打开解压后的文件夹，进入`bin`文件夹，复制该路径。
2. 右击开始菜单，依次点击“系统”→“高级系统设置”→“环境变量”→“Path”→“编辑”→“新建”，将刚才复制的路径粘贴进去，然后点击确定。
3. 验证环境变量是否配置成功：打开命令提示符，输入`gcc -v`，如果显示gcc版本号，则配置成功。

### 第三步：安装C/C++扩展

1. 打开VSCode，在扩展商店中搜索并安装“Microsoft C/C++”扩展。
2. 安装完成后，重启VSCode。

### 第四步：配置编译器

1. 在VSCode中新建一个文件夹，并在文件夹中创建一个C语言或C++文件。
2. 输入一段测试代码，例如：
   ```c
   #include <stdio.h>
   int main() {
       printf("Hello World\n");
       return 0;
   }
   ```
3. 按`Ctrl+Shift+P`调出命令面板，输入`C/C++`，选择“编辑配置（Edit Configurations(UI)）”进入配置。
4. 修改编译器路径为MinGW所在路径，例如：`D:\mingw-w64\x86_64-8.1.0-release-win32-seh-rt_v6-rev0\mingw64\bin\gcc.exe`。
5. 选择IntelliSense模式为`windows-gcc-x64`，完成后会出现一个`.vscode`文件夹，其中包含`c_cpp_properties.json`文件。
6. 回到测试程序文件，点击`F5`运行，选择`GDB/LLDB`调试器。
7. 点击“生成和调试活动文件”，此时`.vscode`文件夹中会出现`tasks.json`文件。
8. 再次点击`F5`运行程序，底边终端出现`Hello World`，即为成功运行程序。

## 注意事项

- 确保MinGW的路径配置正确，否则编译器无法找到。
- 在配置过程中，如果遇到任何问题，请参考CSDN博客中的详细步骤进行排查。

## 参考资料

- [CSDN博客：【c/c++】安装MinGW，在VSCode配置 c/c++ 环境（免踩坑超详细必成功步骤）](https://blog.csdn.net/zad000000/article/details/125758747)

通过以上步骤，您应该能够在VSCode中成功配置C/C++开发环境，并开始编写和调试C/C++程序。

## 下载链接

[在VSCode中配置CC开发环境使用MinGW分享](https://pan.quark.cn/s/fa41349906a4)

## 下载链接

[在VSCode中配置CC开发环境使用MinGW分享](https://pan.quark.cn/s/67de69203dd9)