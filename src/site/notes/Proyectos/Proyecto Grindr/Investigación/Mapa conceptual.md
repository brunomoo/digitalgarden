---
{"dg-publish":true,"permalink":"/proyectos/proyecto-grindr/investigacion/mapa-conceptual/","created":"2025-02-27T12:14:19.761-05:00","updated":"2025-03-03T23:09:01.761-05:00"}
---

El mapa conceptual se elaboró en base a la investigación, por tanto de la revisión de autores y las [[Proyectos/Proyecto Grindr/Investigación/Entrevistas Grindr\|entrevistas]]

<div class="svg-container" style="width: 100vw; height: 100vh; display: flex; justify-content: center; align-items: center;">
</div>

<script>
fetch("https://brunomoo.github.io/Grindr_web/digitalgarden/img/Mapa_Grindr_final_______.svg")
  .then(response => response.text())
  .then(svg => {
    // Inyecta el SVG en el contenedor
    document.querySelector(".svg-container").innerHTML = svg;

    // Asegura que el SVG ocupe el 100% del ancho y alto del contenedor
    const svgElement = document.querySelector(".svg-container svg");
    svgElement.style.width = "100%";
    svgElement.style.height = "100%";
  });
</script>

