---
layout: post
title: "瑞芯微RK356x3588系列图像ISP调试工具"
date:   2024-04-17
tags: [rkaiq,server,瑞芯微,ISP,tool]
comments: true
author: admin
---
# 瑞芯微RK356x/3588系列图像ISP调试工具

## 简介
本仓库提供了一个已经编译好的瑞芯微RK356x/3588系列图像ISP调试工具 `rkaiq_tool_server`，用户可以直接将其拷贝至板卡上运行使用。

## 资源文件
- `rkaiq_3A_server`
- `librkmedia.so`

## 使用方法
1. 将上述文件拷贝至板卡的 `/data/` 目录下。
2. 运行以下命令启动 `rkaiq_tool_server`：
   ```sh
   $ sudo ./rkaiq_tool_server -d 0 -s /dev/video22 &
   ```
   参数详细说明请参考官方指南。

## 注意事项
- 确保文件权限正确，建议使用 `sudo` 运行命令。
- 请根据实际设备情况调整命令中的参数。

## 参考资料
- [官方指南](链接地址)

## 许可证
本项目遵循 [许可证名称] 许可证。详细信息请参阅 [LICENSE](LICENSE) 文件。

## 贡献
欢迎提交问题和建议，或者直接提交 Pull Request 进行代码贡献。

## 联系方式
如有任何问题，请联系 [邮箱地址]。

---
感谢使用本仓库提供的资源文件，希望对您的开发工作有所帮助！

## 下载链接

[瑞芯微RK356x3588系列图像ISP调试工具](https://pan.quark.cn/s/33a7b6ef839f)