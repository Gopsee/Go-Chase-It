# **Go-Chase-It**
### A part Udacity Nanodegree Program

#### **Introduction**
  A Wheeled robot that scans for a white ball in its environment and move navigates the target.
  
#### **Description**
  We have two ROS packages: the drive_bot and the ball_chaser.
  Here are the steps to design the robot, house it inside your world, and program it to chase white-colored balls:
  
**my_robot:**

my_robot ROS package holds our robot model, the white ball, and the gazebo world file.  

##### **Robot model**

 - 4 Wheeled mobile robot with Differential drive. 
 - A lidar sensor - [Hokuyo](http://gazebosim.org/tutorials?tut=add_laser).
 - A camera.
 
**ball_chaser:**

ball_chaser ROS package holds our C++ nodes.
 - drive_botC++
    - This node provide a ball_chaser/command_robot service to drive the robot by controlling its linear x and angular z velocities. The service should publish to the wheel joints and return back the requested velocities.
 - process_imageC++
    - This node reads our robot’s camera image, analyzes it to determine the presence and position of a white ball. If a white ball exists in the image, the node should request a service via a client to drive the robot towards it.
 
  
