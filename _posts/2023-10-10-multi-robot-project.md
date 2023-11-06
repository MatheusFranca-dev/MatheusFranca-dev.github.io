---
title: Multi-Robot System
date: 2023-10-10 12:00:00 +/-TTTT
categories: [Robotic, UFBA]
tags: [robotic, ROS2, multi-robot, object manipulation, heterogeneous robots, simulator, computer vision, additive manufacturing, civil constructio, Pygame, Unity] # TAG names should always be lowercase
math: true
mermaid: true
pin: false
image:
  src: /assets/img/multi-robot/wide-multi-robot.jpeg
  alt: MULTI-ROBOT
---

Industrial automation is undergoing significant changes due to technological advances. Although the application of robotic systems in assembly lines is a reality, civil construction has been more resistant to the adoption of these technologies. However, additive manufacturing (3D printing) has demonstrated potential to increase productivity and optimize operations on construction sites. Despite these advances, there are still specific tasks that require the presence of human workers, as current robotic systems may not be suitable to perform them. In this context, this work proposes the development of collaborative tasks in heterogeneous multi-robot environments, with an emphasis on communication and collaboration between different types of robots. To this end, a simulated environment will be developed that will allow the investigation and analysis of behavioral strategies that involve the use of computer vision to detect flaws and objects in the environment, in addition to object manipulation. The ultimate goal is to develop an adaptable system that can improve construction operations by reducing dependence on human labor for specific tasks. This study contributes to the advancement of automation in the sector, promoting greater efficiency and productivity.

## Development

The research aims to develop a simulated environment to explore and analyze computer vision strategies for detecting faults and relevant objects in the construction site, as well as object manipulation. The ultimate goal is to develop an adaptable system that can enhance operations in the construction industry, reducing the reliance on human labor for specific tasks. This study will contribute to the advancement of automation in the sector, promoting greater efficiency and productivity.

The proposed multi-robot system for construction consists of four types of robots, each with specific functions (as shown in the figure below). The blue robot (R1) is responsible for additive manufacturing of structural components using 3D printing technology. The green robot (R2) specializes in delicate object manipulation, such as tube insertion and placement of power boxes. The yellow robot (R3) inspects the printed walls to identify possible flaws and unsafe points in the work environment. Additionally, it acts as an inspector for the restart of the printing process, providing spatial coordinates where the R1 robot should begin or resume printing the structure. Drones (R4, in pink) are employed for 3D terrain scanning and mapping, enabling precise construction planning and ensuring that the additive manufacturing robot (R1) stays within designated boundaries. The purple robot (R5) creates a support surface, including beam fixation, to facilitate proper material deposition by R1. The system can also incorporate other robots (Rn, in gray) to add specific capabilities to the environment, such as object manipulation.

![robots](/assets/img/multi-robot/mission.png){: .dark .shadow .rounded-10 w='700' h='700' }
_Operating environment and robot tasks._

Effective communication and coordination among the robots are crucial for their successful operation. This includes exchanging mission status information, historical data, and mission details, requiring high data transmission bandwidth. Both synchronous and asynchronous coordination approaches are employed, ensuring efficient completion of complex tasks in the construction environment while prioritizing process efficiency and safety.

To achieve the desired set of tasks, three main blocks have been defined: (1) simulation, which defines the environment using Unity for 3D implementation and Pygame for 2D implementation; (2) application, responsible for robot control, sensing, and communication; and (3) intelligence, incorporating artificial intelligence systems to be integrated with the robots.

By combining collaborative multi-robot systems with additive manufacturing, this research addresses the challenges faced by the construction industry in adopting automation technologies. The study's findings will contribute to advancements in construction automation, leading to improved efficiency and productivity in the sector. This project is part of my master's degree in Mechatronics Engineering at the Federal University of Bahia, the thesis is entitled "HETEROGENEOUS MULTI-ROBOT SYSTEM FOR HANDLING AND INSPECTION OF OBJECTS IN THE CONSTRUCTION INDUSTRY" and is currently in progress.

## Development team

<center>
<div>
  <div class=" col-xl-auto offset-xl-0 col-lg-4 offset-lg-0">
    <table class="table-borderless highlight">
      <thead>
        <tr>
          <th><center><img src="{{ 'assets/img/matheus_franca.jpeg' | relative_url }}" width="100" alt="Matheus" class="img-fluid rounded-circle" /></center></th>
          <th></th>
          <th><center><img src="{{ 'assets/img/herman-lepikson.png' | relative_url }}" width="100" alt="Herman" class="img-fluid rounded-circle"/></center></th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr class="font-weight-bolder" style="text-align: center margin-top: 0">
          <td width="50%"><center><a href="https://www.linkedin.com/in/matheus-frança-b62044150">Matheus França</a></center></td>
          <td></td>
          <td width="50%"><center><a href="http://lattes.cnpq.br/1115148358376830">Herman Lepikson</a></center></td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
</center>

<br>

## Project Summary

1. Category: <font color="#fbb117">Multi-Robot System</font>
2. Start date: <font color="#fbb117">May/2022</font>
3. Expected end date: <font color="#fbb117">July/2024</font>
4. Total articles produced: 1 (for more, see the [publications](https://matheusfranca-dev.github.io/publications/) tab)
