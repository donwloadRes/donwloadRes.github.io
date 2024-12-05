---
layout: post
title: "Java获取IP地址及对应的归属地"
date:   2024-05-27
tags: [IP地址,xdb,ip2region,查询,获取]
comments: true
author: admin
---
# Java获取IP地址及对应的归属地

## 简介

本资源文件提供了一个Java工具类，用于获取访问用户的IP地址及其对应的归属地信息。该工具类基于Java开发，适用于Spring框架，能够帮助开发者快速实现IP地址的获取和归属地查询功能。

## 功能特点

1. **获取IP地址**：通过HttpServletRequest对象获取用户的IP地址。
2. **IP归属地查询**：使用Ip2region库，通过IP地址获取对应的省份、城市等信息。
3. **多种查询方式**：支持基于文件查询、缓存VectorIndex索引、缓存整个xdb数据等多种查询方式，以满足不同场景的需求。

## 使用方法

### 1. 引入Maven依赖

在项目的`pom.xml`文件中添加以下依赖：

```xml
<dependency>
    <groupId>org.lionsoul</groupId>
    <artifactId>ip2region</artifactId>
    <version>2.6.4</version>
</dependency>
```

### 2. 下载ip2region.xdb文件

将`ip2region.xdb`文件放置在项目的`resources`目录下，或者根据实际路径进行配置。

### 3. 实现IP地址获取及归属地查询

参考以下代码示例，实现IP地址的获取及归属地查询：

```java
import lombok.extern.slf4j.Slf4j;
import org.apache.commons.lang3.StringUtils;
import org.lionsoul.ip2region.xdb.Searcher;
import java.util.concurrent.TimeUnit;

@Slf4j
public class IpAddressUtil {
    // ip2region.xdb文件路径
    public static String XDB_PATH = "D:\\IDEA2022.2.3\\workspace\\java\\src\\main\\resources\\ip\\ip2region.xdb";

    /**
     * 基于文件查询IP归属地
     */
    public static String getIpPossessionByFile(String ip) {
        if (StringUtils.isNotEmpty(ip)) {
            try {
                Searcher searcher = Searcher.newWithFileOnly(XDB_PATH);
                long sTime = System.nanoTime();
                String region = searcher.search(ip);
                long cost = TimeUnit.NANOSECONDS.toMicros(System.nanoTime() - sTime);
                region = region.replace("|0", "");
                log.info("[地区: {}  IO操作数: {}  耗时: {} μs]", region, searcher.getIOCount(), cost);
                return region;
            } catch (Exception e) {
                log.error("获取IP地址异常：{} ", e.getMessage());
                throw new RuntimeException("获取IP地址异常");
            }
        }
        return "未知";
    }
}
```

### 4. 其他查询方式

- **缓存VectorIndex索引**：预先加载VectorIndex缓存，减少IO操作。
- **缓存整个xdb数据**：将整个xdb文件加载到内存，实现完全基于内存的查询。

## 注意事项

- 在并发场景下，每个线程需创建独立的Searcher对象。
- 根据实际需求选择合适的查询方式，以优化查询性能。

## 参考资料

- Ip2region GitHub项目：[https://github.com/lionsoul2014/ip2region](https://github.com/lionsoul2014/ip2region)

## 许可证

本项目遵循CC 4.0 BY-SA版权协议，详情请参考LICENSE文件。

## 下载链接

[Java获取IP地址及对应的归属地](https://pan.quark.cn/s/4e6b63871a60)