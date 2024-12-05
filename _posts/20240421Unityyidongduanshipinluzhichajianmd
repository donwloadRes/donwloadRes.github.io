---
layout: post
title: "Unity移动端视频录制插件"
date:   2020-04-07
tags: [录制,视频,插件,自定义,Unity]
comments: true
author: admin
---
# Unity移动端视频录制插件

## 简介

本资源文件提供了一个用于Unity移动端视频录制的插件，支持Android和iOS平台。该插件名为NatCorder，能够帮助开发者在移动设备上轻松实现视频录制功能。

## 功能特点

- **跨平台支持**：支持Android和iOS平台。
- **视频格式**：支持录制MP4格式的视频。
- **自定义分辨率**：可以自定义录制视频的分辨率。
- **录制方法**：支持录制自定义Camera和整个屏幕（带UI）。
- **音频录制**：可以选择是否录制音频，并支持自定义AudioListener。
- **视频质量**：可以自定义录制视频的质量，包括码率、帧率等参数。

## 使用说明

1. **导入插件**：将NatCorder插件导入到Unity项目中。
2. **配置录制参数**：在脚本中配置录制视频的分辨率、帧率等参数。
3. **开始录制**：调用`StartRecording`方法开始录制视频。
4. **停止录制**：调用`StopRecording`方法停止录制视频。
5. **保存视频**：录制完成后，视频将保存到指定路径。

## 示例代码

以下是一个简单的录制视频的示例代码：

```csharp
// 开始录制视频
public void StartRecording(Camera camera, Vector2 videoRatio)
{
    isRecord = true;
    recordingClock = new RealtimeClock();
    videoRecorder = new MP4Recorder(
        (int)videoRatio.x,
        (int)videoRatio.y,
        30,
        recordMicrophone ? AudioSettings.outputSampleRate : 0,
        recordMicrophone ? (int)AudioSettings.speakerMode : 0,
        OnReplay
    );
    cameraInput = new CameraInput(videoRecorder, recordingClock, camera);
    if (recordMicrophone)
    {
        audioInput = new AudioInput(videoRecorder, recordingClock, audioListener);
    }
}

// 停止录制
public void StopRecording()
{
    if (!isRecord)
    {
        return;
    }
    isRecord = false;
    if (recordMicrophone)
    {
        audioInput.Dispose();
    }
    cameraInput.Dispose();
    videoRecorder.Dispose();
}
```

## 注意事项

- 录制视频可能会消耗较多的系统资源，建议在录制时注意设备的性能和电量。
- 插件支持Unity 2018.3.2及以上版本。

## 参考资料

有关该插件的更多详细信息，请参考[CSDN博客文章](https://blog.csdn.net/qq_24807077/article/details/90449439)。

## 版权声明

本资源文件遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[Unity移动端视频录制插件](https://pan.quark.cn/s/7df2297180bd)