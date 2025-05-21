# 深度学习与 NLP 入门指南

## 深度学习与 NLP 基础

  * **深度学习** ：作为机器学习的子领域，深度学习通过多层神经网络（如 CNN、RNN、Transformer）自动提取数据特征，广泛应用于计算机视觉（CV）、自然语言处理（NLP）等领域。推荐李沐《动手学深度学习》。
  * **NLP（自然语言处理）** ：专注于让计算机理解、生成人类语言，核心任务包括文本分类、机器翻译、对话系统等。

### 学习建议

  * 参考车万翔《自然语言处理 - 基于预训练模型的方法》书，简称车万翔。仔细认真读完，[Z - Library](https://zh.z-lib.gd/)（梯子）自取。
  * 参考斯坦福 NLP 课程 [Stanford NLP](https://www.bilibili.com/video/BV1U5RNYgEfp/?spm_id_from=333.337.search-card.all.click&vd_source=47decd48e950a191add86bdbf724a794).
  * 或参考唐宇迪的[NLP入门课](https://www.bilibili.com/video/BV19VfeYMECH/?spm_id_from=333.337.search-card.all.click&vd_source=47decd48e950a191add86bdbf724a794)，重点学习词向量、文本预处理等基础内容，结合代码实践（如 PyTorch），无需深入高阶内容。

## 快速上手：环境与代码基础

  * **小土堆 PyTorch 教程** ：
    * 从环境配置（Anaconda + PyTorch）开始，逐步学习张量操作、模型搭建、训练流程等。参考 [小土堆深度学习入门](https://www.bilibili.com/video/BV1hE411t7RN/?spm_id_from=333.337.search-card.all.click).
    * 特点：代码简单直观，适合培养基础直觉，建议全程跟练。

## 系统学习：理论与代码并重

  * **李沐《动手学深度学习》** ：
    * 覆盖深度学习核心知识（如反向传播、优化算法）及 CV/NLP 应用（ResNet、BERT 等）。
    * 学习内容较多，建议选择性学习（如先掌握基础章节），后续结合论文复现时反复查阅。参考 [动手学深度学习](https://space.bilibili.com/1567748478/lists/358497?type=series).
    * 配套 “[《动手学深度学习》书](https://zh.d2l.ai/)”，看不惯网页版，可以 [Z - Library](https://zh.z-lib.gd/)（梯子）自取。

### 入门路线推荐

[李沐：动手学深度学习](https://space.bilibili.com/1567748478/lists/358497?type=series)（长期）→ [小土堆深度学习入门](https://www.bilibili.com/video/BV1hE411t7RN/?spm_id_from=333.337.search-card.all.click) → NLP 入门课 + 车万翔
PS：小土堆、李沐课并行进行，NLP 入门课和车万翔的书，根据个人进度进行展开。

## NLP 核心模型精读指南

  * **必学模型** ：Transformer、BERT、GPT、BART、T5
  * **学习要求** ：
    * 论文精读：逐句理解模型动机、架构细节（如 Self - Attention、预训练目标），推导关键公式（如 Transformer 的 QKV 计算）。
    * 代码复现：吃透框架源码，分析所有使用到的函数的作用。

  * **关键点** ：
    * Transformer 是基石，需达到手推公式、裸写代码的熟练度。
    * 学习路线：理论 → 源码 → 改进（如修改 Attention 头数观察效果）

## LLMs 培训指南

未完待续...
