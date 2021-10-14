---
layout:      post
title:      ".py | Fedora 上安装 CPU 版 pytorch"
keywords:   "md"
excerpt:    "import torch"
date:        2021-09-23
categories:  post
---

马上要参加一个暑期学校，关于深度学习在显微图像处理当中的应用。

深度学习是机器学习的一个分支，机器学习中的绝大多数数据都可以抽象为向量（一阶张量），绝大多数的算法都可以分解为向量之间的运算，或者对向量的变换，表示为矩阵（二阶张量）。这就对张量计算相关算法的库函数产生了很大的需求。PyTorch 和 TensorFlow，还有其他的一些库，比如 Keras，Caffe 等等等等，都是为此而生。早期版本的 pytorch 和 tensorflow 有很大的区别，但是随着版本的迭代，两者逐渐兼并和挤掉了其他的竞争者，两者的相似之处也越来越多，“变成了自己曾经最讨厌的样子”。lol

不知道课上究竟要使用哪种机器学习的框架，所以决定把 PyTorch 和 TensorFlow 全都安装了（摊手）。正好可以接着上一篇的 [python 教程]({% post_url 2021-06-29-python-interpreter-editor-virtualenv %}) 往下写。

先说一下自己的软硬件环境：Intel 家的 CPU 和集成显卡（玩不了《文明6》）。虽然不在官方支持 Linux 的名单上，但是自己安装了 Fedora，内核更新了几次之后已经没有了兼容性问题。python 版本 3.9.6，包管理器是 pip，编辑器是 vscode。

## 建立虚拟环境

为什么要建立虚拟环境的问题本系列的前一篇已经回答过了，这次直接开干。我给两个虚拟环境分别取名为 `torch` 和`tf` 。关于命令行部分的代码，为了表示各个虚拟环境，特别加上了命令提示符`(env)[me@mycomputer]$`，抄代码的时候注意去掉。

```bash

[me@mycomputer]$ mkvirtualenv torch
(torch)[me@mycomputer]$
```

## 安装

在 PyTorch 官网，找到自己的硬件配制对应的安装命令：[https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)。比如我的就是 `Stable`>`Linux`>`Pip`>`Python`>`CPU`。把生成的命令复制到命令行：

```bash

(torch)[me@mycomputer]$ pip3 install torch==1.9.1+cpu torchvision==0.10.1+cpu torchaudio==0.9.1 -f https://download.pytorch.org/whl/torch_stable.html
```

等待各种提示信息显示安装完成。

## 验证和退出

按照 [官网给出的方法](https://pytorch.org/get-started/locally/#linux-verification)，验证安装是否成功：

```python

import torch
x = torch.rand(5, 3)
print(x)

# tensor([[0.3799, 0.4494, 0.4296],
#       [0.5800, 0.0180, 0.3110],
#       [0.9847, 0.0125, 0.2648],
#       [0.0296, 0.3142, 0.9266],
#       [0.3192, 0.9645, 0.5545]])
```

为了下一步安装 tensorflow，先要退出到默认的虚拟环境：

```bash

(torch)[me@mycomputer]$ deactivate
[me@mycomputer]$
```

## 说好的 TensorFlow 呢

本来这篇文章是打算把  pytorch 和 tensorflow 一起写了，结果 tensorflow 实在是不给力。

- 直接安装

在 [TensorFlow 的官网](https://www.tensorflow.org/install)上方导航栏找到 install 按钮，然后在页面左侧找到 package/pip，[安装命令](https://www.tensorflow.org/install/pip#3.-install-the-tensorflow-pip-package)也是只有一句话

```python

pip install --upgrade tensorflow
```

然而不行，虽然安装过程中没有报错，但是验证安装的时候报出一堆错误。

报错信息里有一句 `Could not load dynamic library 'libcudart.so.11.0'`，怀疑上面命令安装的是 GPU 版本。

- 安装 CPU 版本

在网页正文的“Package Location”一节找到了 CPU 版本的安装文件：`https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow_cpu-2.6.0-cp39-cp39-manylinux2010_x86_64.whl`，于是删除虚拟环境、重建虚拟环境、重新安装。

```bash

(tf)[me@mycomputer]$ deactivate
[me@mycomputer]$ rmvirtualenv tf
[me@mycomputer]$ mkvirtualenv tf
(tf)[me@mycomputer]$ pip install --upgrade pip
(tf)[me@mycomputer]$ pip install https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow_cpu-2.6.0-cp39-cp39-manylinux2010_x86_64.whl
```

运行官方提供的测试之后依然会有警告信息：

```bash

(tf) [shixing@yoga-laptop ~]$ python -c "import tensorflow as tf;print(tf.reduce_sum(tf.random.normal([1000, 1000])))"
20XX-XX-XX XX:XX:XX.XXXXXX: I tensorflow/core/platform/cpu_feature_guard.cc:142] This TensorFlow binary is optimized with oneAPI Deep Neural Network Library (oneDNN) to use the following CPU instructions in performance-critical operations:  AVX2 AVX512F FMA
To enable them in other operations, rebuild TensorFlow with the appropriate compiler flags.
tf.Tensor(-1338.4773, shape=(), dtype=float32)
```

[stackoverflow 的这个回答](https://stackoverflow.com/questions/47068709/your-cpu-supports-instructions-that-this-tensorflow-binary-was-not-compiled-to-u) 说，需要从源码编译 tensorflow，具体的方法在[官网也有](https://www.tensorflow.org/install/source#linux)，但是实在是太麻烦了，~~（还是鸽了）~~ 下次单独写成一篇吧。