---
layout: post
title: "超算集群下编译 VASP  VTST 指南"
date:   2024-02-25
tags: [VASP,VTST,编译,集群,超算]
comments: true
author: admin
---
# 超算集群下编译 VASP + VTST 指南

本文档提供了在超算集群下编译 VASP 和 VTST 的详细步骤。VASP 是一款广泛使用的第一性原理计算软件，而 VTST 是 VASP 的一个扩展工具，提供了多种过渡态计算方法。以下是编译过程的详细说明。

## 前提条件

1. **超算集群访问权限**：确保你已经获得了超算集群的访问权限，并且熟悉基本的集群操作。
2. **VASP 和 VTST 源码**：下载 VASP 和 VTST 的源码包，并上传到集群的指定目录。

## 编译步骤

### 1. 解压源码包

首先，解压上传的 VASP 和 VTST 源码包：

```bash
tar -zxvf vasp.5.4.4.tar.gz
gunzip vtstcode-179.gz
```

### 2. 打补丁

如果使用的是 VASP 5.4.4 版本，需要打补丁：

```bash
cp patch.5.4.4.16052018 /vasp.5.4.4
cd /vasp.5.4.4
patch -p0 < patch.5.4.4.16052018
```

### 3. 修改源码

#### 修改 `src/main.F` 源码

在 `src/main.F` 文件中，找到以下代码并进行修改：

```fortran
CALL CHAIN_FORCE(T_INFO%NIONS, DYN%POSION, TOTEN, TIFOR, &
                 LATT_CUR%A, LATT_CUR%B, IO%IU6)
```

修改为：

```fortran
CALL CHAIN_FORCE(T_INFO%NIONS, DYN%POSION, TOTEN, TIFOR, &
                 TSIF, LATT_CUR%A, LATT_CUR%B, IO%IU6)
```

#### 修改编译配置

在 `src/objects` 文件中，在 `chain.o` 前添加以下内容：

```bash
bfgs.o dynmat.o instanton.o lbfgs.o sd.o cg.o dimer.o bbm.o \
fire.o lanczos.o neb.o qm.o opt.o \
```

### 4. 编译 VASP

加载必要的编译库并进行编译：

```bash
module avail
module load apps/vasp/intelmpi/5.4.1
module load mpi/intelmpi/2017.4.239
make all
```

编译完成后，检查生成的可执行文件：

```bash
ls /bin
```

如果显示 `vasp_gam`, `vasp_ncl`, `vasp_std`，则编译成功。

## 结束语

至此，你已经成功在超算集群下编译了 VASP 和 VTST。接下来，你可以提交脚本进行计算模拟。注意，运行脚本时需要加载自己用户下的 `vasp_std`，以避免使用集群默认的版本。

希望本文档对你有所帮助！

## 下载链接

[超算集群下编译VASPVTST指南](https://pan.quark.cn/s/0b48bdd41b16)