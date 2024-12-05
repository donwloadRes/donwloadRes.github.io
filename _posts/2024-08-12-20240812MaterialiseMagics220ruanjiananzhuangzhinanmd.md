---
layout: post
title: "Materialise Magics 220软件安装指南"
date:   2024-04-15
tags: [Materialise,22.0,Magics,点击,选项]
comments: true
author: admin
---
# Materialise Magics 22.0软件安装指南

## 简介
Materialise Magics 22.0是一款由比利时Materialise公司开发的快速成型辅助设计软件。它为处理平面数据的简单易用性和高效性确立了标准，提供了先进的、高度自动化的STL操作，使我们能够在强大的互动帮助工具帮助下，在几分钟内改正具有瑕疵三角的STL文件。Magics 22.0在模型修复、切片输出、医疗设备以及城市建设方面都有广泛的应用。

## 软件支持语言
Materialise Magics 22.0支持以下语言：
- 简体中文
- 英语
- 法语
- 德语
- 日本语
- 朝鲜语
- 西班牙语
- 俄罗斯语
- 意大利语

## 安装教程
1. 打开Install文件夹，找到`MagicsRP_Setup_64bit_22.0.exe`程序，右键选择“以管理员身份运行”。
2. 根据提示点击“OK”选项。
3. 在安装界面中，勾选“Materialise China”选项和“我同意Materialise最终用户许可协议”选项，然后点击“安装”。
4. 等待安装完成，点击右上角的关闭按钮关闭程序。
5. 依次打开`C:\Program Files (x86)\Common Files\Materialise\LicenseFiles6`文件夹，找到`LicSrvConfig.exe`程序，右键选择“以管理员身份运行”。
6. 点击“Stop”选项停止Materialise Local License服务。
7. 将`AutoPassword server URL`后面的网址替换成`https://localhost/MatPasswordsWS/MatPasswordsWS.asmx`。
8. 点击右下方的“Close”选项关闭程序。
9. 打开Crack文件夹，找到里面的`MatGlobal.dll`文件，将其复制后粘贴至Materialise Magics 22.0软件默认安装路径`C:\Program Files (x86)\Common Files\Materialise\LicenseFiles6`中覆盖源文件。
10. 重新回到`C:\Program Files (x86)\Common Files\Materialise`文件夹，找到`LicSrvConfig.exe`程序，右键选择“以管理员身份运行”。
11. 点击“Start”选项启动Materialise Local License服务，然后点击右下方的“Close”选项关闭程序窗口。
12. 打开安装好的Materialise Magics 22.0软件，勾选“显示许可和系统信息”选项，获取系统ID。
13. 打开Crack文件夹，找到`magics22.matkey`文件，右键选择记事本文件打开，将系统ID替换到`<SystemID></SystemID>`之间的代码中，保存并关闭。
14. 回到Materialise Magics 22.0软件激活界面，点击注册下方的“浏览”，将位置指向Crack文件夹中的`magics22.matkey`文件，点击“注册”选项，然后点击“确定”即可完成注册。

## 注意事项
- 安装过程中请确保所有步骤严格按照教程操作，特别是第八节中的内容，否则可能导致注册失败。
- 如果需要修改Materialise Magics 22.0软件的显示语言，可以打开左上角文件菜单中的“选项”-“设置”，在“常规”里面的“语言”中进行切换。

## 结语
Materialise Magics 22.0软件已经安装完成，您可以正常使用了。希望本指南能帮助您顺利完成软件的安装和配置。

## 下载链接

[MaterialiseMagics22.0软件安装指南](https://pan.quark.cn/s/51a2e0196fb0)