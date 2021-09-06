---
title: '3-2.5'
date: 2021
draft: false
weight: 4
summary: Mecanizado 2.5 ejes CNC.
---


# ¿Qué es tallar?

Tallar es desgastar y pulir un material hasta obtener la figura deseada. Esto se viene haciendo en diferentes materiales desde hace miles de años, mediante la utilización de mazos, gubias, cinceles, martillos y muchísimo antes de esto, piedras. 

Esta técnica de construcción ha sido utilizada, a lo largo de la historia, para producir innumerables objetos.

Estos objetos han sido decorativos; como esta escultura japonesa. También han sido funcionales, como el molde para una espada de bronce. 


{{< gallery dir="/img/galeria25/" />}} {{< load-photoswipe >}}
Escultura japonesa ___________ Molde espada bronce ___________ Estatua Miguel Ángel



El perfeccionamiento de esta técnica permitió grandes y rápidos avances en muchisimas áreas del saber y en distintas artes, como la arquitectura, metalurgia, creación de esculturas, e incluso, para poder encender fuego. 

Hoy en día, con las máquinas de CNC, maquinaria que reemplaza el tallado con gubia y martillo, se puede elaborar objetos con aún más precisión que la que tiene la mano humana.

# Mecanizado en 2.5 ejes

Existe una herramienta, comúnmente conocida como fresadora, la cual mediante el uso de un computador, realiza un proceso automatizado de tallado. Esto, lo logra  moviéndose en un máximo de 3 ejes (XYZ), sin moverse por los 3 ejes al mismo tiempo, al tener un patrón que hace planos paralelos al eje XZ. Se denomina  mecanizado en 2.5 ejes 


#### Orden de Construcción.

Esta simulación funciona con cualquier objeto, para efectos del curso se utilizará el respaldo de una silla fresia. 

##### Paso 1: Objeto a tallar

Exportar el respaldo. 

### Frase clave **Create a Components from Bodies**

![Talla](/img/2.5/Paso1.png)

Para esta simulación, se tallará el respaldo de la silla, a partir de un bloque de material, con forma de paralelepípedo. El software imitará el bloque de madera del cual queremos tallar el objeto.
En el software Fusion360,  es importante poner los objetos de forma ortogonal al plano. Esto implica, que el objeto debe estar paralelo al plano XY, y por encima de este.
Para imaginarlo, de apoyarlo sobre una mesa, la mesa sería el eje XY y el respaldo formaría una concava. 

![Talla](/img/2.5/IMG4.png)

##### Paso 2: Material a Tallar

Comando clave **Proyect**

Con el comando proyect, o la letra "P", se seleccionará el respaldo y el software creará un rectángulo perfecto del área que nos interesa. Este paso es el final para terminar el sketch. 
Deberíamos tener el bloque, el respaldo y el rectángulo

![Talla](/img/2.5/Sketch.jpg)



###### **2.5**: Comando
Es bueno recordar que en este software, los comandos se pueden configurar de diferentes formas dependiendo de lo que queramos simular.
![Talla](/img/2.5/buildordercomando1.jpg)

##### Paso 3: Desbaste Adaptativo 

En la parte de manufacturing, realizaremos un **Desbaste Adaptativo**

Esto removerá un poco de material para agilizar el proceso de obtención de la superficie. 

Esta opción nos deja elegir el tipo de fresia que queremos usar. Utilizaremos la fresia de 6MM con terminación plana. 

![Talla](/img/2.5/Fresia6mm.png)

![Talla](/img/2.5/buildordercomando2.jpg)



## ![Talla](/img/2.5/error.png)    **Warning: Empty toolpath.**

[Error común y como solucionarlo. ](https://help.autodesk.com/view/fusion360/ENU/?caas=caas/sfdcarticles/sfdcarticles/Empty-toolpth-warning-on-boring-and-drilling-toolpaths-in-Fusion-360-Manufacture.html)

Es bueno recordar que este software cuenta con un foro para responder dudas de los errores más comunes.

##### Paso 4: Terminación

**Terminación Adaptative 1** En este paso, se retira una gran cantidad de material de forma rápida, es un proceso más brusco y menos preciso.

[![Terminación Adaptativa](https://img.youtube.com/vi/watch?v=vC47vRni_5g/0.jpg)](https://www.youtube.com/watch?v=vC47vRni_5g) (ver video en youtube)

**Terminación Paralela 1** En esta parte podemos elegír diferentes tipos de configuraciones para obtener resultados más prolijos y eficientes.

{{< video-local src="/img/25paralel1.mp4" >}}

**Terminación Paralela 2** Pule aun más la figura

{{< video-local src="/img/25-Adaptative.mp4" >}}



Descarga el Modelo para Fusion360 haciendo click [[AQUI]](/descargas/Desbaste.f3d)


