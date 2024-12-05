---
layout: post
title: "FastAPI Swagger UI 无法打开问题解决方案
date   20200223
tags swaggeruiredocurlstr
comments true
author admin

 FastAPI Swagger UI 无法打开问题解决方案

 简介

在使用 FastAPI 框架时可能会遇到 Swagger UI 无法打开的问题表现为页面显示空白本文档提供了一个解决方案帮助你解决这个问题

 问题描述

在某些情况下FastAPI 的 Swagger UI 和 Redoc 可能无法正常打开页面显示空白这通常是由于请求的静态资源文件加载失败导致的

 解决方案

 1 下载文件

首先你需要从 GitHub 上下载所需的静态资源文件这些文件包括 swaggeruicss 和 swaggeruibundlejs你可以从以下地址下载这些文件

 swaggeruidisthttpsgithubcomswaggerapiswaggerui
 redochttpsgithubcomRedoclyredoc

 2 修改代码引用

下载文件后你需要修改 FastAPI 代码中的引用路径将默认的 CDN 链接替换为本地文件路径具体步骤如下

1 打开 FastAPI 安装目录下的 fastapiopenapidocspy 文件
2 找到以下代码并注释掉
   python
   swaggerjsurl str  httpscdnjsdelivrnetnpmswaggeruidist4swaggeruibundlejs
   swaggercssurl str  httpscdnjsdelivrnetnpmswaggeruidist4swaggeruicss
   swaggerfaviconurl str  httpsfastapitiangolocomimgfaviconpng
   
3 将上述代码替换为本地文件路径
   python
   swaggerjsurl str  staticswaggeruiswaggeruibundlejs
   swaggercssurl str  staticswaggeruiswaggeruicss
   swaggerfaviconurl str  staticswaggeruifavicon32x32png
   
4 同样地注释掉 Redoc 的默认引用
   python
   redocjsurl str  httpscdnjsdelivrnetnpmredocnextbundlesredocstandalonejs
   redocfaviconurl str  httpsfastapitiangolocomimgfaviconpng
   
5 替换为本地文件路径
   python
   redocjsurl str  staticredocbundlesredocstandalonejs
   redocfaviconurl str  staticredocfaviconpng"
date:   2020-02-23
tags: [swagger,ui,redoc,url,str]
comments: true
author: admin
---
# FastAPI Swagger UI 无法打开问题解决方案

## 简介

在使用 FastAPI 框架时，可能会遇到 Swagger UI 无法打开的问题，表现为页面显示空白。本文档提供了一个解决方案，帮助你解决这个问题。

## 问题描述

在某些情况下，FastAPI 的 Swagger UI 和 Redoc 可能无法正常打开，页面显示空白。这通常是由于请求的静态资源文件加载失败导致的。

## 解决方案

### 1. 下载文件

首先，你需要从 GitHub 上下载所需的静态资源文件。这些文件包括 `swagger-ui.css` 和 `swagger-ui-bundle.js`。你可以从以下地址下载这些文件：

- [swagger-ui-dist](https://github.com/swagger-api/swagger-ui)
- [redoc](https://github.com/Redocly/redoc)

### 2. 修改代码引用

下载文件后，你需要修改 FastAPI 代码中的引用路径，将默认的 CDN 链接替换为本地文件路径。具体步骤如下：

1. 打开 FastAPI 安装目录下的 `fastapi/openapi/docs.py` 文件。
2. 找到以下代码并注释掉：
   ```python
   swagger_js_url: str = "https://cdn.jsdelivr.net/npm/swagger-ui-dist@4/swagger-ui-bundle.js"
   swagger_css_url: str = "https://cdn.jsdelivr.net/npm/swagger-ui-dist@4/swagger-ui.css"
   swagger_favicon_url: str = "https://fastapi.tiangolo.com/img/favicon.png"
   ```
3. 将上述代码替换为本地文件路径：
   ```python
   swagger_js_url: str = "/static/swagger-ui/swagger-ui-bundle.js"
   swagger_css_url: str = "/static/swagger-ui/swagger-ui.css"
   swagger_favicon_url: str = "/static/swagger-ui/favicon-32x32.png"
   ```
4. 同样地，注释掉 Redoc 的默认引用：
   ```python
   redoc_js_url: str = "https://cdn.jsdelivr.net/npm/redoc@next/bundles/redoc.standalone.js"
   redoc_favicon_url: str = "https://fastapi.tiangolo.com/img/favicon.png"
   ```
5. 替换为本地文件路径：
   ```python
   redoc_js_url: str = "/static/redoc/bundles/redoc.standalone.js"
   redoc_favicon_url: str = "/static/redoc/favicon.png"
   ```

### 3. 添加静态文件目录

最后，在主程序中添加静态文件目录：

```python
from starlette.staticfiles import StaticFiles

# 先引用包
app.mount('/static', StaticFiles(directory='static'), name='static')
```

## 验证

完成上述步骤后，重新启动 FastAPI 应用，再次访问 Swagger UI 和 Redoc 页面，应该可以正常显示了。

## 总结

通过下载所需的静态资源文件并修改代码中的引用路径，可以有效解决 FastAPI Swagger UI 无法打开的问题。希望这个解决方案对你有所帮助。

## 下载链接

[FastAPISwaggerUI无法打开问题解决方案](https://pan.quark.cn/s/faf6eac47cca)