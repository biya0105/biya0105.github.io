---
    layout: post
    title: "GraphCleaner: Detecting Mislabelled Samples in Popular Graph Learning Benchmarks"
    author: Hao Ma
    categories: [Detection]
    image: assets/images/mahao0927.png
---

- 数据是任何人工智能系统的主要输入，用于学习和评估。因此，认识到数据质量对于人工智能系统的成功至关重要，数据中心的人工智能在近年迅速崭露头角。数据中心人工智能的愿景是在项目生命周期的各个阶段确保干净和高质量的数据，并开发用于监测和改善数据质量的工具和流程。特别是在监督学习环境中，纠正标签噪声，包括错误标记和模糊标记的数据，因为标签在训练和评估过程中的关键重要性而成为高优先级的任务。

- 现有的标签错误检测解决方案是为通用数据上的机器学习而设计的，如图像、音频和文本，其中实例在很大程度上被视为相互独立的。然而，这意味着当在图设置中使用时，这些方法不能有效地利用节点及其邻居之间的密切依赖关系，这是图数据的一个关键特征。相比之下，我们方法的一个关键思想是，节点与其邻居之间依赖模式的严重违反作为一个重要信号，表明该节点更有可能被标记错误。

- GRAPHCLEANER结合了两种新颖的思想：1) 合成误标数据集生成，旨在生成逼真的误标；2) 考虑邻域的误标检测，其中在标签和基本分类器预测中都利用了邻域依赖关系.


[PPT](20230927-Detecting%20Mislabelled%20Samples%20in%20Popular%20Graph%20Learning%20Benchmarks.pptx)
