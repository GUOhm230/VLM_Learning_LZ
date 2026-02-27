当前是窗口期，黄金时期，需要好好学啊
学习计划和目标需要根据学习进度，掌握内容进行不断纠正
需要不断的反馈，回溯学习。
# 第一阶段：python基础
继续学习，记录相关技巧
# 第二阶段：transformers基础
## 学习目标与计划
掌握基础概念，原理，知道什么作用，有哪些缺陷，相关变体，训练技巧（在ViT中学习）。推荐的论文要看完
不过分追求细节，本就需要不断的精进。
学习计划：1-2周。周日回家要学习。
## 必须掌握的核心概念：
├── 自注意力机制 (Self-Attention)   复习下就行
│   ├── Scaled Dot-Product Attention
│   ├── Multi-Head Attention
│   └── 注意力可视化与可解释性
├── 位置编码 (Positional Encoding) 难点，这个地方要重点学习下
│   ├── 绝对位置编码 (Sinusoidal)
│   ├── 相对位置编码 (RoPE, ALiBi) ⭐ 重点 
│   └── 旋转位置编码的推导与实现
├── 前馈网络与归一化    复习下
│   ├── Pre-Norm vs Post-Norm
│   ├── RMSNorm (LLaMA, InternLM使用)
│   └── SwiGLU激活函数
└── 解码策略
    ├── Greedy/Beam Search
    ├── Temperature Sampling
    └── Top-p/Top-k Sampling
## 相关论文
《Attention Is All You Need》(2017) - 奠基之作
《RoFormer: Enhanced Transformer with Rotary Position Embedding》- RoPE
《GLU Variants Improve Transformer》- SwiGLU
## 继续学习
# 第三阶段：ViT
## 目标与计划
目标：该部分主要是训练技巧，一些先进技巧的处理，训练遇到哪些问题，针对具体效果缺陷怎么改进的。
重在训练技巧的梳理和掌握。也是不要过分关注细节，需要不断的在实操过程中与同事请教，讨论。
计划学习时间2-4周
## 3.1 基础架构
## 3.2 演进路线
ViT演进路线（必须按顺序学习）：
ViT (2020) - 原始版本，理解图像如何变成token序列
DeiT (2021) - 数据高效训练，知识蒸馏
Swin Transformer (2021) - 层次化设计，局部注意力 ⭐
ConvNeXt (2022) - CNN与ViT的融合思考
EVA-02/CLIP-ViT - 大规模预训练视觉编码器
## 3.3 先进知识点
动态分辨率处理：NaViT, FlexiViT（处理不同尺寸图像）
2D RoPE在视觉中的应用：InternVL, CogVLM使用
视觉编码器的缩放规律：如何设计1B/6B参数的视觉模型
## 3.4 继续探索

# 第四阶段：LLM
目标：这里只需要掌握一些基础概念就可以了。其中的训练细节主要是下一阶段，这部分的基础东西也比较少。多看看论文把
## 一些基础的东西
token是什么
怎么得到token啥的
## 核心架构变体：
├── Decoder-only (GPT风格) - 主流
│   ├── GPT-3/4架构细节
│   ├── LLaMA/LLaMA2/LLaMA3架构演进
│   └── InternLM2/3架构特点 ⭐
├── Encoder-Decoder (T5风格)
│   └── 适用于特定任务
└── 混合专家 (MoE)
    ├── Switch Transformer
    ├── Mixtral 8x7B
    └── DeepSeek-MoE ⭐ 前沿
## 关键实现细节（影响训练稳定性和效果）：
KV-Cache优化：推理加速核心
FlashAttention v1/v2/v3：内存与计算优化 ⭐ 必须掌握
激活检查点 (Activation Checkpointing)：节省显存
梯度累积与混合精度训练
# 第五阶段：训练方法
目标：实现的重要部分，掌握先进的训练技巧。这里多和邱博，晓鹏请教讨论
计划：学习周期4-6周。到这一步，就比较有条不紊了。
## 预训练及其训练技术
## 对齐训练
## 多模态专项训练
