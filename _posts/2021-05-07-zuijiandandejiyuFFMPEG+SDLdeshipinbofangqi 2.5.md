---
layout: post
title: "最简单的基于FFMPEG+SDL的视频播放器 2.5"
date:   2023-07-04
tags: [simplest,FFmpeg,ffmpeg,SDL,解码]
comments: true
author: admin
---
# 最简单的基于FFMPEG+SDL的视频播放器 2.5

## 项目描述

本程序实现了视频文件的解码和显示（支持HEVC，H.264，MPEG2等）。是最简单的FFmpeg视频解码方面的教程。通过学习本例子可以了解FFmpeg的解码流程。项目包含6个工程：

1. **simplest_ffmpeg_player**：标准版，FFmpeg学习的开始。
2. **simplest_ffmpeg_player_su**：SU（SDL Update）版，加入了简单的SDL的Event。
3. **simplest_ffmpeg_decoder**：一个包含了封装格式处理功能的解码器。使用了libavcodec和libavformat。
4. **simplest_ffmpeg_decoder_pure**：一个纯净的解码器。只使用libavcodec（没有使用libavformat）。
5. **simplest_video_play_sdl2**：使用SDL2播放YUV的例子。
6. **simplest_ffmpeg_helloworld**：输出FFmpeg类库的信息。

## 使用说明

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo-link.git
   ```

2. **编译和运行**：
   - 进入相应的工程目录，按照工程内的编译说明进行编译。
   - 运行生成的可执行文件，查看效果。

## 依赖库

- FFmpeg
- SDL

## 贡献

欢迎提交Issue和Pull Request，共同完善本项目。

## 许可证

本项目采用[MIT许可证](LICENSE)。

## 下载链接

[最简单的基于FFMPEGSDL的视频播放器2.5](https://pan.quark.cn/s/d43a5fdf9a1e)