---
{"dg-publish":true,"permalink":"/proyectos/proyecto-grindr/investigacion/tipos-de-perfiles/","created":"2025-02-27T12:20:26.596-05:00","updated":"2025-04-10T13:04:56.852-05:00"}
---

Estos fueron algunos de los datos que me dieron de cómo identifican distinciones entre perfiles. Se puede hacer click en los contenedores para ver cada mapa.
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
        "https://www.dropbox.com/scl/fi/w22kjr6sa9dn1zdo3mn9x/fals1.webp?rlkey=fy7a7epu39dk340iljlq7ghoj&st=2slvry19&raw=1",
        "https://www.dropbox.com/scl/fi/rspm9hy5pr5sgo9qefdhr/fals2.webp?rlkey=ubueky4j12qsha44vtueesgqq&st=n9o5ap8m&raw=1"
      ],
      texto1: "Falso + Caleta: Representación de perfiles encubiertos.",
      imagenes2: [
        "https://www.dropbox.com/scl/fi/b3vrslann9aysrv9mfqmm/calet1.webp?rlkey=49cuosymb2mfggb73oubix97f&st=vieny1wp&raw=1",
        "https://www.dropbox.com/scl/fi/fut1rv4ytf941rzww7fvw/calet3.webp?rlkey=s9w8cainscrz7yian49nnfiom&st=s6munmde&raw=1"
      ],
      texto2: "Ejemplo de interacciones en perfiles ocultos."
    },
    anonimo: {
      imagenes1: [
	      "https://www.dropbox.com/scl/fi/f8nvx3ynmx78m9lr8at8t/anonim1.webp?rlkey=v77gi6qmhv98ab7jpxqxi1qm3&st=z5v45q6n&raw=1",
	      "https://www.dropbox.com/scl/fi/p7ch4jp77pqm0d9uzq9kd/anonim2.webp?rlkey=ktumv38b9sttsyhhmlvm78op5&st=0c7d4nbz&raw=1"
		],
      texto1: "Anónimo: La invisibilidad en los espacios digitales.",
      imagenes2: [],
      texto2: ""
    },
    cuerpo: {
      imagenes1: [
        "https://www.dropbox.com/scl/fi/qej7nk2kyttnrji4pf0ch/cuerp1.webp?rlkey=a9pqs1l0dv48u5ifkwuyyyroe&st=6arofw1c&raw=1",
        "https://www.dropbox.com/scl/fi/dpxl8v7gcaaidus28ftls/cuerp3.webp?rlkey=tttos5kv3th1gn9g2h2arb84x&st=96g6lk3m&raw=1"
      ],
      texto1: "Cuerpo: La exposición de lo físico en la red.",
      imagenes2: [],
      texto2: ""
    },
    selfie: {
      imagenes1: [
        "https://www.dropbox.com/scl/fi/1t6xrpxhdg5z7mwiimbvm/fotrostr.webp?rlkey=h3gry7ie5yshoaddp6xjif445&st=9xkpa9nf&raw=1",
        "https://www.dropbox.com/scl/fi/4mscpf6pc8iqwsuetnva5/fotrostr2.webp?rlkey=tu0if6a9j1g311ef5kadkwrz3&st=fgkxrsio&raw=1"
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
      imagenes2: [
      "https://www.dropbox.com/scl/fi/inbkpm2c1sqe1xuysmcpg/gim1.webp?rlkey=4435crgbuxeiz0prph1v33rxm&st=halna48h&raw=1",
      "https://www.dropbox.com/scl/fi/xpduor4m07sotmqiz7036/gim2-copia.webp?rlkey=gze7ta1jasyibvc1a9ro6p73a&st=fmvv4q82&raw=1"
      ],
      texto2: "Perfiles de gimnasio"
    }
  };

  document.getElementById("grupo1").innerHTML = contenido[tipo].imagenes1.map(imgSrc => `<img src="${imgSrc}">`).join("");
  document.getElementById("texto1").textContent = contenido[tipo].texto1;
  document.getElementById("grupo2").innerHTML = contenido[tipo].imagenes2.map(imgSrc => `<img src="${imgSrc}">`).join("");
  document.getElementById("texto2").textContent = contenido[tipo].texto2;
}
</script>
