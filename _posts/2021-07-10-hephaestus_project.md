---
title: Hephaestus 
date: 2021-07-10 11:00:00 +/-TTTT
categories: [Robotic, Humanoid, Senai Cimatec]
tags: [robotic, ROS, Gazebo, control, CAD, biped]     # TAG names should always be lowercase
math: true
mermaid: true
pin: false
image:
  src: /assets/img/hephaestus/hephaestus_wide.png
  # width:  750   # in pixels
  # height: 750   # in pixels
  alt: Hephaestus
---

## Introduction

Hephaestus features a 22 Degrees of Freedom (DOF) articulated design. Its structure is based on Robotis models [OP3](https://emanual.robotis.com/docs/en/platform/op3/getting_started/) and [OP2](https://emanual.robotis.com/docs/en/platform/op2/getting_started/). In addition, Hephaestus is developed under [ROS](https://www.ros.org/) (Robot Operating System) to use various packages in the ROS ecosystem. All the technology involved and support for ROS, allow developers to focus more on advancing research and techniques in the field of robotics and computer vision.

The project was part of a research on anthropomorphic robot at the institution **Senai Cimatec**.

![hephaestus](/assets/img/hephaestus/hephaestus.png){: width="350" height="350" }
_Hephaestus in the final CAD_

## Components

The diagram below shows how the robot is divided. On the **head** block is the stereo camera (Mynt Eye S1030) and two controllers for changing the head orientation. The **arm** block has 6 actuators. The **spine** contains the robot's main electronics, with the controllers and the system's power supply (lipo 11.1v), in addition to the IMU, the sensor responsible for measuring the robot's inclination. In the **leg** block, 10 actuators are distributed for each leg, two of which have greater effort capacity, for the joint demand (dynamixel mx-106).

![diagram](/assets/img/hephaestus/components_diagram.png){: width="450" height="450" }
_Component diagram_

It is possible to notice that the connections between the components are divided into power (red) and data (black). The actuators are shown only with a power “line” as they are connected in a chain, so we opted for this description in the diagram.

## 3D model

A preview of the Hephaestus model can be seen below.

<div class="container"> <iframe class="responsive-iframe" title="Hephaestus" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share src="https://sketchfab.com/models/f0c0c4a783194cedb17844991a279fcc/embed?autostart=1"> </iframe> </div>

## Detailed view

For more details about the project, see the project website [HERE](https://braziliansinrobotics.com/project-hephaestus/). We have all the steps to create this project.

Also see the following:
- Project sponsor: [Senai CIMATEC](http://www.senaicimatec.com.br/en/).
- The lab website: [Robotics & Autonomous Systems](https://braziliansinrobotics.com/).

## Development team

<center>
<div>
  <div class=" col-xl-auto offset-xl-0 col-lg-4 offset-lg-0">
    <table class="table-borderless highlight">
      <thead>
        <tr>
          <th><center><img src="{{ 'assets/img/matheus_franca.jpeg' | relative_url }}" width="100" alt="Matheus" class="img-fluid rounded-circle" /></center></th>
          <th></th>
          <th><center><img src="{{ 'assets/img/breno-portela.png' | relative_url }}" width="100" alt="Breno" class="img-fluid rounded-circle"/></center></th>
          <th></th>
          <th><center><img src="{{ 'assets/img/marco.jpg' | relative_url }}" width="100" alt="Marco" class="img-fluid rounded-circle"/></center></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr class="font-weight-bolder" style="text-align: center margin-top: 0">
          <td width="33%"><center><a href="https://www.linkedin.com/in/matheus-frança-b62044150">Matheus França</a></center></td>
          <td></td>
          <td width="33%"><center><a href="https://www.linkedin.com/in/breno-portela-051270166/">Breno Portela</a></center></td>
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

## Project Summary

1. Category: <font color="#fbb117">Mobile Robotics</font>
3. Start date: <font color="#fbb117">May/2021</font>
4. End date: <font color="#fbb117">July/2021</font>