---
layout: post
title: "C WinForm使用AForge拍照及录像"
date:   2022-04-30
tags: [AForge,录像,writer,Video,private]
comments: true
author: admin
---
# C# WinForm使用AForge拍照及录像

## 概述

本文档旨在指导开发者如何在C#的WinForm应用程序中集成摄像头功能，实现拍照和录像。通过利用AForge.NET框架及其相关组件（包括AForge.Controls、AForge.Video.DirectShow、AForge.Video.FFMPEG），您可以轻松地将这些功能添加到您的应用中。AForge.NET是一个用于计算机视觉和人工智能的.NET框架，提供了丰富的库支持视频处理、图像处理等多个领域。

## 快速入门

### 安装必要的NuGet包

1. 打开Visual Studio，创建一个新的Windows Forms Application项目。
2. 使用NuGet包管理器搜索并安装以下包：
   - AForge
   - AForge.Controls
   - AForge.Video.DirectShow
   - AForge.Video.FFMPEG
3. 安装完成后，这些库会自动添加到你的项目引用中。

### 示例代码

#### 初始化摄像头

首先，你需要初始化一个`VideoCaptureDevice`来获取摄像头数据。

```csharp
using AForge.Video;
using AForge.Video.DirectShow;

// 获取可用的视频源
FilterInfoCollection videoDevices = new FilterInfoCollection(FilterCategory.VideoInputDevice);
if (videoDevices.Count == 0)
{
    MessageBox.Show("没有找到摄像头!");
}
else
{
    // 使用第一个摄像头
    VideoCaptureDevice videoSource = new VideoCaptureDevice(videoDevices[0].MonikerString);
    
    // 设置帧到达事件处理
    videoSource.NewFrame += new NewFrameEventHandler(OnNewVideoFrame);
    videoSource.Start(); // 开始捕获
}

private void OnNewVideoFrame(object sender, NewFrameEventArgs eventArgs)
{
    Bitmap bitmap = (Bitmap)eventArgs.Frame.Clone();
    // 处理或显示帧图像
}
```

#### 拍照

在`OnNewVideoFrame`事件处理器中，你可以保存当前帧作为图片来实现拍照功能。

```csharp
private void TakeSnapshot(Bitmap bitmap)
{
    string path = "snapshot.jpg";
    bitmap.Save(path);
    MessageBox.Show("照片已保存！");
}
```

#### 录像

录像需要你创建一个`VideoFileWriter`对象，并在每一帧到来时写入视频流。

```csharp
private VideoFileWriter writer;

public Form1()
{
    InitializeComponent();
    // 初始化录像所需的参数
    if (InitializeRecorder())
    {
        // 开启录像
        buttonRecord.Text = "停止录像";
    }
}

private bool InitializeRecorder()
{
    writer = new VideoFileWriter();
    writer.Open("record.avi", 640, 480, 25, VideoCodec.MotionJpeg);
    return true;
}

private void buttonRecord_Click(object sender, EventArgs e)
{
    if (writer.IsOpen)
    {
        // 关闭录像
        writer.Close();
        buttonRecord.Text = "开始录像";
    }
    else
    {
        // 开始录像
        if (InitializeRecorder())
            buttonRecord.Text = "停止录像";
    }
}

private void OnNewVideoFrame(object sender, NewFrameEventArgs eventArgs)
{
    Bitmap bitmap = (Bitmap)eventArgs.Frame.Clone();
    
    if (writer.IsOpen)
    {
        writer.WriteVideoFrame(bitmap);
    }
    // 其他处理逻辑
}
```

### 注意事项

- 确保安装了正确的驱动程序并且摄像头工作正常。
- 调试时请检查权限问题，特别是在Windows 10及以上版本，可能需要管理员权限运行以访问摄像头。
- 根据实际需求调整视频分辨率、帧率等设置。

通过以上步骤，您就可以在C# WinForm应用中实现基本的拍照和录像功能了。实验过程中，根据具体应用场景可能还需要进一步优化性能与用户体验。

## 下载链接

[CWinForm使用AForge拍照及录像](https://pan.quark.cn/s/ebb7d7cf34e8)