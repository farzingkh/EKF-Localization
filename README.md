# Sensor Fusion using EKF
This repository include an example application of Extended Kalman Filter using  ```robot_pose_ekf``` cROS package on gazebo turtle bot simulation package using its IMU and wheel odometry data

## Directory Structure
```sh
.
├── README.md
└── src
    ├── CMakeLists.txt -> /opt/ros/kinetic/share/catkin/cmake/toplevel.cmake
    ├── EKF.rviz
    ├── RvizLaunch.launch
    ├── main
    │   ├── CMakeLists.txt
    │   ├── launch
    │   │   └── main.launch
    │   └── package.xml
    ├── odom_to_trajectory
    │   ├── CMakeLists.txt
    │   ├── Images
    │   │   └── Output.png
    │   ├── LICENSE
    │   ├── README.md
    │   ├── launch
    │   │   └── create_trajectory.launch
    │   ├── package.xml
    │   └── scripts
    │       ├── path_ekf_plotter.py
    │       └── path_odom_plotter.py
    ├── robot_pose_ekf
    │   ├── 3-Clause_BSD_license
    │   ├── CHANGELOG.rst
    │   ├── CMakeLists.txt
    │   ├── Images
    │   │   └── Output.png
    │   ├── README.md
    │   ├── example_with_gps.launch
    │   ├── package.xml
    │   ├── plotekf.m
    │   ├── robot_pose_ekf.launch
    │   ├── scripts
    │   │   └── wtf.py
    │   ├── src
    │   │   ├── nonlinearanalyticconditionalgaussianodo.cpp
    │   │   ├── odom_estimation.cpp
    │   │   └── odom_estimation_node.cpp
    │   └── srv
    │       └── GetStatus.srv
    ├── turtlebot
    │   ├── LICENSE
    │   ├── README.md
    │   ├── setup_create.sh
    │   ├── setup_kobuki.sh
    │   ├── turtlebot
    │   ├── turtlebot.rosinstall
    │   ├── turtlebot_bringup
    │   ├── turtlebot_capabilities
    │   ├── turtlebot_capabilities.rosinstall
    │   ├── turtlebot_description
    │   └── turtlebot_teleop
    └── turtlebot_simulator
        ├── README.md
        ├── turtlebot_gazebo
        ├── turtlebot_simulator
        ├── turtlebot_simulator.rosinstall
        ├── turtlebot_stage
        └── turtlebot_stdr
```

## Steps to launch the simulation

## Output

# Kalman Filter

One way of looking at Kalman filter is to consider it as any other types of filter. Filters are designed to eliminate or reduce noise from signal. Kalman filter, similarly, tries to eliminate uncertainty and noise from the data regarding the states of a system. Kalman fiter accepts a noisy measurement from sensors and assumes that the signals have Gaussian ditribution, and therefore, they can be described by their means and variance. This assumption is the main basis for Kalman filters. It also accepts inital guess about the states of the system, and then, it uses system models (State Transition Function in State Space modelling) to predict the next values for states of the system. Later, it updates the states based on next observations of the states from measured values by sensors. In general, Kalman Filter ca be described by two steps of measurement update and prediction:

![alt text](./images/equations.png)

# Extended Kalman Filter
