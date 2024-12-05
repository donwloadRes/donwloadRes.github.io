---
layout: post
title: "SolidWorks Electrical 安装错误解决办法记录"
date:   2022-08-30
tags: [安装,SolidWorks,Electrical,MSSQL,2014]
comments: true
author: admin
---
# SolidWorks Electrical 安装错误解决办法（记录）

本文档记录了在安装 SolidWorks Electrical 过程中可能遇到的常见错误及其解决办法。通过参考本文档，用户可以有效地解决安装过程中遇到的问题，确保 SolidWorks Electrical 能够顺利安装并正常运行。

## 主要内容

1. **安装 MSSQL 2014 英文版**
   - 由于中文版 MSSQL 与 SolidWorks Electrical 存在冲突，建议先安装 MSSQL 2014 英文版。
   - 确保 MSSQL 2014 能够正常连接到 TEW_SQLEXPRESS。

2. **使用 X:\swelectric\setup.exe 安装**
   - 在安装过程中，确保选择 SQL 的所有功能。
   - 如果遇到错误，可以使用安装程序卸载并重新安装。

3. **常见错误及解决办法**
   - **无法连接到 SQL Server**：确保 MSSQL 服务已启动，并检查用户名和密码是否正确。
   - **数据库出错**：确保 MSSQL 2014 已正确安装，并尝试重新安装 SolidWorks Electrical。

## 注意事项

- 在安装 SolidWorks Electrical 之前，建议先安装 MSSQL 2014 英文版，以避免潜在的冲突。
- 如果在安装过程中遇到问题，可以参考本文档中的解决办法，或联系技术支持获取帮助。

通过遵循本文档中的步骤和建议，用户可以有效地解决 SolidWorks Electrical 安装过程中遇到的问题，确保软件能够顺利安装并正常运行。

## 下载链接

[SolidWorksElectrical安装错误解决办法记录](https://pan.quark.cn/s/3a2341ae78d9)