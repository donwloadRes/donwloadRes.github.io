---
layout: post
title: "Windows 64位环境下Qt5.14版本的openssl动态库"
date:   2022-05-20
tags: [openssl,Qt,动态,版本,Qt5.14]
comments: true
author: admin
---
# Windows 64位环境下Qt5.14版本的openssl动态库

本仓库提供了一个适用于Windows 64位环境下Qt5.14版本的openssl动态库资源文件。压缩包内包含了msvc和mingw64两个版本的openssl动态库，方便用户在不同编译器环境下使用。

## 资源文件内容

- **msvc版本的openssl动态库**：适用于使用MSVC编译器的Qt项目。
- **mingw64版本的openssl动态库**：适用于使用MinGW编译器的Qt项目。

## 使用方法

1. **下载压缩包**：从本仓库下载包含openssl动态库的压缩包。
2. **解压缩**：将下载的压缩包解压到任意目录。
3. **放置动态库**：将解压后的dll文件放置在Qt安装目录下对应的bin目录中。例如：
   - 对于MSVC版本：`D:\Qt\Qt5.14.2\5.14.2\msvc2017_64\bin`
   - 对于MinGW版本：`D:\Qt\Qt5.14.2\5.14.2\mingw73_64\bin`

## 验证是否生效

你可以通过以下方法验证openssl动态库是否生效：

1. **使用`QSslSocket::supportsSsl()`**：
   ```cpp
   if (QSslSocket::supportsSsl()) {
       qDebug() << "OpenSSL is supported.";
   } else {
       qDebug() << "OpenSSL is not supported.";
   }
   ```

2. **使用`QNetworkAccessManager`**：
   ```cpp
   qInfo() << QScopedPointer<QNetworkAccessManager>(new QNetworkAccessManager)->supportedSchemes();
   ```
   如果输出结果中包含`https`，则说明openssl动态库已生效。

## 注意事项

- 请确保将dll文件放置在正确的Qt安装目录下，否则可能会导致无法正常使用。
- 如果你在其他版本的Qt或不同的操作系统上使用，可能需要重新编译或下载相应的openssl动态库。

希望这个资源文件能帮助你在Windows 64位环境下顺利使用Qt5.14版本的openssl动态库。如果有任何问题或建议，欢迎提出。

## 下载链接

[Windows64位环境下Qt5.14版本的openssl动态库](https://pan.quark.cn/s/069aae9cf780)