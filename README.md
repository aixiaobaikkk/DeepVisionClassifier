
# DeepVisionClassifier

## 概述

**DeepVisionClassifier** 是一个基于深度学习的图像分类仓库，提供了多个经典神经网络架构的实现，包括：

- AlexNet
- GoogleNet
- LeNet
- Mamba
- ResNet
- VGG

每个模型都包含专门的脚本，用于定义模型结构、在GPU上进行训练以及进行预测。

## 仓库结构

项目的目录结构如下：

```
DeepVisionClassifier/
│
├── AlexNet/
│   ├── calss_indices.json  # 类别索引映射
│   ├── model.py            # AlexNet 模型定义
│   ├── predict.py          # 预测脚本
│   └── train_gpu.py        # 基于GPU的训练脚本
│
├── GoogleNet/
│   ├── calss_indices.json  # 类别索引映射
│   ├── model.py            # GoogleNet 模型定义
│   ├── predict.py          # 预测脚本
│   └── train_gpu.py        # 基于GPU的训练脚本
│
├── LeNet/
│   ├── gpu_test.py         # 测试GPU兼容性的脚本
│   ├── model.py            # LeNet 模型定义
│   ├── predict.py          # 预测脚本
│   └── train_gpu.py        # 基于GPU的训练脚本
│
├── Mamba/
│   └── train_gpu.py        # 基于GPU的训练脚本
│
├── ResNet/
│   ├── calss_indices.json  # 类别索引映射
│   ├── model.py            # ResNet 模型定义
│   ├── predict.py          # 预测脚本
│   └── train_gpu.py        # 基于GPU的训练脚本
│
└── VGG/
    ├── calss_indices.json  # 类别索引映射
    ├── model.py            # VGG 模型定义
    ├── predict.py          # 预测脚本
    └── train_gpu.py        # 基于GPU的训练脚本
```

## 依赖项

要运行本项目，你需要以下依赖：

- Python 3.x
- PyTorch
- 支持CUDA的GPU（如果在GPU上训练）
- 其他依赖项见 `requirements.txt`

可以使用以下命令安装依赖：

```bash
pip install -r requirements.txt
```

## 使用方法

### 训练

要使用GPU训练某个模型，请进入对应的模型目录（如 `AlexNet`），并运行训练脚本：

```bash
cd AlexNet
python train_gpu.py
```

### 预测

要使用预训练模型进行预测，使用 `predict.py` 脚本。确保你已经加载了一个预训练的模型：

```bash
cd AlexNet
python predict.py --image_path /path/to/image.jpg
```

### 类别索引

每个模型目录中的 `calss_indices.json` 文件包含类别名称与索引的映射关系，该文件用于训练和预测阶段。

## 包含的模型

1. **AlexNet**：一个经典的卷积神经网络，用于图像分类。
2. **GoogleNet**：一个基于Inception架构的网络，旨在提高分类性能。
3. **LeNet**：早期的CNN架构之一，最初用于手写数字识别。
4. **Mamba**：基于SSM的长序列预测模型，效果有待验证。
5. **ResNet**：YYDS，深度残差网络，解决了深度网络中的梯度消失问题。
6. **VGG**：以其简洁和深度著称的网络，在图像分类任务中取得了出色的效果。


