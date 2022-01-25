---
title: Bbot - Balancing Robot
date: 2022-01-18 07:00:00 +/-TTTT
categories: [Robotic, SBR]
tags: [robotic, ROS, Gazebo, control, CAD, biped]     # TAG names should always be lowercase
math: true
mermaid: true
pin: false
image:
  src: /assets/img/bbot/bbot_wide.png
  width:  750   # in pixels
  height: 750   # in pixels
  alt: BBOT
---

### Introduction

Bbot or Balancing Robot, is a self-balancing autonomous robot project. Our goal is to build a mobile robot operated via ROS Noetic capable of balancing and moving on two wheels. In addition, he must be able to read a TAG (fiducial framework). The TAG will send the robot a target position to which it must navigate autonomously. To perform navigation, this robot must be able to create a map of where it is and locate itself there, allowing it to update its position throughout the mission and avoid obstacles while navigating to its objective.

![bbot](/assets/img/bbot/bbot_cad.png){: width="350" height="350" }
_Bbot in a) extended pose b) bent pose._

### LEG Architecture

The project was started with the leg part. It was chosen to make a robot with leg joints to help balance the robot, varying the length of the leg to smooth over obstacles. In order to improve the robot's grip on the ground, a silicone rubber tire was designed.

The legs are subdivided into 3 degrees of freedom each, as follows:

- Wheels: robot locomotion.
- Lower legs: robot medial angulation.
- Upper legs: they promote the angulation of the robot's base.

![bbot_leg](/assets/img/bbot/pernas_explode_ok.png){: width="350" height="350" }
_Leg components in exploded view._

### BASE Architecture

The Bbot base, on the other hand, is designed to accommodate the sensors and all of their electronics. The exploded view of the base can be seen below, and it demonstrates all the parts.

The shock absorbers (front and rear) were designed in case of robot failure and impact, protecting the sensitive parts of the sensors.

![bbot_base](/assets/img/bbot/base_explode_ok.png){: width="350" height="350" }
_Base components in exploded view._

### Implementation

Using the _Gazebo - ROS_ as a simulation tool for the environment and the robot, we were able to achieve the stability and teleoperation of **Bbot**. For this, we use the LQR controller.

<center>
<iframe width="300" height="220" src="https://www.youtube.com/embed/ycF7wwak_io" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="300" height="220" src="https://www.youtube.com/embed/yk-3Swis2Z4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

Not least, we managed to make the robot autonomous, using algorithms for navigation and location.

<center>
<iframe width="360" height="315" src="https://www.youtube.com/embed/r0i4qWGY8_Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

After the implementation and study to validate the model with the simulation, we implemented the real robot!!

<center>
<iframe width="360" height="315" src="https://www.youtube.com/embed/Q13y1XcuO6Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

The tests presented show that the robot can stabilize itself and with stand small disturbances.

### 3D model

A preview of the 3D model of Bbot can be seen below.

<center>
<div class="sketchfab-embed-wrapper"> <iframe title="Bbot - Balancing Robot" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share width="720" height="400" src="https://sketchfab.com/models/af1e9072e976453ca8ecdd8a06ac1db3/embed?autostart=1"> </iframe> <p style="font-size: 13px; font-weight: normal; margin: 5px; color: #4A4A4A;"> <a href="https://sketchfab.com/3d-models/bbot-balancing-robot-af1e9072e976453ca8ecdd8a06ac1db3?utm_medium=embed&utm_campaign=share-popup&utm_content=af1e9072e976453ca8ecdd8a06ac1db3" target="_blank" style="font-weight: bold; color: #1CAAD9;"> Bbot - Balancing Robot </a> by <a href="https://sketchfab.com/matheus.nfranca97?utm_medium=embed&utm_campaign=share-popup&utm_content=af1e9072e976453ca8ecdd8a06ac1db3" target="_blank" style="font-weight: bold; color: #1CAAD9;"> matheus.nfranca97 </a> on <a href="https://sketchfab.com?utm_medium=embed&utm_campaign=share-popup&utm_content=af1e9072e976453ca8ecdd8a06ac1db3" target="_blank" style="font-weight: bold; color: #1CAAD9;">Sketchfab</a></p></div>
</center>

### Detailed view

For more details about the project, see the project website [HERE](https://braziliansinrobotics.com/project-bbot/). We have all the steps to create this project.

Also see the following:
- Project sponsor: [Senai CIMATEC](http://www.senaicimatec.com.br/en/).
- The lab website: [Robotics & Autonomous Systems](https://braziliansinrobotics.com/).

### Development team

<center>
<div>
  <div class=" col-xl-auto offset-xl-0 col-lg-4 offset-lg-0">
    <table class="table-borderless highlight">
      <thead>
        <tr>
          <th><center><img src="{{ 'assets/img/matheus_franca.jpeg' | relative_url }}" width="100" alt="Matheus" class="img-fluid rounded-circle" /></center></th>
          <th></th>
          <th><center><img src="{{ 'assets/img/lucaslins-1.png' | relative_url }}" width="100" alt="Lucas" class="img-fluid rounded-circle" /></center></th>
          <th></th>
          <th><center><img src="{{ 'assets/img/marco.jpg' | relative_url }}" width="100" alt="Marco" class="img-fluid rounded-circle"/></center></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr class="font-weight-bolder" style="text-align: center margin-top: 0">
          <td width="33%"><center><a href="https://www.linkedin.com/in/matheus-frança-b62044150">Matheus França</a></center></td>
          <td></td>
          <td width="33%"><center><a href="linkedin.com/in/lucas-lins-souza-51b1909a">Lucas Souza</a></center></td>
          <td></td>
          <td width="33%"><center><a href="https://mhar-vell.github.io/portfolio/">Marco Reis</a></center></td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
</center>

<br>

### Project Summary

1. Category: <font color="#fbb117">Mobile Robotics</font>
3. Start date: <font color="#fbb117">May/2021</font>
4. End date: <font color="#fbb117">December/2021</font>