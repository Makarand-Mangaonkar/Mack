#Mack-Autonomous Robot

## Prerequisites

Before using Mack, ensure you have the following dependencies installed:

- ROS2 `Humble` distribution
- Additional packages:
  - `gazebo*`
  - `xacro`
  - `rmw_cyclonedds_cpp`
  - `nav*`

>If you are using **`binary installation`**, you can install these packages using `apt`. 

>If you are using **`source installation`**, make sure you have built your ROS2 Humble source folder, and you'll need the `behaviours_tree_v3` package from the GitHub v3.8 branch. 


## Installation

To get started, clone the repository:

```bash
cd <your workspace name>/src/
```

```bash
git clone https://github.com/Makarand-Mangaonkar/Mack.git
```

#### Build the repository using the following command:

```bash
cd ~/<your workspace name>/
```

```bash
colcon build --symlink-install
```

>Make sure you have sourced ROS2 Humble in your terminal before building.

## Usage

  - Source your build workspace every time before running any files or nodes:

    ```bash
    source <path_to_your_workspace>/install/setup.bash
    ```

  - To launch the Gazebo simulation and spawn the robot with all plugins:

    ```bash
    ros2 launch mack_gazebo gazebo_bringup.launch.py
    ```

  - To run teleop node:

    ```bash
    ros2 run teleop_twist_keyboard teleop_twist_keyboard
    ```
