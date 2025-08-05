# AMCL Localization for MIA Prototype Robot

This repository contains the ROS package for 2D robot localization using the **AMCL (Adaptive Monte Carlo Localization)** package. The launch files and configurations are tuned for the specific sensors and setup Shato MIA robot.


## ✨ Key Features

* **Robust Localization:** Utilizes the industry-standard AMCL package for reliable and accurate robot positioning within a known map.
* **Sensor Integration:** Configured to use laser scan (`/scan`) and odometry (`/odom`) data for the particle filter.
* **Easy Startup:** Includes a main launch file (`amcl_shato.launch`) to bring up all necessary nodes with the correct parameters.

## 🛠️ Tech Stack

* **Framework:** ROS1
* **Core Package:** AMCL (Adaptive Monte Carlo Localization)
* **Visualization:** RViz

## 🚀 How to Run

1.  **Prerequisites:**
    * A working ROS1 installation.
    * This package should be cloned into the `src` folder of your Catkin workspace.
    * Your robot's driver nodes (for laser scanner and odometry) must be running and publishing to the correct topics.

2.  **Launch the Localization:**
    Use `roslaunch` to start the AMCL localization node.
    ```bash
    roslaunch amcl_localization amcl_shato.launch
    ```

3.  **Visualize in RViz:**
    * Open RViz: `rosrun rviz rviz`
    * Add the `Map`, `RobotModel`, and `PoseArray` (for AMCL particles) displays to visualize the robot's position and the filter's state.


