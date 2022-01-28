---
title: DRoILT
date: 2021-04-10 7:00:00 +/-TTTT
categories: [Robotic, Vision, Senai Cimatec]
tags: [robotic, ROS, computer vision, PTL]     # TAG names should always be lowercase
math: true
mermaid: true
pin: false
image:
  src: /assets/img/droilt/droilt.png
  # width:  750   # in pixels
  # height: 750   # in pixels
  alt: DRoILT
---

## Introduction

Many studies have been carried out with the aim of developing autonomous robots to travel along power transmission lines (PTL) to carry out inspection and repair. DRoILT is an autonomous mobile robot that moves on electrical power lines and can overcome different types of obstacles.

## Overview

The electrical energy generated in Brazil has the largest source of production in hydroelectric plants, thermoelectric plants, wind farms and nuclear plants. These sources generally need to be distributed to consumers in regions far from their production, for which PTL (power transmission lines) are used. According to the ONS ((from portugues: Operador Nacional do Sistema Elétrico)) in 2019, Brazil had about 141,000 km of electric power lines, with a perspective of 185,000 km by 2023, with voltages above 100 kV. With the increase in energy supply, it is also necessary to think about the maintenance plans of these PTLs.

PTL inspections in the Brazilian electrical system are still carried out by helicopters, professionals suspended in the PTL, foot patrol along the line's trajectory or with drones. These solutions require a high level of expertise, are expensive, difficult to access and can pose risks to the professional's life.

## Objective

The objective of this project is the simulation of the PTL Inspection Robot called DRoILT, using the Gazebo 9 tool in the Ros Noetic framework. The objective is that the robot can inhabit the PTL and overcome obstacles autonomously, and that it can perform visual inspection of these PTLs while energized.

The robot will use a navigation and simultaneous localization system for its mapping and detailed identification of obstacles present on the line.

## DRoILT robot analysis

The DRoILT robot was developed with three robotic arms arranged in line and driven by a set of pulleys. The robot can be divided into three modules:

The **left module** is designed with a set of pulleys and a
traction unit. 

![left module](/assets/img/droilt/droilt_l_mod.png){: width="350" height="350" }
_DRoILT robot left module._

The **central module** has a vertical rod and a pulley. It also
includes the central electronics.

![central module](/assets/img/droilt/droilt_c_mod.png){: width="350" height="350" }
_DRoILT robot central module._

The **right module** is a mirror of the left module.

![right module](/assets/img/droilt/droilt_r_mod.png){: width="350" height="350" }
_DRoILT robot right module._

The final model proposed has a approximated external dimensions of 1680 x 140 x 650 (W x W x H [mm]).

![dimensions](/assets/img/droilt/droilt_dim.png){: width="350" height="350" }
_DRoILT robot dimensions._

With its modularity, it manages to overcome different types of obstacles.

## Simulation

Below, the DRoILT is shown moving on the power line in the gazebo simulation.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/JjwrBjy1wnE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

<br>

The next video features the DRoILT robot overcoming an obstacle.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/tA8hgesh7sQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

## Detailed view

For more details about the project, see the project website [HERE](https://braziliansinrobotics.com/project-droilt/). We have all the steps to create this project.

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
          <th><center><img src="{{ 'assets/img/jean-paulo.png' | relative_url }}" width="100" alt="Jean" class="img-fluid rounded-circle"/></center></th>
          <th></th>
          <th><center><img src="{{ 'assets/img/marco.jpg' | relative_url }}" width="100" alt="Marco" class="img-fluid rounded-circle"/></center></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr class="font-weight-bolder" style="text-align: center margin-top: 0">
          <td width="33%"><center><a href="https://www.linkedin.com/in/matheus-frança-b62044150">Matheus França</a></center></td>
          <td></td>
          <td width="33%"><center><a href="https://www.linkedin.com/in/jean-paulo-990594127/">Jean Paulo</a></center></td>
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
3. Start date: <font color="#fbb117">April/2021</font>
4. End date: <font color="#fbb117">April/2021</font>