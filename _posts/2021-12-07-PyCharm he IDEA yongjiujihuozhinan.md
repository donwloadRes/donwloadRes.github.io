---
layout: post
title: "PyCharm 和 IDEA 永久激活指南"
date:   2023-09-10
tags: [PyCharm,IDEA,激活,jetbrains,文件]
comments: true
author: admin
---
# PyCharm 和 IDEA 永久激活指南

本仓库提供了一个资源文件，用于永久激活 PyCharm 和 IDEA 两款开发工具。以下是详细的激活步骤和说明。

## 资源文件内容

- **jetbrains-agent.jar**: 这是用于激活 PyCharm 和 IDEA 的补丁文件。

## 激活步骤

### 1. 下载并放置补丁文件

1. 下载 `jetbrains-agent.jar` 文件。
2. 将该文件放置到 PyCharm 或 IDEA 的安装目录下的 `bin` 文件夹中。

### 2. 修改配置文件

1. 打开 PyCharm 或 IDEA，进入项目界面。
2. 点击菜单栏中的 `Help` -> `Edit Custom VM Options...`。
3. 在打开的 `vmoptions` 编辑窗口末行添加以下内容：
   ```
   -javaagent:你的安装目录\jetbrains-agent.jar
   ```
4. 保存并关闭文件，然后重启 PyCharm 或 IDEA。

### 3. 激活软件

1. 重启后，点击菜单栏中的 `Help` -> `Register...`。
2. 选择 `License server` 激活方式。
3. 地址填入 `http://jetbrains-license-server`，或者点击 `Discover Server` 自动填充地址。
4. 完成激活。

## 注意事项

- 请确保补丁文件放置在正确的目录下，避免误操作删除。
- 激活过程中请保持网络连接，以便验证激活信息。

通过以上步骤，您可以成功永久激活 PyCharm 和 IDEA，享受完整的功能和服务。

## 下载链接

[PyCharm和IDEA永久激活指南](https://pan.quark.cn/s/4304b96520f7)