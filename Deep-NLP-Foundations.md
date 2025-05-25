## 1.深度学习与 NLP 简介

  * **深度学习** ：作为机器学习的子领域，深度学习通过多层神经网络（如 CNN、RNN、Transformer）自动提取数据特征，广泛应用于计算机视觉（CV）、自然语言处理（NLP）等领域。推荐李沐《动手学深度学习》。
  * **NLP（自然语言处理）** ：专注于让计算机理解、生成人类语言，核心任务包括文本分类、机器翻译、对话系统等。

## 2.代码基础（Python&Pytorch）资料推荐
  * Python基础需要自学、需要掌握常见的数据类型、语句、以及其中的面向对象相关的特性。
  * Pytorch推荐B站**小土堆 PyTorch 教程**、**刘二大人**、**动手学习深度学习相关章节**：
    * 从环境配置（Anaconda + PyTorch）开始，逐步学习张量操作、模型搭建、训练流程等。.
    * 特点：代码简单直观，适合培养基础直觉，建议全程跟练。

参考 [小土堆深度学习入门](https://www.bilibili.com/video/BV1hE411t7RN/?spm_id_from=333.337.search-card.all.click)、[刘二大人Pytorch](https://www.bilibili.com/video/BV1Y7411d7Ys/?spm_id_from=333.337.search-card.all.click)

## 3.深度学习资料推荐

  * **李沐《动手学深度学习》** ：
    * 覆盖深度学习核心知识（如反向传播、优化算法）及 CV/NLP 应用（ResNet、BERT 等）。
    * 学习内容较多，建议选择性学习（如先掌握基础章节），后续结合论文复现时反复查阅。参考 [动手学深度学习](https://space.bilibili.com/1567748478/lists/358497?type=series).
    * 配套 “[《动手学深度学习》书](https://zh.d2l.ai/)”，看不惯网页版，可以 [Z - Library](https://zh.z-lib.gd/)（梯子）自取。

## 4.NLP相关资料推荐

  * 参考车万翔《自然语言处理 - 基于预训练模型的方法》。仔细认真读完，[Z - Library](https://zh.z-lib.gd/)（梯子）自取。
  * 参考斯坦福 NLP 课程 [Stanford NLP CS224n](https://web.stanford.edu/class/cs224n/) （强烈推荐）.
  * 或参考唐宇迪的[NLP入门课](https://www.bilibili.com/video/BV19VfeYMECH/?spm_id_from=333.337.search-card.all.click&vd_source=47decd48e950a191add86bdbf724a794)，重点学习词向量、文本预处理等基础内容，结合代码实践（基于PyTorch）。

## 5.推荐入门路线推荐
* **阶段一（深度学习理论与代码基础）**：[李沐：动手学深度学习](https://space.bilibili.com/1567748478/lists/358497?type=series)（长期）结合 [小土堆深度学习入门](https://www.bilibili.com/video/BV1hE411t7RN/?spm_id_from=333.337.search-card.all.click)
 
* **阶段二（自然语言处理理论与实战）**：
斯坦福NLP入门课+ 唐宇迪的NLP入门课 + 车万翔《自然语言处理 - 基于预训练模型的方法》

PS：（1）小土堆、李沐课并行进行。（2）NLP 入门课和车万翔的书，可以做入门练习项目时候，在实践中学习。

## 6.NLP 核心模型学习建议

  * **必学模型** ：
  （1）基础深度学习模型：MLP、CNN、LSTM、注意力机制、Transformer等。
  （2）预训练语言模型：BERT、GPT1、GPT2、BART、T5等。
  
  * **学习要求** ：
  （1）论文精读：逐句理解模型动机、架构细节（如 Self - Attention、预训练目标），推导关键公式（如 Transformer 的 QKV 计算）。
  （2）代码复现：吃透框架源码，分析所有使用到的函数的作用。

  * **关键点** ：
  （1）Transformer 是基石，需达到手推公式、裸写代码的熟练度。
  （2）学习路线：理论 → 源码 → 改进（如修改 Attention 头数观察效果）

