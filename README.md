# HOI Optimization Demo

A repository contains HOI-optimization-demo. The hoi(hand object interaction) optimization pipeline is a part of [Robowheel(CVPR 2026)](https://zhangyuhong01.github.io/Robowheel), which improves contact plausibility, reducing penetration, and refining hand-object alignment.

## Overview

## Visualization

### Demo 1: pour cola

| * | before optimization | after optimization |
| --- | --- | --- |
| frame 80 | ![frame80-init](./demo/pour-cola_4265/image/init/frame_0080.png) | ![frame80-optim](./demo/pour-cola_4265/image/optim/frame_0080.png) |
| frame 120 | ![frame120-init](./demo/pour-cola_4265/image/init/frame_0120.png) | ![frame120-optim](./demo/pour-cola_4265/image/optim/frame_0120.png) |

whole sequences:

| before optimization | after optimization |
| --- | --- |
| ![video-init](demo/pour-cola_4265/video/init/render-3_105_45-init.mp4) | ![video-optim](demo/pour-cola_4265/video/optim/render-3_105_45-optim.mp4) |

### Demo 2: pick-up milk

| * | before optimization | after optimization |
| --- | --- | --- |
| frame 80 | ![frame80-init](./demo/pickup-milk_9708/image/init/frame_0080.png) | ![frame80-optim](./demo/pickup-milk_9708/image/optim/frame_0080.png) |
| frame 125 | ![frame125-init](./demo/pickup-milk_9708/image/init/frame_0125.png) | ![frame125-optim](./demo/pickup-milk_9708/image/optim/frame_0125.png) |

whole sequences:

| before optimization | after optimization |
| --- | --- |
| ![video-init](demo/pickup-milk_9708/video/init/render-3_105_45-init.mp4) | ![video-optim](demo/pickup-milk_9708/video/optim/render-3_105_45-optim.mp4) |

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
