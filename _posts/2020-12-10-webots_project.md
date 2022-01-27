---
title: Webots
date: 2020-12-10 07:00:00 +/-TTTT
categories: [Robotic, Senai Cimatec]
tags: [mobile robotic, robotic]     # TAG names should always be lowercase
math: true
mermaid: true
pin: false
image: 
  src: /assets/img/webots/webots-banner.png
  # width: 800   # in pixels
  # height: 800   # in pixels
  alt: Webots
---

## Introduction

This project was made to carry out the simulation of the **Challenge** related to the Robotics and Autonomous Systems Laboratory to act as an undergraduate intern at SENAI CIMATEC.

The challenge was to develop an autonomous system that presents abilities to recognize the environment through sensors, providing an adequate autonomous navigation. For this we use the _WeBots_ simulator, an open-source platform to develop robots!!

The robot's mission will be to arrive in the region with a lamp, which is next to a STOP sign. The region starts right after the sign towards the lamp. The robot must always start near the START board.

<p align="center">
    <img id="myImg" src="{{ 'assets/img/webots/webots-fast.gif' | relative_url }}" alt="Nonlinear model" width="750"/>
</p>

## The path

The path was performed in 1 minute and 11 seconds in total. The explanation can be seen below:

1. For the robot to stop at the indicated location, a lightsensor has been added to its extensionSlot. 

2. A maximum value has been set for the light sensor, which indicates when it should stop.

3. The sensors have been initialized and the weights that each sensor has in relation to the robot movement selected.

4. In the simulation loop, its values were then read and the robot started moving forward.

5. Then, if the light sensor reading is greater than or equal to the set value, the robot stops (we arrived at the lamp).

6. If you haven't reached the goal yet, evaluate the weights of the sensors, deviate from the goals and go forward.

7. Steps 5 and 6 store as assigned chosen in a vector, so that it is only later assigned to the motor pair.

All code can be found in the repository by following the [link](https://github.com/MatheusFranca-dev/desafiorobotica). 

## Development team

<center>
<div>
  <div class=" col-xl-auto offset-xl-0 col-lg-4 offset-lg-0">
    <table class="table-borderless highlight">
      <thead>
        <tr>
          <th><center><img src="{{ 'assets/img/matheus_franca.jpeg' | relative_url }}" width="100" alt="Matheus" class="img-fluid rounded-circle" /></center></th>
          <th></th>
          <th><center><img src="{{ 'assets/img/marco.jpg' | relative_url }}" width="100" alt="Marco" class="img-fluid rounded-circle" /></center></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr class="font-weight-bolder" style="text-align: center margin-top: 0">
          <td width="50%"><center><a href="https://www.linkedin.com/in/matheus-frança-b62044150">Matheus França</a></center></td>
          <td></td>
          <td width="50%"><center><a href="https://mhar-vell.github.io/portfolio/">Marco Reis</a></center></td>
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
3. Start date: <font color="#fbb117">December/2020</font>
4. End date: <font color="#fbb117">December/2020</font>