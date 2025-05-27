---
title: Bbot - Conclusion
date: 2021-12-09 12:00:00 +/-TTTT
categories: [Robotic, SBR, Senai Cimatec]
tags: [bbot] # TAG names should always be lowercase
math: true
mermaid: true
pin: false
thumbnail: /assets/img/bbot/bbot.png
image:
  src: /assets/img/bbot/bbot_wide.png
  alt: MULTI-ROBOT
---

Through the conceptual map, it is possible to visualize the main ideas and concepts addressed in Bbot and the relationships between these points. This map was developed to highlight the key aspects of the project and make it easier to understand.

![img](/assets/img/bbot/articles-img/bbot-cmap.png){: width="350" height="350" }
_Conceptual Map._

As the last stage of development of the [Bbot project](https://matheusfranca-dev.github.io/posts/bbot-project/), we decided to make a few more adjustments to the controller so that the robot could achieve smoother stability.

During some tests to implement the robot's teleoperation function, we noticed that the linear velocity reading was incorrect. The values were much higher than the robot could actually reach. The error was in the conversion from the Dynamixel encoder data to rad/s. After correcting this error, the controller's behavior changed significantly, requiring the controller to be retuned. We also observed that changing this parameter caused a lot of vibration in the robot, much more than before.

We then implemented a **moving average filter** to try to attenuate the control signal coming from the controller. However, although the response became less oscillatory, the controller became weaker. So we continued adjusting the controller parameters until we reached an ideal value for the robot to become more stable.

In the end, we managed to parameterize the controller ideally and **the robot can now balance itself** without vibrations and is much more stable!

<center>
<iframe width="720" height="315" src="https://www.youtube.com/embed/L74pwDNFQ-Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

After a few more adjustments to the Kalman filter and controller parameterization, we were able to teleoperate Bbot! We tested teleoperation in a maze and with obstacles, which Bbot overcame. We also tested the robot climbing a ramp. All these tests can be seen below.

<center>
<iframe width="720" height="315" src="https://www.youtube.com/embed/Q13y1XcuO6Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

Here is also the [link](https://drive.google.com/file/d/1hK2yDdlPlVJKzNW8LdJWVODII6iUBTKq/view?usp=sharing) to the presentation made to discuss the main ideas of Bbot with other researchers at the Center of Competence in Robotics and Autonomous Systems. This same presentation can be viewed below.

<iframe src="https://drive.google.com/file/d/1hK2yDdlPlVJKzNW8LdJWVODII6iUBTKq/preview" width='740' height='430' allowfullscreen mozallowfullscreen webkitallowfullscreen></iframe>

**Phase 1** of Bbot comes to an end, but **Phase 2** is about to begin with many new challenges and improvements!

From the development team ([Matheus França](https://www.linkedin.com/in/matheus-frança-b62044150) and [Lucas Souza](https://www.linkedin.com/in/lucas-lins-souza-51b1909a/)), a special thanks to our advisor [Marco Reis](https://mhar-vell.github.io/portfolio/) and to the important support of our colleagues [Diogo Martins](https://www.linkedin.com/in/diogo-alexandre-martins-02b528163/), [Mateus Seixas](https://www.linkedin.com/in/mateus-seixas-59296a190), [Caio Maia](https://www.linkedin.com/in/caiomaia3/) and Luiz Ledezma.

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

<!-- **************************************** MATH script **************************************** -->
<style TYPE="text/css">
code.has-jax {font: inherit; font-size: 100%; background: inherit; border: inherit;}
</style>
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
    tex2jax: {
        inlineMath: [['$','$'], ['\\(','\\)']],
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'] // removed 'code' entry
    }
});
MathJax.Hub.Queue(function() {
    var all = MathJax.Hub.getAllJax(), i;
    for(i = 0; i < all.length; i += 1) {
        all[i].SourceElement().parentNode.className += ' has-jax';
    }
});
</script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-AMS_HTML-full"></script>

> This is an automatically translated version of the original post from the site 'brazilians in robotics' (no longer available).
