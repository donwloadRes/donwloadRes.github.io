---
layout: post
title: "使用 Photoshop 工具直接导出 SVG 路径"
date:   2020-02-12
tags: [SVG,Photoshop,路径,导出,脚本]
comments: true
author: admin
---
# 使用 Photoshop 工具直接导出 SVG 路径

本资源文件提供了一个脚本，帮助用户在 Adobe Photoshop 中直接导出 SVG 路径。通过使用该脚本，用户可以在没有安装 Adobe Illustrator 的情况下，利用 Photoshop 完成简单的 SVG 图标绘制和导出。

## 使用方法

1. **下载脚本文件**：
   - 下载 `save-ps-to-svg1.0.jsx` 脚本文件。

2. **安装脚本**：
   - 将脚本文件放置在 Photoshop 安装目录下的 `/Presets/Scripts` 文件夹中。
   - 如果 Photoshop 正在运行，请重启 Photoshop。

3. **绘制图形**：
   - 打开 Photoshop，新建一个图层。
   - 使用形状工具绘制所需的图形。注意，只有使用形状工具绘制的图像才能转换为 SVG 路径。

4. **保存文件**：
   - 保存整个文件，使用默认设置即可。

5. **导出 SVG 路径**：
   - 在图层名称上双击，将图层重命名为以 `.svg` 为后缀的名称，例如 `tosvg.svg`。
   - 依次点击 `文件` -> `脚本` -> `Save as SVG`，即可在保存 PSD 文件的相同目录下生成一个以 `.svg` 结尾的文件。

## 注意事项

- **路径不规范问题**：导出的路径可能存在不规范的情况，用户需要手动调整路径中的字母，确保路径符合 SVG 规范。
- **形状翻转问题**：导出的 SVG 路径可能存在翻转问题，用户需要手动调整 Y 坐标，以确保图形显示正确。

## 总结

通过使用本资源提供的脚本，用户可以在 Photoshop 中直接导出 SVG 路径，避免了安装额外软件的麻烦。虽然导出过程中可能需要手动调整一些细节，但总体上能够满足简单的 SVG 图标绘制需求。

## 下载链接

[使用Photoshop工具直接导出SVG路径分享](https://pan.quark.cn/s/1febaa3acd7d)