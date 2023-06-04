## Getting started 
Clone this workspace (WS) and compile the packages either using catkin_make or catkin build. 
```bash
$ catkin build
```
source the compiled files
```bash
$ source devel/setup.bash
```

To activate the robot use `/dynamixel_workbench` to open the `JointTrajectory` topic for changing the manipulator configuration. 
```bash
$ roslaunch px_robot px_controllers.launch
```

## How to vizualize different positions with rviz 
Start the nodes. 
```bash
$ roslaunch px_planner check_ikinem.launch
```
After rviz has been initizalizated correctly, you can call the ikinem service in order to vizualize the config for the desiredpose of the end-effector. 

```bash
$ rosservice call /px_ikinem "desiredPosition:
  x: 13.0
  y: 21.0
  z: 0"
```

