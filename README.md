# Control-Robot-Arm-Using-ROS

To use the robot arm package, first you have to install Robot Operating System (ROS) following the steps below.

Note: in this project I used ROS Melodic, if you want to use ROS Kinetic then replace 'melodic' with 'kinetic'.

Open Ubuntu's Terminal and type the follwing:

`sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'`

`sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654`

`sudo apt-get update`

`sudo apt-get install ros-melodic-desktop-full`

`apt-cache search ros-melodic`

`echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc`
`source ~/.bashrc`

`sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential`

`sudo apt install python-rosdep`

`sudo rosdep init`

`rosdep update`

`sudo apt-get install ros-noetic-catkin`

`mkdir -p ~/catkin_ws/src`

`cd ~/catkin_ws/`

`catkin_make`

`cd ~/catkin_ws/src`

`git clone https://github.com/smart-methods/arduino_robot_arm.git`

`cd ~/catkin_ws`

`rosdep install --from-paths src --ignore-src -r -y`

`sudo apt-get install ros-melodic-moveit`

`sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui`

`sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher`

`sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control`

`sudo nano ~/.bashrc`

Scroll down to reach the end of the (bashrc) file and add the link between the parantheses:

(source /home/ruwaa/catkin_ws/devel/setup.bash), then press ctrl + o, then press Enter, then press ctrl + x

Note: in the link above you should write the name of your system instead of 'ruwaa'.

`source ~/.bashrc`

`roslaunch robot_arm_pkg check_motors.launch`

Now the robot arm package is launched.
