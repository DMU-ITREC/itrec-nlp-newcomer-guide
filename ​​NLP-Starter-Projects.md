# 🚀 实战 Demo 指南

本指南汇总了由往届师兄亲自实战验证、并适合初学者上手的自然语言处理任务 Demo，涵盖文本分类、命名实体识别以及可结合具体科研课题开展大语言模型微调等内容。鼓励大家独立完成完整训练流程，并借助可视化工具进行结果分析与总结。

### 📂 数据集获取

* 🔗 [百度网盘下载](https://pan.baidu.com/s/10XRGQAIKGDI5eWLjmaB9Xg?pwd=1111[)
* 🔑 提取码：`1111`

---

## 🧪 Demo 1：文本分类任务

### ✅ 任务目标

基于 [bert-base-chinese](https://huggingface.co/google-bert/bert-base-chinese) 模型，完成文本分类任务的训练与评估，掌握完整的模型构建与调参流程。

### 🔧 实现要求

1. 使用 PyTorch 和 Hugging Face 生态，**独立实现如下模块**：

   * 数据预处理流程
   * 训练与测试全过程
2. 使用 [SwanLab](https://www.swanlab.cn/) 等工具进行训练过程与结果的可视化。
3. 使用**今日头条文本分类**数据集见，详见网盘数据集中的demo1文本分类，[数据来源参考](https://github.com/aceimnorstuvwxz/toutiao-text-classfication-dataset)。

### 📊 实验汇报要求

* 参考指标：acc：83%
* 分析超参数（如学习率、batch size、dropout 等）对结果的影响
* 结合可视化图表，对实验结果进行深入解读

---

## 🧪 Demo 2：命名实体识别（NER）任务

### ✅ 任务目标

基于  [bert-base-chinese](https://huggingface.co/google-bert/bert-base-chinese)  模型，完成中文实体识别任务，理解序列标注模型的构建逻辑与评估指标。

### 🔧 实现要求

1. 使用 PyTorch 和 Hugging Face 生态，**独立完成以下模块**：

   * 数据加载与预处理（BIO标注格式）
   * 模型设计与训练流程
   * 模型评估与结果可视化
2. 使用 [SwanLab](https://www.swanlab.cn/) 等工具进行训练过程与结果的可视化。
3. 使用**微博实体识别数据集**，详见网盘数据集中的demo2实体识别，[数据来源参考](https://aclanthology.org/D15-1064.pdf)。

### 📊 实验汇报要求

* 参考指标：F1：63%
* 参数调优对实体识别性能的变化趋势

---

## 🧪 Demo 3：**大模型**的指令微调的实体识别（NER）任务

### ✅ 任务目标

基于 [Qwen2.5-7B](https://huggingface.co/Qwen/Qwen2.5-7B)模型，完成实体识别任务，理解指令微调原理。

### 🔧 实现要求

1. 使用 PyTorch 和 Hugging Face 生态，**独立完成以下模块**：

   * 数据预处理
   * 模型设计与训练流程
   * 模型评估与结果可视化
2. 使用 [SwanLab](https://www.swanlab.cn/) 等工具进行训练过程与结果的可视化。
3. 使用**bc2gm**数据集，详见网盘数据集中的demo3指令微调，[数据来源参考](https://github.com/spyysalo/bc2gm-corpus?utm_source=chatgpt.com)。

### 📊 实验汇报要求

* 参考指标：

  Qwen2.5-7B-lora：显存占用27G、F1:84%

  Qwen2.5-7B-qlora：显存占用12G、F1:83%

* 参数调优对实体识别性能的变化趋势

* 可视化示例分析模型识别结果与错误案例
