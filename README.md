# RoboticsND-WhereAmI
Implement robot with camera sensor in ROS/Gazebo and make it localize itself in simulated world using AMCL.

# Setup

```
mkdir -p WhereAmI/catkin_ws/src
cd WhereAmI/catkin_ws/src
git clone https://github.com/max-kazak/RoboticsND-WhereAmI.git .
catkin_init_workspace
cd ..
catkin_make
```

# Run code
Terminal1 (launching simulation):
```
cd WhereAmI/catkin_ws/
source devel/setup.bash
roslaunch my_robot world.launch
```

Terminal2 (launching AMCL localization):
```
cd WhereAmI/catkin_ws/
source devel/setup.bash
roslaunch my_robot amcl.launch
```

Terminal3 (launching robot control):
```
cd WhereAmI/catkin_ws/
source devel/setup.bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
