---
layout: post
title: "SpringAI通过Ollama连接大语言模型通义千问"
date:   2023-06-14
tags: [Ollama,千问,模型,通义,SpringAI]
comments: true
author: admin
---
# SpringAI通过Ollama连接大语言模型通义千问

## 简介

本仓库提供了一个资源文件，用于演示如何通过SpringAI框架连接Ollama，并使用大语言模型通义千问。该资源文件基于Spring Boot框架，展示了如何配置和调用通义千问模型，实现自然语言处理和生成功能。

## 功能特点

- **SpringAI框架**：利用SpringAI简化包含人工智能功能的应用程序开发，避免不必要的复杂性。
- **Ollama连接**：通过Ollama连接大语言模型，支持多种模型类型，如“聊天”和“文本到图像”。
- **通义千问模型**：集成通义千问模型，实现高效准确的自然语言处理能力。
- **流式调用**：支持流式调用，实时接收和处理数据，避免数据量大导致的系统崩溃或响应缓慢。

## 使用说明

1. **环境搭建**：
   - 参考文章中的第三部分【三、LLM语言模型搭建】，搭建Ollama环境。
   - 确保JDK版本为17。

2. **配置文件**：
   - 配置Spring Boot应用的端口和名称。
   - 配置Ollama的连接信息，包括基础URL和模型选项。

3. **Java连接关键代码**：
   - 使用SystemPromptTemplate和UserMessage类构建用户和系统消息。
   - 通过Flux流式处理模型响应，实时输出结果。

4. **测试**：
   - 访问`http://localhost:8080/chat`，使用Apifox工具进行测试。

## 源代码下载

本仓库提供了两个工程：
- **AI-Auto-config**：使用Spring Boot的bootstrap.yml配置连接Ollama。
- **AI-Manual-Config**：手动配置连接Ollama方式。

## 参考资料

- [SpringAI官方文档](https://spring.io/projects/spring-ai)
- [Ollama官方文档](https://ollama.ai/docs)
- [通义千问模型介绍](https://www.aliyun.com/product/ai/tongyi-qianwen)

## 贡献

欢迎提交Issue和Pull Request，共同完善本项目。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[SpringAI通过Ollama连接大语言模型通义千问](https://pan.quark.cn/s/76ac97c07709)