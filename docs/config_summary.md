# configuation

Each HOI optimization uses a config file to set the number of optimization stages and parameters, which could be view at [config.yaml](../src/configs/config.yaml)

## Shared settings

- Initialized HOI parameters(pose and geometry) are used as the optimization input.
- MANO segmentation and palm-related configuration are used for part-level control.
- Some other configuration for saving results, record log, visualization and rendering.

## stages

### stage 0

- Coarse optimization of mano sequences' pose makes the hand's action more reasonable.
- Use 1 or more rounds of alternatives, adjusting 1-2 parameters in each round.
- Provides a generally reasonable interaction pose for fine-tuning.

### stage 1

- Optimization of mano sequences' position, achieve reasonable interaction positions.
- Then refine the pose by penetraction, contact and smooth loss to obtain detailed interaction.

### stage 2

- if necessary, more stages for optimization can be set.

## Design Concept

- Modular design to achieve low coupling.
- Multi-stage optimization reduces optimization difficulty and facilitates inspection.
- CUDA and data parallel processing acceleration.
- Convenient visualization tools.
