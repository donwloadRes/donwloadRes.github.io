---
layout: post
title: "树莓派舵机控制1"
date:   2021-06-03
tags: [GPIO,舵机,树莓,pin,pwm]
comments: true
author: admin
---
# 树莓派舵机控制1

## 资源描述

本资源文件提供了树莓派控制舵机的详细接线方式和相关代码示例。通过本资源，您可以轻松实现树莓派对舵机的控制。

## 接线方式

1. **GND 连接**：将舵机的棕色线（或黑色线）连接至树莓派的 GND（pin #6）。
2. **5V 连接**：将舵机的红色线连接至树莓派的 5V（pin #2）。
3. **信号线连接**：将舵机的黄色线连接至树莓派的任意 GPIO 引脚。

## 注意事项

- 请确保接线正确，避免短路或错误连接导致设备损坏。
- 在接线前，请务必断开树莓派的电源，以确保安全。

## 代码示例

以下是一个简单的 Python 代码示例，用于控制舵机的角度：

```python
import RPi.GPIO as GPIO
import time

# 设置GPIO模式
GPIO.setmode(GPIO.BOARD)

# 设置GPIO引脚
servo_pin = 12  # 请根据实际连接的GPIO引脚进行修改
GPIO.setup(servo_pin, GPIO.OUT)

# 设置PWM频率
pwm = GPIO.PWM(servo_pin, 50)  # 50Hz
pwm.start(0)

try:
    while True:
        # 设置舵机角度为0度
        pwm.ChangeDutyCycle(2.5)
        time.sleep(1)
        
        # 设置舵机角度为90度
        pwm.ChangeDutyCycle(7.5)
        time.sleep(1)
        
        # 设置舵机角度为180度
        pwm.ChangeDutyCycle(12.5)
        time.sleep(1)
        
except KeyboardInterrupt:
    pwm.stop()
    GPIO.cleanup()
```

## 使用说明

1. 将代码复制到树莓派上，并保存为 `.py` 文件。
2. 根据实际连接的 GPIO 引脚修改代码中的 `servo_pin` 变量。
3. 运行代码，观察舵机的运动情况。

## 其他资源

- 如需更多关于树莓派和舵机控制的资料，请参考相关文档或教程。

---

希望本资源对您有所帮助！如有任何问题，欢迎随时联系。

## 下载链接

[树莓派舵机控制1分享](https://pan.quark.cn/s/399b085524b5)