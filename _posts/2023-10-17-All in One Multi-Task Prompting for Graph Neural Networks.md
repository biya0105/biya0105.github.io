---
  layout: post
  title: "All in One Multi-Task Prompting for Graph Neural Networks"
  author: No One
  categories: [ graph neural network, prompt learning ]
  image: assets/images/AllinOne.jpg
  tags: [tags]
---

# 背景
1. 大语言模型的出色性能，仅用少量提示，就能适配下游任务
2. 图结构数据的学习难以运用到大模型中，如何利用少量提示，使得预训练图模型适配图相关下游任务，激发出预训练模型的性能
3. 大语言模型提示学习和预训练图结构模型提示学习的区别和关联,如何统一? (详见PPT )



# 本文解决的难点

1. 提示词如何构建、提示词的结构如何定义、如何与原图结合
2. 如何统一各种下游图任务，已有工作只能适配于其中一种
3. 少样本情况下，如何学习到能运用于快速适配到各种下游任务的初始嵌入



其余信息请见PPT:  

