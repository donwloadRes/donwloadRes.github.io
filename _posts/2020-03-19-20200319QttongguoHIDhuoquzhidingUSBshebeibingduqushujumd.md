---
layout: post
title: "Qt 通过 HID 获取指定 USB 设备并读取数据"
date:   2022-01-04
tags: [HID,wstr,hid,res,handle]
comments: true
author: admin
---
# Qt 通过 HID 获取指定 USB 设备并读取数据

## 简介

本仓库提供了一个资源文件，用于在 Qt 中通过 HID（Human Interface Device）接口获取指定的 USB 设备，并读取其数据。资源文件中包含了 `hidapi.h`、`hidapi.dll` 和 `hidapi.lib`，这些文件是在 Windows 10 系统中使用 Visual Studio 2013 编译的 Release 版本。通过这些文件，您可以在 Qt 项目中实现对 USB 设备的 HID 接口调用。

## 文件说明

- **hidapi.h**: HID API 的头文件，包含了 HID 接口的函数声明。
- **hidapi.dll**: HID API 的动态链接库文件，用于在运行时调用 HID 接口。
- **hidapi.lib**: HID API 的静态链接库文件，用于在编译时链接 HID 接口。

## 使用方法

1. **初始化 HID API**：
   在调用 HID 接口之前，首先需要初始化 HID API。
   ```cpp
   int res;
   res = hid_init();
   ```

2. **打开设备**：
   使用设备的 VID（Vendor ID）和 PID（Product ID）打开指定的 USB 设备。
   ```cpp
   wchar_t wstr[MAX_STR];
   int i;
   // Open the device using the VID, PID, and optionally the Serial number.
   handle = hid_open(0x0483, 0x5750, NULL);
   if(handle == NULL)
   {
       qDebug() << "NULL-----------------------NULL";
       return;
   }
   else
   {
       qDebug() << "not ------------NULL-----------------------NULL";
   }
   ```

3. **读取设备信息**：
   读取设备的制造商字符串、产品字符串和序列号字符串。
   ```cpp
   // Read the Manufacturer String
   res = hid_get_manufacturer_string(handle, wstr, MAX_STR);
   wprintf(L"Manufacturer String: %s\n", wstr);

   // Read the Product String
   res = hid_get_product_string(handle, wstr, MAX_STR);
   wprintf(L"Product String: %s\n", wstr);

   // Read the Serial Number String
   res = hid_get_serial_number_string(handle, wstr, MAX_STR);
   wprintf(L"Serial Number String: (%d) %s\n", wstr[0], wstr);

   // Read Indexed String 1
   res = hid_get_indexed_string(handle, 1, wstr, MAX_STR);
   wprintf(L"Indexed String 1: %s\n", wstr);
   ```

4. **读取数据**：
   设置非阻塞模式并循环读取设备数据。
   ```cpp
   qDebug("hid read start");
   int res = hid_set_nonblocking(handle, 0);
   while (1)
   {
       res = hid_read(handle, buf, sizeof(buf));
       QString asd;
       for(int i = 0; i < sizeof(buf); i++)
       {
           char str[20];
           sprintf(str, "%02x", buf[i]);
           asd += str;
       }
       if(!cardInfo.contains(asd.toUpper()))
       {
           cardInfo.append(asd.toUpper());
           for(int i = 0; i < cardInfo.size(); i++)
           {
               dealWithData(cardInfo[i]);
           }
       }
   }
   ```

## 注意事项

- 本资源文件适用于 Windows 10 系统，使用 Visual Studio 2013 编译的 Release 版本。
- 在使用过程中，请确保设备的 VID 和 PID 正确无误。
- 读取数据时，建议使用非阻塞模式以避免程序卡死。

## 贡献

如果您在使用过程中遇到问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 许可证

本仓库中的资源文件遵循 MIT 许可证。详情请参阅 [LICENSE](LICENSE) 文件。

## 下载链接

[Qt通过HID获取指定USB设备并读取数据](https://pan.quark.cn/s/545392b132a3)