---
layout: post
title: "Vue 3 使用 PingFang 字体"
date:   2020-09-29
tags: [font,PingFang,字体,css,文件]
comments: true
author: admin
---
# Vue 3 使用 PingFang 字体

本仓库提供了一个资源文件，用于在 Vue 3 项目中使用 PingFang 字体。通过本资源文件，您可以轻松地将 PingFang 字体应用到您的 Vue 3 项目中，提升项目的视觉效果。

## 使用方法

1. **下载字体文件**：
   - 将字体文件（如 `PingFang Medium.ttf`）拷贝到项目的 `src/static` 文件夹下。

2. **创建字体样式文件**：
   - 在 `static` 文件夹下新建一个 `font.css` 文件，内容如下：
     ```css
     @font-face {
       font-family: 'PF';
       src: url('/PingFang Medium.ttf');
       font-weight: normal;
       font-style: normal;
     }
     ```

3. **局部使用**：
   - 在需要使用 PingFang 字体的组件中引入 `font.css`：
     ```html
     <style scoped>
       @import '@/static/font.css';
     </style>
     ```

4. **全局使用**：
   - 在 `main.js` 中引入 `font.css`：
     ```javascript
     import '@/static/font.css';
     ```

5. **定义全局样式**：
   - 在全局样式中定义 `font-family`：
     ```css
     #main-content {
       font-family: Helvetica Neue, Helvetica, PF, PingFang SC, Hiragino Sans GB, Microsoft YaHei, '\5FAE\8F6F\96C5\9ED1', Arial, sans-serif;
       height: 100%;
     }
     ```

## 注意事项

- 确保字体文件路径正确。
- 如果需要使用其他字重或样式的 PingFang 字体，请下载相应的字体文件并修改 `font.css` 中的 `src` 路径。

通过以上步骤，您可以在 Vue 3 项目中成功使用 PingFang 字体，提升项目的视觉体验。

## 下载链接

[Vue3使用PingFang字体](https://pan.quark.cn/s/795a167635a8)