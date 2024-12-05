---
layout: post
title: "鱼眼镜头畸变矫正资源文件介绍"
date:   2022-04-28
tags: [矫正,畸变,图像,角点,鱼眼]
comments: true
author: admin
---
# 鱼眼镜头畸变矫正资源文件介绍

## 资源文件标题
鱼眼镜头畸变矫正【亲自改的，可用】

## 资源文件描述
该资源文件提供了一个完整的鱼眼镜头畸变矫正流程，具体步骤如下：

1. **读图**：首先读取需要进行畸变矫正的图像。
2. **灰度化**：将读取的图像转换为灰度图像，便于后续处理。
3. **测角点**：检测图像中的角点，这些角点将用于后续的畸变矫正。
4. **亚像素角点**：对检测到的角点进行亚像素级别的精确定位，提高矫正精度。
5. **画角点**：可选步骤，用于在图像上绘制检测到的角点，方便观察和调试。
6. **计算世界坐标**：根据角点位置计算出对应的世界坐标。
7. **求相机的内参K和畸变系数D**：通过世界坐标和图像坐标，计算出相机的内参矩阵K和畸变系数D。
8. **求矫正后图片的坐标mapx和mapy**：利用内参矩阵K和畸变系数D，计算出矫正后图像的坐标映射关系。
9. **用remap映射到图上**：根据计算出的映射关系，将原始图像映射到矫正后的图像上。
10. **最终imshow**：显示矫正后的图像，完成畸变矫正过程。

## 注意事项
- 该流程经过亲自修改和验证，确保可用性。
- 在画角点步骤中，可以选择是否显示角点图像，方便调试。
- 该资源文件适用于需要进行鱼眼镜头畸变矫正的场景，可以直接使用或根据需要进行进一步修改。