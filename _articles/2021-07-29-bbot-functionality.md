---
title: Bbot - Features
date: 2021-07-29 12:00:00 +/-TTTT
math: true
mermaid: true
pin: false
thumbnail: /assets/img/bbot/articles-img/diagrama_funcionalidades_v2.png
image:
  src: /assets/img/bbot/bbot_wide.png
  alt: MULTI-ROBOT
---

## Previously

It is important that you have seen the previous post, [Definition of the Bbot model](http://matheusfranca-dev.github.io/articles/bbot-model-definition/), for a complete understanding of the development of the project.

In step two of the [Bbot](https://matheusfranca-dev.github.io/posts/bbot-project/) construction process, and any other robotics project, it is important to define the robot's functionalities. Before we start the next steps, the design of the robot's architecture (hands-on!), 👷🔧 we need to list these characteristics and analyze how they are connected to each other, thus having total control of the development of the project.

## Feature diagram

In the diagram built for Bbot, we can see a range of features. To make it easier to understand, let's partition the diagram into functionality sections.

![bbot_arc](/assets/img/bbot/articles-img/diagrama_funcionalidades_v2.png){: width="350" height="350" }
_Feature diagram._

### Localization

The Localization is responsible for monitoring the position and orientation of the robot within the environment in which it is contained. Using the positioning and orientation data sent by the sensors present in the perception system, this functionality provides the mapping and trajectory planning systems with a message containing the robot's position and orientation data in the environment. The Localization feature serves as the basis for other features that promote autonomy to the robot.

![bbot_loc](/assets/img/bbot/articles-img/df-localizacao.png){: width="350" height="350" }
_Localization diagram._

### Navigation

Navigation to bbot uses local and global planning to safely navigate the environment. The navigation system depends on the route planning functionality. As an output of the navigation functionality, the execution of the trajectory will be sent and, in the absence of adequate navigation, a route replanning command will be sent.

![bbot_nav](/assets/img/bbot/articles-img/df-navegacao.png){: width="350" height="350" }
_Navigation diagram._

### Perception

The Bbot's sensing system should provide the robot with the ability to perceive and translate its own conditions and the conditions of the environment in which it is inserted. These functions are ensured by the acquisition and processing of data collected from inertial sensors and optical sensors, which are integrated into the robot's structure. The perception system offers, therefore, modeling of the robot and the environment obtained by the representation of IMU, 2D LiDAR, Camera and Voltage Sensor data and by the treatment algorithms applied to these data.

The perception functionality depends on the sensory data that is embedded in the robot's structure.

The outputs of this functionality are mapping, location, detection and control.

![bbot_perception](/assets/img/bbot/articles-img/df-percepcao.png){: width="350" height="350" }
_Perception diagram._

### Mapping

Using the location information, you can create a map of the environment.

The mapping functionality depends on the perception data (3d points from the LiDAR sensor) and location.

Through the maps, it is possible to generate a global costmap and a local costmap, which is used by the trajectory planning functionality to identify the positions on the map where the robot cannot travel and by the navigation functionality to plan the robot's speed controls so that it does not collide with obstacles.

![bbot_mapping](/assets/img/bbot/articles-img/df-mapeamento.png){: width="350" height="350" }
_Mapping diagram._

### Detection

In Bbot, this functionality is responsible for detecting the TAG (important for the robot's mission). It depends on the data from the perception functionality and has as its output the trajectory planning (sending the target pose).

![bbot_detection](/assets/img/bbot/articles-img/df-deteccao.png){: width="350" height="350" }
_Detection diagram._

### Control

Defines the strategy adopted so that the robot can balance itself. In our case, the PID controller was chosen. It depends on the functionality of perception and has as output the robot's speed commands so that it can balance.

![bbot_control](/assets/img/bbot/articles-img/df-controle.png){: width="350" height="350" }
_Control diagram._

### Behavior

The behavior has the function of evaluating the situations of the environment and the state of the robot. This feature is generic and can be described as a decision-maker that ensures the proper functioning of the robot. In the case of Bbot, this feature will monitor the current battery charge and ensure that the robot interrupts its mission and signals the user if it is below a given value. This functionality, however, can be increased in the future to encompass other decisions.

![bbot_comp](/assets/img/bbot/articles-img/df-comportamento.png){: width="350" height="350" }
_Behavior diagram._

### Inactivity

It is the feature that gives the robot a position of protection for reasons of failure. It has the robot's faults as inputs and the inactivity position as output.

![bbot_ina](/assets/img/bbot/articles-img/df-inatividade.png){: width="350" height="350" }
_Inactivity diagram._

### Trajectory planning

It receives data from mapping, detection, location and navigation and, following a trajectory defined in the interface, makes an appropriate planning for the robot. It outputs the global and local path for the navigation functionality.

![bbot_traj](/assets/img/bbot/articles-img/df-planejamento_de_trajetoria.png){: width="350" height="350" }
_Trajectory diagram._

### Acting

This functionality makes it possible to control the leg and locomotion actuators. It has as input the speed commands given by the control and as output the movement commands for each joint of the robot. This feature communicates directly with the hardware.

![bbot_act](/assets/img/bbot/articles-img/df-atuacao.png){: width="350" height="350" }
_Acting diagram._

## Conclusion

In the second stage of the project, we present the features and how they are related. Based on these parameters proposed here, we can start building Bbot.

<br>

## Author

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

## References

- The original post was published on [braziliansinrobotics](https://braziliansinrobotics.com/project-bbot/), which is a project of the Brazilian Institute of Robotics (BIR). The website is no longer available, so I am reposting it here.

> This is an automatically translated version of the original post from the site 'brazilians in robotics' (no longer available).
