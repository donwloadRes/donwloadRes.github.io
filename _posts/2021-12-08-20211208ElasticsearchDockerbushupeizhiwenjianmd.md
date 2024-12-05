---
layout: post
title: "Elasticsearch Docker 部署配置文件"
date:   2020-05-09
tags: [配置文件,Elasticsearch,elasticsearch,xingyue,Docker]
comments: true
author: admin
---
# Elasticsearch Docker 部署配置文件

## 资源文件介绍

该资源文件名为 `elasticsearch.yml`，用于在 Docker 环境中部署 Elasticsearch 7.16.3 版本。此配置文件适用于正式环境，特别注意在正式环境中不设置堆大小，但需要设置一些系统参数以确保 Elasticsearch 的正常运行。

## 配置文件内容

以下是配置文件的主要内容和相关说明：

```yaml
# 正式环境配置不设置堆大小
# 需要设置下面的参数
# sysctl -w vm.max_map_count=262144
```

## Docker 运行命令

使用以下 Docker 命令来启动 Elasticsearch 容器，并挂载配置文件和数据目录：

```bash
docker run --name elasticsearch7.16.3 \
  -p 127.0.0.1:9200:9200 \
  -p 127.0.0.1:9300:9300 \
  -e discovery.type=single-node \
  -v /Users/xingyue/Home/xingyue/学习/工程化/es/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml \
  -v /Users/xingyue/Home/xingyue/学习/工程化/es/data:/usr/share/elasticsearch/data \
  -v /Users/xingyue/Home/xingyue/学习/工程化/es/config:/usr/share/elasticsearch/config \
  -v /Users/xingyue/Home/xingyue/学习/工程化/es/logs:/usr/share/elasticsearch/logs \
  elasticsearch:7.16.3
```

## 注意事项

1. **系统参数设置**：在正式环境中，需要设置系统参数 `vm.max_map_count` 为 `262144`，以确保 Elasticsearch 的正常运行。可以通过以下命令进行设置：
   ```bash
   sysctl -w vm.max_map_count=262144
   ```

2. **挂载目录**：确保挂载的目录路径正确，并且具有适当的权限，以便 Elasticsearch 能够读取和写入数据。

3. **端口映射**：本配置文件将 Elasticsearch 的 HTTP 端口 `9200` 和传输端口 `9300` 映射到本地的 `127.0.0.1`，确保在访问时使用正确的地址。

## 使用说明

1. **下载配置文件**：下载 `elasticsearch.yml` 配置文件到本地。
2. **修改路径**：根据实际情况修改 Docker 运行命令中的挂载路径。
3. **启动容器**：使用上述 Docker 命令启动 Elasticsearch 容器。

通过以上步骤，您可以在 Docker 环境中成功部署 Elasticsearch 7.16.3，并使用自定义的配置文件进行配置。

## 下载链接

[ElasticsearchDocker部署配置文件](https://pan.quark.cn/s/cba50f4e7d9f)