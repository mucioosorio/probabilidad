---
title: "Inferencia Estadística: Intervalos de confianza del promedio de una población"
output: html_notebook
mathjax: true
---

La inferencia Estadística es la parte de la Estadística que se encarga de obtener conclusiones de una población solo con la información de una muestra, incluyendo una medida de la confianza de los resultados (probabilidad).

![Inferencia Estadística](/probabilidad/figs/inferencia.gif)

Es muy común realizar estudios sobre una población basados solo en la información de una muestra. Imagina que en una empresa se produccen 1 000 000 de tornillos (población) y que quieres conocer la longitud media de todos los tornillos. Pero, ¡medir todos estos tornillos es dificil!, por muchas situaciónes: es tardado, es costoso, etc.

Lo mejor es seleccionar una muestra al azar de por ejemplo 100 tornillos y calcular la media de esta muestra. Y después agregar un margen de error para poder decir algo sobre toda la población de tornillos.

POr ejemplo,  calcular la media de la muestra de 100 y decir más o menos la media de toda la población de los tornillos está entre este valor y este otro con un 95% de confianza.

Esto es precisamente una herramienta de la Estadística que se llama Intervalo de Confianza del promedio de una población.

Cuando se requiere estimar al promedio de una población $\mu$ con una confianza de $100(1-\alpha)%$ de confianza con la información de una muestra obtenida al azar de manera simple aleatoria o sistemática aleatoria se usa:


$$\bar{x}\pm z_{\alpha/2}\left(\dfrac{s}{\sqrt{n}}\right)$$


Ejemplo. Un maestro quiere saber la estatura promedio de todos los alumnos ITSON. No puede medir a todos los alumnos así que decide seleccionar una muestra de 30 estudiantes cuya estatura se muestra a continuación


1.70 1.63 1.72 1.78 1.63 1.67 1.58 1.65 1.64 1.75 1.71 1.62
1.64 1.61 1.73 1.70 1.68 1.59 1.68 1.60 1.62 1.67 1.68 1.64
1.71 1.62 1.71 1.68 1.63 1.77

Para saber por donde se ubicará la estatura promedio de todos los estudiantes ($\mu$), lo único que se tiene que hacer es:

1. calcular el promedio de la muestra ($\bar{x}$)
