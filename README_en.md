# multimodal-samples

> CANN Multimodal-AI SIG — Model Repository

A collection of multimodal AI models organized by application scenario. Currently provides pre-trained weights for multi-sensor fusion models in autonomous driving. Model definitions, training configurations, and Ascend NPU adaptation are planned for community co-development. AIGC and software engineering scenarios are also planned.

## Source Code Download

```bash
git clone https://gitcode.com/cann/multimodal-samples.git
cd multimodal-samples
```

Note: Model weights are managed with Git LFS. After the initial clone, run `git lfs pull` to download the weight files.

## Existing Models

### Autonomous Driving (Multi-sensor Fusion)

| Model | Weight File | Description | Source |
|-------|-------------|-------------|--------|
| BEVFusion | `bevfusion_kitti_fusion_latest.pth` | Camera + LiDAR fused BEV 3D detection | Paper reproduction |
| CLOCs | `clocs_fusion_trained.pth` | Camera-LiDAR late-fusion object detection | Paper reproduction |
| EPNet | `epnet_fusion_refine_best.pth` | Point cloud + image end-to-end fusion detection | Paper reproduction |
| EPNet++ | `epnetpp_residual_car_v5_best.pth` | Improved EPNet with residual fusion | Paper reproduction |
| FarAway | `faraway_gate40_epoch1_best.pth` | Long-range object fusion detection | Paper reproduction |
| HMFI | `hmfi_fusion_trained_best.pth` | Hierarchical multimodal fusion inference | Paper reproduction |
| LOGONet | `logonet_fusion_trained_best_loss.pth` | Local-global fusion network | Paper reproduction |
| PointPainting | `pointpainting_kitti_car_best_ap.pth` | Semantic segmentation projected onto point cloud for fusion detection | Paper reproduction |

Weight files are located in `models/autonomous_driving/checkpoints/` and stored via Git LFS.

## Scenario Classification

| Scenario | Directory | Status | Description |
|----------|-----------|--------|-------------|
| **Autonomous Driving** | `models/autonomous_driving/` | ✅ 8 model weights available | Multi-sensor fusion 3D perception models |
| AIGC | `models/aigc/` | Planned | Multimodal joint generation and conditional control models |
| Software Engineering | `models/software_engineering/` | Planned | Multimodal understanding and generation models for code, documentation, UI, etc. |

## Version Compatibility

| Item | Version |
|------|---------|
| Product Model | Ascend950PR |
| NPU Chip | Ascend 950 |
| Training Environment CANN Version | 9.1.0 |
| PyTorch | 2.7.1 |
| Python | 3.12.3 |

## Directory Structure

```
multimodal-samples/
├── models/                         # Models (organized by scenario)
│   └── autonomous_driving/         #   Autonomous Driving
│       └── checkpoints/            #     Pre-trained weights (Git LFS)
├── configs/                        # Training / inference configuration files (Planned)
├── datasets/                       # Dataset index and preprocessing scripts (Planned)
├── tools/                          # Common utilities (Planned)
├── examples/                       # End-to-end inference examples (Planned)
└── adapters/
    └── cann/                       # Ascend NPU adaptation layer (Planned)
```

## Contributing

Contributions are welcome. Please refer to [CONTRIBUTING.md](CONTRIBUTING.md) for the contribution process and guidelines.

## Security Statement

Please refer to [SECURITY.md](SECURITY.md) for security-related information.

## License

This project is licensed under the [CANN Open Software License Agreement Version 2.0](LICENSE).

## SIG Affiliation

This repository belongs to the CANN community [multimodal-ai SIG](https://gitcode.com/cann/community/blob/master/CANN/sigs/multimodal-ai/README.md).

## Feedback

If you have questions or suggestions, please submit feedback via [Issue](https://gitcode.com/cann/multimodal-samples/issues).
