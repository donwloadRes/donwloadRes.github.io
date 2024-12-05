---
layout: post
title: "Ubuntu 20.04 下 Docker 及 NVIDIA Docker 安装包"
date:   2021-09-10
tags: [deb,amd64,Docker,sudo,dpkg]
comments: true
author: admin
---
# Ubuntu 20.04 下 Docker 及 NVIDIA Docker 安装包

本仓库提供了一系列在 Ubuntu 20.04 系统下安装 Docker 及 NVIDIA Docker 所需的安装包。这些安装包可以帮助用户快速完成 Docker 和 NVIDIA Docker 的安装，适用于需要使用 Docker 进行容器化部署，并且需要利用 NVIDIA GPU 加速的应用场景。

## 资源文件列表

### NVIDIA Docker 安装包

- `libnvidia-container1_1.4.0-1_amd64.deb`
- `libnvidia-container-dev_1.4.0-1_amd64.deb`
- `libnvidia-container-tools_1.4.0-1_amd64.deb`
- `nvidia-container-runtime_3.5.0-1_amd64.deb`
- `nvidia-container-toolkit_1.5.1-1_amd64.deb`
- `nvidia-docker2_2.6.0-1_all.deb`

### Docker 安装包

- `containerd.io_1.6.26-1_amd64.deb`
- `docker-buildx-plugin_0.11.2-1~ubuntu.20.04~focal_amd64.deb`
- `docker-ce_24.0.7-1~ubuntu.20.04~focal_amd64.deb`
- `docker-ce-cli_24.0.7-1~ubuntu.20.04~focal_amd64.deb`
- `docker-compose-plugin_2.21.0-1~ubuntu.20.04~focal_amd64.deb`

## 安装说明

1. **下载安装包**：
   从本仓库下载所需的 `.deb` 安装包。

2. **安装 Docker**：
   依次安装以下 Docker 相关包：
   ```bash
   sudo dpkg -i containerd.io_1.6.26-1_amd64.deb
   sudo dpkg -i docker-buildx-plugin_0.11.2-1~ubuntu.20.04~focal_amd64.deb
   sudo dpkg -i docker-ce_24.0.7-1~ubuntu.20.04~focal_amd64.deb
   sudo dpkg -i docker-ce-cli_24.0.7-1~ubuntu.20.04~focal_amd64.deb
   sudo dpkg -i docker-compose-plugin_2.21.0-1~ubuntu.20.04~focal_amd64.deb
   ```

3. **安装 NVIDIA Docker**：
   依次安装以下 NVIDIA Docker 相关包：
   ```bash
   sudo dpkg -i libnvidia-container1_1.4.0-1_amd64.deb
   sudo dpkg -i libnvidia-container-dev_1.4.0-1_amd64.deb
   sudo dpkg -i libnvidia-container-tools_1.4.0-1_amd64.deb
   sudo dpkg -i nvidia-container-runtime_3.5.0-1_amd64.deb
   sudo dpkg -i nvidia-container-toolkit_1.5.1-1_amd64.deb
   sudo dpkg -i nvidia-docker2_2.6.0-1_all.deb
   ```

4. **验证安装**：
   安装完成后，可以通过以下命令验证 Docker 和 NVIDIA Docker 是否安装成功：
   ```bash
   sudo docker run --rm --gpus all nvidia/cuda:11.0-base nvidia-smi
   ```
   如果安装成功，应该会显示 NVIDIA GPU 的相关信息。

## 注意事项

- 请确保在安装之前已经安装了 NVIDIA 驱动程序。
- 如果遇到依赖问题，可以使用 `sudo apt-get install -f` 命令来解决依赖关系。

## 贡献

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 许可证

本仓库中的安装包遵循其各自的许可证。请在使用前仔细阅读相关许可证信息。

## 下载链接

[Ubuntu20.04下Docker及NVIDIADocker安装包](https://pan.quark.cn/s/75a145bc6af6)