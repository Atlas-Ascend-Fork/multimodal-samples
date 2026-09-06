# multimodal-samples

> CANN Multimodal-AI SIG — 模型层仓库

多模态 AI 模型集合，按应用场景组织，提供端到端的模型定义、训练配置、推理示例与昇腾 NPU 适配。覆盖自动驾驶、AIGC 和软件工程三大多模态场景。

## 源码下载

```bash
git clone https://gitcode.com/cann/multimodal-samples.git
cd multimodal-samples
```

## 场景分类

| 场景 | 目录 | 典型模型 | 说明 |
|------|------|----------|------|
| **自动驾驶** | `models/autonomous_driving/` | BEVFusion、UniAD、StreamPETR | 多传感器（Camera + LiDAR + Radar）融合的 3D 感知、预测与规划模型 |
| **AIGC** | `models/aigc/` | Stable Diffusion、ControlNet、IP-Adapter | 多模态联合生成与条件控制模型（文生图、图生图、风格迁移） |
| **软件工程** | `models/software_engineering/` | Code-LLaVA、DocVQA、UI-Agent | 代码、文档、界面、日志等软件工程场景的多模态理解与生成模型 |

## 目录结构

```
multimodal-samples/
├── models/                         # 模型定义（按场景分目录）
│   ├── autonomous_driving/         #   自动驾驶（多传感器 · 3D 感知）
│   │   ├── backbone/               #     骨干网络
│   │   ├── large_model/            #     大模型（端到端方案）
│   │   └── checkpoints/            #     权重索引（.yml 指向远程存储）
│   ├── aigc/                       #   AIGC（联合生成 · 条件控制）
│   │   ├── backbone/
│   │   ├── large_model/
│   │   └── checkpoints/
│   └── software_engineering/       #   软件工程（代码 · 文档 · 界面 · 日志）
│       ├── backbone/
│       ├── large_model/
│       └── checkpoints/
├── configs/                        # 训练 / 推理配置文件
├── datasets/                       # 数据集索引与预处理脚本
├── tools/                          # 通用工具（可视化、格式转换等）
├── examples/                       # 端到端推理示例
├── adapters/
│   └── cann/                       # 昇腾 NPU 适配层（调用 multimodal-ops 算子）
└── model-index.yml                 # 全局模型索引（名称、场景、精度、权重链接）
```

## 贡献指南

欢迎参与贡献，请参阅 [CONTRIBUTING.md](CONTRIBUTING.md) 了解贡献流程与规范。

## 安全声明

请参阅 [SECURITY.md](SECURITY.md) 了解安全相关信息。

## 许可证

本项目采用 [CANN Open Software License Agreement Version 2.0](LICENSE) 许可证。

## 所属 SIG

本仓库隶属于 CANN 社区 [multimodal-ai SIG](https://gitcode.com/cann/community/blob/master/CANN/sigs/multimodal-ai/README.md)。

## 问题反馈

如有问题或建议，请通过 [Issue](../../issues) 提交反馈。
