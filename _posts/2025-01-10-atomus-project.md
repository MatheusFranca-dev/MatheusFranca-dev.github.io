---
title: Atomus Humanoid
date: 2025-01-10 12:00:00 +/-TTTT
# categories: [Robotic, UFBA]
# tags: [robotic, ROS2, multi-robot, object manipulation, heterogeneous robots, simulator, computer vision, additive manufacturing, civil constructio, Pygame, Unity] # TAG names should always be lowercase
math: true
mermaid: true
pin: false
thumbnail: /assets/img/atomus/atomus-tb.png
image:
  src: /assets/img/adam/evolution.jpg
  alt: HUMANOID-ROBOT
---

Atomus is a custom-designed humanoid robot developed to explore advanced locomotion control strategies. The idea is to create an open-source platform that allows researchers and enthusiasts to experiment with various control algorithms, including reinforcement learning (RL), imitation learning, model predictive control (MPC), and more. The robot is designed to be modular and adaptable, making it suitable for a wide range of research applications in robotics.

## Project Overview and 3D Model

Designed using [Onshape](https://www.onshape.com/en/), the robot features a total of 21 degrees of freedom (DoF): six in each leg, one in the hip, and four in each arm. Equipped with a Velodyne VLP-16 LiDAR sensor as its head and a stereo camera on its chest, Atomus is designed for enhanced environmental perception. The actuators powering Atomus are Xiaomi CyberGear Micromotors, known for their compact design and precise control capabilities.

<div markdown="1" style="display: flex; gap: 1rem; justify-content: center;  align-items: center;">
  ![robot](/assets/img/atomus/atomus-cad-1.png){: .left .shadow .rounded-10 width="300" height="300"}
  ![robot](/assets/img/atomus/atomus-cad-3.png){: .left .shadow .rounded-10 width="300" height="300"}
  _(a) Atomus humanoid in default position (b) Atomus humanoid in custom position_
</div>

Atomus is a 1 meter tall humanoid robot, designed to be lightweight and compact. The robot's design is inspired by the human body structure, featuring a torso, arms, and legs that mimic human proportions.

A preview of the 3D model of Atomus can be seen below.

<div class="container"> <iframe class="responsive-iframe" title="Atomus - Humanoid" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share  width="360" height="315" src="https://sketchfab.com/models/83c910f92a694f889e7e5e15ebbb4df8/embed"> </iframe> </div>

## Initial Development and Simulation

The development of Atomus began with simulations inspired by a MATLAB-based walking control tutorial <a href="#CASTRO">[CASTRO, 2019]</a>, which provided foundational insights into bipedal locomotion control. This initial phase focused on implementing basic walking patterns and understanding the dynamics involved in humanoid gait.

The first result (video) showcases the implementation of <a href="#CASTRO">[CASTRO, 2019]</a> control method, with their humanoid 3D model recreated in [Gazebo](https://gazebosim.org/home) and [ROS2 Jazzy](https://docs.ros.org/en/jazzy/index.html). It demonstrates the foundational walking patterns and control strategies.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/B1VEYI8TX2I" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

<br>

The second result (video) presents the Atomus robot with integrated CAD files, inertia, and other parameters in Gazebo, utilizing the preview control method <a href="#KAJITA">[KAJITA, 2003]</a> and <a href="#RUDIAWAN">[RUDIAWAN, 2019]</a>. This demonstrates the progression towards a more refined and realistic simulation.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/_Xw3JlLqzfo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

<br>

In both videos, visual indicators are used to represent key dynamic parameters:

- **Yellow Sphere**: Denotes the Zero Moment Point (ZMP), indicating the point where the resultant moment due to gravity and inertia forces equals zero.
- **Green Sphere**: Represents the Center of Mass (CoM) of the robot, crucial for maintaining balance during locomotion.

As part of the motion planning stack, I also developed an inverse kinematics (IK) solver tailored for Atomus’s kinematic structure. This solver is based on the methodology proposed by <a href="#RUDIAWAN_2020">[RUDIAWAN, 2020]</a>. The integration of this IK solution is crucial for generating feasible joint trajectories that support stable locomotion.

## Conclusion

The Atomus project exemplifies the integration of advanced control methods and hardware design in humanoid robotics. As development continues, future blog posts will delve deeper into the application of reinforcement learning for bipedal locomotion and the implementation of sophisticated localization algorithms. Code repositories and detailed technical documentation will also be made available to contribute to the broader robotics community.

## Development team

<center>
<div>
  <div class=" col-xl-auto offset-xl-0 col-lg-4 offset-lg-0">
    <table class="table-borderless highlight">
      <thead>
        <tr>
          <th><center><img src="{{ 'assets/img/matheus_franca.jpeg' | relative_url }}" width="100" alt="Matheus" class="img-fluid rounded-circle" /></center></th>
        </tr>
      </thead>
      <tbody>
        <tr class="font-weight-bolder" style="text-align: center margin-top: 0">
          <td width="50%"><center><a href="https://www.linkedin.com/in/matheus-frança-b62044150">Matheus França</a></center></td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
</center>

<br>

## Project Summary

1. Category: <font color="#fbb117">Marine Robot</font>
2. Start date: <font color="#fbb117">2025</font>
3. Expected end date: <font color="#fbb117">2027</font>

## References

1. <a id="CASTRO">CASTRO, Sebastian, et al. **MathWorks Student Lounge - Walking Robot Control** (2019). https://github.com/mathworks-robotics/msra-walking-robot/ [Accessed 29 May. 2025].
2. <a id="RUDIAWAN">RUDIAWAN, Eko. **Omnidirectional Walking Pattern Generation for Humanoid Robot using ZMP Preview Control** (2019). https://github.com/ekorudiawan/Omnidirectional-Walking-ZMP-Preview-Control/ [Accessed 29 May. 2025].
3. <a id="RUDIAWAN_2020">RUDIAWAN, Eko. **Leg IK Humanoid-Robot** (2020). https://github.com/ekorudiawan/Leg-IK-Humanoid-Robot/ [Accessed 29 May. 2025].
4. <a id="KAJITA">KAJITA, Shuuji, et al. **Biped walking pattern generation by using preview control of zero-moment point**. 2003 IEEE International Conference on Robotics and Automation (Cat. No. 03CH37422). Vol. 2. IEEE, 2003.
