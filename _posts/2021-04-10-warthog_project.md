---
title: Warthog 
date: 2021-04-10 10:00:00 +/-TTTT
categories: [Robotic, Vision, Personal]
tags: [robotic, ROS, SLAM, computer vision]     # TAG names should always be lowercase
math: true
mermaid: true
pin: false
image:
  src: /assets/img/warthog/WarthogGallery.jpg
  # width:  750   # in pixels
  # height: 750   # in pixels
  alt: Warthog
---

The idea of this project is to develop mobile robot techniques and autonomous navigation. For that, a mobile platform called Warthog was used, a robot manufactured by the company [Clearpath Robotics](https://clearpathrobotics.com/warthog-unmanned-ground-vehicle-robot/).

### Purpose of the Project

For the movement of a mobile robot to be performed autonomously, it must be able to carry out, without the intervention of an external controller, the planning and execution of trajectories in the desired operating environment, the avoidance of obstacles and the location and mapping of environment, which is known as autonomous navigation. Autonomous navigation is essential for a robot to be able to perform a wide range of tasks, such as moving from one point to another in an unfamiliar environment.

The project aims to use warthog robot for navigation, localization and mapping, to develop and train slam techniques. All this with ROS integration.

## Techniques developed

### Navigation

Navigation is responsible for carrying out the movement of the robot given an objective position.

### Perception: 

The perception module is responsible for providing the robot with the ability to perceive the environment around it through data from on-board sensors.

### Planning: 

Responsible for calculating collision-free routes.

### Mapping: 

From the images of the stereo camera, the area covered by the robot is mapped.

### Localization

The robot location is performed through visual odometry. 

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/HzJX0vbLYgo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

### Rtabmap

I used a ROS package wrapper from RTAB-Map (Real-Time Appearance-Based Mapping), an RGB-D SLAM approach based on a global loop-closing detector with real-time constraints. This package can be used to generate 3D point clouds from the environment and/or to create a 2D occupancy grid map for navigation. Below you can see my experience with this package.

![diagram](/assets/img/warthog/v1_rtabmap.png){: width="450" height="450" }
_Rtabmap with Warthog robot_

## Code

The project was all done in a simulation environment and all the code can be found in the repository following the [link](https://github.com/MatheusFranca-dev/warthog_navigation).

## Development team

<center>
<div>
  <div class=" col-xl-auto offset-xl-0 col-lg-4 offset-lg-0">
    <table class="table-borderless highlight">
      <thead>
        <tr>
          <th><center><img src="{{ 'assets/img/matheus_franca.jpeg' | relative_url }}" width="100" alt="Matheus" class="img-fluid rounded-circle" /></center></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr class="font-weight-bolder" style="text-align: center margin-top: 0">
          <td width="100%"><center><a href="https://www.linkedin.com/in/matheus-frança-b62044150">Matheus França</a></center></td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
</center>

<br>

## Project Summary

1. Category: <font color="#fbb117">Mobile Robotics</font>
3. Start date: <font color="#fbb117">April/2021</font>
4. End date: <font color="#fbb117">April/2021</font>