---
layout: post
title: "DHI Mike后处理工具基于shapefile的污染带面积长度宽度统计工具"
date:   2023-10-19
tags: [shapefile,工具,Linux,统计,DHI]
comments: true
author: admin
---
# DHI Mike后处理工具——基于shapefile的污染带面积、长度、宽度统计工具

## 简介

本工具是一个基于Python编写的后处理工具，专门用于统计DHI Mike模型或其他能够导出shapefile格式的模型计算结果中的污染带面积、长度和宽度。该工具适用于Linux环境，通过Nuitka打包编译成appimage格式，方便用户在Linux系统中直接使用。

## 功能特点

- **支持多种模型结果统计**：不仅限于DHI Mike模型，任何能够导出shapefile格式的模型结果都可以使用本工具进行统计。
- **自动保存计算结果**：统计结果会自动保存到粘贴板，用户可以直接在Excel中粘贴查看。
- **适用于投影坐标系**：工具要求输入的shapefile文件必须在投影坐标系下，经纬度坐标无法进行统计。

## 使用方法

1. **导出shapefile文件**：使用DHI Mike自带的导出工具或其他工具，将模型计算结果导出为shapefile格式。
2. **运行工具**：在Linux环境下运行本工具，输入shapefile文件路径，工具将自动进行统计。
3. **查看结果**：统计结果会自动保存到粘贴板，用户可以在Excel中粘贴查看。

## 注意事项

- **仅限Linux环境**：由于工具是用Nuitka打包编译成appimage格式，目前仅支持Linux环境。如需Windows版本，请联系作者（cyc.sjtu@gmail.com）。
- **投影坐标系要求**：输入的shapefile文件必须在投影坐标系下，经纬度坐标无法进行统计。

## 联系作者

本工具纯属个人兴趣开发，欢迎共同探讨软件优化。如需Windows版本或其他技术支持，请联系作者：cyc.sjtu@gmail.com。

## 其他说明

工具的具体使用方法和详细说明，请参考作者的blog内容。

## 下载链接

[DHIMike后处理工具基于shapefile的污染带面积长度宽度统计工具](https://pan.quark.cn/s/18a6bcba1296)