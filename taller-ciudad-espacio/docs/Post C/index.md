---
title: '2-CnC, trabajo en grupo'
date: 2021
draft: false
weight: 19
summary: 2-CnC, trabajo en grupo
---
## ¿Qué es CNC?

![PA](/taller-ciudad-espacio/img/PostC/MaquinaCNC.png)

La abreviación CNC significa control numérico por computadora, se usa para realizar cortes, moldeados, grabados, tallados, contronos biselados, canales, perforaciones, etc. Funciona con una máquina que opera en base al sistema CNC, que le indica las coordenadas y además controla los movimientos y velocidad que esta debe dar para lograr el resultado deseado.

Una máquina CNC normalmente tiene 6 elementos principales:

* Dispositivo de entrada.
* Controlador.
* Máquina herramienta,
* Sistema de accionamiento.
* Dispositivos de realimentación.
* Monitor.

En base a lo anterior, en términos simples, las máquinas CNC funcionan mediante instrucciones que recibe el controlador de parte de la computadora y mediante su propio software, convierte estas instrucciones en pulsos o señales electricas que activan los diversos motores poniendo en marcha el sistema de accionamiento.

## Tipos de CNC

Hoy en dia, existen una gran diversidad de maquinas CNC, dentro de las cuales podemos encontrar las siguientes:

* Fresadora.
* Torno.
* Rectificadora.
* Cortadora laser (por chorro de agua o por electroerosión).
* Estampadora.
* Prensa.
* Brazo robótico.
* Impresoras 3D.

Luego, los sistemas de CNC se clasifican según cómo cumplen sus funciones - cómo cortan -. Se pueden clasificar en: Máquinas de control punto a punto, de control pariaxal, de control interpolar o continuo.

## Silla Fresia.

```
{{< iframe-fusion link="https://a360.co/3ou4ykZ" >}}
```


## Piezas mecanizadas

En modo DESIGN haremos un rectángulo de 1220 mm x 1220 mm, el cual se extruye hacia arriba en 15 mm para simular media plancha de terciado, la cual será utilizada para hacer las piezas.

Luego se toman las piezas de la silla que deban ser *mecanizadas* , se alinean con el plano xy y luego se acomodan ordenadamente en la plancha para aprovechar bien su espacio; en este paso es importante que la parte donde se hará el calado quede mirando boca arriba para que la máquina pueda hacer bien su trabajo.


![PA](/taller-ciudad-espacio/img/PostC/piezasCarmi02.png)

Luego iremos a MANUFACTURE y creo un nuevo Setup , para este elegiremos la máquina Generic CNC de 3 Axis. Será necesario definir la plancha como el sólido sobre cual se hará el calado; los Modelos que serán las piezas. Luego establecemos la orientación, que definiremos como eje z, la cara superior del rectángulo y eje x el borde de éste. El tipo de operación es Milling.

1. En primer lugar haremos Contour2d sobre los orificios y el contorno inferior de las piezas. Para esto, elegiremos una Fresa de 6mm para realizar los cortes. Debido a que la plancha mide 15mm y la fresa Flat end Mill de 6mm, para que no se dañe la máquina ni nuestras piezas, es necesario ir a Passes y en Multiple Depths poner un alto de 3mm, de esta forma la máquina hará varias pasadas para ir cortando, en vez de sólo 1.

 Universalmente se usa el 50% del largo de la máquina

2. Luego se realiza un Pocket2d sobre las piezas que requieren rebaje en ciertas áreas. Será necesario repetir el paso de Multiple Depths de 3mm de alto.

3. Para que no se dañen las piezas con la vibración de la máquina, es necesario hacer unos pequeños Tab de 3mm que permitirán que no se corte la pieza entera, sino que dejará pequeños espacios que ayudarán a afirmarla.

 Fresa es la herramienta de corte que va insertada en la máquina.

## Asiento 

![PA](/taller-ciudad-espacio/img/PostC/Asiento02.png )


Para el asiento, en Design se debe hacer un Sketch rectangular con extrusión de 9mm para simular la plancha de terciado; luego posicionar el asiento sobre este.

Lo siguiente es ir a Manufacture y crear un Setup similar al hecho para las piezas mecanizadas.

1. Ahora se hace un Contour2d con la misma configuración anterior sobre el contorno del asiento y como sólido la plancha.

2. La última función que haremos es Trace que se encargará de decirle a la máquina por el recorrido que cortar. En este caso la fresa realizará cortes de tan solo 4.5mm de profundidad.

## Simulaciones

{{< video-local src="AsientoCNC.mp4" >}}

Cabe destacar que una optimización en la ruta que se elige para cortar puede reducir considerablemente el tiempo de trabajo.

## Planimetrías
![PA](/taller-ciudad-espacio/img/PostC/planimetrias_cnc-03.png)
![PA](/taller-ciudad-espacio/img/PostC/planimetrias_cnc-02.png)
![PA](/taller-ciudad-espacio/img/PostC/planimetrias_cnc-01.png)
