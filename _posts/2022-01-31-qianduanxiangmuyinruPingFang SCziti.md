---
layout: post
title: "前端项目引入PingFang SC字体"
date:   2021-04-29
tags: [font,字体,family,PingFangSC,sans]
comments: true
author: admin
---
# 前端项目引入PingFang SC字体

## 简介

本资源文件提供了在前端项目中引入PingFang SC字体的方法和相关资源。PingFang SC字体是苹果公司为其操作系统（iOS和macOS）开发的一种中文字体，具有良好的显示效果和易读性。通过引入该字体，可以使前端项目中的文本显示更加美观和一致。

## 实现原理

使用`@font-face`将字体下载在用户电脑中，然后通过`font-family`属性在CSS中使用该字体。

## 使用方法

1. **下载字体文件**：从本资源文件中下载所需的PingFang SC字体文件（如`.ttf`格式）。

2. **引入字体文件**：在CSS文件中使用`@font-face`规则引入下载的字体文件。示例如下：

   ```css
   @font-face {
       font-family: 'myFont';
       src: url('/assets/font/PingFangSC-Light.ttf'); /* 替换为你的资源目录 */
       font-weight: normal;
       font-style: normal;
   }
   ```

3. **应用字体**：在HTML或CSS中使用`font-family`属性应用该字体。示例如下：

   ```css
   body {
       font-family: myFont, sans-serif;
   }
   ```

## 字体字重

PingFang SC字体提供了六个字重，可以根据需要选择合适的字重进行使用：

- 苹方-简 常规体：`font-family: PingFangSC-Regular, sans-serif;`
- 苹方-简 极细体：`font-family: PingFangSC-Ultralight, sans-serif;`
- 苹方-简 细体：`font-family: PingFangSC-Light, sans-serif;`
- 苹方-简 纤细体：`font-family: PingFangSC-Thin, sans-serif;`
- 苹方-简 中黑体：`font-family: PingFangSC-Medium, sans-serif;`
- 苹方-简 中粗体：`font-family: PingFangSC-Semibold, sans-serif;`

## 注意事项

- 确保字体文件路径正确，避免引入失败。
- 字体文件较大，建议在生产环境中使用压缩版本（如`.woff2`格式）以提高加载速度。

## 参考资料

本资源文件的详细实现方法和原理可以参考[CSDN博客文章](https://blog.csdn.net/weixin_30553777/article/details/98260122)。

---

通过以上步骤，您可以轻松地将PingFang SC字体引入到前端项目中，提升项目的视觉效果和用户体验。

## 下载链接

[前端项目引入PingFangSC字体分享](https://pan.quark.cn/s/0cc2fc72ad31)