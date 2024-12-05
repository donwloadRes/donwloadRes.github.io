---
layout: post
title: "MATLAB光的衍射代码 - FDTD Solutions 脚本库：用于超表面全息照相（FSMH）"
date:   2020-04-17
tags: [source,脚本,lsf,FDTD,Solutions]
comments: true
author: admin
---
# MATLAB光的衍射代码 - FDTD Solutions 脚本库：用于超表面全息照相（FSMH）

## 项目简介

本仓库提供了一个用于超表面全息照相（FSMH）的MATLAB脚本库，基于Lumerical FDTD Solutions仿真工具。该脚本库旨在帮助用户构建和分析超表面（Metasurface）的光学特性，特别是光的衍射和相位分析。

## 功能特性

- **材料数据**：
  - `./data/Material/`：存放用于仿真的材料数据。

- **源代码**：
  - `./source/`：存放所有相关的lsf源代码。
  - `./source/Template.lsf`：构建超表面阵列的脚本模板。
  - `./source/GDSII`：导出GDSII文件的脚本。
  - `./source/Analysis/`：用于分析仿真结果的脚本。
  - `./source/Modeling/`：用于构造Metasurface阵列的脚本。
  - `./source/experimental/`：试验性质的代码，谨慎使用。

- **关键脚本**：
  - `FarField.lsf`：远场投影（直角坐标），速度快且无畸变，建议使用。
  - `FarField_polar.lsf`：远场投影（球坐标）。
  - `Diffraction.lsf`：沿光轴衍射分析。
  - `PhaseAnalysis.lsf`：扫描后相位分析。

## 注意事项

- 本项目目前为自用状态，尚未完成，部分功能可能存在不稳定性。
- 试验性质的代码（`./source/experimental/`）请谨慎使用，可能存在未知的错误或问题。

## 使用说明

1. 下载并安装Lumerical FDTD Solutions软件。
2. 将本仓库中的脚本文件导入到Lumerical FDTD Solutions中。
3. 根据需要修改和运行相应的脚本文件，进行超表面的仿真和分析。

## 贡献

欢迎任何形式的贡献，包括但不限于代码优化、功能扩展、文档完善等。请通过提交Issue或Pull Request的方式参与项目。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[MATLAB光的衍射代码-FDTDSolutions脚本库用于超表面全息照相FSMH](https://pan.quark.cn/s/9ccc14a37f0c)