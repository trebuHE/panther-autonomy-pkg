# UGV Panther Autonomy

This repo is based on an official template containing a collection of packages containing autonomous functionalities for Husarion UGV vehicles.

## How to run

### 1. Requrements

- **Just**: to simplify the execution of this project, [just](https://github.com/casey/just) is used. Install it with:
```bash
sudo dnf install just
```

### 2. Config

Depending on the GPU edit [`compose.simulation.yaml`](./compose.simulation.yaml) file. Change config in servicies/gazebo.

For Nvidia use:
```yaml
    <<: [*common-config, *gpu-nvidia]
```

For AMD use:
```yaml
    <<: [*common-config, *gpu-amd]
```
### 3. Run

To run the simulation use:
```bash
just start-simulation
```
