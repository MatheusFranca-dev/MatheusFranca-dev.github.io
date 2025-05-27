---
title: Test Bench - System Identification
date: 2021-11-26 12:00:00 +/-TTTT
categories: [Robotic, Senai Cimatec]
tags: [robotic, ROS, identification, control, CAD, black-box] # TAG names should always be lowercase
math: true
mermaid: true
pin: false
thumbnail: /assets/img/bbot/articles-img/bancada-montagem-final-1.jpeg
image:
  src: /assets/img/testbench/sistemas_wide.png
  alt: MULTI-ROBOT
---

System identification <a href="#COELHO">[COELHO, 2004]</a> is a general term used to describe mathematical tools and algorithms that allow building dynamic models from measured data. A system can be identified through physical equations (called white-box modeling), without prior knowledge of the model (black-box modeling), or using a method that is a middle ground between the two, called gray-box modeling. For identifying the actuator model to be used in the [Bbot project](https://matheusfranca-dev.github.io/posts/bbot-project/), we will use black-box modeling.

## 3D Model

The Bbot model uses torque as the actuation signal for the wheels, but the Bbot actuator (**_Dynamixel xm430 w210_**) uses a PWM signal as input. To convert between these, a test bench was created, where a PWM signal is sent to the motor and a load cell measures the resulting torque.

With this setup, the bench was modeled to allow for these measurements. Below are detailed images of the final bench model.

![testbench-parts](/assets/img/testbench/bancada-explode.png){: width="450" height="400" }
_Test bench in exploded view._

The final bench includes a HUB that supports Dynamixel actuators. Attached to the bench is a 7’’ touchscreen display for the Raspberry Pi 4, allowing the bench to operate autonomously without an external computer. The rendered final model can be seen below.

![testbench-final](/assets/img/testbench/Bancada_de_Teste-new-xm.png){: width="600" height="450" }
_Test bench rendering._

The bench can be easily modified to fit other actuator models; simply copy the model made in **_Onshape_** from this [LINK](https://cad.onshape.com/documents/01cdebe787723337d2d1b1ac/w/ce70b1c60790b8abc436805b/e/980676df2978221cc57a94a0) and make the desired changes. Below is the Dynamixel MX-106 motor also mounted on the bench.

![testbench-parts](/assets/img/bbot/articles-img/bancada.gif){: width="450" height="400" }
_Test bench._

With the 3D model of the bench completed, we move on to modeling the system identification program.

## System Identification

System identification is divided into several steps, described below:

### Data Collection

With the test bench assembled, a step signal is sent to the actuator. The actuator, with the HUB attached, applies force to the load cell. The program then saves a file (dataset) with the input signal, output signal, and the elapsed time for each test signal.

![testbench-parts](/assets/img/bbot/articles-img/coleta-dados.png){: width="450" height="400" }
_Data collection._

### Data Processing and Refinement

With the collected data, we use a Python program ([LINK](https://github.com/Brazilian-Institute-of-Robotics/bir_strength-test-bench/blob/feature/dxl_command/ModelCurve/plotData.ipynb)) for the next steps. To start refining, we calculate the system signal by subtracting the mean from the torque values.

```signal = torque - np.mean(torque)```

Next, we compute the discrete Fourier transform using the numpy library ([LINK](https://numpy.org/doc/stable/reference/routines.fft.html)). The function ```np.fft.fft``` computes the one-dimensional discrete Fourier transform (DFT) using the Fast Fourier Transform (FFT) algorithm.

![testbench-parts](/assets/img/bbot/articles-img/output_signal_fft.png){: width="450" height="400" }
_Output Signal FFT._

We then use the FIR filter, a type of digital filter characterized by an impulse response that becomes zero after a finite time <a href="#OLIVEIRA">[OLIVEIRA, 2007]</a>. Using ```lfilter```, we filter a data sequence x with a digital filter. For more on the filter, see [LINK](https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.lfilter.html).

Finally, we cut off signals with values below 0, resulting in the following signal:

![testbench-parts](/assets/img/bbot/articles-img/output_torque_filtered.png){: width="450" height="400" }
_Output Torque Filtered._

### Model

After these steps, we use the [SIPPY](https://github.com/CPCLAB-UNIPI/SIPPY) library to identify the system. The main goal of this code is to provide different identification methods to build linear models of dynamic systems. For this, we use its internal ARX model (Autoregressive with Extra Input) <a href="#RIBEIRO">[RIBEIRO]</a>. The resulting first-order model is:

<!-- MATH modelo -->
<p align="center">
$$
\frac{0.0006618}{z - 0.8444}, dt = 0.0125
$$
</p>

## Results

The 3D project was successfully assembled, resulting in a test bench with its own autonomy for collecting black-box models. The final assembled test bench can be seen below.

![testbench-parts](/assets/img/bbot/articles-img/bancada-montagem-final-1.jpeg){: width="450" height="400" }
_Model Assembled._

The final model allowed us to control the Bbot correctly, as shown in the control post ([LINK](http://matheusfranca-dev.github.io/articles/bbot-first-time-standing/)). The figure below shows the input torque signal in orange and the identified model from the test bench in blue.

![testbench-parts](/assets/img/bbot/articles-img/output_model.png){: width="450" height="400" }
_Output Model._

To download the test bench code, go to the [github link](https://github.com/Brazilian-Institute-of-Robotics/bir_strength-test-bench/tree/feature/dxl_command) and follow the steps in the Readme.

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

1. <a id="COELHO">COELHO, Antonio Augusto Rodrigues; DOS SANTOS COELHO, Leandro. **Identificação de sistemas dinâmicos lineares. 2004**.
1. <a id="OLIVEIRA">OLIVEIRA, EEC; CORREIA, SEN; MENDONÇA, L. M. Implementação do filtro de resposta finita (FIR) não recursivo através do método das janelas. In: **II CONGRESSO DE PESQUISA E INOVAÇÃO DA REDE NORTE NORDESTE DE EDUCAÇÃO TECNOLÓGICA**. 2007.
1. <a id="RIBEIRO">RIBEIRO, David A. et al. **Validação de modelo linear ARX com base em métodos clássicos de identificação**.

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
