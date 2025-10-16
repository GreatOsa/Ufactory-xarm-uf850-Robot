# UF850 Description

This repository contains the **URDF files** and necessary resources for visualizing and simulating the **UF850 robot** using **ROS 2** and **RViz2**.

---

## Requirements

Make sure you have the following installed before running the setup:

- **ROS 2 Humble** (or compatible version)
- **colcon** build tool
- **urdf_tutorial** package
- **RViz2**

You can install the tutorial package if missing:

```bash
sudo apt install ros-humble-urdf-tutorial
```

## Setup Instructions

### 1 Clone the Repository

Clone this repository into your ROS 2 workspace:

```bash
git clone (the repo)

```

### 2. Create your Workspace

Move the uf850_description to your workspace

### 3. Check for Dependencies

Verify that your workspace detects the package:

```bash
colcon list
```

If dependencies are missing, make sure to install them before proceeding.

### 4. Build the Package

```bash
colcon build
```

### 5. Source the Setup File

After building, source your workspace environment:

```bash
source install/setup.bash
```

### 6. Launch the Robot Model in RViz2

Use the command below to open the UF850 robot in RViz2:

```bash
ros2 launch urdf_tutorial display.launch.py model:=$PWD/uf850_description/urdf/uf850.urdf
```
