# TETRIX-MAX-ROS-Navigation


1) To visualize robot model in Gazebo and RViz in an empty map use:
      
      **roslaunch tetrix gazebo_full.launch**


2) To visualize robot model in Gazebo and RViz in the test environment use:
      
      **roslaunch tetrix gazebo_room.launch**


3) To map the environment using GMapping, in 2nd terminal use:
      
      **roslaunch tetrix tetrix_gmapping.launch** 
      and move robot using **rosrun teleop_twist_keyboard teleop_twist_keyboard.py** 


4) To visualize pose guesses in RViz using AMCL use:
      
      **roslaunch tetrix tetrix_amcl.launch** 


5) To execute navigation use:

      **roslaunch tetrix tetrix_move_base_launcher_1.launch** 
      and use **2D NavGoal button in RViz** to set a goal position


      
      





