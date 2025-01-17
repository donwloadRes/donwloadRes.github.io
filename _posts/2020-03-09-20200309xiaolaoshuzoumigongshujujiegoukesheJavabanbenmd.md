---
layout: post
title: "小老鼠走迷宫 数据结构课设 Java版本"
date:   2024-10-23
tags: [迷宫,单元,老鼠,Java,当前]
comments: true
author: admin
---
# 小老鼠走迷宫 数据结构课设 Java版本

## 项目描述

本项目是一个基于Java的数据结构课设，主题为“小老鼠走迷宫”。程序启动时会显示一个迷宫地图，迷宫中央有一只老鼠，迷宫的右下方有一个粮仓。玩家的任务是使用键盘上的方向键操纵老鼠在规定的时间内走到粮仓处。

## 基本要求

1. **老鼠形象可辨认**：老鼠形象清晰可见，玩家可以通过键盘操纵老鼠上下左右移动。
2. **迷宫墙体不可穿越**：迷宫的墙体足够结实，老鼠不能穿墙而过。
3. **结果检测**：程序能够正确检测老鼠是否在规定时间内到达粮仓。如果成功，提示成功并给出一条路径；否则提示失败。
4. **迷宫编辑功能**：玩家可以修改当前迷宫，包括将墙变为路或将路变为墙。

## 提高要求

1. **闯关和计分功能**：增加闯关模式，并记录玩家的得分。
2. **路径搜索**：找出走出迷宫的所有路径及最短路径。

## 迷宫生成算法

### 算法功能描述

利用递归回溯/深度优先算法随机生成迷宫。

### 算法描述

1. 将起点作为当前迷宫单元并标记为已访问。
2. 当还存在未标记的迷宫单元时，进行循环：
   - 如果当前迷宫单元有未被访问过的相邻迷宫单元：
     1. 随机选择一个未访问的相邻迷宫单元。
     2. 将当前迷宫单元入栈。
     3. 移除当前迷宫单元与相邻迷宫单元的墙。
     4. 标记相邻迷宫单元并用它作为当前迷宫单元。
   - 如果当前迷宫单元不存在未访问的相邻迷宫单元，并且栈不空：
     1. 将栈顶迷宫单元出栈，并将其作为当前迷宫单元。

## 使用说明

1. 下载资源文件并解压。
2. 打开项目文件夹，找到主程序文件并运行。
3. 使用键盘上的方向键操纵老鼠移动。
4. 在规定时间内将老鼠移动到粮仓处，完成游戏。

## 注意事项

- 确保Java环境已正确配置。
- 游戏过程中请勿关闭控制台窗口，否则游戏将终止。

## 贡献

欢迎对本项目进行改进和优化，提交Pull Request或Issue。

## 下载链接

[小老鼠走迷宫数据结构课设Java版本](https://pan.quark.cn/s/0f1e0a0c3178)