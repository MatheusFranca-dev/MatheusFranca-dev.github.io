---
title: Publications
icon: fas fa-file
order: 3
---

<link rel="stylesheet" href="../assets/css/hover_publi.css" />

<div id="myBtnContainer">
  <button class="btn ativo" onclick="filterSelection('all')"> Show all</button>
  <button class="btn" onclick="filterSelection('adam')"> Adam</button>
  <button class="btn" onclick="filterSelection('horus')"> Horus</button>
</div>

<div class="container">
    <div class="filterDiv adam" style="background-color:rgba(255, 255, 255, 0.05);color:white;padding:20px; cursor: pointer;" onclick="window.location='http://www.brazilianjournals.com/index.php/BASR/article/view/15611/12841';">
        <h2 class="category">{{"DESENVOLVIMENTO DE UM PROTÓTIPO HUMANOIDE POR MEIO DE IMPRESSÕES 3D PARA DESENVOLVIMENTO DE NOVAS TECNOLOGIAS"}}</h2>
        <hr style="height:2px;border-width:0;color:gray;background-color:gray">
        <p> Matheus Henrique Nunes França, Fredson da Silva Oliveira and Oberdan Rocha Pinheiro <br>
            &bull; Journal: Brazilian Applied Science Review &emsp; &bull; Volume: 4 &emsp; &bull; Number: 4 &emsp; &bull; Year: 2020 </p>
    </div>
    <div class="filterDiv adam" style="background-color:rgba(255, 255, 255, 0.05);color:white;padding:20px; cursor: pointer;" onclick="window.location='http://www.proceedings.blucher.com.br/article-details/adam-a-virtual-humanoid-robot-model-based-on-open-source-approach-35595';">
        <h2 class="category">{{"ADAM-A VIRTUAL HUMANOID ROBOT MODEL BASED ON OPEN SOURCE APPROACH"}}</h2>
        <hr style="height:2px;border-width:0;color:gray;background-color:gray">
        <p> Matheus Henrique Nunes França, Fredson da Silva Oliveira and Oberdan Rocha Pinheiro <br>
            &bull; Journal: Blucher Proceedings &emsp; &bull; Volume: 7 &emsp; &bull; Number: 2 &emsp; &bull; Year: 2020 </p>
    </div>
    <div class="filterDiv adam" style="background-color:rgba(255, 255, 255, 0.05);color:white;padding:20px; cursor: pointer;" onclick="window.location='http://www.jbth.com.br/index.php/JBTH/article/view/90';">
        <h2 class="category">{{"HUMANOID PROTOTYPE DEVELOPMENT THROUGH 3D PRINTING FOR NEW TECHNOLOGIES"}}</h2>
        <hr style="height:2px;border-width:0;color:gray;background-color:gray">
        <p> Matheus Henrique Nunes França, Fredson da Silva Oliveira and Oberdan Rocha Pinheiro <br>
            &bull; Journal of Bioengineering and Technology Applied to Health &emsp; &bull; Volume: 2 &emsp; &bull; Number: 4 <br> &bull; Year: 2020 </p>
    </div>
    <div class="filterDiv horus" style="background-color:rgba(255, 255, 255, 0.05);color:white;padding:20px; cursor: pointer;" onclick="window.location='https://doity.com.br/certificados_artigos/imprimir_certificado_artigo/fe8203438726a11102539362f53c450d0723828f';">
        <h2 class="category">{{"ANÁLISE COMPARATIVA DE MÉTODOS DE REGRESSÃO MULTIVARIADA PARA CALIBRAÇÃO ENTRE CÂMERA RGB E SCANNER LASER 3D"}}</h2>
        <hr style="height:2px;border-width:0;color:gray;background-color:gray">
        <p> Matheus Henrique Nunes França e Tiago Souza <br>
            &bull; Centro Universitário SENAI CIMATEC - Doity &emsp; &bull; Year: 2020 </p>
    </div>
    <div class="filterDiv adam" style="background-color:rgba(255, 255, 255, 0.05);color:white;padding:20px; cursor: pointer;" onclick="window.location='https://www.proceedings.blucher.com.br/article-details/33259';">
        <h2 class="category">{{"DESENVOLVIMENTO DE UM PROTÓTIPO HUMANOIDE POR MEIO DE IMPRESSÕES 3D PARA DESENVOLVIMENTO DE NOVAS TECNOLOGIAS"}}</h2>
        <hr style="height:2px;border-width:0;color:gray;background-color:gray">
        <p> Matheus Henrique Nunes França, Fredson da Silva Oliveira and Oberdan Rocha Pinheiro <br>
            &bull; Journal: Blucher Proceedings &emsp; &bull; Volume: 6 &emsp; &bull; Number: 3 &emsp; &bull; Year: 2019 </p>
    </div>
</div>





<!-- ------------------- SCRIPT ------------------- -->
<script>
filterSelection("all")
function filterSelection(c) {
  var x, i;
  x = document.getElementsByClassName("filterDiv");
  if (c == "all") c = "";
  for (i = 0; i < x.length; i++) {
    w3RemoveClass(x[i], "show");
    if (x[i].className.indexOf(c) > -1) w3AddClass(x[i], "show");
  }
}

function w3AddClass(element, name) {
  var i, arr1, arr2;
  arr1 = element.className.split(" ");
  arr2 = name.split(" ");
  for (i = 0; i < arr2.length; i++) {
    if (arr1.indexOf(arr2[i]) == -1) {element.className += " " + arr2[i];}
  }
}

function w3RemoveClass(element, name) {
  var i, arr1, arr2;
  arr1 = element.className.split(" ");
  arr2 = name.split(" ");
  for (i = 0; i < arr2.length; i++) {
    while (arr1.indexOf(arr2[i]) > -1) {
      arr1.splice(arr1.indexOf(arr2[i]), 1);     
    }
  }
  element.className = arr1.join(" ");
}

// Add active class to the current button (highlight it)
var btnContainer = document.getElementById("myBtnContainer");
var btns = btnContainer.getElementsByClassName("btn");
for (var i = 0; i < btns.length; i++) {
  btns[i].addEventListener("click", function(){
    var current = document.getElementsByClassName("ativo");
    current[0].className = current[0].className.replace(" ativo", "");
    this.className += " ativo";
  });
}
</script>