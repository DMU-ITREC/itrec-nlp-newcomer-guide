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

---

## 🧪 Demo 4：**LLM-based**上下文学习的实体识别（ICL-NER）任务

### ✅ 任务目标

通过大语言模型 API（如 **GPT-4、Qwen2.5、Deepseeek** 等） 实现命名实体识别任务，掌握以下核心技能：
1. Prompt 模板设计与上下文示例构造；
2. 使用小样本学习实现实体识别；
3. 评估大模型在不同提示策略下的 NER 表现。

### 🔧 实现要求

1. **模型调用方式**

   * 使用 OpenAI、阿里通义、智谱 AI 或其他可用大模型 API；
   * 需自行编写 Python 脚本实现接口调用；
   * 建议封装统一的接口函数，便于批量处理。

2. **Prompt 设计与实验设置**

   * 设计多种 Prompt 模板：

     * **零样本 (Zero-shot)**：直接要求模型识别文本中的实体；
     * **少样本 (Few-shot)**：在输入中提供 1～3 个示例；
   * 对比不同 Prompt 结构、上下文数量对识别效果的影响。

3. **数据与输出**

   * 输入：BC5CDR 前 500 条文本；
   * 输出：每条文本对应的识别结果（化学品、疾病两类实体）；
   * 格式示例：

     ```json
     {
       "text": "Aspirin is used to treat headache.",
       "entities": [
         {"entity": "Aspirin", "type": "Chemical"},
         {"entity": "headache", "type": "Disease"}
       ]
     }
     ```

### 📊 实验汇报要求

* 参考指标：

  GPT4o: F1:70%-80%
  Qwen2.5-72B和deepseek-v3稍弱，65%-75%之间
  GPT-4o接口推荐api网站：https://api.gpt.ge
  Qwen和DS推荐api网站：https://openrouter.ai/ 这里有免费的api调用次数

* 重点注意：
  如何设定prompt让llm返回你想要的格式？也就是说，如何从输出文本解析实体。
  建议调研json_repair库，方便解析prompt。接口有参数，可以设定固定的json返回格式，但不一定满足所有任务需求。
  如何计算F1？建议完全自己手写，F1需要解析的结果完整匹配才算对。即strict match而不是partial match。




















当然可以！以下是按照你提供的格式与风格，为 **“ICL-NER 实战项目”** 编写的完整项目指南，保持了与你实验室 Demo 文档一致的排版、层次和细节。

---

# 🚀 实战 Demo 指南：ICL-NER（In-Context Learning 实体识别）

本指南面向具备基础自然语言处理与大语言模型（LLM）使用经验的同学，旨在帮助大家掌握**利用大模型的上下文学习能力（In-Context Learning, ICL）完成命名实体识别任务**的基本方法。项目基于 API 方式调用大语言模型，通过精心设计的 prompt 实现零样本或少样本实体识别实验。

---

## 📂 数据集获取

* 🔗 [百度网盘下载](https://pan.baidu.com/s/10XRGQAIKGDI5eWLjmaB9Xg?pwd=1111)
* 🔑 提取码：`1111`
* 数据路径：`demo4_ICL_NER`
* 说明：本实验推荐使用 **BC5CDR** 数据集，可选取**前 500 条样本**作为实验集（含化学品与疾病两类实体）。

---

## 🧪 Demo 4：ICL 实体识别任务（In-Context Learning NER）

### ✅ 任务目标

通过**大语言模型 API（如 GPT-4、Qwen2.5、GLM-4、Claude 等）** 实现命名实体识别任务，掌握以下核心技能：

1. Prompt 模板设计与上下文示例构造；
2. 使用少样本学习实现实体识别；
3. 评估大模型在不同提示策略下的 NER 表现。

---

### 🔧 实现要求

1. **模型调用方式**

   * 使用 OpenAI、阿里通义、智谱 AI 或其他可用大模型 API；
   * 需自行编写 Python 脚本实现接口调用；
   * 建议封装统一的接口函数，便于批量处理。

2. **Prompt 设计与实验设置**

   * 设计多种 Prompt 模板：

     * **零样本 (Zero-shot)**：直接要求模型识别文本中的实体；
     * **少样本 (Few-shot)**：在输入中提供 1～3 个示例；
   * 对比不同 Prompt 结构、上下文数量对识别效果的影响。

3. **数据与输出**

   * 输入：BC5CDR 前 500 条文本；
   * 输出：每条文本对应的识别结果（化学品、疾病两类实体）；
   * 格式示例：

     ```json
     {
       "text": "Aspirin is used to treat headache.",
       "entities": [
         {"entity": "Aspirin", "type": "Chemical"},
         {"entity": "headache", "type": "Disease"}
       ]
     }
     ```

4. **可视化与分析**

   * 使用 [SwanLab](https://www.swanlab.cn/) 或 matplotlib/seaborn 进行实验记录与结果可视化；
   * 对不同 prompt 设计、样本数量下的 F1 值变化进行分析。

---

### ⚙️ 技术实现参考

| 模块    | 推荐实现                            |
| ----- | ------------------------------- |
| 模型调用  | OpenAI / 通义千问 / 智谱AI API        |
| 实验语言  | Python                          |
| 可视化工具 | SwanLab / matplotlib            |
| 指标计算  | 精确率 (Precision)、召回率 (Recall)、F1 |

---

### 📊 实验汇报要求

* **参考指标：**
  F1 ≈ 70%（Zero-shot 基线）
  F1 ≈ 80%（Few-shot 优化后）

* **汇报内容要求：**

  1. 对比不同 Prompt 模板与样本数量下的实验结果；
  2. 分析大模型识别错误的典型案例；
  3. 结合可视化图表（如 F1-变化曲线、示例对比），阐述模型的上下文理解能力；
  4. 讨论 ICL 的优势与局限性（如对上下文数量敏感、结果随机性等）。

---

### 🌟 可选进阶探索

* 尝试不同大模型（GPT-4、Qwen2.5、GLM-4-turbo）在同一任务下的表现差异；
* 将 ICL 与 **LoRA 微调结果（Demo 3）** 对比，分析二者在性能、成本、可解释性上的区别；
* 尝试引入 Chain-of-Thought 或逐步提示策略（Step-by-step Prompting）提升识别准确率。

---

### 📘 参考资料

* [BC5CDR 数据集论文 (BioCreative V)](https://aclanthology.org/W15-1501.pdf)
* [In-Context Learning Survey](https://arxiv.org/abs/2301.00234)
* [OpenAI API 文档](https://platform.openai.com/docs)
* [SwanLab 可视化平台](https://www.swanlab.cn/)

---

是否希望我帮你**补充一份可直接运行的项目结构与示例代码框架**（包括 API 调用、prompt模板与评估脚本）？那样你就可以直接交给新生做实验了。

