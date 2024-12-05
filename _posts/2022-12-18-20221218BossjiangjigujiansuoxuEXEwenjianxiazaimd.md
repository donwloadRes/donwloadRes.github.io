---
layout: post
title: "Boss降级固件所需EXE文件下载"
date:   2022-02-26
tags: [降级,文件,Bose,Updater,Boss]
comments: true
author: admin
---
# Boss降级固件所需EXE文件下载

## 资源文件描述

本仓库提供了一个用于Boss降级固件的EXE文件，具体操作步骤如下：

1. **卸载Bose Updater**  
   确保你已经安装了Bose Updater。请前往 `C:\Program Files (x86)\Bose Updater` 目录，双击 `uninstall.exe` 进行卸载。

2. **下载所需软件**  
   下载本仓库提供的两个软件文件。

3. **重新安装Bose Updater**  
   双击 `boseupdatreinstaller` 进行安装。安装完成后，将下载的 `boseupdater.exe` 文件覆盖到 `C:\Program Files (x86)\Bose Updater` 目录下的同名文件。

4. **连接耳机与电脑**  
   使用数据线将耳机与电脑连接。

5. **打开BTU网站**  
   打开浏览器，访问 `btu.bose.com`。

6. **进入高级模式**  
   在电脑键盘上按顺序敲击 `a`、`d`、`v`、`↑`、`↓`。页面会变成高级模式。

7. **开始降级**  
   点击页面上的绿色按钮 `Update Now`，等待读条完成，即降级完成。

8. **错误处理**  
   如果出现错误，请查看 `C:\Users\***\AppData\Local\Temp\BoseUpdater.log` 日志文件。如果发现无法访问 `raw.githubusercontent.com` 导致错误，可以通过域名IP查询，该域名的IP为 `151.101.8.133`。

9. **修改Hosts文件**  
   修改 `C:\Windows\System32\drivers\etc\hosts` 文件，添加以下内容：
   ```
   151.101.8.133 raw.githubusercontent.com
   ```

## 注意事项

- 请确保按照步骤操作，避免因操作不当导致的降级失败。
- 在修改Hosts文件时，请确保你有管理员权限。

希望这些步骤能帮助你顺利完成Boss降级固件的操作。如果有任何问题，请随时联系我们。

## 下载链接

[Boss降级固件所需EXE文件下载](https://pan.quark.cn/s/f19a9d7e30fb)