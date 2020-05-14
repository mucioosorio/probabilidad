---
title: "Tara para viernes 15 de mayo. Probabilidad y Estadística y Métodos Estadísticos."
output: html_notebook
---

### Regresión Lineal Simple

Un modelo de **regresión** es un modelo que permite describir cómo influye una variable **X** sobre otra variable **Y**.

* X: Variable independiente o explicativa o exógena o predictora

* Y: Variable dependiente o respuesta o endógena

El objetivo es obtener estimaciones razonables de **Y** para distintos valores de **X** a partir de una muestra de **n* pares de valores $$(x_1, y_1), (x_2,y_2),. . . ,(x_n, y_n)$$.

### Ejemplos

* Estudiar cóomo influye la estatura del padre (X) sobre la estatura del hijo (Y).

* Estimar el precio de una vivienda (Y) en función de su superficie (X).

* Aproximar la calificación obtenida en una materia (Y) según el número de horas de estudio semanal (X).

* Prever el tiempo de cálculo de un programa en función de la
velocidad del procesador (X).

* Predecir la duración de una leche en días (Y) a partir de la temperatura a la que se almacena (X).

Supongamos que queremos encontrar la relación que hay entre las estaturas (X) y pesos (Y) de alumnos universitarios y que se consiguen las siguientes mediciones en 8 alumnos:

Estatura (X)  | Peso (Y)
------------- | -------------
1.58          | 60
1.63          | 64
1.68          | 69
1.74          | 75
1.78          | 80
1.85          | 84
1.90          | 91
1.94          | 95


Para encontrar el modelo lo que se debe hacer es:

1.Ver la forma que tiene la relación entre las variables. Esto se consigue a través de un gráfico de dispersión

![Grafico de Dispersión](/probabilidad/figs/regresion.PNG)

En éste puede verse que la forma de la relación es cómo un línea recta. Pero no solo puede haber relaciones lineales:

![Tipos de relación](/probabilidad/figs/tipos.png)

2.Se debe describir el sentido y la fuerza de la relación.

### Sentido de la relación

* Puede ser positivo, si cuando **X** crece tambien lo hace **Y** o viceversa.

* Negativo, si **Y** disminuye cuando **X** crece.

### Fuerza de la relación

Tiene que ver con lo cercano que están los puntos originales a una linea (ya sea recta o curva) imaginaria que pasa entre los puntos.

![Grafico de Dispersión](/probabilidad/figs/fuerzadiagr.PNG)

En este caso puede decirse que hay una relación fuerte.

Dado que es subjetivo hablar sobre la fuerza de la relación sólo con ver el gráfico, hay un número que mide esa relación. Este número es el coeficiente de correlación de Pearson:

$$r = \frac{n \sum{XY}-(\sum{X}\sum{Y})}{\sqrt{ [n \sum{x^2}-(\sum{x})^2 ][n \sum{y^2}-(\sum{y})^2 }]}$$


![Coeficiente de correlación](/probabilidad/figs/fuerza.png)
