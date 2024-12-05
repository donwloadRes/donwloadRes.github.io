---
layout: post
title: "Win10 下编译 OpenCV 470详细全过程包含xfeatures2d"
date:   2024-03-31
tags: [OpenCV,4.7,编译,xfeatures2d,opencv]
comments: true
author: admin
---
# Win10 下编译 OpenCV 4.7.0详细全过程，包含xfeatures2d

本仓库提供了一个详细的教程，帮助你在Windows 10系统下编译OpenCV 4.7.0，并包含xfeatures2d模块。以下是编译过程的步骤概述：

## 编译步骤

1. **下载源文件**  
   从GitHub上下载OpenCV 4.7.0源文件及opencv_contrib-4.7.0。如果下载不方便，可以使用提供的百度网盘链接。

2. **解压文件**  
   解压opencv-4.7.0.zip，并在opencv-4.7.0目录下新建build文件夹。

3. **配置CMake**  
   打开Cmake-gui，设置源文件路径及build路径，选择VS2019及x64选项，点击完成。

4. **配置EXTRA_MODULES路径**  
   在Search框中输入“extra”，配置EXTRA_MODULES路径（事先解压opencv_contrib-4.7.0.zip）。

5. **配置第三方文件**  
   点击Configure按钮，等待配置完成。如果xfeatures2d_boostdesc和xfeatures2d_vgg等文件下载失败，可以使用提供的opencv_3rdparty.zip文件。

6. **勾选NONFREE选项**  
   在配置Configure的时候，勾选上NONFREE，否则C++调用SURF::create会报错。

7. **取消不必要的勾选**  
   如果用不上java和python，可以取消勾选，节约后续编译时间。同样可以取消各种test的勾选。

8. **选择生成opencv_world库**  
   根据个人使用习惯，选择是否生成opencv_world库。如果不勾选，编译时会按模块进行生成库。

9. **设置安装路径**  
   设置OpenCV的安装路径。

10. **生成项目**  
    全部设置好后，再次点击Configure按钮，待Configuring done后，点击Generate按钮，生成项目。

11. **编译项目**  
    点击Open Project或者在build目录下，用VS2019打开OpenCV.sln，选择Release/Debug，右键点击“ALL_BUILD”点击“生成”。经过大约十多分钟，编译完成。

12. **安装OpenCV**  
    右键点击“INSTALL”点击“生成”，最终OpenCV头文件和库都会被拷贝到install路径下。

## 注意事项

- 第三方文件的下载地址可以在GitHub上找到，如果自己从GitHub上下载可以直接从以上地址下载。
- 如果缺失第三方文件，在后续编译时会出现无法解析的外部符号cv::xfeatures2d::VGG::getDefaultName的报错。

通过以上步骤，你可以在Windows 10系统下成功编译OpenCV 4.7.0，并包含xfeatures2d模块。希望本教程对你有所帮助！

## 下载链接

[Win10下编译OpenCV4.7.0详细全过程包含xfeatures2d](https://pan.quark.cn/s/ec1490c72383)