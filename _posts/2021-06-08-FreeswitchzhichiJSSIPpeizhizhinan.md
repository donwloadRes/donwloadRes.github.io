---
layout: post
title: "Freeswitch支持JSSIP配置指南"
date:   2021-12-17
tags: [Freeswitch,JSSIP,配置,WebSocket,xml]
comments: true
author: admin
---
# Freeswitch支持JSSIP配置指南

## 概述

本文档专为希望在Freeswitch平台上集成JSSIP以实现本地或服务器端视频语音通话的开发者准备。JSSIP是一个纯JavaScript SIP客户端库，允许在浏览器中直接进行VoIP通信。通过配置Freeswitch来支持JSSIP，您可以开启基于Web的通信解决方案，极大地拓展应用的可能性。以下内容基于实际操作经验整理而成，旨在帮助您顺利完成配置过程。

## 目标

- **理解配置需求**：明确Freeswitch为了支持JSSIP所需的基本配置。
- **实施配置步骤**：详细指导每一步的配置更改，确保Freeswitch能正确识别并处理来自JSSIP的通信请求。
- **测试验证**：提供简单的测试方法，确认配置成功并能正常通话。

## 配置前准备

1. **安装Freeswitch**: 确保您的环境中已安装最新版本的Freeswitch，并运行正常。
2. **了解SIP基础**：建议对SIP协议有一定了解，这将有助于理解配置逻辑。
3. **编辑能力**：准备好修改Freeswitch的配置文件，通常涉及`sip_profile.xml`和可能的用户配置。

## 主要配置步骤

### 1. 修改SIP Profile

- 打开Freeswitch配置文件夹中的`sip_profiles/external.xml`（或根据你的需求选择合适的profile）。
  
- 添加或修改配置段落以启用WebSocket支持（因为JSSIP主要通过WebSocket连接），示例：

```xml
<extension name="JSSIP Support">
    <condition field="destination_number" expression="^js[0-9]*$">
        <action application="bridge" data="sofia/internal/${EXTEN}@${domain}"/>
    </condition>
</extension>
```

这里`${EXTEN}`是您期望接听的号码，`${domain}`是指定的域，根据实际情况调整。

### 2. 启用WebSocket模块

确保Freeswitch启动时加载了WebSocket模块。检查或添加如下到`autoload_configs/modules.conf.xml`:

```xml
<load module="mod_websocket"/>
```

### 3. 配置WebSocket监听

在`freeswitch.cfg`或相应的配置文件中添加WebSocket监听端口：

```ini
; 示例: 开启WebSocket监听在端口8088
ws_api_port=8088
```

### 4. 测试与验证

- 使用JSSIP在Web前端建立连接到上述配置的WebSocket地址。
- 拨测一个预设的号码，验证两端是否能够顺利通话。

## 注意事项

- 安全性：公开的WebSocket端口需要考虑适当的安全措施，如TLS加密。
- 版本兼容：请确认所使用的Freeswitch版本与JSSIP版本之间的兼容性。
- 日志分析：遇到配置问题时，检查Freeswitch的日志文件，寻找错误线索。

完成以上步骤后，您的Freeswitch环境应已经具备了支持JSSIP的能力，打开了通往现代Web通信世界的大门。持续实践和调试将是掌握这一技术的关键。

---

本指南提供的步骤是一个基本框架，具体实施时可能需依据实际情况做出调整。祝您配置顺利，享受自由沟通的乐趣。

## 下载链接

[Freeswitch支持JSSIP配置指南分享](https://pan.quark.cn/s/f35e500be58b)