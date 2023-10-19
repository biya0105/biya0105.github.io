---
    layout: post
    title: "Cascading Residual Graph Convolutional Network for Multi-Behavior Recommendation"
    author: Yunhang Yao
    categories: [推荐系统]
    image: assets/images/CRGCN.png
---

# 主要问题

- 大多数现有的工作没有利用包含在不同行为之间的联系中的用户偏好信息，这些行为在真实场景中经常以一定的顺序发生，例如，查看->购物车->购买。而用户与物品交互的顺序行为往往揭示了用户对目标物品不同程度的偏好。

- 现有的多行为推荐往往是**独立地**对不同类型的行为进行建模，没有很好地利用不同行为之间的偏好依赖关系。只有少数方法试图对行为之间的依赖关系进行建模，但它们并没有显式地将连接信息纳入嵌入学习过程。

# 框架

![](https://raw.githubusercontent.com/dmml-cqu/dmml-cqu.github.io/main/assets/images/CRGCN.png)

本文提出了一种级联图卷积网络：

- 每个残差块学习一种行为特征，所有残差块通过级联结构共享基本特征。

- 为了保证模型的有效学习，将每个残差块的输出作为当前行为的预测任务。由于在级联结构中传递信息，在当前任务的训练过程中，既可以训练当前的残差块，也可以训练之前的残差块。

# 改进

第二篇论文在第一篇的基础上将多任务训练策略改成了单任务训练，同时去掉了残差块，将上一个模块学到的特征嵌入经过特征变换后传到下一个模块。



![](https://raw.githubusercontent.com/dmml-cqu/dmml-cqu.github.io/main/assets/images/MB-CGCN.png)

[PPT](https://github.com/DMML-CQU/DMML-CQU.github.io/blob/main/assets/ppt/20231017-Cascading%20Residual%20Graph%20Convolutional%20Network%20for%20Multi-Behavior%20Recommendation.pptx)

