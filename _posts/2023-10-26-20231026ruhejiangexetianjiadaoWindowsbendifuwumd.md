---
layout: post
title: "如何将exe添加到Windows本地服务
date   20240722
tags exeWindowsmyService服务instsrv
comments true
author admin

 如何将exe添加到Windows本地服务

本文详细介绍了如何将一个exe程序添加到Windows本地服务中使其能够在系统启动时自动运行文章提供了两种方法使用Windows自带的sc命令和使用instsrv与srvany工具

 方法一使用Windows自带的sc命令

1 以管理员身份运行cmd命令行窗口
2 输入以下命令
   
   sc create myService binpath Cpathtoyourexefileexe
   
   其中myService是创建的本地服务名称binpath是exe程序所在的绝对路径
3 打开系统服务可以看到刚刚创建好的服务
4 右键单击服务属性将启动类型改为自动
5 删除服务命令
   
   sc delete 创建的服务名称"
date:   2024-07-22
tags: [exe,Windows,myService,服务,instsrv]
comments: true
author: admin
---
# 如何将exe添加到Windows本地服务

本文详细介绍了如何将一个exe程序添加到Windows本地服务中，使其能够在系统启动时自动运行。文章提供了两种方法：使用Windows自带的`sc`命令和使用`instsrv`与`srvany`工具。

## 方法一：使用Windows自带的sc命令

1. **以管理员身份运行cmd命令行窗口**。
2. **输入以下命令**：
   ```
   sc create myService binpath= "C:\path\to\your\exe\file.exe"
   ```
   其中，`myService`是创建的本地服务名称，`binpath`是exe程序所在的绝对路径。
3. **打开系统服务**，可以看到刚刚创建好的服务。
4. **右键单击服务属性**，将启动类型改为自动。
5. **删除服务命令**：
   ```
   sc delete "创建的服务名称"
   ```

## 方法二：使用instsrv + srvany工具

1. **下载并解压instsrv.exe和srvany.exe**。
2. **将instsrv.exe和srvany.exe拷贝到C:\Windows\SysWOW64目录下**（如果是32位系统则拷贝到C:\Windows\system32目录下）。
3. **以管理员身份打开cmd**，进入到C:\Windows\SysWOW64目录（或C:\Windows\system32目录）。
4. **输入命令**：
   ```
   instsrv myService C:\Windows\SysWOW64\srvany.exe
   ```
   其中，`myService`是创建的服务名称。
5. **配置服务**：
   - 打开注册表（在cmd或者Windows自带的搜索中输入: `regedit`）。
   - 在`HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services`目录下找到`myService`。
   - 右击`myService`，点击“新建项”，命名为“Parameters”。
   - 在`Parameters`中新建几个字符串值：
     - 名称: `Application`，值: exe程序的绝对路径。
     - 名称: `AppDirectory`，值: exe程序所在的文件夹路径。
     - 名称: `AppParameters`，无需设置值。
6. **打开系统服务**，找到创建的`myService`服务，将启动类型设置为自动。

通过以上两种方法，你可以轻松地将一个exe程序添加到Windows本地服务中，使其在系统启动时自动运行。

## 下载链接

[如何将exe添加到Windows本地服务分享](https://pan.quark.cn/s/0eb211075621)