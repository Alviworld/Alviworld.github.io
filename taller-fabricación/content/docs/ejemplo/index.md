---
title: 'Ejemplo Shortcodes'
date: 2020-06-17T19:30:08+10:00
draft: false
weight: 14
summary: Uso de los Shortcodes para agregar contenido en el sitio de documentación.
---

<!-- Ejemplo Shortcodes -->

# Contenido Shortcodes

- [Iframe de Fusion 360](#agregar-iframe-de-fusion-360)
- [Agregar Video Local MP4](#agregar-video-local-mp4)
- [Galería Fotos Lightbox](#agregar-galería-fotos-lightbox)
- [Botón de Descarga](#agregar-botón-de-descarga)
- [Agregar Visor de PDF](#agregar-visor-de-archivos-pdf)
- [Agregar link a Youtube](#Agregar-link-a-Youtube)

<!-- Agregar Iframe de Fusion 360 -->
---

### Agregar Iframe de Fusion 360

{{< iframe-fusion link="https://myhub.autodesk360.com/ue2ce4e3a/shares/public/SH56a43QTfd62c1cd968edbffd1ceafd2764?mode=embed" >}}

##### Código `Iframe de Fusion 360` Markdown 

```
{{</* iframe-fusion link="https://myhub.autodesk360.com/ue2ce4e3a/shares/public/SH56a43QTfd62c1cd968edbffd1ceafd2764?mode=embed" */>}}
```

##### Código `Iframe de Fusion 360` HTML Shortcode 

```
<div>
    <iframe 
    src='{{ index .Params "link" }}'
    width="100%" 
    height="450" 
    allowfullscreen="true" 
    webkitallowfullscreen="true" 
    mozallowfullscreen="true"  
    frameborder="0">
    </iframe>    
</div>
```

[[Volver Arriba]](#contenido-shortcodes)

<!-- Agregar Video Local MP4 -->
---

### Agregar Video Local MP4

{{< video-local src="video.mp4" >}}

##### Código `Video Local MP4` Markdown 

Carpeta de videos se encuentra en `/static/img`

```
{{</* video-local src="video.mp4" */>}}
```

##### Código `Video Local MP4` HTML Shortcode 

```
<div>
    <video 
    width="100%" 
    height="450" 
    autoplay muted loop controls preload>
    <source src="/{{ index .Params "src" }}"  type="video/mp4">
    </video>
</div>
```

[[Volver Arriba]](#contenido-shortcodes)
 
<!-- Agregar Galería Fotos Lightbox -->
---

### Agregar Galería Fotos Lightbox

{{< gallery dir="/img/galeria/" />}} {{< load-photoswipe >}}

##### Código `Galería Fotos Lightbox` Markdown 

Carpeta de galeria se encuentra en `/static/img`. Es importante que cada galería de imágenes esté contenida en una carpeta.

Para acceder a esa carpeta, se debe poner la ruta de acceso en el shortcode. Ejemplo con una carpeta llamada `galeria` dentro de `/static/img`.

```
{{</* gallery dir="/img/galeria/" />}} {{< load-photoswipe */>}}
```

[[Volver Arriba]](#contenido-shortcodes)

<!-- Agregar Botón de Descarga -->
---

### Agregar Botón de Descarga

{{< boton-descargar src="documento.pdf" >}}

##### Código `Botón de Descarga` Markdown 

```
{{</* boton-descargar src="documento.pdf" */>}}
```

##### Código `Botón de Descarga` HTML Shortcode 

```
<a class="face-button" href="/descargas/{{ index .Params "src" }}" download>
    <div class="face-primary">
        <span class="icon fa fa-cloud"></span>
        Descargar
    </div>
    <div class="face-secondary">
        <span class="icon fa fa-hdd-o"></span>
    </div>
</a>
```

[[Volver Arriba]](#contenido-shortcodes)

<!-- Agregar visor de archivos PDF -->
---

### Agregar visor de archivos PDF

{{< pdf-viewer id="pdf-hugo" link="/pdf/documento.pdf"  >}}

{{< pdf-viewer id="ejemplo-adobe" link="https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"  >}}

<!-- Agregar código -->
---

##### Código `Visor de archivos PDF` Markdown 

Ejemplo con PDF en carpeta `/static/pdf`.

```
{{</* pdf-viewer id="pdf-hugo" link="/pdf/documento.pdf" */>}}
```

Ejemplo con PDF en link externo:

```
{{</* pdf-viewer id="ejemplo-adobe" link="https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf" */>}}
```

##### Código `Visor de archivos PDF` HTML Shortcode 

```
<iframe id='{{ index .Params "id" }}' src='{{ index .Params "link" }}'
frameborder="0" scrolling="yes" seamless="seamless" style="display:block; width:100%; height:60vh;"></iframe>

<button onclick="myFunction('{{ index .Params "id" }}')" class="button button-primary mb-2" style="width: 100%;">Ver Pantalla Completa</button>

<script>
    function myFunction(id) {
      document.getElementById(id).classList.add("full-screen");
    }
    document.addEventListener('keydown', function(event){
	if(event.key === "Escape"){
        document.getElementById('{{ index .Params "id" }}').classList.remove("full-screen");
	}
});
</script>
```

<!-- Agregar link a Youtube -->
---

##### Agregar `Agregar link a Youtube` with the video ID


[![Aca puedes poner lo que sea](https://img.youtube.com/vi/watch?v=ACA_PONES_LA_ID/0.jpg)](https://www.youtube.com/watch?v=ACA_PONES_LA_ID_DEL_VIDEO_DE_YOUTUBE)

ejemplo real de id: vC47vRni_5g

