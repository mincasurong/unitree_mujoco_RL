# Unitree MuJoCo Reinforcement Learning Integration

This repository builds upon the original Unitree MuJoCo repository, adding integration with reinforcement learning (RL) capabilities. The goal is to simulate and enhance the behaviors of Unitree quadruped robots using advanced machine learning algorithms within the MuJoCo environment.

- Original repository link: [Unitree MuJoCo Original Repository](https://github.com/unitreerobotics/unitree_mujoco)
- Forked and enhanced repository: [mincasurong's Unitree MuJoCo RL Integration](https://github.com/mincasurong/unitree_mujoco_RL/tree/main)

## Features Added

- **Reinforcement Learning (RL) Environment**: Integrated support for reinforcement learning, enabling the use of RL agents to train and optimize the behavior of Unitree robots.
- **ROS2 Communication**: Enhanced interaction between the MuJoCo simulation and ROS2, facilitating real-time control and state feedback.
- **New Motion Capabilities**: Included support for various robotic behaviors, such as standing up, balancing, velocity movement, and trajectory following, simulated in the MuJoCo environment.
- **Sport Mode Integration**: Added the functionality to use the sport mode commands, enabling dynamic movement control in the MuJoCo simulation.

## Requirements

- **MuJoCo**: You need to have MuJoCo installed and properly configured. For installation instructions, refer to the [original Unitree MuJoCo repository](https://github.com/unitreerobotics/unitree_mujoco).
- **Python 3.x**: Python is required for running the simulation scripts and reinforcement learning integration.
- **ROS2 Humble or Rolling**: For real-time robot control, ROS2 Humble or Rolling is recommended.
- **Unitree SDK**: Ensure that the Unitree SDK dependencies are installed.

## Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/mincasurong/unitree_mujoco_RL.git
    cd unitree_mujoco_RL
    ```

2. **Install Dependencies**:
    Ensure all the necessary Python libraries are installed. Run the following command:
    ```sh
    pip install -r requirements.txt
    ```

3. **MuJoCo Setup**:
    Follow the original [Unitree MuJoCo repository](https://github.com/unitreerobotics/unitree_mujoco) instructions for configuring MuJoCo.

4. **Set Environment Variables**:
    Configure the environment variables for MuJoCo and ROS2 if necessary:
    ```sh
    export MUJOCO_PY_MJKEY_PATH=~/.mujoco/mjkey.txt
    export MUJOCO_PY_MUJOCO_PATH=~/.mujoco/mujoco210
    ```

## Usage

- **Run the Simulation**:  
  The MuJoCo simulation can be started by running the `unitree_mujoco.py` script:
  ```sh
  python unitree_mujoco.py
