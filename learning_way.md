# 第一阶段：python基础
# 第二阶段：transformers基础
## 学习目标与计划
## 必须掌握的核心概念：
├── 自注意力机制 (Self-Attention)
│   ├── Scaled Dot-Product Attention
│   ├── Multi-Head Attention
│   └── 注意力可视化与可解释性
├── 位置编码 (Positional Encoding)
│   ├── 绝对位置编码 (Sinusoidal)
│   ├── 相对位置编码 (RoPE, ALiBi) ⭐ 重点
│   └── 旋转位置编码的推导与实现
├── 前馈网络与归一化
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
# 第五阶段：训练方法
