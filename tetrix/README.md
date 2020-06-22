## Mapping, Localisation and GMapping with Tetrix Prizm ##

<!-- Steps to follow before running the simulation -->

1) Clone the file and don't change file name
2) Open terminal and in your worskspace directory, use catkin_make. Eg: roscd catkin_ws; catkin_make 
3) Then type source devel/setup.bash


<!-- Simulation -->

For getting simulation in Gazebo and RViz use:   roslaunch tetrix gazebo_room.launch

         In RViz, change the Fixed Frame to base_link.
         To move the robot, open a new terminal and use "rostopic pub cmd_vel [TAB][TAB]" and input linear.x and angular.z velocities only
         OR you can use "rosrun teleop_twist_keyboard teleop_twist_keyboard.py" and use the keyboard to control the robot.


For creating map in RViz, open a new terminal and use: roslaunch tetrix tetrix_gmapping.launch
         
         In RViz, chnage the fixed frame to odom.
         Move the robot using teleop and see the map getting updated in RViz.
         Complete the map and stop the node using [CTRL-C]
         To restart the map creation use, launch the node again

To save the map created use: rosrun map_server map_saver

To visualize AMCL in RViz, use: rosrun tetrix amcl.launch

          In RViz, change the fixed frame to map
          Use the 2D Pose button on the top right side of the window and click anywhere on the map and see what happens.


To start the path planning process, make sure all nodes are closed and use: roslaunch tetrix tetrix_move_base_launcher_1.launch

         Use the 2D Nav goal and press anywhere in RViz
         You can also add an obstacle in Gazebo.

















