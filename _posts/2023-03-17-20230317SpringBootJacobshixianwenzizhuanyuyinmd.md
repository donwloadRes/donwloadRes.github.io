---
layout: post
title: "Spring Boot  Jacob 实现文字转语音"
date:   2020-11-08
tags: [Dispatch,new,Variant,ax,spVoice]
comments: true
author: admin
---
# Spring Boot + Jacob 实现文字转语音

## 简介

本资源文件提供了一个基于 Spring Boot 和 Jacob 库的文字转语音（Text-to-Speech, TTS）实现方案。该方案适用于在离线环境下，利用 Java 和 Jacob 库在 Windows 系统中实现文字转语音功能。

## 功能特点

- **离线支持**：无需联网即可实现文字转语音功能。
- **Windows 系统兼容**：专门为 Windows 系统环境设计，未测试 Linux 环境。
- **多语言支持**：能够处理英文单词的语音转换。

## 使用步骤

### 1. 引入 Jacob 库

在项目的 `pom.xml` 文件中引入 Jacob 库依赖：

```xml
<dependency>
    <groupId>com.hynnet</groupId>
    <artifactId>jacob</artifactId>
    <version>1.18</version>
</dependency>
```

### 2. 配置 DLL 文件

下载 `jacob-1.18-x64.dll` 或 `jacob-1.18-x86.dll` 文件，并将其复制到 `JAVA_HOME\bin` 目录下。注意根据 JDK 的安装版本选择合适的 DLL 文件。

### 3. 编写 Java 代码

参考以下 Java 代码示例，实现文字转语音功能：

```java
import com.jacob.activeX.ActiveXComponent;
import com.jacob.com.Dispatch;
import com.jacob.com.Variant;

public class JacobTest {
    public static void main(String[] args) {
        ActiveXComponent ax = null;
        String str = "Elasticsearch 是一个分布式、RESTful 风格的搜索和数据分析引擎，它提供了一个分布式多用户能力的全文搜索引擎，搜索速度很快。";

        try {
            ax = new ActiveXComponent("Sapi.SpVoice");
            Dispatch spVoice = ax.getObject();
            ax.setProperty("Volume", new Variant(100));
            ax.setProperty("Rate", new Variant(-2));
            Dispatch.call(spVoice, "Speak", new Variant(str));

            ax = new ActiveXComponent("Sapi.SpFileStream");
            Dispatch spFileStream = ax.getObject();
            ax = new ActiveXComponent("Sapi.SpAudioFormat");
            Dispatch spAudioFormat = ax.getObject();
            Dispatch.put(spAudioFormat, "Type", new Variant(22));
            Dispatch.putRef(spFileStream, "Format", spAudioFormat);
            Dispatch.call(spFileStream, "Open", new Variant("E:\\test.wav"), new Variant(3), new Variant(true));
            Dispatch.putRef(spVoice, "AudioOutputStream", spFileStream);
            Dispatch.put(spVoice, "Volume", new Variant(100));
            Dispatch.put(spVoice, "Rate", new Variant(-2));
            Dispatch.call(spVoice, "Speak", new Variant(str));
            Dispatch.call(spFileStream, "Close");
            Dispatch.putRef(spVoice, "AudioOutputStream", null);
            spAudioFormat.safeRelease();
            spFileStream.safeRelease();
            spVoice.safeRelease();
            ax.safeRelease();
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

## 注意事项

- 该方案仅适用于 Windows 系统环境，未测试 Linux 环境。
- 生成的语音文件格式为 WAV。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个项目。

## 许可证

本项目遵循 [CC 4.0 BY-SA 版权协议](https://creativecommons.org/licenses/by-sa/4.0/)，转载请附上原文出处链接和本声明。

## 下载链接

[SpringBootJacob实现文字转语音](https://pan.quark.cn/s/85b3f3c0572e)