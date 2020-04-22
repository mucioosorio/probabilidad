---
title: "Inferencia Estadística: Intervalos de confianza del promedio de una población. SOLO ALUMNOS DE PROBABILIDAD  ESTADISTICA"
output: html_notebook
mathjax: TRUE
---

La inferencia Estadística es la parte de la Estadística que se encarga de obtener conclusiones de una población solo con la información de una muestra, incluyendo una medida de la confianza de los resultados (probabilidad).

![Inferencia Estadística](/probabilidad/figs/inferencia.gif)

Es muy común realizar estudios sobre una población basados solo en la información de una muestra. Imagina que en una empresa se produccen 1 000 000 de tornillos (población) y que quieres conocer la longitud media de todos los tornillos. Pero, ¡medir todos estos tornillos es dificil!, por muchas situaciónes: es tardado, es costoso, etc.

Lo mejor es seleccionar una muestra al azar de por ejemplo 100 tornillos y calcular la media de esta muestra. Y después agregar un margen de error para poder decir algo sobre toda la población de tornillos.

POr ejemplo,  calcular la media de la muestra de 100 y decir más o menos la media de toda la población de los tornillos está entre este valor y este otro con un 95% de confianza.

Esto es precisamente una herramienta de la Estadística que se llama Intervalo de Confianza del promedio de una población.

Cuando se requiere estimar al promedio de una población $\mu$ con una confianza de $100(1-\alpha)%$ de confianza con la información de una muestra obtenida al azar de manera simple aleatoria o sistemática aleatoria se usa:


$$\bar{x}\pm z_{\alpha/2}\left(\dfrac{s}{\sqrt{n}}\right)$$


Ejemplo. Un maestro quiere saber la estatura promedio de todos los alumnos ITSON. No puede medir a todos los alumnos así que decide seleccionar una muestra de 30 estudiantes cuya estatura se muestra a continuación:


1.70 1.63 1.72 1.78 1.63 1.67 1.58 1.65 1.64 1.75 1.71 1.62
1.64 1.61 1.73 1.70 1.68 1.59 1.68 1.60 1.62 1.67 1.68 1.64
1.71 1.62 1.71 1.68 1.63 1.77

El maestro establece una confianza de 95%.

Para saber por donde se ubicará la estatura promedio de todos los estudiantes ($$\mu$$), lo único que se tiene que hacer es:

1. calcular el promedio de la muestra ($$\bar{x}$$)

El promedio es 1.67 m

2. Calcular la desviación estándar (s)

La desviación estándar de las estaturas es 0.05 m

3. Según la confianza el valor de $$Z_{\alpha /2}$$ será cómo sigue:

* 99% --------- 2.58
* 95% --------- 1.96
* 90% --------- 1.65

En este caso cómo la confianza se establece en 95% el valor de **z** será 1.96.

4. Luego sustituimos en la fórmula del intervalo:

$$\bar{x}\pm z_{\alpha/2}\left(\dfrac{s}{\sqrt{n}}\right)$$

$$1.67 + 1.96 * 0.05 /\sqrt{30} = 1.69$$


$$1.67 - 1.96 * 0.05 /\sqrt{30} = 1.65 $$
5. Finalmente la interpretación será:

Al 95% de confianza, la estatura promedio de TODOS los alumnos de ITSON se estima que está entre 1.65 m y 1.69m.

Note que la conclusión fue hecha considerando a la población.

Ejercicios.

* Se quiere saber con 90% de confianza el promedio de las calificaciones de los alumnos de ITSON. Para estimarlo se obruvo una muestra de 35 alumnos y las calificaciones son las siguientes:

7 8 8 8 8 8 7 9 8 7 8 8 8 8 8 7 8 8 7 9 8 8 8 8 8 8 8 8 8 8 8 8
7 8 8

Construya el intervalo de confianza de la calificación promedio de los alumnos ITSON e interprételo.

* En una industria se pesaron 30 bolsas de botanas:

98  96 102 100  99 104  99 100 101 101  98  97  95  99  99 102
101 104  99 100 102 100 100  98 102 100  99 100 100  99 102 103
100 101 101

Construya e interpréte el intervalo de confianza del 95% de los pesos promedios de las bolsas de botanas.

* Se muestran a continuación los rendimientos (ton/ha) en un cultivo de parcelas de productores: 

9 12  5  9 10  3  9  4  9  7 10 10  8 10  7 10 12  5  9  7  8  9 12 12 8 9 7 9 10 10 11 12 8 9 7

Construya e interpréte el intervalo de confianza del rendimiento promedio al 99% de confianza.



Asignación para entregar como máximo hasta el viernes 24 de abril.

Enviar al correo mucio.osorio@gmail.com

Dudas: se atienden en el correo mucio.osorio@itson.edu.mx
