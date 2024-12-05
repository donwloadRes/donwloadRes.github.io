---
layout: post
title: "最新版 Burp Suite Professional 2023.12.1.3 优雅使用步骤【MacOS】"
date:   2023-08-31
tags: [Burp,Suite,Professional,app,1.3]
comments: true
author: admin
---
# 最新版 Burp Suite Professional 2023.12.1.3 优雅使用步骤【MacOS】

## 简介
本仓库提供最新版 Burp Suite Professional 2023.12.1.3 在 MacOS 系统上的优雅使用步骤。Burp Suite 是一款广泛使用的网络安全工具，适用于渗透测试和网络安全分析。

## 资源文件内容
- **Burp Suite Professional 2023.12.1.3**: 最新版本的 Burp Suite 专业版。
- **BurpLoaderKeygen**: 用于激活 Burp Suite 的插件。

## 使用步骤
1. **下载官网原包**: 从官方网站下载 Burp Suite Professional 2023.12.1.3 版本。
2. **下载插件**: 获取 BurpLoaderKeygen 插件。
3. **修改配置**:
   - 将 BurpLoaderKeygen 文件粘贴到以下目录中：
     ```
     /Applications/Burp Suite Professional.app/Contents/Resources/app
     ```
   - 修改 `vmoptions.txt` 文件，路径为：
     ```
     /Applications/Burp Suite Professional.app/Contents/vmoptions.txt
     ```
   - 在文件末尾追加以下代码：
     ```
     --add-opens=java.desktop/javax.swing=ALL-UNNAMED
     --add-opens=java.base/java.lang=ALL-UNNAMED
     --add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED
     --add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED
     --add-opens=java.base/jdk.internal.org.objectweb.asm.Opcodes=ALL-UNNAMED
     -javaagent:/Applications/Burp Suite Professional.app/Contents/Resources/app/BurpLoaderKeygen_v1.17.jar
     -noverify
     ```
4. **解决报错问题**:
   - 直接点击 Burp Suite 应用程序图标可能会出现报错。
   - 使用终端执行以下命令，需要输入开机密码：
     ```
     sudo xattr -d com.apple.quarantine /Applications/Burp\ Suite\ Professional.app
     ```
   - 执行后再次点击 Burp Suite 应用程序图标即可正常打开。

5. **手动启动**:
   - 如果上述步骤未成功，尝试手动启动：
     ```
     cd /Applications/Burp Suite Professional.app/Contents/Resources/app
     java -jar BurpLoaderKeygen_v1.17.jar
     ```
   - 激活步骤与老版本的相同，按照此步骤启动一次，后续即可直接点击应用程序图标来启动。

## 注意事项
- 请确保使用 JDK 17 及以上版本。
- License Text 可以根据个人需求进行定制修改，但请注意必须在首次激活之前进行更改，因为 License 会根据 License Text 的内容而发生变化。

## 贡献
如果您认为本仓库对您有帮助，欢迎点赞、留言或将其分享给更多人。您的支持将激励我继续创作更多有用的资源。

---

希望本指南能帮助您顺利使用 Burp Suite Professional 2023.12.1.3 版本。如有任何问题，请随时联系。

## 下载链接

[最新版BurpSuiteProfessional2023.12.1.3优雅使用步骤MacOS](https://pan.quark.cn/s/c670d1e0fc49)

## 下载链接

[最新版BurpSuiteProfessional2023.12.1.3优雅使用步骤MacOS](https://pan.quark.cn/s/76d503aa428b)