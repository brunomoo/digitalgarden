---
{"dg-publish":true,"permalink":"/proyectos/proyecto-grindr/investigacion/imagenes-de-perfiles/","created":"2025-03-20T01:17:56.151-05:00","updated":"2025-03-20T21:40:36.491-05:00"}
---


Esta clasificación se hizo en base a [Los chicos sólo quieren divertirse by tony robles on Prezi](https://prezi.com/view/hiFN5Nz8IukcPMbjM5y6/).
Luego, estos perfiles fueron los que me interesaron en profundizar
[[Proyectos/Proyecto Grindr/Investigación/Corporales (anónimos)\|Corporales (anónimos)]]
[[Proyectos/Proyecto Grindr/Investigación/Heteronormativos\|Heteronormativos]]
<div class="container">
  <div class="title">Perfil</div>
  <div class="button-container">
    <button onclick="cargarContenido('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil falso y caleta___.svg', 'falsoCaleta')">
      Falso + Caleta
    </button>
    <button onclick="cargarContenido('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil anonimo____.svg', 'anonimo')">
      Anónimo
    </button>
    <button onclick="cargarContenido('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil de cuerpo___.svg', 'cuerpo')">
      Cuerpo
    </button>
    <button onclick="cargarContenido('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil de selfie de rostro___.svg', 'selfie')">
      Selfie de rostro
    </button>
    <button onclick="cargarContenido('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil viajero y de gimnasio___.svg', 'viajero')">
      Viajero + Gimnasio
    </button>
  </div>
</div>

<!-- Contenedor para SVG -->
<div class="svg-container"></div>

<!-- Contenedor para imágenes y texto -->
<div class="image-container">
  <div class="image-group" id="grupo1"></div>
  <p class="image-text" id="texto1"></p>
  
  <div class="image-group" id="grupo2"></div>
  <p class="image-text" id="texto2"></p>
</div>

<style>
  .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 50px;
    max-width: 100%;
    padding: 20px;
  }

  .title {
    font-size: 50px;
    font-weight: 900;
    text-align: left;
    flex-shrink: 0;
    padding-left: 20px;
  }

  .button-container {
    display: flex;
    flex-direction: column;
    gap: 15px;
    align-items: flex-start;
  }

  .button-container button {
    padding: 30px 45px;
    font-size: 28px;
    font-weight: 900;
    cursor: pointer;
    border: none;
    border-radius: 12px;
    background-color: #007bff;
    text-align: center;
    white-space: nowrap;
    min-width: fit-content;
    width: auto;
    max-width: 100%;
  }

  .button-container button:hover {
    background-color: #0056b3;
    transform: scale(1.1);
  }

  .svg-container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    margin-top: 20px;
  }

  .image-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .image-group {
    display: flex;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
    margin-top: 15px;
  }

  .image-group img {
    max-width: 100%;
    height: auto;
    width: 250px;
  }

  .image-text {
    margin-top: 5px;
    font-size: 14px;
  }

  @media (max-width: 768px) {
    .container {
      flex-direction: column;
      align-items: center;
      text-align: center;
      gap: 20px;
    }
    
    .title {
      font-size: 40px;
      text-align: center;
    }

    .button-container {
      align-items: center;
    }

    .button-container button {
      font-size: 22px;
      padding: 15px 30px;
    }
  }
</style>

<script>
function cargarContenido(svgUrl, tipo) {
  // Cargar SVG
  fetch(svgUrl)
    .then(response => {
      if (!response.ok) throw new Error("No se pudo cargar el SVG");
      return response.text();
    })
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
      document.querySelector(".svg-container").innerHTML = "<p style='color: red;'>Error al cargar el SVG</p>";
    });

  // Definir imágenes y textos
  const contenido = {
    falsoCaleta: {
      imagenes1: [
        "https://www.dropbox.com/scl/fi/lohzvgh0t8udaudiujmln/Calet2-17.webp?rlkey=twzgj46b02s1j3nwlw2aqwtfu&st=rrsyxv2z&raw=1",
        "https://www.dropbox.com/scl/fi/do1a8o34qsom63hsly4hc/Calet1-68.webp?rlkey=dv4w6fn50ehv3n80709f2swnh&st=wf97wnt9&raw=1"
      ],
      texto1: "Falso + Caleta: Representación de perfiles encubiertos.",
      imagenes2: [
        "https://www.dropbox.com/scl/fi/lohzvgh0t8udaudiujmln/Calet2-17.webp?raw=1",
        "https://www.dropbox.com/scl/fi/do1a8o34qsom63hsly4hc/Calet1-68.webp?raw=1"
      ],
      texto2: "Ejemplo de interacciones en perfiles ocultos."
    },
    anonimo: {
      imagenes1: [],
      texto1: "Anónimo: La invisibilidad en los espacios digitales.",
      imagenes2: [],
      texto2: ""
    },
    cuerpo: {
      imagenes1: [
        "https://www.dropbox.com/scl/fi/mnopqr789/body1.webp?raw=1",
        "https://www.dropbox.com/scl/fi/stuvwx101/body2.webp?raw=1"
      ],
      texto1: "Cuerpo: La exposición de lo físico en la red.",
      imagenes2: [],
      texto2: ""
    },
    selfie: {
      imagenes1: [
        "https://www.dropbox.com/scl/fi/xyz987/selfie1.webp?raw=1",
        "https://www.dropbox.com/scl/fi/abc654/selfie2.webp?raw=1"
      ],
      texto1: "Selfie de rostro: Identidad y autenticidad.",
      imagenes2: [],
      texto2: ""
    },
    viajero: {
      imagenes1: [
        "https://www.dropbox.com/scl/fi/vzhks9btzny6oz83l5a4g/Viaj1-85.webp?rlkey=6zety75glc58h7aqea9xnucm3&st=lx4yfsa3&raw=1",
        "https://www.dropbox.com/scl/fi/wasufuvepkfarmf9def5n/Viaj-2-85.webp?rlkey=1h6d1edj8zl4n16aqn89yiqbz&st=zs73e0cy&raw=1"
      ],
      texto1: "Viajero + Gimnasio: Perfiles en movimiento.",
      imagenes2: [],
      texto2: ""
    }
  };

  document.getElementById("grupo1").innerHTML = contenido[tipo].imagenes1.map(imgSrc => `<img src="${imgSrc}">`).join("");
  document.getElementById("texto1").textContent = contenido[tipo].texto1;
}
</script>

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
