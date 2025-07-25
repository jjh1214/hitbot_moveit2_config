# Hitbot_moveit2
[![license - MIT](https://img.shields.io/:license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![ROS2 Jazzy](https://img.shields.io/badge/ROS2-Jazzy-purple.svg)](https://index.ros.org/doc/ros2/Releases/)

# Note
This repository is ROS2-Jazzy Package for the [Z-Arm of Hitbot.](https://www.hitbotrobot.com/category/product-center/4-axis-robot-arm/)

This repository is able [Moveit2 simulation.](https://moveit.ros.org/)

# Build
### *This Package is implemented at ROS2-Jazzy.*
```
### I assume that you have installed the ros-jazzy-desktop package using the apt-get command.
### I recommand the /home/<user_home>/hitbot_ws/src
### Before activate simulation, please install moveit2



$ mkdir -p ~/hitbot_ws/src
$ cd ~/hitbot_ws/src
$ git clone https://github.com/jjh1214/hitbot.git
$ git clone -b jazzy-devel https://github.com/jjh1214/hitbot_sim.git
$ git clone https://github.com/jjh1214/hitbot_msgs.git
$ git clone -b jazzy https://github.com/jjh1214/hitbot_moveit2_config.git

$ sudo apt-get install ros-jazzy-joint-state-publisher-gui

$ cd ~/hitbot_ws
$ colcon build
$ . install/setup.bash
$ source hitbot_ws/install/local_setup.bash



### if you want
# $ echo 'source ~/hitbot_ws/install/local_setup.bash' >> ~/.bashrc 
```

# Run - Moveit2 simulation
```
$ ros2 launch hitbot_moveit2_config demo.launch.py
```
![alt text](<Screenshot from 2024-05-13 13-23-45.png>)