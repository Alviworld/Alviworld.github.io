---
title: '5-Impresión 3D'
date: 2021
draft: false
weight: 6
summary: 5-Impresión 3D.
---

## Impresión en FDM

![Molde](/img/post3d/cura.png)

El Software Cura, powered by Ultimaker, es un programa para la impresión de objetos, debido a su gran presición y que es un software fácil de usar, como nos cuenta Ultimaker en su página web:

Fácil de usar
La fabricación no tiene que ser complicada. Diseñamos nuestro software para que cualquiera pueda usarlo, tanto usuarios experimentados como novatos en el campo de las impresoras 3D.

Prepare su modelo 3D para imprimir en minutos con la configuración recomendada

Simplemente elija la configuración de velocidad y calidad, y puede comenzar a imprimir

Ultimaker Cura es un software gratuito y de código abierto

https://ultimaker.com/es/software/ultimaker-cura

## Instalación y Configuración

Recomendación al momento de instalar: decidir bien que tipos de archivos quieren ser abiertos por el software. 

Con respecto a la interface, es lo que se espera, una visualización en 360° de una impresora 3d.

![Molde](/img/post3d/a1.jpg)

Tiene una barra para configurar la posición, el tamaño, el ángulo. Esto es útil por si necesitamos añadirle soporte a la estructura que queremos imprimir, que este software también hace.

{{< video-local src="m2funciones.mp4" >}}

Tiene opciones para configurar muchas variables, tales como el tipo de material, el grosor o incluso, el peso de relleno del modelo.

### Configuraciónes de impresión. 

Cure cuenta con muchisimas variables para configurar. Ejemplo de esto es la función Infill, que nos permite disminuir o aumentar el peso de una estructura, o material y cooling que nos permiten buscar combinaciónes óptimas de impresión con diferentes tipos de material.

![Molde](/img/post3d/a3.jpg)

### Función Slicer:

El software hace cortes al modelo con el objetivo de poder hacer un archivo digital a imprimible, con esta opción se permite que el nozzle de la impresora extruya un material. Se puede configurar la velocidad, el espaciado de cada slice, la temperatura, la cantidad de material, el diamentro del snozzle, etc.

![Molde](/img/post3d/a2.jpg)


## Impresión

Como ejemplo, se hará una simulación de impresión de [[este]](/descargas/macetero.obj) objeto, es un macetero.  

### Interface
{{< video-local src="m1.mp4" >}}


### Configuraciónes y Slicer 

En la simulación se puede ver la forma en que el software planeó la estrategia de impresión.


![Molde](/img/post3d/a4.jpg)


Notemos en la anteriór figura, la parede del macetero está compuesta de 9 lineas de material de 0.2mm de grosor.
Imaginemos que una vuelta de la impresora tarde 1 segundo, para completar 1 slice tardaría 9 segundos, pero si configuraramos la impresora para imprimir con un grosor de 0.06mm tardaría mucho más, lo cual no siempre implica que los resultados podrían ser mejores.

Esto repercute directamente en la calidad de los objtetos a imprimir, dependiendo de este tipo de configuraciones es como los resultados finales quedan, pudiendo tener variadas formas de imprimir de buena forma cualquier tipo de objeto.


{{< video-local src="m3moverse.mp4" >}}

{{< video-local src="m4simu.mp4" >}}