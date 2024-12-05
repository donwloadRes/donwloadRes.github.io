---
layout: post
title: "百度网盘分享链接的提取码查询API"
date:   2022-08-27
tags: [API,百度网,链接,提取,分享]
comments: true
author: admin
---
# 百度网盘分享链接的提取码查询API

本资源文件提供了一个用于查询百度网盘分享链接提取码的API接口。通过该API，用户可以方便地获取百度网盘分享链接的提取码，从而简化下载过程。

## 功能介绍

- **API地址**: 提供了一个特定的URL，用户可以通过该URL查询百度网盘分享链接的提取码。
- **使用方法**: 用户只需在API地址后附加百度网盘分享链接，即可获取相应的提取码。
- **返回格式**: API返回的提取码信息以JSON格式呈现，包含提取码、链接状态等详细信息。

## 示例

假设百度网盘分享链接为：`https://pan.baidu.com/s/1FOX8GE1qQ0H9VK5M4nZeDQ`，

组合API地址后为：`https://nuexini.gq/bdp.php?url=https://pan.baidu.com/s/1FOX8GE1qQ0H9VK5M4nZeDQ`

返回的JSON文本中包含提取码信息，例如：
```json
{
  "_id": "5c59338a4b3f411eac7a6375",
  "type": "BDY",
  "pid": "FOX8GE1qQ0H9VK5M4nZeDQ",
  "invalid_count": 0,
  "state": "VALID",
  "updated_at": "2019-02-05 15:28:28",
  "created_at": "2019-02-05 14:56:10",
  "access_code": "rie7",
  "referrer": [
    {
      "0363d7f8c949b9b4d516e014d1f03dcf": {
        "url": "http://www.gscq.me/thread-10276.htm",
        "title": "[GSCQ][湖南卫视《歌手2019》第四期：齐豫洒泪唱《今世》忆三毛 波琳娜炸裂高音强势补位][1080I/TS][720P/MP4][6.96G+2.03G]-音乐/综艺-乐赏 GSCQ.ME"
      }
    }
  ]
}
```

## 注意事项

- 该API仅适用于已收录的百度网盘分享链接，未收录的链接无法查询提取码。
- 提取码区分大小写，输入时请确保正确。

## 更新日志

- **2024-09-13**: 发布最新版本，优化API查询速度和准确性。

## 联系我们

如有任何问题或建议，请联系我们。

## 下载链接

[百度网盘分享链接的提取码查询API分享](https://pan.quark.cn/s/2703d85b816b)