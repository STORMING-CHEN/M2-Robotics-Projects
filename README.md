![](https://github.com/STORMING-CHEN/M2-Robotics-Projects/raw/main/rosimages/ub.png)  
<p align="center">
   <p align="center">
   <img src = "rosimages/ub.png" width = 400>
   </p >
</p >
# <p align="center">Master of Computer vision and Robotics</p >  
**<p align="center">Robotics Project</p >** 
<p align="center">Supervisors: Ralph SEULIN</p >  
<p align="center">Students: CHEN CHENG</p >  
 
## Introduction
The Robot Operating System (ROS) is a flexible framework for writing robot software. It is a collection of tools, libraries, and conventions that aim to simplify the task of creating complex and robust robot behavior across a wide variety of robotic platforms. It can be considered as an API to make the process of developing a robotic related projects more flexible, and simplified. There will be no need for an extensive knowledge of the hardware in which it saves much effort and time in the development phase.
Many operating systems support ROS, such as ubunto and windows. Ubunto is a more stable operating system using ROS. However, for the development of this project, we used the Construct Web platform, which is an online robot working environment. The platform uses ubunto as the main operating system with ROS kinetic, and uses Gazebo as the real-world simulator to simulate turtlebot 3 or other robot models. This platform will enable us to learn some basic ROS technologies so that we can apply robot control, mapping, robot positioning, path planning and navigation with several waypoints.

## Tasks to accomplish

The project goal is to apply the learned ROS techniques and packages to apply the navigation task on Turtlebot3:
1. Motion Control: Moving the robot around the environment using /cmd_vel topic.
2. Mapping and localization: Construct a map of the whole environment. We need to fully occupy the whole environment, then we need to localize the Robot.
3. Path planning: we need to publish a goal to move base navigation system in which Turtlebot3 can reach that goal without colliding with any obstacles.
4. Waypoints Navigation: Create waypoints that allows Turtlebot3 to navigate within the environment.
