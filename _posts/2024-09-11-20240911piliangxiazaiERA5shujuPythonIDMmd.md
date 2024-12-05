---
layout: post
title: "批量下载ERA5数据PythonIDM
date   20220402
tags 00ERA5IDM下载批量
comments true
author admin

 批量下载ERA5数据PythonIDM

 简介
本资源文件详细介绍了如何通过Python脚本结合Internet Download ManagerIDM软件实现对ERA5气候数据的批量下载ERA5是第五代ECMWF大气再分析全球气候数据提供了每小时的大气陆地和海洋气候变量的估计值通过本教程您可以高效地下载ERA5数据提高下载速度和效率

 准备工作
1 注册CDS帐号在Climate Data StoreCDS网站上注册帐号获取API key
2 配置并安装CDS API在本地配置CDS API安装cdsapi第三方库
3 安装和配置IDM软件安装Internet Download ManagerIDM并进行相关配置

 批量下载步骤
1 下载单个数据通过Python脚本创建下载任务利用CDSAPI获取下载链接
2 批量下载数据通过循环批量下载ERA5数据并使用IDM软件进行快速下载

 代码示例
以下是批量下载ERA5数据的Python代码示例

python
import cdsapi
import calendar
from subprocess import call

def idmDownloadertaskurl folderpath filename
     IDM下载器 
    idmengine  CProgram Files x86Internet Download ManagerIDManexe"
date:   2022-04-02
tags: [00,ERA5,IDM,下载,批量]
comments: true
author: admin
---
# 批量下载ERA5数据（Python+IDM）

## 简介
本资源文件详细介绍了如何通过Python脚本结合Internet Download Manager（IDM）软件，实现对ERA5气候数据的批量下载。ERA5是第五代ECMWF大气再分析全球气候数据，提供了每小时的大气、陆地和海洋气候变量的估计值。通过本教程，您可以高效地下载ERA5数据，提高下载速度和效率。

## 准备工作
1. **注册CDS帐号**：在Climate Data Store（CDS）网站上注册帐号，获取API key。
2. **配置并安装CDS API**：在本地配置CDS API，安装cdsapi第三方库。
3. **安装和配置IDM软件**：安装Internet Download Manager（IDM），并进行相关配置。

## 批量下载步骤
1. **下载单个数据**：通过Python脚本创建下载任务，利用CDSAPI获取下载链接。
2. **批量下载数据**：通过循环批量下载ERA5数据，并使用IDM软件进行快速下载。

## 代码示例
以下是批量下载ERA5数据的Python代码示例：

```python
import cdsapi
import calendar
from subprocess import call

def idmDownloader(task_url, folder_path, file_name):
    """ IDM下载器 """
    idm_engine = "C:\\Program Files (x86)\\Internet Download Manager\\IDMan.exe"
    call([idm_engine, '/d', task_url, '/p', folder_path, '/f', file_name, '/a'])
    call([idm_engine, '/s'])

if __name__ == '__main__':
    c = cdsapi.Client()
    dic = {
        'product_type': 'reanalysis',
        'format': 'netcdf',
        'variable': '2m_temperature',
        'year': '',
        'month': '',
        'day': [],
        'time': [
            '00:00', '01:00', '02:00', '03:00', '04:00', '05:00',
            '06:00', '07:00', '08:00', '09:00', '10:00', '11:00',
            '12:00', '13:00', '14:00', '15:00', '16:00', '17:00',
            '18:00', '19:00', '20:00', '21:00', '22:00', '23:00'
        ]
    }

    for y in range(1979, 2021):
        for m in range(1, 13):
            day_num = calendar.monthrange(y, m)[1]
            dic['year'] = str(y)
            dic['month'] = str(m).zfill(2)
            dic['day'] = [str(d).zfill(2) for d in range(1, day_num + 1)]
            r = c.retrieve('reanalysis-era5-single-levels', dic)
            url = r.location
            path = 'E:\\Data\\ERA5\\1979-2020\\2m_temperature'
            filename = str(y) + str(m).zfill(2) + '.nc'
            idmDownloader(url, path, filename)
```

## 注意事项
- 确保IDM软件已正确安装并配置。
- 不要更新IDM，否则可能会导致软件不可用。
- 本教程内容仅供学习参考，如有不足之处，敬请批评指正。

通过以上步骤，您可以轻松实现ERA5数据的批量下载，提高数据获取的效率。

## 下载链接

[批量下载ERA5数据PythonIDM分享](https://pan.quark.cn/s/5f88f041f769)