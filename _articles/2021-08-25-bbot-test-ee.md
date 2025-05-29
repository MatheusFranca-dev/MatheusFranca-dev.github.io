---
title: Bbot - Electronic Tests
date: 2021-08-25 12:00:00 +/-TTTT
math: true
mermaid: true
pin: false
thumbnail: /assets/img/bbot/articles-img/base_explode.png
image:
  src: /assets/img/bbot/bbot_wide.png
  alt: MULTI-ROBOT
---

## Previously

It is important that you have seen the previous post [Bbot Assembly](http://matheusfranca-dev.github.io/articles/bbot-assembly/) for a complete understanding of the project development.

## Introduction

With the selection of the parts to assemble the robot, it was necessary to carry out physical tests to understand and validate the chosen components.

This post covers the electronic tests, showing the setup, date, and results found.

## Electronics Testing

The electronics tests are divided according to the respective components. We started the tests on June 10, 2021, with the stepper motor.

### Test 1 - Stepper

**Date:** 06/10/2021

The tests were carried out with the following setup:

- NEMA 17 stepper motor
- Sparkfun driver (Big Easy Driver)
- OpenCM9.04

The NEMA 17 stepper motor was tested with the OpenCM904 microcontroller (STM32) interfacing with the Sparkfun Big Easy Driver. The motor driver was powered with 11.1 V from a bench power supply, and the OpenCM904 was powered via the computer's USB. The algorithm used was a test example from Sparkfun's own website.

All components worked as expected. Only the stepper motor showed concerning results, not having enough torque for the robot's weight. It was then decided to replace the actuator with a __*Dynamixel XM430-W210-R* (tests shown later in the post).

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/LyrG0p-TM_Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

### Test 2 - Gyro GS-12

**Date:** 06/14/2021

The tests were carried out with the following setup:

- ROBOTIS GS-12 gyro sensor
- OpenCM9.04

The test was performed with an algorithm to read the sensor's output values. The __*OpenCM*__ board was powered by USB, and we had to use a non-standard cable for the sensor, as its supply was 5V but the OpenCM only provided 3.3V.

The sensor proved accurate for angular velocity measurements, with output between 0 ~ 1000 for w = [-300º/s : 300º/s], and a stable output around 450. However, it was found that angular position data would also be needed. Therefore, we will switch to an IMU with a __*MPU6050*__ chip (tests shown later in the post).

### Test 3 - Phidgets 1135 Voltage Sensor

**Date:** 06/14/2021

The tests were carried out with the following setup:

- Precision Voltage Sensor 1135
- Bench power supply
- LiPO 3S
- OpenCM904

The tests were performed in two ways, with a bench power supply and with an 11.1 V LiPO battery. The output was read by the OpenCM904's analog input.

The sensor showed stable readings for voltages below 10V. Above this value, the reading became quite noisy. We believe this is because the OpenCM904's analog reference is 3.3V, but the sensor's output is 5V. Voltages of 11.1V with the bench supply resulted in an output of approximately 3.27 V, but this value was already enough to add noise to the _OpenCM904_ reading. To continue using this sensor, an alternative is to indicate voltage below the minimum (e.g., 10V) if the reader shows a high number of consecutive readings within a small range, which proves stability and, therefore, that the voltage is below 10V.

### Test 4 - Dynamixel MX-106

**Date:** 06/15/2021

The tests were carried out with the following setup:

- Dynamixel MX-106
- OpenCM904
- OpenCM485 Expansion board

The test was performed by powering the _OpenCM485_ with a bench supply at 11.1V and connecting the _OpenCM904_ to it. After configuring all IDs (141, 151, 112, 122) and Baudrate (1Mbps), some Dynamixel example codes were tested for position and speed control.

The Dynamixel showed satisfactory results for speed and position control. The position ranges from 0 - 306º (0 ~ 4095) and the speed from 0 to 41 rpm (-1023 ~ 1023), for a voltage of 11.1 V.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/s95iISFyurc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

<br>

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/-lRE_ntTgp0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

### Test 5 - MPU6050

**Date:** 06/15/2021

The tests were carried out with the following setup:

- IMU MPU6050
- Raspberry Pi

The test was performed with the IMU MPU6050 connected to a Raspberry Pi running Ubuntu 20.04 + ROS Noetic. The IMU communicated with the Raspberry via I2C protocol, and a ROS package [mpu6050_driver](https://github.com/Brazilian-Institute-of-Robotics/mpu6050_driver) processed the data and published orientation, angular velocity, and angular acceleration to ROS topics.

It was possible to read the data via terminal, and they were consistent with the movements applied to the sensor.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/d2jDFID_kvw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

### Test 6 - Dynamixel XM430-W210-R

**Date:** 07/16/2021

The tests were carried out with the following setup:

- Dynamixel XM430-W210-R
- OpenCM904
- OpenCM485 Expansion board

The test was performed by powering the OpenCM485 with a bench supply between 11.1V ~ 14.8V and connecting the OpenCM904 to it. Only standard Dynamixel codes for speed control were tested, as this actuator will replace the Nema 17 for wheel movement.

The Dynamixel showed satisfactory results for speed control. At 14.8 V it reaches a speed of approximately 95 rpm.

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/ku5Ztdp1ibE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

<br>

<div class="container"> <iframe class="responsive-iframe" src="https://www.youtube.com/embed/E79M9DK45sI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

## Results

At this stage of the project, we presented the electronics tests of **Bbot**.

The results for the electronic tests were presented in their respective descriptions. For the next steps, tests with the real robot will be presented, demonstrating the PID control and its adjustments.

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
