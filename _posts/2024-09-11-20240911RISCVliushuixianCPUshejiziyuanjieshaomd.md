---
layout: post
title: "RISC-V流水线CPU设计资源介绍"
date:   2023-10-10
tags: [CPU,流水线,RISC,设计,资源]
comments: true
author: admin
---
# RISC-V流水线CPU设计资源介绍

本资源为武汉大学计算机学院计算机组成与设计课程实验项目，基于RISC-V流水线CPU设计的Verilog实现。该设计主要实现了以下指令集：

- **S1**: `{sb, sh, sw, lb, lh, lw, lbu, lhu}`
- **S2**: `{add, sub, xor, or, and, srl, sra, sll}`
- **S3**: `{xori, ori, andi, srli, srai, slli}`
- **S4**: `{slt, sltu, slti, sltiu}`
- **S5**: `{jal, jalr}`
- **S6**: `{beq, bne, blt, bge, bltu, bgeu}`

该设计具有冒险检测与冲突解决功能，确保CPU在执行流水线操作时能够正确处理数据依赖和控制依赖。

资源中包含了Modelsim工程和Vivado工程，方便用户在不同的开发环境中进行仿真和验证。

欢迎下载并使用本资源进行学习和研究。

## 下载链接

[RISC-V流水线CPU设计资源介绍](https://pan.quark.cn/s/1b52ef2039e9)