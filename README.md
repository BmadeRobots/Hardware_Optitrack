## Requirements
## Hardware Setup
## Motive Setup
## Grasshopper Setup

## ROS Setup

### Install ROS Melodic
https://wiki.ros.org/melodic/Installation/Ubuntu <br>

### Create Catkin Workspace
https://wiki.ros.org/catkin/Tutorials/create_a_workspace

### Download to catkin ws src folder
https://github.com/ros-drivers/vrpn_client_ros/tree/kinetic-devel <br>

### Rename Folder
vrpn_client_ros <br>

### Edit the IP address in launch file
go to sample.launch file and edit the ip address of the PC running Motive software <br>
\<arg name="server" default="localhost"/> <br>
\<arg name="server" default="ip_address"/>

### Install ROS bridge
https://wiki.ros.org/rosbridge_suite

### Terminal
    cd ~/catkin_ws/ 
<br>

    rosdep install --from-paths ./src/
<br>

    catkin build
<br>

    source devel/setup.bash
<br>

    export ROS_MASTER_URI=http://192.168.100.170:11311
<br>

    roslaunch rosbridge_server rosbridge_websocket.launch
<br>

    roslaunch optitrack_fake_localization Optitrack_odom.launch
<br>
