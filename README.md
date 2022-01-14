# GSSS_FDP

First launch simulation using
```
roslaunch fdpbot_simulation gazebo.launch
```
this will launch it in default world which is a home world.<br>
If you want it in separate world, provide an optional world argument<br>

***OPTIONAL***-
```
roslaunch fdpbot_simulation gazebo.launch world:=maze
```

for mapping start the folllowing script in a new terminal
```
roslaunch fdpbot_slam slam.launch
```

move the robot around using this ROS Node
```
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

to save the map,
```
rosrun map_server map_saver -f name_of_map
```
this will be stored in home, copy paste yaml and pgm file in slam package inside maps folder

to run navigation
```
roslaunch fdpbot_navigation navigation.launch map_file:=name_of_map
```
