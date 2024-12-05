---
layout: post
title: "透明窗体画图 C WINFORM 解决方案"
date:   2020-04-01
tags: [窗体,透明,解决方案,drawForm,TransparencyKey]
comments: true
author: admin
---
# 透明窗体画图 C# WINFORM 解决方案

## 描述

通过长时间的研究，我终于找到了在C# WINFORM下制作真正的透明窗体并在系统桌面上进行画图的完美解决方案。我的解决方案采用了两层透明窗体重叠的方式：

1. **透明窗体 `showForm`**：用于显示图像。由于使用了 `TransparencyKey`，该窗体可以实现鼠标穿透，但字迹显示清晰正常。
2. **透明窗体 `drawForm`**：用于绘制图形的轨迹。该窗体使用了 `Opacity`，因此鼠标不会穿透，但可以不必显示图像。

通过这种方式，`Opacity` 透明绘图层的轨迹可以在 `TransparencyKey` 图画层上显示。直接上代码：`drawForm.cs` 只需新建窗体 `drawForm` 即可，可以不用写其它代码。

## 使用方法

1. 下载资源文件。
2. 打开项目并导入 `drawForm.cs`。
3. 运行项目，即可体验在透明窗体上绘图的效果。

## 注意事项

- 该解决方案适用于需要在透明窗体上进行绘图的场景。
- 由于使用了 `TransparencyKey` 和 `Opacity`，确保在不同系统环境下测试以获得最佳效果。

希望这个解决方案能帮助到你！

## 下载链接

[透明窗体画图CWINFORM解决方案](https://pan.quark.cn/s/54f25f41676f)