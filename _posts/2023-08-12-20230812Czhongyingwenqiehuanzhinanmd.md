---
layout: post
title: "C 中英文切换指南"
date:   2022-01-13
tags: [资源,文件,Resources,C#,resx]
comments: true
author: admin
---
# C# 中英文切换指南

在开发多语言支持的C#应用程序时，实现界面和文本的中英文动态切换是一个常见需求。本资源将引导您通过使用资源文件（.resx），实现这一功能。资源文件作为一种存储国际化字符串和其他 culture-specific 资源的方式，是C#中处理多语言的关键。

### 实现步骤：

1. **创建资源文件**:
   - 首先，在您的项目中为每种语言创建一个资源文件。例如，对于英语和中文，你需要至少两个文件：`Resources.en.resx`(英语) 和 `Resources.zh.resx`(中文)。默认情况下，Visual Studio会为你创建一个无后缀的文化默认资源文件，如`Resources.resx`，通常代表程序的默认语言。

2. **填充资源文件**:
   - 每个资源文件中，定义键值对，键为字符串ID，值为对应语言的文本。例如，键为"HelloWorld"，英语值为"Hello World"，中文值为"你好，世界"。

3. **设置当前线程的文化**:
   - 运行时，根据用户选择或系统设置更改线程的文化。使用以下代码片段：
     ```csharp
     Thread.CurrentThread.CurrentUICulture = new CultureInfo("en-US"); // 英语
     或
     Thread.CurrentThread.CurrentUICulture = new CultureInfo("zh-CN"); // 简体中文
     ```

4. **从资源中获取字符串**:
   - 在你的应用程序中，避免直接硬编码字符串，而是通过资源文件动态获取。例如：
     ```csharp
     string greeting = Resources.HelloWorld;
     ```
     这样做使得程序能够根据当前线程的文化自动调整显示的文字。

5. **控件本地化**:
   - 对于UI元素如按钮、标签等，不在属性窗口直接设置文字，而是在程序加载时或文化变更时，动态地设置它们的`Text`属性。例如：
     ```csharp
     button1.Text = Resources.SaveButton;
     ```

### 注意事项：
- 保持资源文件的结构清晰，便于维护。
- 当新增或修改资源项时，确保重新编译应用以更新资源。
- 考虑到兼容性和扩展性，尽量使用标准的ISO语言代码。
- 实际应用中，可能还需要考虑日期格式、数字格式等其他文化相关的本地化调整。

通过上述步骤，您的C#应用程序就能够轻松实现中英文之间的切换，为用户提供更友好的多语言体验。这不仅限于简单的文本替换，也可以应用于整个应用的国际化策略之中。

## 下载链接

[C中英文切换指南](https://pan.quark.cn/s/37903de4291a)