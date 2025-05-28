# Parol6 - ROS 2 and Moveit2! integration 

This repository is intended to provide integration of ROS 2 and Moveit2! with open-source [PAROL6](https://source-robotics.com/products/parol6-robotic-arm?srsltid=AfmBOorfz9PGXg0knbwoitNNCGVRZiu3OLCqjC-Vrxij9PlOtbnFI9js) robot manipulator 
from [Source robotics](https://source-robotics.com/). 

### Run: 

Run PAROL6 with following command: 

```
ros 2 launch parol6_moveit2_config demo.launch.py 
```

But first build and source. 

### Build package with: 

```
colcon build --packages-select parol6_description parol6_moveit2_config
```

### Source with: 

```
source ~/<ros2_ws>/install/setup.bash 
```

## Potential problems: 

Joint limits are wrong (didn't follow official documentation). 

No end effector at this point and no root link, (maybe will require fix at some point) 

`capabilities` bug from Moveit2! and ROS 2 humble, fixed as [here](https://github.com/moveit/moveit2/issues/2734#issuecomment-2055368880).  

## TODO: 
- [x] Convert URDF from the PAROL 6 to xacro 
- [x] Convert URDF ROS 1 package to ROS 2
- [x] Create ros2 parol6_description repository
- [x] Convert STLs to DAE files
- [x] Create Moveit2! config package 
- [x] Run Moveit2! demo for the Parol6
- [x] Check URDF used 
- [x] Run in the simulation
- [ ] Fix SDF for the simulation 
- [ ] Connect with the `arm_api2` 


