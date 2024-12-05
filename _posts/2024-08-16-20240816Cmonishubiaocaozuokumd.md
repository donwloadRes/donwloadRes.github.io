---
layout: post
title: "C# 模拟鼠标操作库"
date:   2020-10-12
tags: [IntPtr,hWnd,窗口,鼠标,指定]
comments: true
author: admin
---
# C# 模拟鼠标操作库

## 简介

本仓库提供了一个用于模拟鼠标操作的C#库，该库通过封装Windows API实现了多种鼠标操作功能，包括鼠标移动、单击、双击、拖动等。此外，还提供了窗口操作的相关功能，如窗口的查找、移动、调整大小、截图等。通过使用本库，开发者可以轻松地在C#项目中实现复杂的鼠标和窗口操作。

## 功能概述

### 鼠标操作

- **鼠标点击**：
  - `LeftClick()`：模拟鼠标左键单击。
  - `RightClick()`：模拟鼠标右键单击。
  - `MiddleClick()`：模拟鼠标中键单击。
  - `LeftDown()`：模拟鼠标左键按下。
  - `LeftUp()`：模拟鼠标左键释放。
  - `RightDown()`：模拟鼠标右键按下。
  - `RightUp()`：模拟鼠标右键释放。
  - `MiddleDown()`：模拟鼠标中键按下。
  - `MiddleUp()`：模拟鼠标中键释放。

- **鼠标移动**：
  - `Move(int x, int y)`：将鼠标移动到指定坐标。
  - `LeftDrag(Point point1, Point point2, int interval, int lag)`：模拟鼠标左键拖动操作。

### 窗口操作

- **窗口查找与操作**：
  - `DoesExist(string windowTitle)`：检查指定标题的窗口是否存在。
  - `Get(string windowTitle)`：获取指定标题窗口的句柄。
  - `GetFocused()`：获取当前焦点窗口的句柄。
  - `SetFocused(IntPtr hWnd)`：设置指定窗口为焦点窗口。
  - `IsFocused(IntPtr hWnd)`：检查指定窗口是否为焦点窗口。
  - `Move(IntPtr hWnd, int x, int y)`：移动指定窗口到指定坐标。
  - `Resize(IntPtr hWnd, int width, int height)`：调整指定窗口的大小。
  - `Hide(IntPtr hWnd)`：隐藏指定窗口。
  - `Show(IntPtr hWnd)`：显示指定窗口。
  - `GetDimensions(IntPtr hWnd)`：获取指定窗口的尺寸。
  - `GetSize(IntPtr hWnd)`：获取指定窗口的大小。
  - `GetLocation(IntPtr hWnd)`：获取指定窗口的位置。
  - `GetTitle(IntPtr hWnd)`：获取指定窗口的标题。
  - `SetTitle(IntPtr hWnd, string title)`：设置指定窗口的标题。
  - `Maximize(IntPtr hWnd)`：最大化指定窗口。
  - `Minimize(IntPtr hWnd)`：最小化指定窗口。
  - `Normalize(IntPtr hWnd)`：恢复指定窗口到正常大小。
  - `Screenshot(IntPtr hWnd)`：截取指定窗口的屏幕截图。
  - `RemoveMenu(IntPtr hWnd)`：移除指定窗口的菜单。
  - `Close(IntPtr hWnd)`：关闭指定窗口。
  - `DisableCloseButton(IntPtr hWnd)`：禁用指定窗口的关闭按钮。
  - `DisableMaximizeButton(IntPtr hWnd)`：禁用指定窗口的最大化按钮。
  - `DisableMinimizeButton(IntPtr hWnd)`：禁用指定窗口的最小化按钮。
  - `EnableMouseTransparency(IntPtr hWnd)`：启用指定窗口的鼠标穿透功能。
  - `ConvertToWindowCoordinates(IntPtr hWnd, int x, int y)`：将屏幕坐标转换为窗口坐标。
  - `GetCoordinateRelativeToWindow(IntPtr hWnd)`：获取鼠标相对于指定窗口的坐标。

### 桌面操作

- **桌面截图**：
  - `Screenshot()`：截取整个桌面的屏幕截图。
  - `HideTaskBar()`：隐藏任务栏。
  - `ShowTaskBar()`：显示任务栏。
  - `GetWidth()`：获取桌面的宽度。
  - `GetHeight()`：获取桌面的高度。

## 使用方法

1. **编译代码**：在`windows api`文件夹中编译代码，生成一个`.dll`文件。
2. **引用DLL**：在您的C#项目中引用生成的`.dll`文件。
3. **调用方法**：根据需要调用库中的方法，实现鼠标和窗口操作。

## 注意事项

- 本库依赖于Windows API，因此仅适用于Windows操作系统。
- 代码中有详细的注释，建议查看代码以获取更多关于方法和参数的详细信息。

## 贡献

欢迎提交Issue和Pull Request，帮助改进本库。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[C模拟鼠标操作库](https://pan.quark.cn/s/78514614b8ca)