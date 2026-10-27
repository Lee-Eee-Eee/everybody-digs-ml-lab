# Everybody Digs ML · 交互学习室

[English](README.en.md) · [打开学习室](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/) · [配套课程](https://github.com/Lee-Eee-Eee/everybody-digs-ml)

**改变一个参数，看看数字怎样沿计算图变化。**

这是 [Everybody Digs ML](https://github.com/Lee-Eee-Eee/everybody-digs-ml) 的浏览器交互学习室。18 节实验从一个两层小网络出发，逐步追踪前向计算、反向传播和参数更新，再探索批量训练、Softmax、优化、卷积和残差。图形、数值和训练都在浏览器中计算。

> 先猜结果 → 调整参数 → 追踪计算 → 用小题检查理解。

## 立即体验

**如果输入为零，改变它所连接的权重会影响输出吗？**

1. [打开第一节](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#network)，调整输入 `x₁` 和权重 `w₁₁`。
2. 分别用 `x₁ = 0` 和 `x₁ = 0.6` 改变权重，比较乘积、隐藏节点和预测。
3. 继续进入下一节，逐步展开乘法、求和和 Sigmoid；再回到[配套课程第 04 课](https://github.com/Lee-Eee-Eee/everybody-digs-ml/blob/main/lessons/neural_network_basics/04_derivatives_numpy_mlp.ipynb)，用 NumPy 写出反向传播。

无需注册或安装即可在线使用。学习进度保存在当前浏览器的本地存储中；清除浏览器站点数据会清除进度。

## 18 节实验

| 阶段 | 实验 | 可以观察什么 |
| --- | --- | --- |
| 01–02 | [认识网络里的数](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#neuron) · [乘法、求和与激活](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#chain) | 输入、权重、加权和与激活函数 |
| 03–06 | [完整前向](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#paths) · [损失怎样传回](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#forward) · [分支相加](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#output) · [梯度与更新](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#hidden) | 修改输入、权重和目标，沿路径计算预测、梯度和更新 |
| 07–08 | [共用权重](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#matrix) · [Softmax](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#softmax) | 样本梯度怎样汇合，共同平移如何影响概率 |
| 09–13 | [激活与梯度](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#activations) · [初始化](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#initialization) · [真实训练](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#training) · [优化器](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#optimizers) · [容量](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#capacity) | 改变深度、尺度、激活或优化器，比较曲线和决策边界 |
| 14–15 | [残差](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#residual) · [堆叠残差块](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#deep-residual) | 对照捷径和分支，查看梯度与训练表现 |
| 16–18 | [卷积](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#convolution) · [BN 与 Dropout](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#regularization) · [实验与研究](https://lee-eee-eee.github.io/everybody-digs-ml-lab/interactive/#synthesis) | 编辑输入和核，查看归一化及训练、验证对照 |

学习室界面以中文为主；[English guide](README.en.md) 提供英文导航。完整推导、可填写练习和模型训练 Notebook 位于[配套课程](https://github.com/Lee-Eee-Eee/everybody-digs-ml)。

## 离线运行

克隆本仓库，保留 `interactive/` 文件夹的结构，然后在浏览器中打开 `interactive/index.html`。也可直接打开无需其他脚本文件的 [单文件版](interactive/neural-network-lab.html)。浏览器须启用 JavaScript。

```bash
git clone https://github.com/Lee-Eee-Eee/everybody-digs-ml-lab.git
cd everybody-digs-ml-lab
```

数学渲染脚本随仓库提供；实验计算不需要后端服务。课程 Notebook 链接指向配套课程仓库，离线时可阅读已下载的课程副本。

## 维护与验证

```bash
# 数值检查：有限差分、优化器、卷积、归一化和章节声明（需要 Node.js）
node tools/check_interactive.cjs
# 从源码重建单文件版（需要 Python）
python interactive/build_standalone.py
```

`interactive/` 保存页面、实验声明、计算引擎和样式。对应的课程仓库保留了一个学习室副本，供课程本地离线使用。

## 致谢

感谢 [3Blue1Brown](https://www.3blue1brown.com/lessons/backpropagation/)、[Chris Olah](https://colah.github.io/posts/2015-08-Backprop/) 及相关论文提供的学习材料。页面使用 [MathJax](https://www.mathjax.org/)；其许可证保存在 [interactive/vendor/MathJax-LICENSE.txt](interactive/vendor/MathJax-LICENSE.txt)。
