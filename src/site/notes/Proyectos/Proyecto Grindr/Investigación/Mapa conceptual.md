---
{"dg-publish":true,"permalink":"/proyectos/proyecto-grindr/investigacion/mapa-conceptual/","created":"2025-02-27T12:14:19.761-05:00","updated":"2025-03-19T22:13:07.939-05:00"}
---

Elaborar mapas mentales como el presente me ayuda a orientar qué me interesa investigar o qué quiero abordar. Detrás de este mapa, hubieron muchos esquemas anteriores y luego de profundizar en la investigación, como la revisión de autores y [[Proyectos/Proyecto Grindr/Investigación/Entrevistas Grindr\|entrevistas]] a usuarios de la plataforma, elaboré esta guía.
<div class="svg-container" style="display: flex; justify-content: center; align-items: center; width: 100%;"></div>

<script>
fetch("https://brunomoo.github.io/Grindr_web/digitalgarden/img/Mapa_Grindr_final_______.svg")
  .then(response => response.text())
  .then(svg => {
    // Inyecta el SVG en el contenedor
    document.querySelector(".svg-container").innerHTML = svg;

    // Asegura que el SVG ocupe el 100% del ancho y alto del contenedor
    const svgElement = document.querySelector(".svg-container svg");
    if (svgElement) {
      svgElement.style.width = "100%";
      svgElement.style.height = "100%";
    }
  })
  .catch(error => {
    console.error("Error al cargar el SVG:", error);
  });
</script>


La conclusión que pude obtener fue que los conceptos principales del proyecto son heteronormatividad, hiperrealidad y performatividad sexual en Grindr.