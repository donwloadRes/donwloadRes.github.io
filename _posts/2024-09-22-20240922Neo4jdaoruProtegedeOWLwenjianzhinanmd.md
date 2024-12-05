---
layout: post
title: "Neo4j导入Protege的OWL文件指南"
date:   2020-10-25
tags: [Neo4j,OWL,导入,文件,Protege]
comments: true
author: admin
---
# Neo4j导入Protege的OWL文件指南

本文档旨在提供一个详细的指南，帮助用户将Protege导出的OWL文件导入到Neo4j数据库中。通过本指南，您将了解如何准备OWL文件、配置Neo4j环境以及执行导入操作。

## 目录
1. [前言](#前言)
2. [Protege导出OWL文件](#protege导出owl文件)
3. [Neo4j导入OWL文件](#neo4j导入owl文件)
4. [两种导入方法对比](#两种导入方法对比)
5. [总结](#总结)

## 前言
Protégé软件是斯坦福大学医学院生物信息研究中心基于Java语言开发的本体编辑和知识获取软件，而Neo4j是一个高性能的图形数据库。本文将介绍如何将Protege中的本体以图的形式在Neo4j中展示。

## Protege导出OWL文件
参考相关教程，Protege导出的OWL文件格式为‘RDF/XML’。您可以直接导出该类型文件，其他类型文件未测试。

## Neo4j导入OWL文件
### 3.1 下载相关jar包
1. 下载扩展neosemantics jar包，并将其复制到neo4j/plugins目录下。
2. 确保neosemantics jar包与Neo4J版本相匹配。
3. 修改配置文件：在neo4j/neo4j.conf文件中添加以下内容：
   ```
   dbms.unmanaged_extension_classes=semantics.extension=/rdf
   ```
4. 重新启动Neo4j。
5. 访问web端Neo4j并登录，查看列表中是否包含可扩展的rdf、owl。

### 3.2 两种导入方法对比
#### 方法一：直接导入OWL文件（不可取）
- 导入命令：
  ```
  CALL semantics.liteOntoImport('file:///C:/Users/user/Desktop/creature.owl', 'RDF/XML')
  ```
- 结果：只成功加载了19个元素，无实例。

#### 方法二：将OWL文件转换成RDF文件再导入
1. 使用rdf2rdf-1.0.1-2.3.1.jar包将OWL文件转换成RDF文件。
2. 导入命令：
   ```
   CALL semantics.importRDF('file:///C:/Users/user/Desktop/creature.turtle', 'RDF/XML', [])
   ```
3. 结果：虽然能将实例导入，但原OWL文件的实例与所属类的关系不存在，实例的属性信息不存在，会多出几个不被需要的节点。

## 总结
综上所述，第二种方法更可靠一些，但也并不完美，还需人工操作Neo4j以达到预期图库。掌握了规律会使工作更流畅。

希望本指南对您有所帮助！

## 下载链接

[Neo4j导入Protege的OWL文件指南](https://pan.quark.cn/s/c89512dd79a4)