---
layout: post
title: "MP3封面添加工具使用指南"
date:   2024-02-24
tags: [封面,添加,MP3,歌曲,new]
comments: true
author: admin
---
# MP3封面添加工具使用指南

本仓库提供了一个用于批量给MP3文件添加封面的工具。该工具可以帮助用户快速、方便地为MP3文件添加专辑封面，提升音乐文件的视觉效果。

## 功能特点

- **批量处理**：支持批量添加封面，适用于大量MP3文件的管理。
- **自动匹配**：工具会自动根据歌曲和封面文件的名称进行匹配，确保封面正确添加。
- **简单易用**：操作简单，用户只需指定歌曲和封面文件夹，点击按钮即可完成添加。

## 使用步骤

1. **下载软件**：点击下载批量添加歌曲封面软件。
2. **解压软件**：下载之后点击解压软件，双击打开Mp3AddCover.exe。
3. **添加歌曲和封面**：
   - 添加歌曲（mp3格式）所在文件夹。
   - 添加封面（jpg格式）所在文件夹。
4. **开始添加封面**：点击“添加封面”按钮，工具将自动匹配歌曲和封面，并完成添加。

## 注意事项

- 请确保歌曲和封面文件的名称一致，以便工具能够正确匹配。
- 如果需要添加歌手信息，请确保mp3文件名称为“歌手 - 歌曲”格式。

## 主要代码

该工具使用了TagLib库来处理MP3文件的元数据，具体代码如下：

```csharp
public static void SetAlbumArt(string coverPath, string filePath, bool isReplace)
{
    var fileInfo = new FileInfo(filePath);
    Stream stream = fileInfo.Open(FileMode.Open);
    var abstraction = new TagLib.StreamFileAbstraction(fileInfo.Name, stream, stream);
    var file = TagLib.File.Create(abstraction);
    var picture = file.Tag.Pictures;
    if (picture.Length > 0 && !isReplace)
    {
        return;
    }
    Picture pic = new Picture()
    {
        Type = PictureType.FrontCover,
        Description = "Cover",
        MimeType = System.Net.Mime.MediaTypeNames.Image.Jpeg
    };
    Image image = Image.FromFile(coverPath);
    MemoryStream ms = new MemoryStream();
    image.Save(ms, System.Drawing.Imaging.ImageFormat.Jpeg);
    ms.Position = 0;
    pic.Data = ByteVector.FromStream(ms);
    file.Tag.Pictures = new IPicture[] { pic };
    file.Save();
    file.Dispose();
}
```

## 贡献

欢迎大家提出改进建议和贡献代码，帮助完善这个工具。

## 许可证

本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[MP3封面添加工具使用指南](https://pan.quark.cn/s/1cf50864983c)