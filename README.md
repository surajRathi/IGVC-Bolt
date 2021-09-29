# Bolt
#### Team Abhiyaan's ROS based robot model <br />
Getting Started
---------------
#### To launch robot in gazebo, run
```
roslaunch igvc_bolt gazebo.launch
```

#### To visualize simulaion in rviz, run
```
roslaunch igvc_bolt display.launch
```
<p>
<img align="left" src="https://user-images.githubusercontent.com/79641410/133905236-7023b5ff-2c5e-4e3f-9a67-a97987c9d481.png" width="350"/>
<img src="https://user-images.githubusercontent.com/79641410/133905351-7a96e0bd-31d5-49a0-97f8-bdc45e899926.png" width="350"/>
 </p>

## Robot components
## Collision objects
* Chassis
* Four wheels ( front & back )
* Two front steers
* Front steer and Rear wheel ( Bicycle model )
* ##### TF Tree
<img src="https://user-images.githubusercontent.com/79641410/133905922-143effc9-71ff-4827-a306-c62fd6a0e8e3.png" width="700"> <br />

## Controller

Ackermann steering model is implemented using `ROS Control` with [`steer_bot_hardware_gazebo`](http://wiki.ros.org/steer_bot_hardware_gazebo) and [`ackermann_steer_controller`](http://wiki.ros.org/ackermann_steering_controller)
* ##### Subscribed topics
  - `cmd_vel`
* ##### Published topics
  - `odom`
  - `tf` <br />

Note: Line 63 in [`steer_bot_hardware_gazebo.cpp`](https://github.com/CIR-KIT/steer_drive_ros/blob/kinetic-devel/steer_bot_hardware_gazebo/src/steer_bot_hardware_gazebo.cpp) should be [modified](https://github.com/ros-simulation/gazebo_ros_pkgs/issues/487) before compiling `steer_bot_hardware_gazebo` package.

## Tasks
- [x] Import Chassis from fusion360
- [x] Create gazebo model with collision objects
- [x] Add actuators to Joints
- [x] Implement ackermann steering mechanism
- [ ] Add sensors
- [ ] Tune controller parameters for accurate control
- [ ] Final testing
