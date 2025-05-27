---
title: Bbot - Assembly Process
date: 2021-08-18 12:00:00 +/-TTTT
math: true
mermaid: true
pin: false
thumbnail: /assets/img/bbot/articles-img/base_2.jpg
image:
  src: /assets/img/bbot/bbot_wide.png
  alt: MULTI-ROBOT
---

## Previously

It is important that you have seen the previous post [Bbot Simulation](http://matheusfranca-dev.github.io/articles/bbot-simulation/) for a complete understanding of the project development.

## Assembly

In the fifth stage of the [Bbot](https://matheusfranca-dev.github.io/posts/bbot-project/) construction process, we analyze the development of its assembly.

You can see the development and processing of the 3D printer in the previous post, [Bbot Mechanical Drawing](http://matheusfranca-dev.github.io/articles/bbot-mechanical-design/).

### Wheel

For greater grip of the robot on the ground, we decided to build silicone rubber wheels. With the mold and rim already 3D printed, we assembled the two and covered them with silicone.

![myImg](/assets/img/bbot/articles-img/molde_roda.jpg){: width="350" height="350" }
_Molde Roda._

![myImg](/assets/img/bbot/articles-img/roda.jpeg){: width="350" height="350" }
_Roda._

After 2 days for the rubber to cure, we opened the mold and cleaned the part, obtaining the complete wheel.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/SNo7njk5Hwg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

### Legs

Simultaneously with the wheel construction, we assembled the robot's legs. The parts were 3D printed and the materials cleaned.

![myImg](/assets/img/bbot/articles-img/perna_1.jpeg){: width="350" height="350" }
_Leg 1._

![myImg](/assets/img/bbot/articles-img/perna_2.jpeg){: width="350" height="350" }
_Leg 2._

Each leg has 2 DOFs (Degrees of Freedom), giving Bbot greater mobility to overcome obstacles.

![myImg](/assets/img/bbot/articles-img/perna_3.jpeg){: width="350" height="350" }
_Leg 3._

![myImg](/assets/img/bbot/articles-img/perna_4.jpeg){: width="350" height="350" }
_Leg 4._

The drive motor has a coupling part for the wheel, making maintenance easier. It also allows changing the wheel or its actuator without major impact on the project.

### Base

The robot's base houses all the power components and Bbot's sensors.

An essential part of self-balancing, the IMU, was placed at the center of the base, providing important feedback for balance. The shock absorbers were attached to the base to protect the LiDAR, which is in an unprotected area (on top of the robot).

![myImg](/assets/img/bbot/articles-img/base_1.jpeg){: width="350" height="350" }
_Base 1._

![myImg](/assets/img/bbot/articles-img/base_2.jpg){: width="350" height="350" }
_Base 2._

For a complete list of internal Bbot components, see the [Bbot Mechanical Drawing](http://matheusfranca-dev.github.io/articles/bbot-mechanical-design/) post.

## Results

In the **fifth stage** of the project, we present the construction of **Bbot**.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/f9vfHLqY0YA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

In the next stages, tests with the real robot will be presented.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/6xNG0_EvZec" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

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
