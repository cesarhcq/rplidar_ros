RPLIDAR ROS package
=====================================================================

ROS node and test application for RPLIDAR

Visit following Website for more details about RPLIDAR:

rplidar roswiki: http://wiki.ros.org/rplidar

rplidar HomePage:   http://www.slamtec.com/en/Lidar

rplidar Tutorial:  https://github.com/robopeak/rplidar_ros/wiki

hector_slam: https://github.com/cesarhcq/hector_slam

How to build rplidar ros package
=====================================================================
    1) Clone this project to your catkin's workspace src folder
    2) Running catkin_make to build rplidarNode and rplidarNodeClient

Configuration of the RPLIDAR A1
=====================================================================
	1) Plug your RPLidar in your PC
	2) The RPLidar need to use the serial ports in Ubuntu. Then, we need to provide permissions for it to work.
	3) Check the location of the RPLidar serial port with this command

```
ls -l /dev|grep ttyUSB
```

This should list all the available serial devices in your computer. After that, we give permissions to the serial line:

```
sudo chmod 666 /dev/ttyUSB0
```

How to run rplidar ros package
=====================================================================
There're two ways to run rplidar ros package

I. Run rplidar node and view in the rviz
------------------------------------------------------------
roslaunch rplidar_ros view_rplidar.launch

You should see rplidar's scan result in the rviz.

II. Run rplidar node and view using test application
------------------------------------------------------------
roslaunch rplidar_ros rplidar.launch

rosrun rplidar_ros rplidarNodeClient

You should see rplidar's scan result in the console

RPLidar frame
=====================================================================
RPLidar frame must be broadcasted according to picture shown in
rplidar-frame.png
