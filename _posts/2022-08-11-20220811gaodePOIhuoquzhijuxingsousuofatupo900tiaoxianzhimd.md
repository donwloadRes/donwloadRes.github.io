---
layout: post
title: "高德POI获取之矩形搜索法（突破900条限制）"
date:   2024-08-29
tags: [POI,高德,获取,900,API]
comments: true
author: admin
---
# 高德POI获取之矩形搜索法（突破900条限制）

## 简介

本资源文件提供了一种通过矩形搜索法获取高德地图POI（兴趣点）数据的方法，旨在突破高德地图API对单次请求返回POI数量的限制（通常为900条）。通过该方法，用户可以更高效地获取大范围内的POI数据，适用于需要大量POI数据的地理信息系统（GIS）项目、数据分析等场景。

## 功能特点

- **突破900条限制**：通过矩形搜索法，将大区域划分为多个小区域，逐个获取POI数据，从而突破单次请求的900条限制。
- **多边形搜索**：支持多边形区域内的POI搜索，适用于不规则区域的POI数据获取。
- **数据保存**：将获取的POI数据保存为CSV文件，方便后续的数据处理和分析。

## 使用方法

1. **环境准备**：确保已安装Python 3.x，并安装所需的第三方库（如requests、json、csv等）。
2. **API密钥**：在高德地图开放平台申请API密钥，并在代码中进行配置。
3. **区域设置**：根据需求设置搜索区域，可以是矩形或多边形区域。
4. **运行代码**：运行提供的Python脚本，获取POI数据并保存为CSV文件。

## 注意事项

- **API调用频率**：请注意高德地图API的调用频率限制，避免因频繁请求导致API调用受限。
- **数据准确性**：由于矩形搜索法可能会获取到超出目标区域的POI数据，建议在获取数据后进行进一步的筛选和处理。

## 参考资料

本资源文件的实现方法参考了CSDN博客文章《高德poi获取之矩形搜索法(冲出900条限制)》，详细的技术细节和代码实现可参考该文章。

## 贡献与反馈

如果您在使用过程中遇到问题或有改进建议，欢迎通过GitHub提交Issue或Pull Request。

---

通过本资源文件，您可以更高效地获取高德地图的POI数据，为您的GIS项目或数据分析提供有力支持。

## 下载链接

[高德POI获取之矩形搜索法突破900条限制](https://pan.quark.cn/s/d79aa8da6563)