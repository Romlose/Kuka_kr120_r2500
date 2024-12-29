# Kuka_kr120_r2500 
This repository is made to control the manipulator _Kuka kr120_ through the digital twin in the context of scientific activities
## Gazebo 
To launch the model in Gazebo, write down the follow command:
```
roslaunch kuka_kr120_gazebo/launch/kr120r2500pro_gazebo.launch
```
**Note**: to rotate joints for the pose like in technical requirements, edit the ._xacro_ file, particularly _rpy_

## MoveIt 
To controll model with framework _Moveit_, write down follow command:
```
roslaunch kuka_kr120_moveit_config/launch/moveit_planning_execution_gazebo.launch
```

## Test_node
To make manipulator's end-effector move it coordinates {1.0, 1.0., 1.0}, write down the follow command: 
```
rosrun kuka_test test_custom_kuka_node
```
**Note**: if the execution will be aborted due to the "joint could not acheive the desired pose", edit PID in _kuka_kr120_gazebo/config/kr120r2500pro_arm_controller.yaml_
