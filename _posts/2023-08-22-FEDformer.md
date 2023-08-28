---
layout: post
title:  "FEDformer: Frequency Enhanced Decomposed Transformer for Long-term Series Forecasting"
author: 王顺楠
categories: [ 时间序列 ]
image: assets/images/FEDformer.png
---

FEDformer (Frequency Enhanced DecomposedTransformer )设计了两个注意模块，分别用傅里叶变换和小波变换处理频域中的注意操作。 通过傅里叶变换中的随机模式部分实现线性复杂度。 自 Autoformer 和 FEDformer ，时间序列在频域的独特属性引起了关注。

傅立叶变换和逆傅立叶变换可以将信号在**时域**和**频域**之间相互转换。

作者提出将Transformer和傅里叶变换相结合，取代以往将Transformer应用于时间特征提取，改为使用Transformer对傅里叶变换后的频域数据进行特征提取。然而时域数据转化为频域数据带来的是大量的频率分量，是否针对所有数据进行特征提取或者如何选择这些分量将是一个问题。

一般想法：

- **使用所有频率分量：**虽然数据一点**不会丢失**，但会带来的将是**冗余**的信息资源、庞大的机器和时间开销以及过拟合的风险，因此不适用于对所有数据进行特征提取。

- **使用部分高频分量：**高频分量代表时间序列中**变化的突变型特征**，过度地对高频分量进行特征提取，或许模型最终学习到更多噪声的内容，而难以关注时间序列本身。

- **使用部分低频分量：**低频分量较为平缓，而时间序列中趋势的变化往往与重要事件的发生有关，缺少了高频分量对趋势的影响，时间序列将**不具个性**，预测的意义也大大降低。

作者的做法：

- **随机选择分量：**作者通过论证得到随机选取分量更有效，大大降低了复杂度。

### 注意力改进

分解模块增加了FEB(绿色，相当于self-attention机制)和FEA(红色，相当于cross attention)在频域进行表示学习

![](https://raw.githubusercontent.com/biya0105/biya0105.github.io/main/assets/images/FEDformer2.png)

### contributions

1. 为了捕捉时间序列的全局特性，提出了基于混合专家(mixture of experts)的频率增强分解的Transformer结构来进行季节趋势分解。

2. 提出傅立叶增强块和小波增强块，通过频域映射捕获重要结构，代替自我注意和交叉注意。

3. 随机选择固定数量的傅里叶分量，该模型实现了线性计算复杂度和存储成本。
