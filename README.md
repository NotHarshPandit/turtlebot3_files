Ensure that Isaac Sim is installed.  
Open terminal and go to the Isaac Sim directory.  
Run the following command to open Isaac Sim:

```bash
./isaac-sim.selector.sh
```
For the Differential drive for the turtlebot3 robot, open Turtlebot_tut6.usd and Differential_Drive.usd.  
Open a new terminal and type the following command to install Twist message type:
```bash
sudo apt install ros-humble-geometry-msgs
```

Then type the following command to publish the command velocity:
```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0, y: 0.0, z: 0.0}, angular: {x: 0.0, y: 0.0, z: 0.2}}"
```

For the Ackermann drive for the leatherback robot, open Leatherback.usd and Ackermann_Drive.usd.  
Open a new terminal and type the following command to install Twist message type:

```bash
sudo apt install ros-humble-ackermann-msgs
```

Then type the following command to publish the command velocity:
```bash
ros2 topic pub /ackermann_cmd ackermann_msgs/msg/AckermannDriveStamped "{drive: {speed : 1.0, steering_angle: 0.2}}"
```