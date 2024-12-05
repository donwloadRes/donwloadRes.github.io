---
layout: post
title: "C-C++ Windows BLE 蓝牙操作库"
date:   2023-07-07
tags: [Windows,include,winrt,Devices,BLE]
comments: true
author: admin
---
# C/C++ Windows BLE 蓝牙操作库

## 简介

本仓库提供了一个用于在Windows平台上通过C/C++和WinRT API操作BLE（蓝牙低功耗）的资源文件。该资源文件包含了必要的头文件和示例代码，帮助开发者快速上手并实现BLE设备的操作。

## 功能描述

该资源文件主要包含以下内容：

- 必要的WinRT头文件，用于蓝牙操作。
- 示例代码，演示如何使用WinRT API进行BLE设备的扫描、连接和数据交互。

## 包含的头文件

```c++
#include <windows.h>
#include <iostream>
#include <winrt/Windows.Foundation.h>
#include <winrt/Windows.Foundation.Collections.h>
#include <winrt/Windows.Devices.Bluetooth.h>
#include <winrt/Windows.Devices.Enumeration.h>
#include <winrt/Windows.Devices.Bluetooth.Advertisement.h>
#include <winrt/Windows.Devices.Bluetooth.GenericAttributeProfile.h>
#include <winrt/Windows.Storage.Streams.h>
```

## 使用方法

1. **克隆仓库**：
    ```sh
    git clone https://github.com/your-repo-url.git
    ```

2. **包含头文件**：
    在你的C/C++项目中包含上述头文件，并根据示例代码进行开发。

3. **编译运行**：
    确保你的开发环境支持WinRT API，并正确配置项目以包含必要的库和依赖项。

## 示例代码

以下是一个简单的示例代码，演示如何扫描附近的BLE设备：

```c++
#include <iostream>
#include <winrt/Windows.Devices.Bluetooth.h>
#include <winrt/Windows.Devices.Enumeration.h>

using namespace winrt;
using namespace Windows::Devices::Bluetooth;
using namespace Windows::Devices::Enumeration;

int main()
{
    init_apartment();

    DeviceWatcher deviceWatcher = DeviceInformation::CreateWatcher(
        BluetoothLEDevice::GetDeviceSelector());

    deviceWatcher.Added([](const DeviceInformation& info) {
        std::wcout << L"Found device: " << info.Name().c_str() << std::endl;
    });

    deviceWatcher.Start();

    // 等待一段时间以便扫描设备
    std::this_thread::sleep_for(std::chrono::seconds(10));

    deviceWatcher.Stop();

    return 0;
}
```

## 注意事项

- 确保你的Windows版本支持WinRT API。
- 在开发过程中，可能需要管理员权限来访问蓝牙设备。
- 请根据实际需求调整示例代码，以适应具体的BLE设备和应用场景。

## 贡献

欢迎提交问题和拉取请求，共同完善本仓库的内容。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[CCWindowsBLE蓝牙操作库](https://pan.quark.cn/s/75409ba9f7c3)