---
layout: post
title: "Mac M1 版本下载 Java JDK 1.8 详细指南"
date:   2023-03-11
tags: [JDK,JAVA,HOME,配置文件,Java]
comments: true
author: admin
---
# Mac M1 版本下载 Java JDK 1.8 详细指南

本仓库提供了一个详细的指南，帮助你在 Mac M1 设备上下载并安装 Java JDK 1.8 版本。该指南分为十个步骤，涵盖了从下载到配置环境变量的全过程。

## 指南内容概述

1. **下载 Zulu JDK**：从指定网盘下载 Zulu JDK 1.8 版本。
2. **安装 JDK**：按照提示完成 JDK 的安装。
3. **打开终端**：使用快捷键 `Command + 空格` 打开终端。
4. **查看 JDK 路径**：通过命令 `/usr/libexec/java_home -V` 查看已安装的 JDK 路径。
5. **复制 JDK 路径**：找到并复制 JDK 的安装路径。
6. **编辑 Shell 配置文件**：使用命令 `open -e ~/.zshrc` 打开并编辑 Shell 配置文件。
7. **设置 JAVA_HOME**：在配置文件中添加或更新以下行来设置 `JAVA_HOME`：
   ```bash
   export JAVA_HOME="复制的JDK路径"
   export PATH="$JAVA_HOME/bin:$PATH"
   ```
8. **保存并关闭编辑器**：保存修改并关闭编辑器。
9. **重新加载配置文件**：使用命令 `source ~/.zshrc` 重新加载配置文件。
10. **验证设置**：通过命令 `echo $JAVA_HOME` 和 `java -version` 验证 `JAVA_HOME` 设置和 Java 版本。

## 注意事项

- 确保按照步骤操作，避免遗漏。
- 如果遇到问题，可以参考原文中的详细说明。

通过本指南，你可以轻松地在 Mac M1 设备上安装并配置 Java JDK 1.8 版本。

## 下载链接

[MacM1版本下载JavaJDK1.8详细指南](https://pan.quark.cn/s/085d6e95da1e)