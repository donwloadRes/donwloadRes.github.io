---
layout: post
title: "五子棋大作业C资源实现"
date:   2020-11-06
tags: [对战,AI,黑屏,玩家,人机]
comments: true
author: admin
---
# 五子棋大作业（C++资源实现）

## 项目概述

本项目是一个用C++实现的五子棋游戏，囊括两种对战模式：玩家对战和人机对战。游戏采用黑屏字符输入输出方式打造用户界面（UI），并运用评分算法赋予AI对手智能博弈能力。

## 特色功能

1. **对弈模式**：
   - **玩家对战模式**：两位玩家轮流下棋，体验传统五子棋对决的乐趣。
   - **人机对战模式**：玩家与AI展开对弈，AI凭借评分算法做出明智决策。

2. **UI界面**：
   - 黑屏字符输入输出方式，简洁易懂。
   - 棋盘尺寸为15*15，行列号以字母A-O标识，方便玩家定位落子。

3. **棋子规则**：
   - 两种棋子颜色：黑子与白子，代表对弈双方。
   - 黑方先手，棋子布局于棋盘行列交叉点。

4. **胜负判定**：
   - 黑或白方率先连成5个棋子形成直线（水平、垂直或对角线）则获胜。
   - 若棋盘已满，双方均未连成直线，则为和局。

5. **特殊标记**：
   - 最后一步落子的位置会以特殊标记标识，方便玩家回顾棋局。

## 使用指南

### 编译与运行

- 使用C++编译器编译源代码。
- 启动编译所得的可执行文件，即可开启游戏。

### 游戏操作

- 根据提示输入行列号（A-O）放置棋子。
- 在人机对战模式下，AI将自动做出下一步决策。

### 注意事项

- 请确保输入的行列号在有效范围内（A-O）。
- 人机对战模式中，AI的决策基于评分算法，可能会稍有延时。

## 优点

- 规则易懂，老少咸宜。
- 双重对战模式，满足不同游戏需求。
- 黑屏字符界面，营造复古经典氛围。
- AI对手，增添趣味性和挑战性。
- 便捷的行列号定位，加快落子速度。

## 资源共享与反馈

欢迎提出改进建议或贡献代码以完善本资源。如遇问题，请在资源内提交Issue。

## 关键词

- 五子棋
- C++
- 游戏
- 人机对战
- 智能决策
- 黑屏字符UI
- 行列号定位
- 对弈模式