---
{"dg-publish":true,"permalink":"/proyectos/proyecto-grindr/investigacion/mapa-conceptual/","created":"2025-02-27T12:14:19.761-05:00","updated":"2025-03-03T19:08:16.976-05:00"}
---

El mapa conceptual se elaboró en base a la investigación, por tanto de la revisión de autores y las [[Proyectos/Proyecto Grindr/Investigación/Entrevistas Grindr\|entrevistas]]

<embed src="https://www.dropbox.com/scl/fi/iozhb6gboueypn06hp14b/Mapa_mental.svg?rlkey=rt7xn21ccfx4n27rbffz4ckk9&st=2zbxhuus&raw=1" 
        type="image/svg+xml" 
        width="100%" height="100%" style="mix-blend-mode: screen;">
    </embed>
<div class="theme-container">
    <object type="image/svg+xml" data="https://www.dropbox.com/s/t2ux4w8pbmwzu7i/prueva.svg?st=y490wkcm&raw=1"></object>
</div>

<style>
    .theme-light {
        color: black;
    }
    .theme-dark {
        color: white;
    }
</style>

<div class="theme-container theme-light">
    <svg width="200" height="100" viewBox="0 0 200 100" version="1.1" xmlns="http://www.w3.org/2000/svg">
        <rect x="10" y="10" width="180" height="80" stroke="currentColor" stroke-width="5" fill="none"/>
        <text x="50" y="60" font-size="24" fill="currentColor">Hola</text>
    </svg>
</div>

<style>
    .theme-light {
        color: black;
    }
    .theme-dark {
        color: white;
    }
</style>

<div class="theme-container theme-light">
    <div id="svg-container"></div>
</div>

<script>
    fetch("https://www.dropbox.com/s/t2ux4w8pbmwzu7i/prueva.svg?raw=1")
        .then(response => response.text())
        .then(data => {
            document.getElementById("svg-container").innerHTML = data;
        });
</script>

<style>
    .theme-light {
        color: black;
    }
    .theme-dark {
        color: white;
    }
</style>

<body data-theme="light">
    <button onclick="toggleTheme()">Cambiar Tema</button>
    <div class="theme-container">
        <object id="svgObject" type="image/svg+xml" data="dibujo.svg"></object>
    </div>
</body>

<style>
    [data-theme="light"] {
        color: black;
    }
    [data-theme="dark"] {
        color: white;
    }
</style>

<script>
    function toggleTheme() {
        let body = document.body;
        body.setAttribute("data-theme", body.getAttribute("data-theme") === "light" ? "dark" : "light");
    }
</script>
<button onclick="changeSVGColor()">Cambiar Tema</button>

<div class="theme-container">
    <object id="svgObject" type="image/svg+xml" data="dibujo.svg"></object>
</div>

<script>
    function changeSVGColor() {
        let svgObject = document.getElementById("svgObject");
        let theme = document.body.classList.toggle("dark-mode") ? "white" : "black";

        svgObject.addEventListener("load", function () {
            let svgDoc = svgObject.contentDocument;
            svgDoc.documentElement.style.color = theme;
        });
    }
</script>


