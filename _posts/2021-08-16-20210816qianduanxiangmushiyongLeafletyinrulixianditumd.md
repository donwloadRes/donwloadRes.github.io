---
layout: post
title: "前端项目使用Leaflet引入离线地图"
date:   2023-08-16
tags: [地图,Leaflet,map,离线,下载]
comments: true
author: admin
---
# 前端项目使用Leaflet引入离线地图

## 简介

本资源文件提供了一个前端项目中使用Leaflet库引入离线地图的完整解决方案。通过本资源，您可以学习如何在项目中下载瓦片地图、将瓦片地图静态文件放置在服务器上，并使用Leaflet库在前端代码中初始化地图。

## 主要步骤

### 1. 下载瓦片地图

1. **下载工具**：使用MapDownloader工具下载瓦片地图。需要对工具进行配置，保存后运行MapDownloader.exe文件。
2. **开始下载瓦片地图**：选择MySQL数据库，选择要下载地图的地方，根据需求选择地图，然后选择数据库下载。导出位置已经在上面配置，最后双击地图选择下载的等级进行下载。
3. **生成静态的图片文件放在服务器**：使用GISMysqlToLocal工具导出一个文件夹，里面文件是有规律的数字，从1开始。

### 2. 在前端代码中使用地图

1. **引入Leaflet**：可以使用CDN或通过npm安装Leaflet库。
   ```html
   <link rel="stylesheet" href="https://unpkg.com/leaflet@1.4.0/dist/leaflet.css" />
   <script src="https://unpkg.com/leaflet@1.4.0/dist/leaflet.js"></script>
   ```
2. **初始化地图**：在生命周期中节点生成后，通过id选择一个节点进行初始化。
   ```html
   <body>
     <div id="map" style="width:90%; height:600px; margin-top:30px; text-align:center; margin:0 auto;"></div>
     <script type="text/javascript">
       window.onload = function () {
         var map = L.map('map').setView([22.56414255434805, 114.153442382813], 11);
         L.tileLayer('/img/788865972/[z]/[x]/[y].png', {
           minZoom: 10,
           maxZoom: 12,
           attribution: '<b style="color:#dddddd">百度地图</b>'
         }).addTo(map);
       };
     </script>
   </body>
   ```

## 注意事项

- 全局引入Leaflet时，最好直接使用npm安装，并确保引入Leaflet的CSS文件，否则地图碎片会乱飘。
- 地图瓦片文件导入时，文件名必须按规律命名。
- 打点、标记、图层的使用必须在地图节点挂载之后进行。

## 适用场景

本资源适用于需要在网络受限环境下展示地图、打点、显示等操作的前端项目。通过本资源，您可以轻松实现离线地图的引入和展示。

## 作者

芝芝葡萄

## 版权声明

本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[前端项目使用Leaflet引入离线地图分享](https://pan.quark.cn/s/213413654ed5)