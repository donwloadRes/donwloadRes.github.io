---
layout: post
title: "Ubuntu 1804 安装和配置 ORBSLAM2非ROSROS环境
date   20200825
tags ORBSLAM2bashsudoROS
comments true
author admin

 Ubuntu 1804 安装和配置 ORBSLAM2非ROSROS环境

 简介

本资源文件提供了在 Ubuntu 1804 系统上安装和配置 ORBSLAM2 的详细步骤适用于非 ROS 和 ROS 环境ORBSLAM2 是一个用于单目双目和 RGBD 相机的实时 SLAM 库能够计算相机轨迹和稀疏 3D 重建

 安装步骤

 1 安装工具

在终端中输入以下命令安装必要的工具

bash
sudo aptget install cmake
sudo aptget install git
sudo aptget install gcc g


 2 安装 Eigen 库

在终端中输入以下命令安装 Eigen 库

bash
sudo aptget install libeigen3dev


 3 安装 Pangolin 05

安装 Pangolin 05 的依赖项

bash
sudo aptget install libglewdev libpython27dev
sudo aptget install libxkbcommonx11dev


下载 Pangolin 05 版本并解压

bash
unzip Pangolinv05zip


进入 Pangolin 文件夹进行编译和安装

bash
cd Pangolin
mkdir build
cd build
cmake 
make
sudo make install


 4 安装 OpenCV 341

下载 OpenCV 341 版本并解压

bash
unzip opencv341zip


安装依赖项

bash
sudo addaptrepository deb httpsecurityubuntucomubuntu xenialsecurity main"
date:   2020-08-25
tags: [ORB,SLAM2,bash,sudo,ROS]
comments: true
author: admin
---
# Ubuntu 18.04 安装和配置 ORB_SLAM2（非ROS、ROS环境）

## 简介

本资源文件提供了在 Ubuntu 18.04 系统上安装和配置 ORB_SLAM2 的详细步骤，适用于非 ROS 和 ROS 环境。ORB_SLAM2 是一个用于单目、双目和 RGB-D 相机的实时 SLAM 库，能够计算相机轨迹和稀疏 3D 重建。

## 安装步骤

### 1. 安装工具

在终端中输入以下命令安装必要的工具：

```bash
sudo apt-get install cmake
sudo apt-get install git
sudo apt-get install gcc g++
```

### 2. 安装 Eigen 库

在终端中输入以下命令安装 Eigen 库：

```bash
sudo apt-get install libeigen3-dev
```

### 3. 安装 Pangolin 0.5

安装 Pangolin 0.5 的依赖项：

```bash
sudo apt-get install libglew-dev libpython2.7-dev
sudo apt-get install libxkbcommon-x11-dev
```

下载 Pangolin 0.5 版本并解压：

```bash
unzip Pangolin_v0.5.zip
```

进入 Pangolin 文件夹进行编译和安装：

```bash
cd Pangolin
mkdir build
cd build
cmake ..
make
sudo make install
```

### 4. 安装 OpenCV 3.4.1

下载 OpenCV 3.4.1 版本并解压：

```bash
unzip opencv-3.4.1.zip
```

安装依赖项：

```bash
sudo add-apt-repository "deb http://security.ubuntu.com/ubuntu xenial-security main"
```

### 5. 安装 ORB_SLAM2

克隆 ORB_SLAM2 的代码库：

```bash
git clone https://github.com/raulmur/ORB_SLAM2.git ORB_SLAM2
```

编译 ORB_SLAM2：

```bash
cd ORB_SLAM2
chmod +x build.sh
./build.sh
```

设置环境变量：

```bash
export ROS_PACKAGE_PATH=$[ROS_PACKAGE_PATH]:path/to/ORB_SLAM2/Examples/ROS
```

### 6. 运行数据集

进入 ORB_SLAM2 的 Examples 目录并运行示例：

```bash
rosrun ORB_SLAM2 Stereo Vocabulary/ORBvoc.txt Examples/Stereo/EuRoC.yaml true
```

## 注意事项

- 如果是虚拟机，务必学会使用快照功能，以便在出现问题时可以快速恢复。
- 安装过程中可能会遇到版本兼容性问题，建议严格按照本文提供的版本进行安装。

## 参考资料

本文参考了 CSDN 博客文章，详细步骤和更多信息请参阅原文。

---

通过以上步骤，您可以在 Ubuntu 18.04 系统上成功安装和配置 ORB_SLAM2，并运行示例数据集。希望本资源对您的学习和研究有所帮助。

## 下载链接

[Ubuntu18.04安装和配置ORB_SLAM2非ROSROS环境分享](https://pan.quark.cn/s/dd309efe4ff2)