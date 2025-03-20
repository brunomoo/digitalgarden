---
{"dg-publish":true,"permalink":"/proyectos/proyecto-grindr/investigacion/tipos-de-perfiles/","created":"2025-02-27T12:20:26.596-05:00","updated":"2025-03-19T23:37:55.527-05:00"}
---

Prueba 1
<div class="button-container">
  <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">
    "FALSO" Y "CALETA"
  </button>
  <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">
    "ANÓNIMO"
  </button>
  <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">
    "CUERPO"
  </button>
  <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">
    "SELFIE DE ROSTRO"
  </button>
  <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">
    "VIAJERO" Y "GIMNASIO"
  </button>
</div>

<div class="svg-container"></div>

<style>
  /* Contenedor de los botones */
  .button-container {
    display: flex;
    flex-wrap: wrap;
    gap: 15px; /* Espacio entre botones */
    justify-content: center;
    max-width: 100%;
    padding: 20px;
  }

  /* Botones */
  .button-container button {
    padding: 25px 50px; /* Botones más grandes */
    font-size: 28px; /* Texto más grande */
    font-weight: 900; /* Negrita fuerte */
    cursor: pointer;
    border: none;
    border-radius: 12px;
    background-color: #007bff;
    color: white;
    text-align: center;
    white-space: normal; /* Permite saltos de línea si el texto es largo */
    max-width: 280px; /* Evita que se hagan demasiado anchos */
    word-wrap: break-word;
  }

  .button-container button:hover {
    background-color: #0056b3;
    transform: scale(1.1);
  }

  /* Contenedor del SVG */
  .svg-container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    margin-top: 20px;
  }
</style>

