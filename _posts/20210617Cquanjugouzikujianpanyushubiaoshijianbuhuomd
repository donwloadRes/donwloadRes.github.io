---
layout: post
title: "C# 全局钩子库 - 键盘与鼠标事件捕获"
date:   2020-07-28
tags: [Hook,mouseHook,鼠标,keyboardHook,键盘]
comments: true
author: admin
---
# C# 全局钩子库 - 键盘与鼠标事件捕获

## 概述

本仓库提供了完整的C#源码实现，用于全局捕获和处理键盘及鼠标的所有基本事件。通过高效的Hook技术，开发者能够实现在任何应用程序前端下的键盘输入和鼠标操作监听，这对于开发屏幕录制软件、游戏助手、辅助工具等场景极具价值。

## 特性

- **全局键盘Hook**：支持`KeyPress`, `KeyDown`, `KeyUp`事件的监听。
- **全局鼠标Hook**：全面覆盖`MouseMove`, `MouseClick`, `MouseDown`, `MouseUp`, `MouseDoubleClick`以及鼠标滚轮(`MouseWheel`)事件。
- **完全源码**：提供的代码涵盖了Hook的安装、消息处理以及卸载的整个流程，便于学习与自定义扩展。
- **兼容性**：适用于.NET Framework及更高版本，确保在多种Windows平台上运行稳定。

## 使用方法

1. **导入项目**：将源码导入到您的Visual Studio环境中作为新的解决方案或现有项目的引用。
2. **初始化Hook**：在应用程序启动时初始化键盘和鼠标Hook，通常在主函数或应用程序初始化阶段进行。
3. **事件处理**：实现对应的事件处理器方法，根据需要响应特定的键盘或鼠标事件。
4. **卸载Hook**：在应用程序退出前，记得正确卸载Hook，避免资源泄露。

## 示例代码片段

```csharp
// 初始化键盘Hook
KeyboardHook keyboardHook = new KeyboardHook();
keyboardHook.KeyPress += OnKeyPress;
keyboardHook.KeyDown += OnKeyDown;
keyboardHook.KeyUp += OnKeyUp;
keyboardHook.Start();

// 初始化鼠标Hook
MouseHook mouseHook = new MouseHook();
mouseHook.MouseDown += OnMouseDown;
mouseHook.MouseUp += OnMouseUp;
mouseHook.MouseMove += OnMouseMove;
mouseHook.MouseClick += OnMouseClick;
mouseHook.MouseDoubleClick += OnMouseDoubleClick;
mouseHook.MouseWheel += OnMouseWheel;
mouseHook.Start();

// 事件示例
private void OnKeyPress(object sender, KeyEventArgs e)
{
    Console.WriteLine("按键按下：" + e.KeyCode);
}

// 记得在适当的时候停止Hook并清理资源
protected override void OnFormClosed(FormClosedEventArgs e)
{
    base.OnFormClosed(e);
    keyboardHook.Stop();
    mouseHook.Stop();
}
```

## 注意事项

- 在使用全局Hook时，请注意隐私和安全考虑，确保合法合规地使用此类技术。
- 确保应用程序具有足够的权限以在系统级别执行Hook操作，特别是在用户账户控制(UAC)严格的环境下。
- 测试过程中留意不同Windows版本可能存在的兼容性差异。

通过此资源，开发者可以深入理解C#中的Hook机制，并灵活应用于各种需要底层输入事件监听的场景中。祝您开发顺利！

## 下载链接

[C全局钩子库-键盘与鼠标事件捕获](https://pan.quark.cn/s/2254fc82866e)