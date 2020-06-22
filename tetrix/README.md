## GMapping, AMCL and Navigation with 4-wheeled TETRIX MAX robot  ##

The robot model is used to go from start to goal in the environment and avoid an obstacle using the ROS Navigation Stack

<!-- Steps to follow before running the simulation -->

1) Open terminal and in your worskspace directory, use catkin_make. Eg: roscd catkin_ws; catkin_make 
2) Then type source devel/setup.bash


<!-- Simulation -->

To visualize robot model in Gazebo and RViz use:   **roslaunch tetrix gazebo_room.launch**

         In RViz, keep the Fixed Frame as robot_footprint
         To move the robot, open a new terminal and use "rostopic pub cmd_vel [TAB][TAB]" 
         and input linear.x and angular.z velocities only
         OR you can use "rosrun teleop_twist_keyboard teleop_twist_keyboard.py" 
         and use the keyboard to control the robot.

To visualize the robot model in Gazebo and RViz in the test environment use:   **roslaunch tetrix gazebo_room.launch**


For creating the map in RViz using GMapping, open a new terminal and use: **roslaunch tetrix tetrix_gmapping.launch**
         
         In RViz, keep the Fixed Frame as /odom.
         Move the robot using teleop and see the map getting updated in RViz.
         Complete the map and save it 
         To restart the map creation close the node and launch again.
         
While the node is running, save the map created using: **rosrun map_server map_saver**

To visualize the pose guesses in RViz using AMCL, use: **roslaunch tetrix amcl.launch**

          In RViz, keep the Fixed Frame as /map
          Use the 2D Pose button to manually apply the robot's position.


To start the path planning process, make sure all the nodes are closed and use: 
**roslaunch tetrix tetrix_move_base_launcher_1.launch**

         Use the 2D Nav goal to set the goal position
         You can also add an obstacle in Gazebo.

















