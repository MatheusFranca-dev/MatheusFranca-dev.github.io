---
title: Multi-Robot System
date: 2023-10-10 12:00:00 +/-TTTT
# categories: [Robotic, UFBA]
# tags: [robotic, ROS2, multi-robot, object manipulation, heterogeneous robots, simulator, computer vision, additive manufacturing, civil constructio, Pygame, Unity] # TAG names should always be lowercase
math: true
mermaid: true
pin: false
thumbnail: /assets/img/multi-robot/marl.png
image:
  src: /assets/img/multi-robot/wide-multi-robot.jpeg
  alt: MULTI-ROBOT
---

Industrial automation is undergoing significant changes due to technological advances. Although the application of robotic systems in assembly lines is a reality, civil construction has been more resistant to the adoption of these technologies. However, additive manufacturing (3D printing) has demonstrated potential to increase productivity and optimize operations on construction sites. Despite these advances, there are still specific tasks that require the presence of human workers, as current robotic systems may not be suitable to perform them. In this context, this work proposes the development of collaborative tasks in heterogeneous multi-robot environments, with an emphasis on communication and collaboration between different types of robots. To this end, a simulated environment will be developed that will allow the investigation and analysis of behavioral strategies that involve the use of computer vision to detect flaws and objects in the environment, in addition to object manipulation. The ultimate goal is to develop an adaptable system that can improve construction operations by reducing dependence on human labor for specific tasks. This study contributes to the advancement of automation in the sector, promoting greater efficiency and productivity.

## Development

The research aims to develop a simulated environment to explore and analyze computer vision strategies for detecting faults and relevant objects in the construction site, as well as object manipulation. The ultimate goal is to develop an adaptable system that can enhance operations in the construction industry, reducing the reliance on human labor for specific tasks. This study will contribute to the advancement of automation in the sector, promoting greater efficiency and productivity.

The proposed multi-robot system for construction consists of four types of robots, each with specific functions (as shown in the figure below). The blue robot (R1) is responsible for additive manufacturing of structural components using 3D printing technology. The green robot (R2) specializes in delicate object manipulation, such as tube insertion and placement of power boxes. The yellow robot (R3) inspects the printed walls to identify possible flaws and unsafe points in the work environment. Additionally, it acts as an inspector for the restart of the printing process, providing spatial coordinates where the R1 robot should begin or resume printing the structure. Drones (R4, in pink) are employed for 3D terrain scanning and mapping, enabling precise construction planning and ensuring that the additive manufacturing robot (R1) stays within designated boundaries. The purple robot (R5) creates a support surface, including beam fixation, to facilitate proper material deposition by R1. The system can also incorporate other robots (Rn, in gray) to add specific capabilities to the environment, such as object manipulation.

![robots](/assets/img/multi-robot/mission.png){: .dark .shadow .rounded-10 w='400' h='400' }
_Operating environment and robot tasks._

Effective communication and coordination among the robots are crucial for their successful operation. This includes exchanging mission status information, historical data, and mission details, requiring high data transmission bandwidth. Both synchronous and asynchronous coordination approaches are employed, ensuring efficient completion of complex tasks in the construction environment while prioritizing process efficiency and safety.

![robots](/assets/img/multi-robot/final-ray-view.png){: .dark .shadow .rounded-10 w='400' h='400' }
_Isometric view with ray sensor._

To achieve the desired set of tasks, three main blocks have been defined: (1) simulation, which defines the environment using Unity for 3D implementation and Pygame for 2D implementation; (2) application, responsible for robot control, sensing, and communication; and (3) intelligence, incorporating artificial intelligence systems to be integrated with the robots.

![robots](/assets/img/multi-robot/r2-rm-obstacle-view.png){: .dark .shadow .rounded-10 w='400' h='400' }
_Robots in Unity Simulator._

![robots](/assets/img/multi-robot/n-envs-rand-pos.png){: .dark .shadow .rounded-10 w='400' h='400' }
_Reinforcement Learning in Unity._

## Experiments

Below are three experiments: the first focuses on the use of two robots, the second involves multiple manipulation robots working together with a printing robot, and finally, an experiment using a printing robot and another for material support in hard-to-reach locations.

For a detailed view of the experiments, including videos and results, see the [publications](https://matheusfranca-dev.github.io/publications/) section of this site.

### Two-Robot Collaboration Experiment

Conducted using one robot dedicated to object manipulation and another responsible for printing ceramic construction blocks.

<center>
<iframe width="360" height="315" src="https://www.youtube.com/embed/kZLIPbeN0SQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

### Multi-Robot Manipulation and Printing Integration Experiment

In this experiment, the robots were previously trained and are fully integrated with ROS 2 and Behavior Tree CPP. In the environment, the yellow robots (R3) are responsible for identifying possible obstacles (represented by red cubes) and dragging them to a disposal area. The obstacles are categorized as small, which can be handled by a single robot; medium, which require the cooperation of two or more robots; and large, which require the collaboration of three or more robots. This behavior is essential to assist the blue robot (R1) in printing ceramic blocks in the environment, ensuring that no obstacle hinders its progress.

<center>
<iframe width="360" height="315" src="https://www.youtube.com/embed/1wFDXl8tHWQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

### Multi-Robot Collaboration Experiment in Complex Structure Printing

In this experiment, the blue robot (R1) starts the process of printing sections to simulate the construction of a door. To print in a challenging area, specifically between both sides of the door, R1 requires support. At this point, the purple robot (R4) is called by R1. This request occurs after R1 prints the left and right supports of the door. R4 then navigates to position itself in the middle of the door. This strategic position allows R1 to successfully complete the printing of the door frame.

<center>
<iframe width="360" height="315" src="https://www.youtube.com/embed/DOPk4aFZuio" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

## Conclusion

By combining collaborative multi-robot systems with additive manufacturing, this research addresses the challenges faced by the construction industry in adopting automation technologies. The study's findings will contribute to advancements in construction automation, leading to improved efficiency and productivity in the sector. This project was part of my master's degree in Mechatronics Engineering at the Federal University of Bahia, and the thesis is entitled "Collaboration of Heterogeneous Robots in a Civil Construction Environment: A Modular and Integrative Proposal (<i>In Portuguese</i>)".

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
4. Two articles produced and my Master's Thesis (for more, see the [publications](https://matheusfranca-dev.github.io/publications/) tab)
