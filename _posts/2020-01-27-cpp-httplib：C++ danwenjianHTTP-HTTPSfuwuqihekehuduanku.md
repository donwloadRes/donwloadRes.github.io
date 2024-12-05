---
layout: post
title: "cpp-httplib：C++ 单文件HTTP-HTTPS服务器和客户端库"
date:   2024-04-08
tags: [httplib,HTTP,cpp,HTTPS,res]
comments: true
author: admin
---
# cpp-httplib：C++ 单文件HTTP/HTTPS服务器和客户端库

## 简介

`cpp-httplib` 是一个基于 C++11 的单文件、纯头文件的跨平台 HTTP/HTTPS 库。它非常易于使用，只需在你的代码中包含 `httplib.h` 文件即可开始使用。该库支持多线程的“阻塞”模式，适合需要简单快速实现 HTTP/HTTPS 服务器和客户端的场景。如果你需要“非阻塞”的库，请考虑其他选项。

## 特点

- **单文件库**：只需包含一个头文件即可使用。
- **跨平台**：支持多种操作系统，包括 Windows、Linux 和 macOS。
- **HTTP/HTTPS 支持**：同时支持 HTTP 和 HTTPS 协议。
- **多线程**：支持多线程操作，适合并发请求处理。
- **简单易用**：API 设计简洁，易于上手。

## 使用示例

### 服务器端

以下是一个简单的 HTTP 服务器示例：

```cpp
#define CPPHTTPLIB_OPENSSL_SUPPORT
#include "path/to/httplib.h"

// 创建 HTTP 服务器
httplib::Server svr;

// 定义路由处理函数
svr.Get("/hi", [](const httplib::Request &req, httplib::Response &res) {
    res.set_content("Hello World!", "text/plain");
});

// 启动服务器，监听 8080 端口
svr.listen("0.0.0.0", 8080);
```

### 客户端

以下是一个简单的 HTTP 客户端示例：

```cpp
#define CPPHTTPLIB_OPENSSL_SUPPORT
#include "path/to/httplib.h"

// 创建 HTTP 客户端
httplib::Client cli("http://example.com");

// 发送 GET 请求
auto res = cli.Get("/hi");
if (res) {
    std::cout << res->status << std::endl;
    std::cout << res->body << std::endl;
}
```

## 注意事项

- 该库是一个“阻塞”的 HTTP 库，适合处理简单的请求和响应。如果你需要高性能的“非阻塞”处理，请考虑其他库。
- 使用 HTTPS 时，需要定义 `CPPHTTPLIB_OPENSSL_SUPPORT` 宏，并确保 OpenSSL 库已正确安装。

## 许可证

`cpp-httplib` 使用 MIT 许可证，可以自由使用、修改和分发。

## 贡献

欢迎提交问题和拉取请求，帮助改进 `cpp-httplib`。

## 下载链接

[cpp-httplibC单文件HTTPHTTPS服务器和客户端库](https://pan.quark.cn/s/abfa1147629b)