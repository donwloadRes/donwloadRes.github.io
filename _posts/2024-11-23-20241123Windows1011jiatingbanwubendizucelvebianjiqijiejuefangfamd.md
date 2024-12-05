---
layout: post
title: "Windows 1011家庭版无本地组策略编辑器解决方法"
date:   2024-07-15
tags: [gpedit,bat,Windows,家庭版,组策略]
comments: true
author: admin
---
# Windows 10/11家庭版无本地组策略编辑器解决方法

## 简介

Windows 10家庭版在运行输入`gpedit.msc`，按回车时，会弹出以下报错界面。（亲测WINDOWS 11家庭版也适用）出现“Windows 找不到文件gpeditmsc。请确定文件名是否正确后，再试一次。”解决办法：下载`gpedit.bat`，右键以管理员身份运行等待下载完毕后，出现“按任意键退出”即可使用本地组策略编辑器。

## 使用方法

1. 下载本仓库中的`gpedit.bat`文件。
2. 右键点击`gpedit.bat`文件，选择“以管理员身份运行”。
3. 等待脚本执行完毕，出现“按任意键退出”提示后，即可使用本地组策略编辑器。

## 注意事项

- 请确保以管理员身份运行`gpedit.bat`文件，否则可能无法正常执行。
- 本方法适用于Windows 10和Windows 11家庭版用户。

## 下载链接

[下载 gpedit.bat](./gpedit.bat)

## 贡献

如果您有任何改进建议或发现了问题，欢迎提交Issue或Pull Request。

## 许可证

本项目采用[MIT许可证](./LICENSE)。

## 下载链接

[Windows1011家庭版无本地组策略编辑器解决方法](https://pan.quark.cn/s/a60251058cf3)