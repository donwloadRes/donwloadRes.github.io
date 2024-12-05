---
layout: post
title: "Linux 服务器中提高CPU使用率脚本"
date:   2022-02-05
tags: [press,etc,使用率,CPU,bash]
comments: true
author: admin
---
# Linux 服务器中提高CPU使用率脚本

## 简介

本仓库提供了一个用于在Linux服务器中提高CPU使用率的脚本。通过使用该脚本，您可以定时启动任务，将CPU使用率控制在指定的范围内，并持续运行指定的时间。

## 资源文件说明

### 文件列表

- `press_v3.1.sh`: 主脚本文件，用于控制CPU使用率。
- `README.md`: 本说明文件。

### 使用步骤

1. **创建存放脚本文件目录**

   ```bash
   mkdir -p /etc/press
   chmod 777 /etc/press
   ```

2. **启动定时任务进程**

   ```bash
   echo "systemctl start crond.service" >> /etc/rc.d/rc.local
   ```

3. **将定时任务策略输入至定时任务进程中**

   每天18点启动一次，执行 `/etc/press/press_v3.1.sh` 文件，设置CPU使用率为31-36之间，执行时间为24小时（86400秒）。

   ```bash
   echo "30 15 * * *  /bin/bash  /etc/press/press_v3.1.sh -c=31 -t=86400" >> /etc/crontab
   ```

4. **使用命令启动定时任务**

   ```bash
   crontab /etc/crontab
   systemctl restart crond.service
   ```

5. **部署成功后查看当前使用率**

   ```bash
   top -n 1 | grep Cpu | awk '{print "当前CPU使用率: "$2"%"}'
   ```

## 注意事项

- 请确保将压缩包中的两个文件（`press_v3.1.sh` 和 `README.md`）放入目录 `/etc/press` 中。
- 部署成功后，您可以使用 `top` 命令查看当前CPU使用率。

## 贡献

如果您有任何改进建议或发现了问题，欢迎提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅 `LICENSE` 文件。

## 下载链接

[Python爬虫入门实例教程](https://pan.quark.cn/s/5a3d1c9f3b81)