---
layout: post
title: "Kafka可视化管理工具kafkamanager部署安装和使用已更名为CMAK"
date:   2020-11-06
tags: [Kafka,集群,Topic,Manager,kafka]
comments: true
author: admin
---
# Kafka可视化管理工具kafka-manager部署安装和使用-已更名为CMAK

## 简介
Kafka Manager（现已更名为CMAK）是由Yahoo开源的一款基于Web的Kafka集群管理工具。它旨在简化开发者和服务工程师维护Kafka集群的工作，提供了一个直观的界面来管理和监控Kafka集群。Kafka Manager可以帮助用户轻松发现集群中哪些Topic分布不均匀，或者分区在整个集群中分布不均匀的情况。它支持管理多个Kafka集群、选择副本、副本重新分配以及创建Topic等功能。

## 功能特性
- **管理多个Kafka集群**：支持同时管理多个Kafka集群。
- **检查集群状态**：便捷地检查Kafka集群状态，包括Topics、Brokers、备份分布情况、分区分布情况等。
- **副本管理**：选择要运行的副本，进行副本重新分配。
- **创建和删除Topic**：支持创建和删除Topic，并可以为已存在的Topic增加分区或更新配置。
- **批量重分区**：支持在多个Topic上进行批量重分区操作。

## 安装步骤
1. **环境要求**：
   - JDK：OpenJDK 1.8.0_302
   - Kafka集群信息：例如192.168.131.171:9092, 192.168.131.171:9093, 192.168.131.171:9094
   - Zookeeper：Apache Zookeeper 3.5.9

2. **下载安装**：
   - 下载Kafka Manager的zip包，并上传到Linux服务器。
   - 解压zip包：`unzip kafka-manager-1.3.3.7.zip`

3. **配置修改**：
   - 修改配置文件`conf/application.conf`，将Zookeeper地址替换为自己的地址。
   - 例如：`kafka-manager.zkhosts="192.168.131.171:2181"`

4. **启动服务**：
   - 使用默认端口号启动：`nohup bin/kafka-manager -Dconfig.file=conf/application.conf &`
   - 启动后，可以通过浏览器访问`http://<服务器IP>:9000`来使用Kafka Manager。

## 使用说明
1. **添加集群**：
   - 点击【Cluster】>【Add Cluster】，输入集群名称和Zookeeper地址，选择Kafka版本，保存配置。

2. **管理Topic**：
   - 点击【Topic】>【Create】可以创建新的Topic。
   - 点击已存在的Topic名称，可以查看和管理该Topic的详细信息。

3. **监控集群**：
   - 通过Kafka Manager的Web界面，可以实时监控Kafka集群的状态，包括Brokers、Topics、分区分布等。

## 注意事项
- 如果Kafka集群中未配置JMX_PORT，请勿勾选“Enable JMX Polling”选项，否则Kafka Manager可能无法正常启动。
- 在删除Topic时，确保Kafka版本为0.8.2以上，并且在Broker配置中设置了`delete.topic.enable=true`。

通过Kafka Manager，用户可以更加高效地管理和监控Kafka集群，提升运维效率。

## 下载链接

[Kafka可视化管理工具kafka-manager部署安装和使用-已更名为CMAK分享](https://pan.quark.cn/s/7e553ca95637)