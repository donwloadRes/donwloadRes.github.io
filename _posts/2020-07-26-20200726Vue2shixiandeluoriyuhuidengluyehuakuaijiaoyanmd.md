---
layout: post
title: "Vue2实现的落日余晖登录页滑块校验"
date:   2021-11-28
tags: [Vue2,background,滑块,校验,背景图]
comments: true
author: admin
---
# Vue2实现的落日余晖登录页+滑块校验

这是一个用Vue2实现的登录页demo，背景图可直接替换，成品案例直接可运行。该demo使用了Vue2、Element-UI、Vue-Router以及滑块校验技术。

## 功能特点

- **背景图替换**：背景图可直接替换，方便自定义页面风格。
- **滑块校验**：集成滑块校验功能，提升登录安全性。
- **技术栈**：使用Vue2、Element-UI、Vue-Router等技术实现。

## 安装与运行

1. **安装依赖**：
   ```bash
   npm install
   ```

2. **开发运行**：
   ```bash
   npm run serve
   ```

3. **编译运行**：
   ```bash
   npm run build
   ```

## 代码解读

### 背景图设置

在`login.vue`组件中，我们定义了一个名为`background`的CSS类，用于设置背景图、大小、位置、重复方式和高度等属性。你可以根据需要完全自定义这些样式。

```css
.background {
  background-image: url('your-image-url.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  height: 100vh;
}
```

### 全局样式注意事项

由于全局样式会作用于整个应用程序，因此在设计样式时要注意不要影响到其他页面。特别需要注意的是`body`标签，默认情况下`body`标签有`margin: 8px`，这可能会导致后续页面出现白边。建议在样式中进行处理，例如：

```css
body {
  margin: 0;
}
```

## 后续文章

关于如何处理`body`标签的默认`margin`问题，以及更多Vue2开发技巧，后续会有详细的文章进行介绍。欢迎关注我的主页以获取更多内容。

## 下载链接

[Vue2实现的落日余晖登录页滑块校验](https://pan.quark.cn/s/52769752619f)