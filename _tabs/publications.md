---
title: Publications
icon: fas fa-file
order: 3
---

<!-- Style -->
<link rel="stylesheet" href="../assets/css/hover_publi.css" />

<!-- Btn Selector -->
<div id="myBtnContainer">
  <button class="btn ativo" onclick="filterSelection('all')"> Show all</button>
  <button class="btn" onclick="filterSelection('adam')"> Adam</button>
  <button class="btn" onclick="filterSelection('horus')"> Horus</button>
  <button class="btn" onclick="filterSelection('subot')"> SUBOT</button>
  <button class="btn" onclick="filterSelection('bbot')"> Bbot</button>
  <button class="btn" onclick="filterSelection('multi-robot')"> Multi-robot</button>
</div>

<!-- Publications -->
<div class="filterDiv multi-robot" onclick="window.location='';">
    <h2 class="category">{{"Towards Efficient Heterogeneous Multi-Robot Collaboration inDynamic Unity-Based Civil Construction Simulations (<i>Under Review</i>)"}}</h2>
    <hr style="height:2px;border-width:0;color:gray;background-color:gray">
    <p> França, Matheus and Lepikson, Herman <br>
        &bull; XII National Congress of Mechanical Engineering (CONEM) &emsp;&bull; Year: 2024 </p>
</div>

<div class="filterDiv subot" onclick="window.location='https://doi.org/10.1109/LARS/SBR/WRE59448.2023.10332970';">
    <h2 class="category">{{"Autonomous Robotic System for Visual Inspection in Electrical Substations and Cable Galleries"}}</h2>
    <hr style="height:2px;border-width:0;color:gray;background-color:gray">
    <p> França, Matheus; Lima, Rebeca; Pinheiro, Oberdan; Cerbantes, Marcel and Lepikson, Herman <br>
        &bull; 20th IEEE Latin American Robotics Symposium - LARS and 15th Brazilian Symposium on Robotics - SBR &emsp;&bull; Year: 2023 </p>
</div>

<div class="filterDiv bbot" onclick="window.location='https://doi.org/10.34178/jbth.v7i1.364';">
    <h2 class="category">{{"Design, Manufacturing and Testing of a Two-Wheeled Self-Balancing Robot"}}</h2>
    <hr style="height:2px;border-width:0;color:gray;background-color:gray">
    <p> França, Matheus and Souza, Lucas <br>
        &bull; IX International Symposium on Innovation and Technology (SIINTEC) &emsp;&bull; Year: 2023 </p>
</div>

<div class="filterDiv multi-robot" onclick="window.location='https://doity.com.br/certificados_artigos/imprimir_certificado_artigo/d15424abebcc17d790cacff9bdbe3a236b07293f';">
    <h2 class="category">{{"Heterogeneous Multi-Robot System for Manipulation and Inspection of Interesting Objects in Civil Construction"}}</h2>
    <hr style="height:2px;border-width:0;color:gray;background-color:gray">
    <p> França, Matheus and Lepikson, Herman <br>
        &bull; Conference on Complex Systems &emsp; &bull; Thematic area: Unraveling the Complexity of Industry 4.0 Technologies &emsp; &bull; Year: 2023 </p>
</div>

<div class="filterDiv subot" onclick="window.location='https://doity.com.br/certificados_artigos/imprimir_certificado_artigo/9f0fc14a1d6f34d13265a654643678f372640bb4';">
    <h2 class="category">{{"Development of an Advanced Perception System for Optimization of the Autonomy of the SUBOT Platform (<i>In Portuguese</i>)"}}</h2>
    <hr style="height:2px;border-width:0;color:gray;background-color:gray">
    <p> França, Matheus and Lima, Rebeca <br>
        &bull; VIII Seminário de Avaliação de Pesquisa Científica e Tecnológica (SAPCT) e VII Workshop de Integração e Capacitação em Processamento de Alto Desempenho (ICPAD) &emsp; &bull; Year: 2023 </p>
</div>

<div class="filterDiv adam" onclick="window.location='http://www.proceedings.blucher.com.br/article-details/adam-a-virtual-humanoid-robot-model-based-on-open-source-approach-35595';">
    <h2 class="category">{{"ADAM - A Virtual Humanoid Robot Model Based on Open-Source Approach"}}</h2>
    <hr style="height:2px;border-width:0;color:gray;background-color:gray">
    <p> França, Matheus; oliveira, Fredson and Pinheiro, Oberdan <br>
        &bull; Journal: Blucher Proceedings &emsp; &bull; Volume: 7 &emsp; &bull; Number: 2 &emsp; &bull; Year: 2020 </p>
</div>
<div class="filterDiv adam" onclick="window.location='http://www.jbth.com.br/index.php/JBTH/article/view/90';">
    <h2 class="category">{{"Humanoid Prototype Development Through 3D Printing for New Technologies"}}</h2>
    <hr style="height:2px;border-width:0;color:gray;background-color:gray">
    <p> França, Matheus; oliveira, Fredson and Pinheiro, Oberdan <br>
        &bull; Journal of Bioengineering and Technology Applied to Health &emsp; &bull; Volume: 2 &emsp; &bull; Number: 4 <br> &bull; Year: 2020 </p>
</div>
<div class="filterDiv horus" onclick="window.location='https://doity.com.br/certificados_artigos/imprimir_certificado_artigo/fe8203438726a11102539362f53c450d0723828f';">
    <h2 class="category">{{"Comparative Analysis of Multivariate Regression Methods for Calibration Between RGB Camera and 3D Laser Scanner (<i>In Portuguese</i>)"}}</h2>
    <hr style="height:2px;border-width:0;color:gray;background-color:gray">
    <p> França, Matheus and Souza, Tiago <br>
        &bull; V Seminar for Evaluation of Scientific and Technological Research (SAPCT) and IV Workshop on Integration and Training in High - Performance Processing (ICPAD) &emsp; &bull; Year: 2020 </p>
</div>
<div class="filterDiv adam" onclick="window.location='https://www.proceedings.blucher.com.br/article-details/33259';">
    <h2 class="category">{{"Development of a Humanoid Prototype Through 3D Printing for the Development of New Technologies (<i>In Portuguese</i>)"}}</h2>
    <hr style="height:2px;border-width:0;color:gray;background-color:gray">
    <p> França, Matheus; Oliveira, Fredson and Pinheiro, Oberdan <br>
        &bull; Journal: Blucher Engineering Proceedings &emsp; &bull; Volume: 6 &emsp; &bull; Number: 3 &emsp; &bull; Year: 2019 </p>
</div>

<!-- ------------------- SCRIPT ------------------- -->
<script src="{{ base.url | prepend: site.url }}/assets/js/custom/publication.js"></script>
