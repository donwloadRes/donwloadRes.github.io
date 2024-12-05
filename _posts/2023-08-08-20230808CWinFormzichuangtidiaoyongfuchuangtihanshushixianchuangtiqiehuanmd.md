---
layout: post
title: "C# WinForm 子窗体调用父窗体函数实现窗体切换"
date:   2024-05-28
tags: [窗体,panel1,From2,form,From3]
comments: true
author: admin
---
# C# WinForm 子窗体调用父窗体函数实现窗体切换

## 资源描述

本资源文件演示了如何在C# WinForm应用程序中实现子窗体调用父窗体函数，从而实现关闭当前窗体并打开另一个窗体的功能。具体实现方式如下：

1. **父窗体（From1）**：在父窗体中嵌入一个 `Panel` 控件（`panel1`）。
2. **子窗体（From2 和 From3）**：在 `panel1` 中载入子窗体 `From2`。当用户在 `From2` 中点击按钮时，`panel1` 会清除当前内容并载入 `From3`。同样，当用户在 `From3` 中点击按钮时，`panel1` 会清除当前内容并重新载入 `From2`。

## 实现步骤

1. **父窗体设计**：
   - 在父窗体 `From1` 中添加一个 `Panel` 控件，命名为 `panel1`。
   - 编写函数 `LoadForm(Form form)`，用于在 `panel1` 中加载指定的子窗体。

2. **子窗体设计**：
   - 在子窗体 `From2` 和 `From3` 中分别添加按钮，并为按钮编写事件处理程序。
   - 在按钮事件处理程序中，调用父窗体的函数来清除当前窗体并加载新的窗体。

3. **代码示例**：
   - 父窗体 `From1` 中的 `LoadForm` 函数：
     ```csharp
     public void LoadForm(Form form)
     {
         panel1.Controls.Clear();
         form.TopLevel = false;
         form.FormBorderStyle = FormBorderStyle.None;
         form.Dock = DockStyle.Fill;
         panel1.Controls.Add(form);
         form.Show();
     }
     ```
   - 子窗体 `From2` 中的按钮事件处理程序：
     ```csharp
     private void btnSwitchToForm3_Click(object sender, EventArgs e)
     {
         ((From1)this.ParentForm).LoadForm(new From3());
     }
     ```
   - 子窗体 `From3` 中的按钮事件处理程序：
     ```csharp
     private void btnSwitchToForm2_Click(object sender, EventArgs e)
     {
         ((From1)this.ParentForm).LoadForm(new From2());
     }
     ```

## 使用说明

1. 下载并解压资源文件。
2. 打开解决方案文件（.sln），使用 Visual Studio 或其他 C# IDE 打开项目。
3. 运行项目，观察子窗体如何通过调用父窗体函数实现窗体切换。

## 注意事项

- 确保父窗体和子窗体的命名与代码示例中的命名一致。
- 如果需要修改窗体名称或控件名称，请确保相应代码中的引用也进行相应修改。

通过本资源文件，您可以学习如何在C# WinForm应用程序中实现子窗体与父窗体之间的交互，并实现窗体的动态切换。

## 下载链接

[CWinForm子窗体调用父窗体函数实现窗体切换](https://pan.quark.cn/s/e05eed7c7f31)