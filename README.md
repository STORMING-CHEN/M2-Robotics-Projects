<p align="right">  
   <img src = "rosimages/vibot.png" width = 80>
</p >

<p align="center">  
   <img src = "rosimages/ub.png" width = 400>
</p >

# <p align="center">Master of Computer vision and Robotics</p >   
<h3 align="center">Robotics Project</h3> <br>

<p align="center">Supervisors: Ralph SEULIN</p >  
<p align="center">Students: CHEN CHENG</p >  

## Contents
- [Introduction](#introduction)
- [Tasks to accomplish](#Tasks-to-accomplish)
- [Related techniques](#Related-techniques)
- [Implementation](#Implementation)
- [Conclusion](#Conclusion)
- [Demo videos](#Demo-videos)
- [References](#References)
## Introduction
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Robot Operating System (ROS) is a flexible framework for writing robot software. It is a collection of tools, libraries, and conventions that aim to simplify the task of creating complex and robust robot behavior across a wide variety of robotic platforms. It can be considered as an API to make the process of developing a robotic related projects more flexible, and simplified. There will be no need for an extensive knowledge of the hardware in which it saves much effort and time in the development phase.   
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Many operating systems support ROS, such as ubuntu and windows. Among them ubuntu is the most used one for ROS develop since it's clean, stable, and easy to manage packages. For the development of this project, we used the Construct Web platform, which is an online robot working environment. The platform uses ubuntu as the main operating system with ROS kinetic, and uses Gazebo as the real-world simulator to simulate turtlebot 3 or other robot models. The platform provides us with a lot of useful courses, to enable us master the basic of Linux, Python and ROS. Through learning, we can realize the autonomous navigation of the turtlebot3 robot.

## Tasks to accomplish

The project goal is to apply the learned ROS techniques and packages to apply the navigation task on Turtlebot3:
1. **Motion Control**: Moving the robot around the environment using /cmd_vel topic.
2. **Mapping and localization**: Construct a map of the whole environment. We need to fully occupy the whole environment, then we need to localize the Robot.
3. **Path planning**: we need to publish a goal to move base navigation system in which Turtlebot3 can reach that goal without colliding with any obstacles.
4. **Waypoints Navigation**: Create waypoints that allows Turtlebot3 to navigate within the environment.

## Related techniques
 <h3>1.Motion Control</h3>  
              
    
    
    
    
 <h3>2.Map Building</h3>  
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In the field of robot, the common research problems include mapping, localization and path planning. Simultaneous localization and mapping belongs to the intersection of location and mapping.
              <p align="center">  
   <img src = "rosimages/module.png" width = 300>
</p >
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;gmapping package provides **slam_gmapping** node. This node is implementing the gmapping SLAM algorithm. It creates a 2D map of the environment using the data the Robot is providing during movement like laser data, in which it will be transformed to an Occupancy Grid Map (OGM) data format (nav_msgs/OccupancyGrid.msg) where it represents a 2-D grid map and each cell of the grid represents the occupancy.
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The figure below is the framework of gmapping package.
    
<p align="center">  
   <img src = "rosimages/gmapping_frame.png" width = 350>
</p >
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The topics and services in the gmapping packages and corresponding description are shown blow:
 <p align="center">  
   <img src = "rosimages/table1.png" width = 350>
</p >

1. **tf**: used for the transformation between lidar coordinate system, base coordinate system and odometer coordinate system.  
2. **scan**: used to subscribe to lidar scan data.  
-- **map_metadata**: publishes map Metadata.  
**map**: publishes map raster data.  
**entropy**: releases estimation of robot poses distribution entropy.  
**dynamic_map**: used to obtain map data.  







 <h3>3.Localization</h3>  
 
 <h3>4.Path Planning</h3>  
 
 <h3>5.Waypoints Navigation</h3>  
 

## Implementation

## Conclusion
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The purpose of this project is to let us understand the related knowledge of robot navigation, and make a preliminary attempt. Robot navigation is mainly composed of three parts: map building, localization (Simultaneously 2 called SLAM) and path planning. In order to help us understand, the task we are required to complete in turn is to first build a mobile platform and make it subscribe / CMD_ Vel topic, then use slam_mapping node to build the scene map, and use AMCL node to localization, and then use move_base node which integrates all the above functions to implement path planning,  in the end tried multiple waypoints navigation.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In order to prepare for the project, we need to study the corresponding basic courses, they are: linux4robotics, python4robotics, ROS basic in 5 days, ROS navigation in 5 days, mastering Turtle 3. All the related courses are studied and practiced on the construction platform, and the final project is unit 8 of the turtlebot3 course. There is no real machine operation in the whole process. The operating system supported by the construct platform is Ubuntu, and the simulated environment is gazebo. Construct is a very good robot virtual platform, the tutorial is written reasonably and efficiently. But there is a disadvantage that the platform is unstable. So in order not to be affected by the emergency crash, the simulation experiment needs to be carried out in advance.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Through this whole project, I have gained experience in the principle of ROS, the use of Linux system, the framework of python, the principle of navigation technology, the use of various robots and markdown language in githup.
## Demo videos
- [Motion control](https://www.loom.com/share/c9cc85b31b6c4e6692d15c345f1530b0)
- [Path planing navigation](https://www.loom.com/share/c9cc85b31b6c4e6692d15c345f1530b0)
- [Waypoints navigation](https://www.loom.com/share/c9cc85b31b6c4e6692d15c345f1530b0)
## References
1. [Construct Platform](http://theconstructsim.com)
2. [Wiki ROS](http://wiki.ros.org/)
3. [Construct course support](https://get-help.robotigniteacademy.com/c/course-support/masteringwithrosturtlebot3/27)
