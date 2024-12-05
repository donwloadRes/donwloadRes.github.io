---
layout: post
title: "使用highlight.js和marked.js格式代码和高亮代码"
date:   2024-06-16
tags: [js,highlight,marked,代码,高亮]
comments: true
author: admin
---
# 使用highlight.js和marked.js格式代码和高亮代码

本仓库提供了一个资源文件，用于帮助开发者在使用highlight.js和marked.js时格式化代码并实现代码高亮。通过结合这两个工具，您可以轻松地在网页中展示格式化的代码，并使其具有语法高亮效果。

## 功能介绍

- **代码格式化**：使用marked.js将Markdown格式的代码转换为HTML格式，便于在网页中展示。
- **代码高亮**：通过highlight.js为代码块添加语法高亮，提升代码的可读性。

## 使用方法

1. **引入依赖**：在您的项目中引入highlight.js和marked.js库。
2. **配置marked.js**：使用marked.js解析Markdown代码，并将其转换为HTML格式。
3. **应用highlight.js**：在转换后的HTML代码中应用highlight.js，实现代码高亮效果。

## 示例代码

以下是一个简单的示例，展示了如何使用highlight.js和marked.js来格式化和高亮代码：

```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="path/to/highlight.js/styles/default.min.css">
    <script src="path/to/highlight.js/highlight.min.js"></script>
    <script src="path/to/marked.js"></script>
</head>
<body>
    <div id="content"></div>
    <script>
        const markdown = `
        # 示例代码
        \`\`\`javascript
        function helloWorld() {
            console.log('Hello, World!');
        }
        \`\`\`
        `;

        const html = marked.parse(markdown);
        document.getElementById('content').innerHTML = html;
        hljs.highlightAll();
    </script>
</body>
</html>
```

## 注意事项

- 确保在引入highlight.js和marked.js时，路径正确无误。
- 根据需要选择合适的highlight.js样式文件，以实现不同的代码高亮效果。

通过本资源文件，您可以快速上手使用highlight.js和marked.js，提升代码展示的效果。

## 下载链接

[使用highlight.js和marked.js格式代码和高亮代码](https://pan.quark.cn/s/feb3a7ba03c0)