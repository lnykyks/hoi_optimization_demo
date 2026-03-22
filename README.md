# HOI Optimization Demo

A repository contains HOI-optimization-demo. The hoi(hand object interaction) optimization pipeline is a part of [Robowheel(CVPR 2026)](https://zhangyuhong01.github.io/Robowheel), which improves contact plausibility, reducing penetration, and refining hand-object alignment.

## Overview

This repository showcases some demos that optimize the hand-object interaction mesh sequence which obtained from the initial reconstruction.

This pipeline supports multi-stage dynamic parameter optimization and is mainly used to adjust the following aspects.:

- Hand trajectory position
- Penetration between hand and object
- Contact and local interaction quality
- Smoothness across frames

## Visualization

### Demo 1: pour cola

| * | before optimization | after optimization |
| --- | --- | --- |
| frame 80 | ![frame80-init](./demo/pour-cola_4265/image/init/frame_0080.png) | ![frame80-optim](./demo/pour-cola_4265/image/optim/frame_0080.png) |
| frame 120 | ![frame120-init](./demo/pour-cola_4265/image/init/frame_0120.png) | ![frame120-optim](./demo/pour-cola_4265/image/optim/frame_0120.png) |
| all | [video-init](./demo/pour-cola_4265/video/init/render-3_105_45-init.mp4) | [vdeo-optim]("./demo/pour-cola_4265/video/optim/render-3_105_45-optim.mp4") |

<!-- whole sequences:

| before optimization | after optimization |
| --- | --- |
| <video src="./demo/pour-cola_4265/video/init/render-3_105_45-init.mp4" controls="controls" width="100%"></video> | <video src="demo/pour-cola_4265/video/optim/render-3_105_45-optim.mp4" controls="controls" width="100%"></video> | -->

### Demo 2: pick-up milk

| * | before optimization | after optimization |
| --- | --- | --- |
| frame 80 | ![frame80-init](./demo/pickup-milk_9708/image/init/frame_0080.png) | ![frame80-optim](./demo/pickup-milk_9708/image/optim/frame_0080.png) |
| frame 125 | ![frame125-init](./demo/pickup-milk_9708/image/init/frame_0125.png) | ![frame125-optim](./demo/pickup-milk_9708/image/optim/frame_0125.png) |
| all | [video-init](./demo/pickup-milk_9708/video/init/render-3_105_45-init.mp4) | [vdeo-optim]("./demo/pickup-milk_9708/video/optim/render-3_105_45-optim.mp4") |

<!-- whole sequences:

| before optimization | after optimization |
| --- | --- |
| <video src="./demo/pickup-milk_9708/video/init/render-3_105_45-init.mp4" controls="controls" width="100%"></video> | <video src="demo/pickup-milk_9708/video/optim/render-3_105_45-optim.mp4" controls="controls" width="100%"></video> | -->

### Qualitative improvements

- Better grasping pose and position
- Less penetration between hand and object
- Improved contact plausibility and motion alignment
- Smoother interaction across frames

## Method Highlights

- Initialized HOI inputs(pose & geometry sequence)
- Stage-wise optimization
- Part-level control of hand during optimization
- Geometric and time-consistency losses
- Structured outputs for reproducibility
- Visualization for qualitative comparison

## Configuration Summary

Please refer to [doc](./docs/config_summary.md)

## Structure

```text
hoi_optimization_demo/
├── README.md
├── demo/
|   ├── pickup-milk_9708/
|   |   ├── image/
|   |   |   ├── init/
|   |   |   |   ├── frame_0080.png
|   |   |   |   └── frame_0125.png
|   |   |   └── optim/
|   |   |       ├── frame_0080.png
|   |   |       └── frame_0125.png
|   |   └── video/
|   |       ├── init/
|   |       |   └── render-3_105_45-init.mp4
|   |       └── optim/
|   |           └── render-3_105_45-optim.mp4
|   └──pour-cola_4265/
|       ├── ...
|       └── ...
├── docs/
|   └── config_summary.md
├── src/
|   ├── configs/
|   ├── core/
|   ├── optim/
|   ├── scripts/
|   └── utils/
└── output/
    └── example_output_structure.md
```

## Quick Start

### 1. Browse the qualitative results

- view sampled frames for comparsion at [Visualization](#visualization)
- view video at path[demo/*/video]: e.g. [video of pickup-milk after optimization](./demo/pickup-milk_9708/video/optim/render-3_105_45-optim.mp4)

### 2. Inspect the code structure

- `src/configs/`: configuration files
- `src/core/`: geometry-related and hand/object processing modules
- `src/optim/`: code for optimization
- `src/scripts/`: script file to run optimizaiton
- `src/utils/`: helpers for logging, transforms, visualization and so on.

### 3. Review saved outputs

- The directory structure of the output results after each code run is as follows:
  - backup
    - ..., backup code
  - log
    - text log
    - loss curves
  - results
    - saved hoi parameters
  - vis
    - before/after visualization outputs(could be used for rendering)
  - config.yaml

## Citation

If you find this repository relevant, please also refer to and cite the broader RoboWheel project:

```bibtex
@article{zhang2025robowheel,
  title={RoboWheel: A Data Engine from Real-World Human Demonstrations for Cross-Embodiment Robotic Learning},
  author={Zhang, Yuhong and others},
  journal={arXiv preprint arXiv:2512.02729},
  year={2025}
}
```

## Contact

Email: lnykyks@gmail.com
