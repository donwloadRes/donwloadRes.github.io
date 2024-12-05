---
layout: post
title: "Python加CH9329模块实现云顶之弈自动刷局数"
date:   2020-04-15
tags: [脚本,自动,对局,CH9329,模块]
comments: true
author: admin
---
# Python加CH9329模块实现云顶之弈自动刷局数

## 简介

本资源文件提供了一个使用Python和CH9329模块实现《云顶之弈》自动刷局数的脚本。该脚本旨在帮助玩家自动完成游戏中的对局，节省时间和精力。

## 功能特点

- **自动寻找对局**：脚本能够自动点击“寻找对局”按钮，进入匹配队列。
- **自动接受对局**：检测到对局匹配成功后，自动点击“接受”按钮，进入游戏。
- **自动游戏操作**：在游戏内，脚本会模拟玩家操作，如购买英雄、刷新商店、升级等。
- **自动投降**：在特定回合（如3-2回合），脚本会自动发起投降，并确认退出游戏。
- **自动重复对局**：游戏结束后，脚本会自动点击“再来一局”按钮，重复上述流程。

## 使用方法

1. **环境准备**：
   - Python 3.7
   - pyautogui
   - PIL
   - serial
   - opencv-python

2. **硬件准备**：
   - CH9329模块
   - CH340 USB转TTL模块（可选，如果没有的话需要购买）

3. **配置脚本**：
   - 根据设备管理器中的COM口实际名称，配置串口名称。
   - 根据游戏界面截图，配置需要检测的按钮图片路径。

4. **运行脚本**：
   - 启动脚本后，脚本会自动执行上述功能，无需人工干预。

## 注意事项

- 该脚本仅供学习和研究使用，请勿用于商业用途或违反游戏规则的行为。
- 使用该脚本可能会导致账号被封禁，请谨慎使用。
- 脚本中的硬件操作部分依赖于CH9329模块，确保硬件连接正确。

## 贡献

欢迎提交问题和改进建议，帮助完善该脚本。

## 许可证

本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[Python加CH9329模块实现云顶之弈自动刷局数](https://pan.quark.cn/s/36a4e2099ee2)