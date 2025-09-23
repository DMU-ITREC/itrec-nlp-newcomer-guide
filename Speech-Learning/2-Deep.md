# 语音信号处理

## 课程二：Listen, Attend and Spell (LAS)
* **参考文献：**
  * [1] Chan W, Jaitly N, Le Q V, et al. Listen, attend and spell[J]. arXiv preprint arXiv:1508.01211,2015.
  * [2] [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记-LAS](https://zhuanlan.zhihu.com/p/124327822)
  * [3] [Speech Recognition(2)-LAS](https://zhuanlan.zhihu.com/p/137081463)
* Listen：即 Encoder；Spell：Decoder，这是一个经典的使用注意力机制的 seq2seq 模型
---

## 课程三：CTC，RNA，RNN-T，Neural Transducer，MoChA
* **参考文献：**
  * [1] Graves A, Fernández S, Gomez F, et al. Connectionist temporal classification: labelling unsegmented sequence data with recurrent           neural networks[C]//Proceedings of the 23rd international conference on Machine learning. 2006: 369-376.
  * [2] Graves A. Sequence transduction with recurrent neural networks[J]. arXiv preprint arXiv:1211.3711, 2012.
  * [3] Jaitly N, Le Q V, Vinyals O, et al. An online sequence-to-sequence model using partial conditioning[J]. Advances in Neural Information Processing Systems, 2016, 29.
  * [4] Chiu C C, Raffel C. Monotonic chunkwise attention[J]. arXiv preprint arXiv:1712.05382,2017.
  * [5] [Speech Recognition - CTC, RNN-T and more (part 3)_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=4&vd_source=c06477a064079dc916ffc3a3b940bb0f)
  * [6] [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 CTC, RNN-T & More - 4](https://zhuanlan.zhihu.com/p/125165696)
  * [7] [语音识别模型CTC,RNN-T,Neural Transducer,MoCha学习笔记](https://zhuanlan.zhihu.com/p/130899095)
* CTC 模型在2006年就出现了，很长一段时间大家并没有用，因为CTC有比较大的问题。
---

## 这里推荐继续下面的语音识别选修课程（共三节）

## 选修一：HMM（Hidden Markov Model）
* **参考文献：**
  * [Speech Recognition (Option) - HMM哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=5&vd_source=c06477a064079dc916ffc3a3b940bb0f)
  * [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 HMM - 6](https://zhuanlan.zhihu.com/p/126752024)
  * [隐马尔可夫（HMM)的解码问题+维特比算法](https://zhuanlan.zhihu.com/p/78414538)
* 让我们穿越回14年前，看看那时的人们在没有神经网络的情况下是如何做语音辨识的。你会发现，当前的技术中有借用HMM的很多思想。

## 选修二：Alignment of HMM, CTC and RNN-T
* **参考文献：**
  * [Speech Recognition (option) - Alignment of HMM, CTC and RNN-T哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=6&vd_source=c06477a064079dc916ffc3a3b940bb0f)
  * [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 Alignment - 7 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/127403727)



## 选修三：RNN-T Training
* **参考文献：**
    * [Speech Recognition (option) - RNN-T Training哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=7&vd_source=c06477a064079dc916ffc3a3b940bb0f)
    * [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 Alignment Train - 8](https://zhuanlan.zhihu.com/p/128123600)
---

## 课程四：Language Modeling
* **参考文献：**
   * [1] [Speech Recognition- Language Modeling哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=8&spm_id_from=333.880.my_history.page.click&vd_source=c06477a064079dc916ffc3a3b940bb0f)
   * [2] [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 Language Model - 9 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/128697931)
---

## 课程五：Voice Conversion
* **参考文献：**
   * [1] [Voice Conversion (1/2)哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=9&vd_source=c06477a064079dc916ffc3a3b940bb0f)
   * [2] [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 Voice Conversion-10](https://zhuanlan.zhihu.com/p/129067006)
   * [3] [Voice Conversion (2/2)哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=10&vd_source=c06477a064079dc916ffc3a3b940bb0f)
   * [4] [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 StarGAN in VC-11](https://zhuanlan.zhihu.com/p/129345757)
   * [5] [台大教授 李宏毅 Flow-based Generative Model哔哩哔哩bilibili](https://www.bilibili.com/video/BV1C4411A7o3/?from=search&seid=7904061540301133082&vd_source=c06477a064079dc916ffc3a3b940bb0f)
---

## 课程六:Speech Separation
* **参考文献：**
   * [1] [Speech Separation (1/2) - Deep Clustering, PIT哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=11&vd_source=c06477a064079dc916ffc3a3b940bb0f)
   * [2] [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 Speech Seperate-12](https://zhuanlan.zhihu.com/p/129883837)
   * [3] [Speech Separation (2/2) - TasNet哔哩哔哩bilibil](https://www.bilibili.com/video/BV1QE411p7z3/?p=12&vd_source=c06477a064079dc916ffc3a3b940bb0f)
   * [4] [2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 TasNet-13](https://zhuanlan.zhihu.com/p/130470329)
---

## 课程七:Speech Synthesis
* **参考文献：**
   * [1][Speech Synthesis（1/2）- Tacotron哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=13&vd_source=c06477a064079dc916ffc3a3b940bb0f)
   * [2][2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 TTS - 14](https://zhuanlan.zhihu.com/p/130999249)
   * [3][Speech Synthesis (2/2) - More than Tacotron哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=14&vd_source=c06477a064079dc916ffc3a3b940bb0f)
   * [4][2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 Beyond Tacotron - 15](https://zhuanlan.zhihu.com/p/133854797)
---

## 课程八:Speaker Verification
* **参考文献：**
  * [1][Speaker Verification哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=15&vd_source=c06477a064079dc916ffc3a3b940bb0f)
  * [2][2020 年 3月 新番 李宏毅 人类语言处理 独家笔记 声纹识别 - 16](https://zhuanlan.zhihu.com/p/134671051)
  * [3][Meta Learning – Metric-based (1/3)](https://www.youtube.com/watch?v=yyKaACh_j3M)
  * [4][如何理解等错误率(EER, Equal Error Rate)？请不要只给定义](https://www.zhihu.com/question/37436914)
---

## 课程九:Vocoder
* **参考文献：**
  * [1][Vocoder (由助教許博竣同學講授)哔哩哔哩bilibili](https://www.bilibili.com/video/BV1QE411p7z3/?p=16&vd_source=c06477a064079dc916ffc3a3b940bb0f)
  * [2] Oord A, Dieleman S, Zen H, et al. Wavenet: A generative model for raw audio[J]. arXiv preprint arXiv:1609.03499,2016.
  * [3] https://deepmind.google/discover/blog/wavenet-a-generative-model-for-raw-audio/
  * [4] Jin Z, Finkelstein A, Mysore G J, et al. FFTNet: A real-time speaker-dependent neural vocoder[C]//2018 IEEE international conference on acoustics, speech and signal processing (ICASSP). IEEE, 2018: 2251-2255.
  * [5] Kalchbrenner N, Elsen E, Simonyan K, et al. Efficient neural audio synthesis[C]//International Conference on Machine Learning. PMLR, 2018: 2410-2419
  * [6] Prenger R, Valle R, Catanzaro B. Waveglow: A flow-based generative network for speech synthesis[C]//ICASSP 2019-2019 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP). IEEE, 2019: 3617-3621.
  * [7] [Flow-based Deep Generative Models | Lil'Log (lilianweng.github.io)](https://lilianweng.github.io/posts/2018-10-13-flow-models/)
  * [8][细水长flow之NICE：流模型的基本概念与实现 - 科学空间|Scientific Spaces (kexue.fm)](https://kexue.fm/archives/5776)
---


