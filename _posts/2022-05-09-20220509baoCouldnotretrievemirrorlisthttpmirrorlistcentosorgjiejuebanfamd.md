---
layout: post
title: "报Could not retrieve mirrorlist httpmirrorlistcentosorg解决办法"
date:   2023-10-19
tags: [CentOS,yum,mirrorlist,centos,releasever]
comments: true
author: admin
---
# 报Could not retrieve mirrorlist http://mirrorlist.centos.org/解决办法

当在CentOS 7系统上尝试安装Docker或其他软件时，你可能会遇到一个常见的错误：“Could not retrieve mirrorlist http://mirrorlist.centos.org/”。这个错误通常意味着你的系统无法访问到CentOS的镜像列表。鉴于自2024年6月30日起，CentOS 7的官方仓库将不再更新yum源，这给许多用户带来了困扰。但请不用担心，这里有简单有效的解决方案，无需复杂地调整DNS设置或清除整个`yum.repos.d`目录。

### 解决步骤：

1. **手动选择镜像源**：
   - 首先，你可以选择一个稳定的国内镜像站作为替代，例如阿里云、清华大学等提供的CentOS镜像。
   
2. **编辑或创建新的Yum Repository配置**：
   - 使用文本编辑器（如`vi`或`nano`）创建一个新的repo文件，例如`/etc/yum.repos.d/CentOS-Base.repo备份.custom`。
   - 在这个文件中，替换原有的mirrorlist为国内镜像站的URL。以下是一个示例配置片段，以阿里云为例：
     ```ini
     [base]
     name=CentOS-$releasever - Base - 阿里云
     failovermethod=priority
     baseurl=http://mirrors.aliyun.com/centos/$releasever/os/$basearch/
     gpgcheck=0
     enabled=1
     
     [updates]
     name=CentOS-$releasever - Updates - 阿里云
     failovermethod=priority
     baseurl=http://mirrors.aliyun.com/centos/$releasever/updates/$basearch/
     gpgcheck=0
     enabled=1
     
     # 可根据需要添加其他仓库如 epel 等
     ```
     
3. **保存并退出编辑器**。

4. **刷新缓存和安装Docker**：
   - 运行命令 `yum clean all` 清理旧的缓存信息。
   - 接着运行 `yum makecache` 生成新的缓存。
   - 此后，你应该可以顺利执行 `yum install docker-ce` 或任何其他软件包的安装命令了。

### 注意事项:
- 确保替换配置中的`$releasever`（如7）与你的CentOS版本相匹配。
- 考虑到安全，正式生产环境中建议验证GPG密钥，但在急于解决问题的情况下，上述例子关闭了GPG检查 (`gpgcheck=0`)，实际应用中请酌情调整。

通过遵循以上步骤，你可以有效解决因 CentOS 官方仓库政策变化导致的 yum 源问题，确保你的系统能够继续稳定地获取所需的软件包。

## 下载链接

[报Couldnotretrievemirrorlisthttpmirrorlist.centos.org解决办法分享](https://pan.quark.cn/s/ab982a975153)