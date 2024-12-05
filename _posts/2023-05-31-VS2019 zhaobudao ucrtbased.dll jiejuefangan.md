---
layout: post
title: "VS2019 找不到 ucrtbased.dll 解决方案"
date:   2022-03-27
tags: [ucrtbased,dll,文件,64,32]
comments: true
author: admin
---
# VS2019 找不到 ucrtbased.dll 解决方案

## 简介

本仓库提供了一个资源文件，用于解决在 Visual Studio 2019 中运行程序时出现的“找不到 ucrtbased.dll，无法继续执行代码”的问题。该问题通常是由于系统中缺少必要的运行时库文件导致的。

## 问题描述

在使用 Visual Studio 2019 编译和运行程序时，可能会遇到以下错误提示：

```
由于找不到 ucrtbased.dll，无法继续执行代码。
```

此错误通常是由于系统中缺少 `ucrtbased.dll` 文件，导致程序无法正常运行。

## 解决方案

本仓库提供的资源文件包含了 `ucrtbased.dll` 文件，用户可以根据自己的系统架构（32位或64位）下载相应的文件，并将其放置在系统的正确路径下。

### 步骤

1. **下载文件**：
   - 对于32位系统，下载 `ucrtbased_32.dll` 文件。
   - 对于64位系统，下载 `ucrtbased_64.dll` 文件。

2. **放置文件**：
   - 将下载的 `ucrtbased.dll` 文件放置在以下路径：
     - 32位系统：`C:\Windows\System32\`
     - 64位系统：`C:\Windows\System32\`（对于64位系统，32位DLL文件应放置在 `C:\Windows\SysWOW64\`）

3. **注册DLL文件**（可选）：
   - 以管理员身份运行命令提示符。
   - 输入以下命令并按回车：
     ```
     regsvr32 "路径\ucrtbased.dll"
     ```
   - 例如，对于64位系统，输入：
     ```
     regsvr32 "C:\Windows\System32\ucrtbased.dll"
     ```

4. **重启电脑**（可选）：
   - 重启电脑以确保更改生效。

## 注意事项

- 请确保下载的 `ucrtbased.dll` 文件与您的系统架构匹配。
- 在放置DLL文件之前，建议备份系统路径中的已有文件，以防止意外覆盖。

## 参考

有关该问题的详细解决方案，请参考 [CSDN博客文章](https://blog.csdn.net/moringacui/article/details/117261683)。

## 贡献

如果您有任何改进建议或发现了新的解决方案，欢迎提交Issue或Pull Request。

## 许可证

本仓库提供的资源文件遵循 [CC 4.0 BY-SA 版权协议](https://creativecommons.org/licenses/by-sa/4.0/)。

## 下载链接

[VS2019找不到ucrtbased.dll解决方案](https://pan.quark.cn/s/5160bccec850)