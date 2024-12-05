---
layout: post
title: "IEEE 39节点系统的Simulink模型"
date:   2020-03-10
tags: [39,Simulink,IEEE,MATLAB,模型]
comments: true
author: admin
---
# IEEE 39节点系统的Simulink模型

## 简介
IEEE 39节点系统是一个在电力系统领域较为有名的区域性输电系统网络，在某些文献中又被称为新英格兰39节点系统（New England 39 Bus System NE39BS）。该基准网络配置于美国新英格兰地区，由39个母线组成，其中包括10个发电机母线和19个负荷母线。IEEE 39节点系统广泛应用于小信号稳定性研究、动态稳定分析、电能质量分析与控制等领域。

2015年，加拿大学者A. Moeini、I. Kamwa、P. Brunelle、G. Sybille通过公开数据搭建了基于MATLAB/Simulink仿真实验平台的开源模型，极大便利了相关领域研究人员的仿真分析工作。

## 使用说明
1. **下载与安装**：
   - 下载本仓库中的Simulink模型文件及相关数据文件。
   - 确保已安装MATLAB及Simulink工具箱。

2. **仿真运行**：
   - 打开MATLAB，加载Simulink模型文件。
   - 运行仿真，观察系统行为。

3. **常见问题与解决**：
   - 若仿真文件报错，请检查`NE39bus_data.m`文件第95行变量`mac_con`的定义语句。
   - 将所定义的`mac_con`变量中第1行第14列元素改为`1.5`，可解决报错问题。

## 参考文献
- A. Moeini, I. Kamwa, P. Brunelle, G. Sybille, "Development of an Open-Source MATLAB/Simulink Model for the IEEE 39-Bus System," 2015.

## 贡献
欢迎对该模型进行改进和优化，提交Pull Request或Issue以帮助完善本项目。

## 许可证
本项目采用开源许可证，具体信息请参阅LICENSE文件。

---

**注意**：本模型仅供学习和研究使用，不得用于商业用途。

## 下载链接

[IEEE39节点系统的Simulink模型](https://pan.quark.cn/s/8c7f8a776df3)