# 🌐 大语言模型（LLM）入门路线指南

本指南旨在为新手提供系统的大语言模型（LLM）学习路线，涵盖理论综述、核心论文、代码框架以及学习建议，帮助你快速掌握当前前沿的大模型技术范式。

---

## 1. 📚 理论资料推荐

* **人大赵鑫老师团队的 LLM 综述**
  内容详尽、更新及时，覆盖模型架构、训练策略、评估方法等核心内容：

  👉 [https://github.com/RUCAIBox/LLMSurvey](https://github.com/RUCAIBox/LLMSurvey)

* **《多模态大模型：新一代人工智能技术范式》**
  来自中山大学 HCPLab 的高质量中文综述书籍，强烈推荐：

  👉 [https://hcplab-sysu.github.io/Book-of-MLM/](https://hcplab-sysu.github.io/Book-of-MLM/)

* **Andrej Karpathy 的教学视频**
  OpenAI 前核心成员，内容深入浅出，涵盖 LLM 基础机制与工程实践：

  👉 [https://www.youtube.com/@AndrejKarpathy](https://www.youtube.com/@AndrejKarpathy)

* **推荐精读的核心论文**：

  * GPT 系列：GPT-1, GPT-2, GPT-3
  * InstructGPT：对人类反馈强化学习（RLHF）有深入讲解
  * DeepSeek 系列：DeepSeek-V3、DeepSeek-R1 等国产优秀开源模型

---

## 2. 🧰 实践与代码资源推荐

### 🔗 Hugging Face 全家桶（强烈推荐）

以下列举两个主要库：
* **Transformers 库**（主库）
  提供主流模型架构的预训练与微调接口：
  👉 [https://huggingface.co/docs/transformers/index](https://huggingface.co/docs/transformers/index)

* **PEFT（Parameter-Efficient Fine-Tuning）库**
  包含 LoRA、IA3、Prefix Tuning 等高效微调方法：
  👉 [https://huggingface.co/docs/peft/index](https://huggingface.co/docs/peft/index)

### 💡 实践框架推荐

* **Firefly（流萤）大模型训练框架**
  基于 Hugging Face 封装的轻量级中文训练框架，适合通过阅读源码学习与实践：
  👉 [https://github.com/yangjianxin1/Firefly](https://github.com/yangjianxin1/Firefly)

* **LLaMA-Factory**
  提供开箱即用的指令微调（SFT）、RLHF、推理等功能：
  👉 [https://github.com/hiyouga/LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory)

* **ms-swiftLLM（魔搭 Swift LLM）**
  ModelScope 官方推出的 LLM 微调与部署工具链：
  👉 [https://github.com/modelscope/ms-swift](https://github.com/modelscope/ms-swift)

---

## 3. 🏁 LLM 入门学习建议

* 建议先完成深度学习与 NLP 基础的学习，再进入 LLM 阶段。根据过往经验，通常花 1～3 个月打好基础后，再用约 1 个月时间即可完成 LLM 的高效入门。
* LLM 学习不应仅停留在理论阅读，需**结合项目实践**，如独立实现指令微调、小模型训练、推理部署等，进一步理解其工作机制与工程细节。
* 推荐以 Huggingface + LLaMA-Factory 等主流软件软件框架为载体，快速上手并完成一个完整的“训练—微调—部署”流程，之后通过不断提升理论和代码水平，提升综合LLM实力。



