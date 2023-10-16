---
    layout: post
    title: "A Watermark for Large Language Models"
    a: Zongwei Wang
    categories: [NLP]
    image: assets/images/zongwei20231016.jpg
---
**大型语言模型的潜在危害可以通过对模型输出加水印来减轻，即将信号嵌入到生成的文本中，这些信号对人类来说是不可见的，但可以通过算法从短跨度的令牌中检测到。 作者提出了一个用于专有语言模型的水印框架。 水印的嵌入对文本质量的影响可以忽略不计，并且可以使用高效的开源算法进行检测，而无需访问语言模型 API 或参数。 

**水印的工作原理是在生成单词之前选择一组随机的“绿色”标记，然后在采样期间温和地促进绿色标记的使用。 作者提出了一种用于检测具有可解释的 p 值的水印的统计测试，并导出了用于分析水印敏感性的信息论框架。 

**作者使用开放式预训练变压器 (OPT) 系列中的数十亿参数模型来测试水印，并讨论鲁棒性和安全性。


[PPT](https://github.com/DMML-CQU/DMML-CQU.github.io/blob/main/assets/ppt/A%20Watermark%20for%20Large%20Language%20Models.pptx)
