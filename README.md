### install
source /opt/ros/humble/setup.bash
colcon build
source install/setup.bash

### run it

start joystick

`ros2 launch picard joystick.launch.py`

start agent

`ros2 launch picard base.launch.py`



### run micro ros agent
`ros2 run micro_ros_agent micro_ros_agent serial --dev /dev/ttyACM0 baudrate=115200`

### control 
`ros2 run teleo_tpwist_keyboard teleop_twist_keyboard _speed_limit:=80 _turn_limit:=80`

### simulation
`ros2 launch picard launch_sim.launch.py world:=./src/worlds/cones.world`

