---
{"dg-publish":true,"permalink":"/proyectos/proyecto-grindr/investigacion/tipos-de-perfiles/","created":"2025-02-27T12:20:26.596-05:00","updated":"2025-03-20T02:09:08.594-05:00"}
---

Estos fueron algunos de los datos que me dieron de cómo identifican distinciones entre perfiles.
<div class="container">
  <div class="title">Perfil</div>
  <div class="button-container">
    <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil falso y caleta___.svg')">
      "Falso" Y "Caleta"
    </button>
    <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil anonimo____.svg')">
      "Anónimo"
    </button>
    <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil de cuerpo___.svg')">
      "Cuerpo"
    </button>
    <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil de selfie de rostro___.svg')">
      "Selfie de rostro"
    </button>
    <button onclick="cargarSVG('https://brunomoo.github.io/Grindr_web/digitalgarden/img/perfil viajero y de gimnasio___.svg')">
      "Viajero" Y "Gimnasio"
    </button>
  </div>
</div>


<div class="svg-container"></div>


<style>
  /* Contenedor principal */
  .container {
    display: flex;
    align-items: center;
    justify-content: space-between; /* Alinea PERFIL a la izquierda y botones a la derecha */
    gap: 50px;
    max-width: 100%;
    padding: 20px;
  }

  /* Texto grande a la izquierda */
  .title {
    font-size: 50px;
    font-weight: 900;
    text-align: left;
    flex-shrink: 0; /* Evita que PERFIL se haga más pequeño */
    padding-left: 20px;
  }

  /* Contenedor de los botones */
  .button-container {
    display: flex;
    flex-direction: column;
    gap: 15px;
    align-items: flex-start; /* Alinea los botones a la derecha */
  }

  /* Botones */
  .button-container button {
    padding: 22px 45px;
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

  /* Contenedor del SVG */
  .svg-container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    margin-top: 20px;
  }

  /* 📱 Ajustes para móviles */
  @media (max-width: 768px) {
    .container {
      flex-direction: column; /* Pone PERFIL arriba y botones abajo en móviles */
      align-items: center;
      text-align: center;
      gap: 20px;
    }
    
    .title {
      font-size: 40px;
      text-align: center;
    }

    .button-container {
      align-items: center; /* Centra los botones en móviles */
    }

    .button-container button {
      font-size: 22px;
      padding: 15px 30px;
    }
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
    });
}
</script>
