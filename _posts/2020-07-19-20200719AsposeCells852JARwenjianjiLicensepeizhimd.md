---
layout: post
title: "Aspose Cells 852 JAR 文件及 License 配置"
date:   2021-11-28
tags: [文件,Aspose,License,license,xml]
comments: true
author: admin
---
# Aspose Cells 8.5.2 JAR 文件及 License 配置

## 资源介绍

本仓库提供了一个名为 `aspose-cells-8.5.2.jar` 的 JAR 文件，以及一个 `license.xml` 文件。该资源文件经过亲测，可以在导出 Excel 文件时多生成一个 Sheet，并且在使用时会提示如下信息：

```
Evaluation Only. Created with Aspose.Cells for Java.
Copyright 2003 - 2023 Aspose Pty Ltd.
```

## 使用方法

1. **下载资源文件**：
   - 下载 `aspose-cells-8.5.2.jar` 文件，并将其添加到你的项目依赖中。
   - 下载 `license.xml` 文件，并将其放置在项目的合适位置。

2. **配置 License**：
   在你的代码中，添加以下代码以配置 License：

   ```java
   try {
       Resource resource = new ClassPathResource("license.xml");
       BufferedReader br = new BufferedReader(new InputStreamReader(resource.getInputStream()));
       License license = new License();
       license.setLicense(br);
   } catch (Exception var3) {
       var3.printStackTrace();
   }
   ```

   确保 `license.xml` 文件的路径正确，并且能够被正确加载。

## 注意事项

- 该资源文件仅用于学习和测试目的，请勿用于商业用途。
- 在使用过程中，如果遇到任何问题，请参考 Aspose 官方文档或联系 Aspose 支持团队。

## 许可证

本仓库中的资源文件遵循 Aspose 的许可证协议。请在使用前仔细阅读相关许可证条款。

## 下载链接

[AsposeCells8.5.2JAR文件及License配置](https://pan.quark.cn/s/e221be816982)