---
layout: post
title: "Unity AVPro Video使用和WebGL播放视频流"
date:   2023-07-23
tags: [播放,视频,mediaPlayer,Media,WebGL]
comments: true
author: admin
---
# Unity AVPro Video使用和WebGL播放视频流

## 简介
本资源文件提供了关于如何在Unity中使用AVPro Video插件以及如何在WebGL平台上播放视频流的详细指南。通过本资源，开发者可以学习如何创建Media Player对象、Display uGui对象，并通过代码控制视频的播放、暂停、停止等操作。

## 主要内容
1. **创建Media Player对象**：在Unity的Hierarchy视图中创建Media Player对象，用于管理视频播放。
2. **创建Display uGui对象**：在Hierarchy视图中创建Display uGui对象，用于显示视频内容。
3. **指定Media Player组件**：将Display uGui对象与Media Player组件关联，确保视频能够正确显示。
4. **视频资源或URL链接**：提供了多个测试视频的URL链接，包括MP4和m3u8格式的视频。
5. **代码控制播放**：通过代码实现视频的播放、暂停、停止等功能，并提供了事件监听机制。

## 使用步骤
1. 在Unity中创建一个新的项目。
2. 导入AVPro Video插件。
3. 按照指南创建Media Player和Display uGui对象。
4. 通过代码控制视频的播放，并根据需要进行事件监听。

## 注意事项
- 在WebGL平台上播放视频流时，建议使用m3u8格式的视频。
- 打包WebGL平台时，需要在index.html中加入hls.min.js文件以支持m3u8格式的视频播放。

## 示例代码
以下是一个简单的示例代码，展示了如何通过代码控制视频的播放：

```csharp
using UnityEngine;
using RenderHeads.Media.AVProVideo;

public class VideoController : MonoBehaviour
{
    [SerializeField] private MediaPlayer mediaPlayer;
    [SerializeField] private DisplayUGUI displayUGUI;

    void Awake()
    {
        Init();
    }

    private void Init()
    {
        if (mediaPlayer == null)
        {
            mediaPlayer = transform.Find("MediaPlayer").GetComponent<MediaPlayer>();
        }
        mediaPlayer.Events.AddListener(OnMediaPlayerEvent);

        if (displayUGUI == null)
        {
            displayUGUI = transform.Find("Bg/VideoDisplay").GetComponent<DisplayUGUI>();
        }
        if (displayUGUI.CurrentMediaPlayer == null)
        {
            displayUGUI.CurrentMediaPlayer = mediaPlayer;
        }
    }

    private void OnMediaPlayerEvent(MediaPlayer arg0, MediaPlayerEvent.EventType arg1, ErrorCode arg2)
    {
        switch (arg1)
        {
            case MediaPlayerEvent.EventType.Started:
                // 视频开始播放时执行的操作
                break;
        }
    }

    // 播放视频
    public void PlayVideo(string url)
    {
        mediaPlayer.OpenMedia(new MediaPath(url, MediaPathType.AbsolutePathOrURL));
    }

    // 停止播放
    public void StopVideo()
    {
        mediaPlayer.Stop();
    }

    // 暂停播放
    public void PauseVideo()
    {
        mediaPlayer.Pause();
    }
}
```

## 总结
通过本资源文件，开发者可以快速掌握在Unity中使用AVPro Video插件进行视频播放的方法，特别是在WebGL平台上播放视频流的技术。希望本资源能够帮助开发者更好地实现视频播放功能。

## 下载链接

[UnityAVProVideo使用和WebGL播放视频流](https://pan.quark.cn/s/2b358fa60e67)