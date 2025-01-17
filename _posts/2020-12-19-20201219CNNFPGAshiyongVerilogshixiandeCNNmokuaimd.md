---
layout: post
title: "CNNFPGA 使用Verilog实现的CNN模块"
date:   2022-05-26
tags: [CNN,FPGA,模块,Verilog,设计]
comments: true
author: admin
---
# CNN-FPGA: 使用Verilog实现的CNN模块

## 项目简介

本项目是一个基于FPGA的CNN（卷积神经网络）加速器实现，使用Verilog语言编写。该项目最初作为本科毕业设计的一部分，旨在探索如何利用FPGA硬件加速CNN的推断过程。尽管项目在设计上存在一些局限性，但它提供了一个基础的CNN模块实现，可以作为FPGA项目中的参考或起点。

## 项目背景

毕业设计初期，本意是希望通过研究机器学习算法（如CNN）来拓宽知识面。然而，由于课题被体系结构实验室的老师选中，最终演变成了一个硬件加速的项目。尽管最初并不情愿，但在大致了解了CNN的工作原理后，还是完成了这个项目。

## 项目特点

- **Verilog实现**：所有CNN模块均使用Verilog语言编写，适合在FPGA平台上使用。
- **全并行设计**：模块设计参照了TensorFlow的架构，采用全并行设计，避免了时序和流水线的复杂性。
- **资源占用较高**：由于采用了全并行设计，模块在资源占用上较为不合理，适合学习参考，但不适合实际应用。

## 项目局限性

- **仅支持推断**：本项目仅实现了CNN的前向传播部分，无法进行学习（后向传播）。这是由于FPGA在处理反向传播时的局限性，Xilinx等厂商也已放弃在这方面的努力。
- **资源占用不合理**：由于全并行设计，模块在FPGA上的资源占用较高，不适合大规模应用。

## 使用说明

1. **模块设计**：模块设计上参照了TensorFlow的架构，便于理解和使用。
2. **资源占用**：由于采用了全并行设计，模块在资源占用上较为不合理，建议仅用于学习和参考。
3. **推断功能**：本项目仅支持CNN的推断功能，无法进行学习（后向传播）。

## 总结

本项目是一个基于FPGA的CNN加速器实现，使用Verilog语言编写。尽管在设计上存在一些局限性，但它提供了一个基础的CNN模块实现，可以作为FPGA项目中的参考或起点。由于仅支持推断功能，且资源占用较高，建议仅用于学习和参考。

## 下载链接

[CNN-FPGA使用Verilog实现的CNN模块](https://pan.quark.cn/s/ad6ea37c9707)