# multimodal-samples

> CANN Multimodal-AI SIG — 模型层仓库

多模态 AI 模型集合，按应用场景组织，提供预训练权重、模型定义、训练配置与昇腾 NPU 适配。当前已收录自动驾驶场景的多传感器融合模型，AIGC 和软件工程场景待社区共建。

## 源码下载

```bash
git clone https://gitcode.com/cann/multimodal-samples.git
cd multimodal-samples
```

注意：模型权重使用 Git LFS 管理，首次 clone 后需执行 `git lfs pull` 下载权重文件。

## 已有模型

### 自动驾驶（多传感器融合）

| 模型 | 权重文件 | 说明 |
|------|----------|------|
| BEVFusion | `bevfusion_kitti_fusion_latest.pth` | Camera + LiDAR 融合的 BEV 3D 检测 |
| CLOCs | `clocs_fusion_trained.pth` | Camera-LiDAR 后融合目标检测 |
| EPNet | `epnet_fusion_refine_best.pth` | 点云 + 图像端到端融合检测 |
| EPNet++ | `epnetpp_residual_car_v5_best.pth` | EPNet 改进版，残差融合 |
| FarAway | `faraway_gate40_epoch1_best.pth` | 远距离目标融合检测 |
| HMFI | `hmfi_fusion_trained_best.pth` | 层次化多模态融合推理 |
| LOGONet | `logonet_fusion_trained_best_loss.pth` | 局部-全局融合网络 |
| PointPainting | `pointpainting_kitti_car_best_ap.pth` | 语义分割投影到点云的融合检测 |

权重文件位于 `models/autonomous_driving/checkpoints/`，通过 Git LFS 存储。

## 场景分类

| 场景 | 目录 | 状态 | 说明 |
|------|------|------|------|
| **自动驾驶** | `models/autonomous_driving/` | ✅ 已有 8 个模型权重 | 多传感器融合的 3D 感知模型 |
| AIGC | `models/aigc/` | 待共建 | 多模态联合生成与条件控制模型 |
| 软件工程 | `models/software_engineering/` | 待共建 | 代码、文档、界面等多模态理解与生成模型 |

## 目录结构

```
multimodal-samples/
├── models/                         # 模型（按场景分目录）
│   └── autonomous_driving/         #   自动驾驶
│       └── checkpoints/            #     预训练权重（Git LFS）
├── configs/                        # 训练 / 推理配置文件（待共建）
├── datasets/                       # 数据集索引与预处理脚本（待共建）
├── tools/                          # 通用工具（待共建）
├── examples/                       # 端到端推理示例（待共建）
└── adapters/
    └── cann/                       # 昇腾 NPU 适配层（待共建）
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