<script>
function cargarSVG(url) {
  fetch(url)
    .then(response => response.text())
    .then(svg => {
      document.querySelector(".svg-container").innerHTML = svg;
      const svgElement = document.querySelector(".svg-container svg");
      if (svgElement) {
        svgElement.style.width = "100%";
        svgElement.style.height = "auto";
      }
    })
    .catch(error => {
      console.error("Error al cargar el SVG:", error);
    }


Prueba 2
<div class="map-container">
  <div class="central-word">IDENTIDAD</div>
  <div class="word word1" onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">"FALSO" Y "CALETA"</div>
  <div class="word word2" onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">"ANÓNIMO"</div>
  <div class="word word3" onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">"CUERPO"</div>
  <div class="word word4" onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">"SELFIE DE ROSTRO"</div>
  <div class="word word5" onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/Grindr_entrevistas_sintetizado_____.svg')">"VIAJERO" Y "GIMNASIO"</div>
</div>

<!-- Contenedor para el SVG flotante -->
<div id="svgModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="cerrarSVG()">&times;</span>
    <div class="svg-container"></div>
  </div>
</div>

<style>
  /* Contenedor del mapa */
  .map-container {
    position: relative;
    width: 400px;
    height: 400px;
    margin: 50px auto;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  /* Palabra central */
  .central-word {
    position: absolute;
    font-size: 32px;
    font-weight: 900;
    text-align: center;
    color: #fff;
    background-color: #ff5733;
    padding: 20px 30px;
    border-radius: 50%;
  }

  /* Palabras alrededor */
  .word {
    position: absolute;
    font-size: 22px;
    font-weight: 900;
    color: white;
    background-color: #007bff;
    padding: 15px;
    border-radius: 50%;
    text-align: center;
    width: 140px;
    cursor: pointer;
    transition: transform 0.3s ease;
  }

  .word:hover {
    background-color: #0056b3;
    transform: scale(1.1);
  }

  /* Posiciones de las palabras en círculo */
  .word1 { top: 10%; left: 50%; transform: translateX(-50%); }
  .word2 { top: 30%; right: 10%; }
  .word3 { bottom: 10%; left: 50%; transform: translateX(-50%); }
  .word4 { top: 30%; left: 10%; }
  .word5 { bottom: 30%; right: 10%; }

  /* Modal para el SVG */
  .modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
  }

  .modal-content {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    width: 80%;
    max-width: 600px;
    text-align: center;
    position: relative;
  }

  .close {
    position: absolute;
    top: 10px;
    right: 20px;
    font-size: 30px;
    cursor: pointer;
    color: #333;
  }

  .svg-container {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .svg-container svg {
    width: 100%;
    height: auto;
  }
</style>

<script>
function cargarSVG(url) {
  fetch(url)
    .then(response => response.text())
    .then(svg => {
      document.querySelector(".svg-container").innerHTML = svg;
      document.getElementById("svgModal").style.display = "flex";
    })
    .catch(error => {
      console.error("Error al cargar el SVG:", error);
    });
}

function cerrarSVG() {
  document.getElementById("svgModal").style.display = "none";
  document.querySelector(".svg-container").innerHTML = "";
}
</script>

prueba 2
[[Proyectos/Proyecto Grindr/Investigación/Corporales (anónimos)\|Corporales (anónimos)]]
[[Proyectos/Proyecto Grindr/Investigación/Heteronormativos\|Heteronormativos]]

Perfil falso y caleta
<!-- Pon el fondo negro para verificar -->
    <embed src="https://www.dropbox.com/scl/fi/4xf98429iztssr03s76dw/perfil-falso-y-caleta___.svg?rlkey=zz2ula0hb9duxb0w50mq7mtyp&st=vwpyyjb7&raw=1" 
        type="image/svg+xml" 
        width="100%" height="100%">
    </embed>

Perfil anonimo
<!-- Pon el fondo negro para verificar -->
    <embed src="https://www.dropbox.com/scl/fi/vbykp0audp2hszagngjk9/perfil-anonimo____.svg?rlkey=k1egny9uufqoq02pev7xu8jrw&st=en7eijsp&raw=1" 
        type="image/svg+xml" 
        width="100%" height="100%">
    </embed>


Perfil de cuerpo
 <!-- Pon el fondo negro para verificar -->
    <embed src="https://www.dropbox.com/scl/fi/ruvvy0o4i9d8796sgcnsk/perfil-de-cuerpo___.svg?rlkey=3057e35kghp0zsllrethr0q6m&st=cqxgzzrc&raw=1" 
        type="image/svg+xml" 
        width="100%" height="100%">
    </embed>


Perfil de selfie de rostro
<body> <!-- Pon el fondo negro para verificar -->
    <embed src="https://www.dropbox.com/scl/fi/3qog0g9yo54hsihchh8fd/perfil-de-selfie-de-rostro___.svg?rlkey=7bb003m025l9ivkmuzrbmos2b&st=pbkffixx&raw=1" 
        type="image/svg+xml" 
        width="100%" height="100%">
    </embed>
</body>

Perfil viajero y de gimnasio
<body> <!-- Pon el fondo negro para verificar -->
    <embed src="https://www.dropbox.com/scl/fi/0kyli24jsvp1l4m3es10a/perfil-viajero-y-de-gimnasio___.svg?rlkey=zepgevi3199lianwfagcj5jet&st=8zebstx2&raw=1" 
        type="image/svg+xml" 
        width="100%" height="100%">
    </embed>
</body>

## Bisexuales
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/lahch8jdya1ofd2rvu2xv/Bisex1-41.webp?rlkey=60bhqe3tzfksp6z8zak2hnmpi&st=2dxidezm&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/9nw7yokp558oms861ofna/Bisex-2-47.webp?rlkey=h5zy0xs5du9dsjokqoaf4ixd9&st=9tu9japc&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Caletas
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">        
        <img src="https://www.dropbox.com/scl/fi/lohzvgh0t8udaudiujmln/Calet2-17.webp?rlkey=twzgj46b02s1j3nwlw2aqwtfu&st=rrsyxv2z&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/do1a8o34qsom63hsly4hc/Calet1-68.webp?rlkey=dv4w6fn50ehv3n80709f2swnh&st=wf97wnt9&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Discriminadores
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/dvztmn60timyf7ob0jdek/Disc1-81.webp?rlkey=o87c8yi1izgpodd1g3buhycu0&st=wxwuwnxl&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/k0vkin6ttmqeriz7oo2hv/Disc2-62.webp?rlkey=nwyjix5gvo9nmx666pz3kg0yf&st=2v5p4dak&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Esperanzados
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/6g66fpe8lodw0ss9grwr8/Esper-1-25.webp?rlkey=47vxdlznrenk27thelb5i986u&st=t1cajgxw&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/88ae1thfvawb1k5xrftr3/Esper-2-99.webp?rlkey=ijsom18bw7odltllrkj287ulq&st=h4idpbin&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Exotizadores
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/6up9tvbgxvzf5o1m90zky/Exot1-56.webp?rlkey=2wdes5ernkqf5v10nrr9wsngd&st=lc4iwwcb&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/pizf6f08bm8xsef1yakmy/Exot2-91.webp?rlkey=o825ljxwtlkaaacnpuwgd0jnt&st=kg0gp7it&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Fetiches
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/zh6tykgm029a9vziv0va4/Fetiche1-7.webp?rlkey=o9q1pqo9v6skmkq9aglr3y873&st=3dom6jo2&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/5e8a0zsb4ke2uwy33fykg/Fetiche2-19.webp?rlkey=a2zjrrwm3kim7cpg8qwq87kwv&st=rnvfm8cj&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Heteronormativos
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/qcbf4in4z27wakvtjj9qi/het-1-83.webp?rlkey=arwbiq05i5eu05a5zg200csl9&st=92a5gx7y&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/ppu3wsok45o0ck67ysegc/het-2-83.webp?rlkey=ttnetie8n0eiy4p96ft57qyu1&st=zk5cnvf3&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Millenial
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/o198jyzzsk9edg8pjpdfc/Millenial-1-73.webp?rlkey=9k9c4oekuibv8b6u9ckxnnzon&st=qxclikl1&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/r3ey48lbug9gvl9flhlvs/Millenial-2-44.webp?rlkey=9n83vephyyir9iwf4xhtxkijm&st=7ueuvzng&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Servicios
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/cjjgzoiyxz40xxxd9klkl/Serv-1-97.webp?rlkey=os509qmlbqd3v33fyxi4rzua5&st=4f6eblos&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/jeor4i0awu5jm25swk3aa/Serv-2-101.webp?rlkey=cdx1shis43b9d6nakrj7x479q&st=u9xzkk8j&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Servicios sexuales
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/oe7a24yj9jm8uu5p11fko/Servsex-1-87.webp?rlkey=hgezi7gzboplfi0kjq62xpy3m&st=bld9kof2&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/pcznpq7bq0sl2vwm2z4yx/Servsex-2-60.webp?rlkey=3f0zq7dhkvu5cr2sodom2codp&st=r7i15fel&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>

## Viajeros
<div style="display: flex; flex-direction: column; align-items: center; text-align: center;">
    <div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
        <img src="https://www.dropbox.com/scl/fi/vzhks9btzny6oz83l5a4g/Viaj1-85.webp?rlkey=6zety75glc58h7aqea9xnucm3&st=lx4yfsa3&raw=1" style="max-width: 100%; height: auto; width: 300px;">
        <img src="https://www.dropbox.com/scl/fi/wasufuvepkfarmf9def5n/Viaj-2-85.webp?rlkey=1h6d1edj8zl4n16aqn89yiqbz&st=zs73e0cy&raw=1" style="max-width: 100%; height: auto; width: 300px;">
    </div>
    <p style="margin-top: 5px; font-size: 14px;">Texto debajo de ambas imágenes</p>
</div>
