---
layout: post
title: "threejs加载3D模型glb格式和gltf格式"
date:   2024-07-03
tags: [加载,模型,3D,gltf,glb]
comments: true
author: admin
---
# three.js加载3D模型（.glb格式和.gltf格式）

本仓库提供了一个使用three.js加载3D模型的示例代码，支持加载.glb和.gltf格式的模型文件。通过本示例，您可以快速了解如何在网页中使用three.js展示3D模型。

## 功能介绍

- **加载3D模型**：支持加载.glb和.gltf格式的3D模型文件。
- **实时展示**：在网页中实时展示加载的3D模型。
- **交互控制**：提供基本的模型旋转和缩放功能，用户可以通过鼠标或触摸操作模型。

## 使用方法

1. **下载仓库**：首先，您需要下载本仓库的代码到本地。
2. **配置模型路径**：在`index.html`文件中，找到`modelUrl`变量，将其值替换为您要加载的模型文件路径。
3. **运行项目**：使用浏览器打开`index.html`文件，即可看到加载的3D模型。

## 示例代码

以下是加载3D模型的核心代码示例：

```javascript
// 创建场景
var scene = new THREE.Scene();

// 创建相机
var camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
camera.position.z = 5;

// 创建渲染器
var renderer = new THREE.WebGLRenderer();
renderer.setSize(window.innerWidth, window.innerHeight);
document.body.appendChild(renderer.domElement);

// 加载模型
var loader = new THREE.GLTFLoader();
loader.load('model.glb', function (gltf) {
    scene.add(gltf.scene);
}, undefined, function (error) {
    console.error(error);
});

// 渲染场景
function animate() {
    requestAnimationFrame(animate);
    renderer.render(scene, camera);
}
animate();
```

## 注意事项

- 确保您的模型文件路径正确，否则模型将无法加载。
- 如果模型文件较大，加载时间可能会较长，请耐心等待。

## 贡献

如果您有任何改进建议或发现了bug，欢迎提交issue或pull request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[three.js加载3D模型.glb格式和.gltf格式分享](https://pan.quark.cn/s/5727cbaab154)