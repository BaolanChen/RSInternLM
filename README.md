# RSInternLM
Multi-modal Remote Sensing LLM based on InternLM

用于遥感图像理解的多模态大模型 | multimodal large-scale model for remote sensing image understanding

## 项目简介
目前的通用多模态大模型如LLaVA、MiniGPT-4、InstructBLIP等，在通用领域的不同任务上均上取得了较好的效果，但这些多模态大模型在垂直领域的应用效果仍有较大提升空间。
由于自然图像与遥感图像存在较大域间差距，通用的多模态大模型在遥感图像分析中仍然存在较大的局限性，
当前还没有用于遥感图像场景分析的多模态大模型，这在一定程度上受限于遥感图像相关数据集的稀缺，
基于通用多模态大模型的微调为遥感大模型的研究提供了可能。

InternLM是浦江实验室研发提出的大语言模型，具有以下模型优势与特点：

- 卓越的推理性能：在数学推理方面取得了同量级模型最优精度，超越了 Llama3 和 Gemma2-9B。
- 有效支持百万字超长上下文：模型在 1 百万字长输入中几乎完美地实现长文“大海捞针”，而且在 LongBench 等长文任务中的表现也达到开源模型中的领先水平。 可以通过 LMDeploy 尝试百万字超长上下文推理。更多内容和文档对话 demo 请查看这里。
- 工具调用能力整体升级：InternLM2.5 支持从上百个网页搜集有效信息进行分析推理，相关实现将于近期开源到 Lagent。InternLM2.5 具有更强和更具有泛化性的指令理解、工具筛选与结果反思等能力，新版模型可以更可靠地支持复杂智能体的搭建，支持对工具进行有效的多轮调用，完成较复杂的任务。可以查看更多样例。

## 数据处理
RS Multimodal Instruction Dataset

整理数据集用于遥感图像多模态大模型进行微调训练。

## 模型结构

## 训练过程

## 测评结果

## 模型定性结果

### Scene Classification

### Visual Question Answering

### Grounded Description 

### Multi-Turn Conversation 

## 使用方法

### 环境配置

### 模型复现

## 后续方向
1.由于遥感图像领域缺少大规模、高精度、精细描述的图文数据集，利用chatgpt生成的数据集仍存在大量重复描述，或者图片描述较短，总体来说质量较低。
因此需要进一步探索更高质量遥感图文数据集，另一种可行方向是在此前生成的数据集上进一步利用chatgpt进行扩写或改写，提高数据集的质量。
此外，初步实验中使用了相同的prompt，因此测试时对于不同遥感分析问题没有很好的理解能力，需要进一步构建指令微调数据集。

2.该项目只是对遥感图像大模型的初步探索，结果有很大改进空间，今后可能在更大的基座模型上进行微调，或在更大数据集上进行预训练。

## 引用
```bibtex
  @article{chenbl2024rsinternlm,
          title={RSInternLM: Multi-Modal Vision-Language Model for Remote Sensing},
          author={BaolanChen},
          journal={arxiv},
          year={2024}
  }
```
## 致谢

1.该项目参考了[RemoteGLM](https://github.com/lzw-lzw/RemoteGLM)、[GeoChat](https://github.com/mbzuai-oryx/GeoChat)进行方案设计。
2. 该项目利用ChatGPT处理数据数据集。