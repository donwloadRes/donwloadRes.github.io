---
layout: post
title: "Bootstrap 文件上传与图片处理指南"
date:   2020-02-06
tags: [上传,文件,script,Bootstrap,path]
comments: true
author: admin
---
# Bootstrap 文件上传与图片处理指南

欢迎使用此资源库，本仓库提供了详细的教程，专注于如何在你的Web项目中集成Bootstrap框架来优雅地实现文件，尤其是图片的上传功能。以下内容基于[CSDN博客上的文章](https://blog.csdn.net/little_code/article/details/122477139)，确保您能够在前端使用Bootstrap，并结合JavaScript，实现文件的选取、预览、上传至服务器，以及后端接收与存储逻辑。

## 快速入门

### 前端配置

首先，确保您的项目已包含了Bootstrap的CSS和JS文件。此外，您需要引入额外的插件——`bootstrap-fileinput.js`，以获得增强的文件上传界面和功能。基本引入方式如下：

```html
<link href="path/to/bootstrap.min.css" rel="stylesheet">
<script src="path/to/jquery.min.js"></script>
<script src="path/to/bootstrap.min.js"></script>
<!-- 引入文件输入插件 -->
<link href="path/to/fileinput.css" rel="stylesheet">
<script src="path/to/fileinput.js"></script>
<!-- 中文语言包，如果需要的话 -->
<script src="path/to/fileinput_locale_zh.js"></script>
```

### HTML 示例

创建文件上传的基本形式，如以下代码片段所示：

```html
<label for="file-1">图片上传：</label>
<input id="file-1" name="file" type="file" class="form-control" multiple/>
```

### JavaScript 初始化

通过jQuery选择器初始化文件上传控件，设定各项参数以满足具体需求：

```javascript
$("#file-1").fileinput({
    uploadUrl: '', // 上传接口地址
    allowedFileExtensions: ['jpg', 'png', 'gif', 'jpeg'], // 允许的文件类型
    overwriteInitial: false,
    language: 'zh', // 设置为中文界面
    maxFileSize: 1500, // 单位KB，限制文件大小
    uploadExtraData: {userid: "XXX"}, // 上传时携带的额外参数
    maxFilesNum: 10, // 最大可上传文件数
    previewSettings: {image: {width: "100px", height: "100px"}}, // 图片预览尺寸
    slugCallback: function(filename){return filename;} // 文件命名规则回调
}).on('filecleared', function(){}); // 文件清除事件处理
```

### 后端接口示例

假设您使用的是ASP.NET后端，以下是一个简单的文件接收处理示例：

```csharp
HttpFileCollection files = Request.Files;
if (files.Count > 0)
{
    foreach (string key in files.Keys)
    {
        HttpPostedFile fileData = files[key];
        if (fileData != null)
        {
            string folderPath = $"/UpFiles/{DateTime.Now:yyyy/MM/dd}/";
            string fileName = Guid.NewGuid().ToString() + Path.GetExtension(fileData.FileName);
            string filePath = Server.MapPath(folderPath) + fileName;
            
            if (!Directory.Exists(Server.MapPath(folderPath)))
                Directory.CreateDirectory(Server.MapPath(folderPath));
            
            fileData.SaveAs(filePath);
            // 返回文件保存成功的响应
            Response.Write($"[{\"info\":\"{folderPath + fileName}\", \"status\":\"ok\"}]");
            Response.End();
        }
    }
}
```

**注意:** 实际部署时，需确保上传接口的安全性，比如添加身份验证、防止恶意文件上传等安全措施。

以上就是使用Bootstrap进行文件和图片上传的简明指南。希望这能让您的项目快速拥有一个美观且实用的文件上传功能。

## 下载链接

[Bootstrap文件上传与图片处理指南](https://pan.quark.cn/s/aecfe10fb7fe)