---
layout: post
title: "自己搭建KMS服务器成功激活Office2010
date   20221226
tags KMS激活Office2010Windows
comments true
author admin

 自己搭建KMS服务器成功激活Office2010

本文详细介绍了如何自己搭建KMS服务器并成功激活Office 2010的过程通过自建KMS服务器您可以确保激活过程的安全性和稳定性

 主要步骤

1 下载Office 2010
    下载原版的Office 2010 Professional Plus 2010 With SP1 VOL 64位版本
    下载完成后务必验证文件的校验值确保文件完整性

2 安装Office 2010
    安装过程已经绑定了产品密钥无需单独输入产品密钥

3 下载KMS模拟激活主机
    下载vlmcsd这是一个KMS模拟激活主机工具
    注意vlmcsd可能会被杀毒软件查杀建议下载前关闭杀毒软件

4 安装KMS模拟激活主机
    解压下载的压缩包将vlmcsdWindowsx64exe复制到CWindowsSystem32目录
    以管理员身份运行命令提示符执行以下命令
     
     sc create KMSSrv binpathwindirSystem32vlmcsdWindowsx64exe typeown startauto displaynameKMS Emulator"
date:   2022-12-26
tags: [KMS,激活,Office,2010,Windows]
comments: true
author: admin
---
# 自己搭建KMS服务器成功激活Office2010

本文详细介绍了如何自己搭建KMS服务器并成功激活Office 2010的过程。通过自建KMS服务器，您可以确保激活过程的安全性和稳定性。

## 主要步骤

1. **下载Office 2010**
   - 下载原版的Office 2010 Professional Plus 2010 With SP1 VOL 64位版本。
   - 下载完成后，务必验证文件的校验值，确保文件完整性。

2. **安装Office 2010**
   - 安装过程已经绑定了产品密钥，无需单独输入产品密钥。

3. **下载KMS模拟激活主机**
   - 下载vlmcsd，这是一个KMS模拟激活主机工具。
   - 注意：vlmcsd可能会被杀毒软件查杀，建议下载前关闭杀毒软件。

4. **安装KMS模拟激活主机**
   - 解压下载的压缩包，将vlmcsd-Windows-x64.exe复制到C:\Windows\System32目录。
   - 以管理员身份运行命令提示符，执行以下命令：
     ```
     sc create KMSSrv binpath=%windir%\System32\vlmcsd-Windows-x64.exe type=own start=auto displayname="KMS Emulator"
     net start KMSSrv
     netsh advfirewall firewall add rule name="KMS Emulator Server" dir=in action=allow protocol=TCP localport=1688
     ```

5. **验证KMS模拟激活主机**
   - 将vlmcs-Windows-x64.exe复制到C:\Windows\SysWOW64目录。
   - 以管理员身份运行命令提示符，执行以下命令验证是否成功：
     ```
     vlmcs-Windows-x64.exe -v -l 3 localhost
     ```

6. **激活Office 2010**
   - 使用管理员身份打开命令提示符，执行以下命令：
     ```
     cd C:\Program Files\Microsoft Office\Office14
     cscript ospp.vbs /sethst:xx.xx.xx
     cscript ospp.vbs /act
     ```
   - 出现“Product activation successful”即表示激活成功。

## 注意事项

- KMS激活仅限于VOL版本，其他零售版无法激活。
- 确保计算机连接到互联网，因为KMS激活需要在线激活。
- 检查计算机的日期和时间是否正确，错误的日期和时间可能会影响KMS激活。

通过以上步骤，您可以成功搭建自己的KMS服务器并激活Office 2010。

## 下载链接

[自己搭建KMS服务器成功激活Office2010](https://pan.quark.cn/s/d01f52801a52)