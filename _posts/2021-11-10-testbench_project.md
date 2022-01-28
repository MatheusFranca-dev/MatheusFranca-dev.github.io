---
title: Test Bench
date: 2021-11-10 12:00:00 +/-TTTT
categories: [Robotic, Senai Cimatec]
tags: [robotic, ROS, identification, control, CAD, black-box]     # TAG names should always be lowercase
math: true
mermaid: true
pin: false
image:
  src: /assets/img/testbench/sistemas_wide.png
  # width:  750   # in pixels
  # height: 750   # in pixels
  alt: BBOT
---

## Introduction

System identification is a generic term used to describe the mathematical tools and algorithms that allow building dynamic models from measured data. We can identify a system through equations of physics (called white box), we can identify systems without knowing the previous model (black box model) and we still have a method that is a middle ground between the white box and the black box, called gray box.

The Test Bench project was a project related to the [Bbot robot](https://matheusfranca-dev.github.io/posts/bbot-project/) and aims to identify the model of the actuators that will be used in it. We will use the black box identification model.

## Operation

The operation of the bench will contain the following logic:

- **Input:** actuator command signal (PWM) and related speed.
- **Output:** torque measured by a load cell and speed measured by an infrared sensor.

Below we show the parts in detail of the final model of the bench.

![testbench-parts](/assets/img/testbench/bancada-explode.png){: width="450" height="400" }
_Test bench in exploded view._

The final bench has a HUB that supports Dynamixel actuators. Attached to the bench is a 7'' touchscreen display for the Raspberry Pi 4, this gives the bench autonomy to work without the use of an external computer. The rendering of the final model can be seen below.

![testbench-final](/assets/img/testbench/Bancada_de_Teste-new-xm.png){: width="600" height="450" }
_Test bench rendering._

## Modifications

The bench can be easily modified to couple other actuator models, just copy the model made in the Onshape software in this [LINK](https://cad.onshape.com/documents/01cdebe787723337d2d1b1ac/w/ce70b1c60790b8abc436805b/e/980676df2978221cc57a94a0) and make the desired modifications.

<center>
<img id="myImg" src="{{ 'assets/img/testbench/Bancada.gif' | relative_url }}" alt="testbench" width="450"/>
</center>

## Model

### 3D preview

A preview of the Test Bench 3D model can be seen below.

<div class="container"> <iframe class="responsive-iframe" title="Test Bench" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share src="https://sketchfab.com/models/5a05062f95ea4d2cb1fdbb6d71deb2ee/embed"> </iframe> </div>

### Real model

The 3D project was correctly assembled, resulting in an autonomous bench for collecting models in the black box type.

![testbench-real](/assets/img/testbench/bancada-montagem-final-2.jpg){: width="400" height="250" }
_Test bench final._


## System identification

For identification we have the following steps:

- **Data collection:** A step-type signal is sent to the actuator, which makes an effort on the load cell. The program then saves the dataset with the input, output and elapsed time.
- **Data processing and refinement:** We use some filters and signal clipping to clean the data.
- **Model:** Using the [SIPPY](https://github.com/CPCLAB-UNIPI/SIPPY) library, we identify the system. For this, we use ARX (Autoregressive with Extra Input) as its internal model.

The model can be seen in the equation below.

$$
\frac{0.0006618}{z-0.8444}, d t=0.0125
$$

The following figure shows the torque input signal in orange and the model identified with the test bench in blue.

![model](/assets/img/testbench/output_model.png){: width="400" height="250" }
_Model identified_

The 3D project was assembled correctly, resulting in a standalone bench for collecting black box models.

For more details, including how to get the actuator model, see the project website link in the next section (detailed view).

## Detailed view

For more details about the project, see the project website [HERE](https://mhar-vell.github.io/rasc/2021-11-26-bbot-strength-test-bench/). We have all the steps to create this project.

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
          <td width="33%"><center><a href="https://linkedin.com/in/lucas-lins-souza-51b1909a">Lucas Souza</a></center></td>
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
3. Start date: <font color="#fbb117">August/2021</font>
4. End date: <font color="#fbb117">November/2021</font>