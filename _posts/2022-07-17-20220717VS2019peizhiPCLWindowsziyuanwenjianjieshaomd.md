---
layout: post
title: "VS2019配置PCL（Windows）资源文件介绍"
date:   2021-06-12
tags: [PCL,pcl,VS2019,1.10,cloud]
comments: true
author: admin
---
# VS2019配置PCL（Windows）资源文件介绍

本资源文件提供了在Windows系统上配置Visual Studio 2019（VS2019）与点云库（PCL）的详细步骤和所需文件。通过本资源，您可以轻松地在VS2019中集成PCL，并开始进行点云处理和开发。

## 资源内容

- **PCL-1.10.1-AllInOne-msvc2019-win64.exe**：PCL的完整安装包，适用于Windows 64位系统。
- **pcl-1.10.1-pdb-msvc2019-win64.zip**：PCL的调试符号文件，用于调试和错误排查。

## 配置步骤

1. **下载并安装PCL**：
   - 下载 `PCL-1.10.1-AllInOne-msvc2019-win64.exe` 并运行安装程序。
   - 在安装过程中，选择“Add PCL to the system PATH for all users”选项，以便自动添加PCL到系统环境变量中。

2. **配置环境变量**：
   - 安装完成后，检查系统环境变量中是否已自动添加PCL相关路径。如果没有，请手动添加。
   - 路径示例：`C:\Program Files\PCL 1.10.1\bin` 和 `C:\Program Files\PCL 1.10.1\3rdParty\FLANN\bin`。

3. **安装OpenNI2**：
   - 在PCL安装目录中找到OpenNI2的安装包，并进行安装。
   - 安装路径示例：`C:\Program Files\OpenNI2`。

4. **配置VS2019**：
   - 在VS2019中创建一个新的空项目。
   - 将项目配置为“Debug x64”模式。
   - 在项目属性中，添加PCL和VTK的包含目录和库目录。
   - 在链接器中添加PCL和VTK的库文件。

5. **测试配置**：
   - 编写一个简单的点云显示程序，使用PCL库加载并显示点云数据。
   - 示例代码：
     ```cpp
     #include <pcl/visualization/cloud_viewer.h>
     #include <pcl/io/io.h>
     #include <pcl/io/pcd_io.h>
     #include <pcl/point_types.h>

     int main() {
         pcl::PointCloud<pcl::PointXYZ>::Ptr cloud(new pcl::PointCloud<pcl::PointXYZ>);
         char strfilepath[256] = "rabbit_t.pcd";
         if (-1 == pcl::io::loadPCDFile(strfilepath, *cloud)) {
             std::cout << "error input" << std::endl;
             return -1;
         }
         std::cout << cloud->points.size() << std::endl;
         pcl::visualization::CloudViewer viewer("Cloud Viewer");
         viewer.showCloud(cloud);
         system("pause");
         return 0;
     }
     ```

## 注意事项

- 确保所有路径和文件名正确无误。
- 在配置过程中，如果遇到任何问题，请参考[CSDN博客文章](https://blog.csdn.net/y18771025420/article/details/110517524)获取更多详细信息。

通过以上步骤，您应该能够在VS2019中成功配置PCL，并开始进行点云处理和开发。祝您使用愉快！

## 下载链接

[VS2019配置PCLWindows资源文件介绍分享](https://pan.quark.cn/s/b27286446089)