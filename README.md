# Turtlebot3-SLAM.
**TurtleBot3 is a 2 wheel robot that operates,it will be ran in Gazebo for the virtual enviroment and RVIZ paired with SLAM (Simultaneous Localization and Mapping) then it display the mapping process the bot goes through.**

**there're two type:**

![image](https://user-images.githubusercontent.com/109751319/186788588-ab5f3247-206d-4ee3-ad7c-024fc327949a.jpeg)

**Installing TurtleBot3:**
----------------------------
**type the following commands in terminal**

- $ sudo apt update

- $ sudo apt upgrade

- $ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_melodic.sh

- $ chmod 755 ./install_ros_melodic.sh

- $ bash ./install_ros_melodic.sh


- $ sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy \

- ros-melodic-teleop-twist-keyboard ros-melodic-laser-proc \
  
- ros-melodic-rgbd-launch ros-melodic-depthimage-to-laserscan \
  
- ros-melodic-rosserial-arduino ros-melodic-rosserial-python \
  
- ros-melodic-rosserial-server ros-melodic-rosserial-client \
  
- ros-melodic-rosserial-msgs ros-melodic-amcl ros-melodic-map-server \
  
- ros-melodic-move-base ros-melodic-urdf ros-melodic-xacro \
  
- ros-melodic-compressed-image-transport ros-melodic-rqt* \
  
- ros-melodic-gmapping ros-melodic-navigation ros-melodic-interactive-markers
  
- $ sudo apt-get install ros-melodic-dynamixel-sdk
  
- $ sudo apt-get install ros-melodic-turtlebot3-msgs

- $ sudo apt-get install ros-melodic-turtlebot3

- $ cd ~/catkin_*workspace name*/src/

- $ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git

- $ cd ~/catkin_*workspace name*

- catkin_make


**Running the Simulation:**
--------------
**we'll be using gazebo to run a virtual enviroment. You can create your own enviroment, but for simplicity we'll use a pre-existing one.**


**1-Run these commands in the terminal to launch the simulation world.**

- $ export TURTLEBOT3_MODEL=burger

- $ roslaunch turtlebot3_gazebo turtlebot3_world.launch


**2-Open another terminal and input the following commands:**

- source /home/*username*/catkin_*workspace name*/devel/setup.bash

- export TURTLEBOT3_MODEL=burger

- roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

**(Note: Replace the username and workspace name tags accordingly)**

**3 - Open another terminal and input the following commands:**

- source /home/*username*/catkin_*workspace name*/devel/setup.bash

- export TURTLEBOT3_MODEL=burger

- roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

**4-Open Rviz and Gazebo**

**5- You can now control the robot through the 3rd terminal using the w a s d x and being the mapping process**

![image](https://user-images.githubusercontent.com/109751319/186791602-34333869-9258-4e70-bc6b-ea7c28531af5.jpeg)

**6 - After covering the entire building the map should look  similar to this :**

![image](https://user-images.githubusercontent.com/109751319/186791851-74349387-6670-40fa-9228-1593b51bfa09.jpeg)


**7-save the map by opening a new terminal then write the commande:**

- rosrun map_server map_saver -f ~/map




