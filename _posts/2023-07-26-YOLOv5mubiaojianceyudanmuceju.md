---
layout: post
title: "YOLOv5目标检测与单目测距"
date:   2021-03-24
tags: [YOLOv5,检测,单目,cv2,distance]
comments: true
author: admin
---
# YOLOv5目标检测与单目测距

## 简介

本仓库提供了一个基于YOLOv5的目标检测与单目测距的资源文件。通过该资源文件，您可以实现对车辆的实时测距，并且可以根据需要替换为自己的模型来检测其他物体。

## 功能特点

- **YOLOv5目标检测**：利用YOLOv5模型进行高效的目标检测，能够实时识别图像或视频中的车辆。
- **单目测距**：结合目标检测结果，通过单目摄像头实现对检测到的车辆的距离测量。
- **模型替换**：支持替换YOLOv5模型，以便检测其他类型的物体，如行人、交通标志等。

## 使用方法

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo-url.git
   cd your-repo-directory
   ```

2. **安装依赖**：
   ```bash
   pip install -r requirements.txt
   ```

3. **运行程序**：
   ```bash
   python main.py
   ```

4. **替换模型**（可选）：
   如果您希望检测其他物体，可以将YOLOv5模型替换为您自己训练的模型，并相应地修改配置文件。

## 示例

以下是一个简单的示例，展示了如何使用该资源文件进行车辆检测与测距：

```python
import cv2
from yolov5_detector import YoloV5Detector
from distance_calculator import DistanceCalculator

# 初始化检测器和测距器
detector = YoloV5Detector()
distance_calculator = DistanceCalculator()

# 读取视频流
cap = cv2.VideoCapture('video.mp4')

while cap.isOpened():
    ret, frame = cap.read()
    if not ret:
        break

    # 检测车辆
    detections = detector.detect(frame)

    # 计算距离
    for detection in detections:
        distance = distance_calculator.calculate(detection)
        print(f"车辆距离: {distance} 米")

    # 显示结果
    cv2.imshow('Frame', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

## 贡献

欢迎大家贡献代码、提出问题或建议。如果您有任何改进的想法，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

---

希望这个README文件能够帮助您更好地理解和使用本仓库中的资源文件。如果您有任何问题，请随时联系我们！

## 下载链接

[YOLOv5目标检测与单目测距](https://pan.quark.cn/s/8d8faf560d20)