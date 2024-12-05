---
layout: post
title: "MATLAB时频分析工具箱"
date:   2020-09-21
tags: [时频,信号,分布,调制,频率]
comments: true
author: admin
---
# MATLAB时频分析工具箱

## 简介
本仓库提供了一个MATLAB时频分析工具箱，包含了多种用于计算线性时频表示和双线性时频分布的函数。该工具箱旨在帮助用户进行时频分析应用的相关讨论和研究。以下是工具箱中主要函数的简介。

## 信号产生函数
- `amexpo1s`：单边指数幅值调制信号
- `amexpo2s`：双边指数幅值调制信号
- `amgauss`：高斯幅值调制信号
- `amrect`：矩形幅值调制信号
- `amtriang`：三角形幅值调制信号
- `fmconst`：定频调制信号
- `fmhyp`：双曲线频率调制信号
- `fmlin`：线性频率调制信号
- `fmodany`：任意频率调制信号
- `fmpar`：抛物线频率调制信号
- `fmpower`：幂指数频率调制信号
- `fmsin`：正弦频率调制信号
- `gdpower`：能量律群延迟信号
- `altes`：时域Altes信号
- `anaask`：幅值键移信号
- `anabpsk`：二进制相位键移信号
- `anafsk`：频率键移信号
- `anapulse`：单位脉冲信号的解析投影
- `anaqpsk`：四进制相位键移信号
- `anasing`：Lipscjitz奇异性
- `anaste`：单位阶跃信号的解析投影
- `atoms`：基本高斯元的线性组合
- `dopnoise`：复多普勒任意信号
- `doppler`：复多普勒信号
- `klauder`：时域Klauder小波
- `mexhat`：时域墨西哥帽小波

## 噪声产生函数
- `noiseecg`：解析复高斯噪声
- `noiseecu`：解析复单位高斯噪声
- `tfrgabor`：Gabor表示
- `tfrstft`：短时傅立叶变换
- `ifestar2`：使用AR(2)模型的瞬时频率估计
- `instfreq`：瞬时频率估计
- `sqrpdlay`：群延迟估计

## 模糊函数
- `ambifunb`：窄带模糊函数
- `ambifuwb`：宽带模糊函数

## Affine类双核线性时频处理函数
- `tfrbert`：单式Bertrand分布
- `tfrdfla`：D-Flandrin分布
- `tfrscalo`：尺度图
- `tfrspaw`：平滑伪Affine类Wigner分布
- `tfrunter`：Unterberger分布

## Cohen类双核线性时频处理函数
- `tfrbj`：Born-Jordan分布
- `tfrbud`：Butterworth分布
- `tfrcw`：Choi-Williams分布
- `tfrgrd`：归一化的矩形分布
- `tfrmh`：Margenau-Hill分布
- `tfrmhs`：Margenau-Hill频谱分布
- `tfrmmce`：谱图的最小平均互熵组合
- `tfrpage`：Page分布
- `tfrwv`：伪Wigner-Ville分布
- `tfrri`：Rihaczek分布
- `tfrridb`：降低交叉项的分布（Bessel窗）
- `tfrridbn`：降低交叉项的分布（二项式窗）
- `tfrridh`：降低交叉项的分布（汉宁窗）
- `tfrridt`：降低交叉项的分布（三角窗）
- `tfrsp`：谱图分布
- `tfrspwv`：平滑伪Wigner-Ville分布
- `tfrwv`：Wigner-Ville分布
- `tfrzam`：Zhao-Atlas-Marks分布

## 其他处理函数
- `friedman`：瞬时频率密度
- `htl`：图像直线检测中的Hough变换
- `margtfr`：时频表示的能量
- `momftfr`：时频表示的频率矩
- `momttfr`：时频表示的时间矩
- `renyi`：Renyi信息度量
- `ridges`：波峰提取
- `plotifl`：绘制归一化的瞬时频率规律
- `tfrparam`：返回用于显示时频表示的参数
- `tfrqview`：时频表示的快速可视化
- `tfrsave`：保存时频表示的参数
- `tfrview`：时频表示的可视化

## 安装方法
1. 克隆或下载本仓库到本地。
2. 将工具箱文件夹添加到MATLAB的搜索路径中。
3. 在MATLAB命令窗口中运行 `addpath(genpath('path_to_toolbox'))`，其中 `path_to_toolbox` 是工具箱文件夹的路径。

## 使用说明
请参考每个函数的帮助文档以了解具体的使用方法和参数设置。您可以在MATLAB命令窗口中输入 `help function_name` 来获取帮助信息，其中 `function_name` 是您想要查询的函数名称。

## 贡献
欢迎大家就时频分析应用展开相关讨论，并贡献代码和改进建议。请通过提交Issue或Pull Request来参与贡献。

## 许可证
本项目采用MIT许可证。详细信息请参阅[LICENSE](LICENSE)文件。

## 下载链接

[MATLAB时频分析工具箱](https://pan.quark.cn/s/a26467eefd6c)