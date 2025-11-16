# 🚀 实战 Demo 指南

本指南汇总了由往届师兄亲自实战验证、并适合初学者上手的自然语言处理任务 Demo，涵盖文本分类、命名实体识别以及可结合具体科研课题开展大语言模型微调等内容。鼓励大家独立完成完整训练流程，并借助可视化工具进行结果分析与总结。

### 📂 数据集获取

* 🔗 [百度网盘下载](https://pan.baidu.com/s/10XRGQAIKGDI5eWLjmaB9Xg?pwd=1111)
* 🔑 提取码：`1111`

---

## 🧪 Demo 1：文本分类任务

### ✅ 任务目标

基于 [bert-base-chinese](https://huggingface.co/google-bert/bert-base-chinese)模型，完成文本分类任务的训练与评估，掌握完整的模型构建与调参流程。

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

分别使用下面二个bert预训练模型[bert-base-chinese](https://huggingface.co/google-bert/bert-base-chinese)和[chinese-bert-wwm](https://huggingface.co/hfl/chinese-bert-wwm)，完成weibo和msra二个数据集中文实体识别任务，理解序列标注模型的构建逻辑与评估指标。

### 🔧 实现要求

1. 使用 PyTorch 和 Hugging Face 生态，**独立完成以下模块**：
   * 数据加载与预处理（BIO标注格式）
   * 模型设计与训练流程
   * 模型评估与结果可视化
2. 使用 [SwanLab](https://www.swanlab.cn/) 等工具进行训练过程与结果的可视化。
3. 使用**微博实体识别数据集和MSRA实体识别数据集**，详见网盘数据集中的demo2实体识别，[微博数据来源参考](https://aclanthology.org/D15-1064.pdf)、[MSRA数据来源参考](https://tianchi.aliyun.com/dataset/144307)。

### 📊 实验汇报要求

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

## 🧪 Demo 4：**LLM-based** 上下文学习的实体识别（ICL-NER）任务

### ✅ 任务目标

本实验旨在通过调用大语言模型（如 **GPT-4、Qwen2.5、DeepSeek** 等）的 API，实现基于上下文学习（In-Context Learning, ICL）的命名实体识别（NER）任务。
学生将掌握以下核心技能：

1. Prompt 模板的设计与上下文示例构造；
2. 基于少样本学习的实体识别实现；
3. 不同提示策略下大模型 NER 性能的评估与分析。

---

### 🔧 实现要求

1. **模型调用方式**

   * 使用 OpenAI、阿里通义、智谱 AI 或其他可用大语言模型 API；
   * 独立编写 Python 脚本实现 API 调用；
   * 建议封装统一的接口函数，方便后续批量测试与结果复现。

2. **Prompt 设计与实验设置**

   * 设计多种 Prompt 模板以探索不同上下文学习策略：

     * **零样本 (Zero-shot)**：直接要求模型识别输入文本中的实体；
     * **少样本 (Few-shot)**：在 Prompt 中提供 1～3 个示例作为上下文参考；
   * 对比不同 Prompt 结构与上下文样本数量对模型识别效果的影响。

3. **数据与输出格式**

   * 实验数据：使用 **BC5CDR** 数据集，选取**前 500 条样本**进行实验；
   * 识别目标：包括 **化学品 (Chemical)** 与 **疾病 (Disease)** 两类实体；
   * 输出格式示例：

     ```json
     {
       "text": "Aspirin is used to treat headache.",
       "entities": [
         {"entity": "Aspirin", "type": "Chemical"},
         {"entity": "headache", "type": "Disease"}
       ]
     }
     ```

---

### 📊 实验汇报要求

* **数据集：**同Demo3（BC2GM）

* **性能参考指标：**

  | 模型                        | 预期 F1 范围  |
  | ------------------------- | --------- |
  | GPT-4o                    | 60% – 70% |
  | Qwen2.5-72B / DeepSeek-V3 | 55% – 70% |

* **推荐 API 平台：**

  * GPT-4o 调用地址：[https://api.gpt.ge](https://api.gpt.ge)
  * Qwen / DeepSeek 调用地址：[https://openrouter.ai/](https://openrouter.ai/)（提供免费调用额度）

---

### ⚙️ 实验提示与注意事项

1. **Prompt 输出格式控制**

   * 重点关注如何通过设计 Prompt，让大语言模型输出符合预期的结构化结果（如 JSON 格式）；
   * 建议学习并使用 [`json_repair`](https://pypi.org/project/json-repair/) 库，用于处理模型返回的非标准 JSON 字符串；
   * 尝试通过 API 参数设定或显式格式约束提升输出一致性，但需认识到模型可能仍有一定随机性。

2. **评估指标计算**

   * 建议**自行实现 F1 值计算脚本**，以加深对指标计算逻辑的理解；
   * 实验采用 **严格匹配（Strict Match）** 标准：实体边界与类别均完全匹配才视为正确；
   * 报告中需展示不同 Prompt 方案下的 F1 值变化趋势。

---













