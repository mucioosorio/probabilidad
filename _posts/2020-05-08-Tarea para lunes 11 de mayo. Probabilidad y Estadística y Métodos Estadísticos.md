---
title: "Tarea para lunes 11 de mayo. Probabilidad y Estadística y Métodos Estadísticos."
output: html_notebook
---


Intervalos de confianza de la diferencia de dos promedios poblacionales $$(\mu_{1}-\mu_{2})$$


Cuando se requiere saber si los promedios de dos poblaciones $$(\mu_{1}~y~ \mu_{2})$$son iguales o no, por ejemplo, la estatura promedio de las mujeres ($$\mu_1$$) y la estatura promedio de los hombres ($$\mu_{2}$$), se construirá un intervalo de confianza para la diferencia de éstos promedios como sigue:


$$(\bar{x}_{1}-\bar{x}_{2})- z_{\alpha/2} \sqrt{\frac{s_{1}^2}{n_1}+\frac{s_{2}^2}{n_2}} \leq \mu_{1}-\mu_{2}\leq (\bar{x}_{1}-\bar{x}_{2})+z_{\alpha/2} \sqrt{\frac{s_{1}^2}{n_1}+\frac{s_{2}^2}{n_2}}$$

o de manera breve


$$(\bar{x}_{1}-\bar{x}_{2})\pm z_{\alpha/2} \sqrt{\frac{s_{1}^2}{n_1}+\frac{s_{2}^2}{n_2}}$$

> Si el intervalo construido contiene al 0 (es decir que un límite sea negativo y el otro positivo) se concluye que los dos promedios poblacionales son iguales.

> Cuando el 0 no este contenido habrá dos maneras de interpretar:

> * Si los dos límites son positivos se dice que el promedio en la población 1 es mayor que el promedio en la población 2.

> * Si los dos límites son negativos se dice que el promedio en la población 1 es menor que el promedio en la población 2.


Ejemplo 1. Se quiere saber si la estatura promedio de las mujeres $$(\mu_1)$$ ITSON es igual o difiere de la estatura promedio de los hombres ITSON $$(\mu_2)$$


Para poder responder a ese cuestionamiento deben seleccionarse muestras aleatorias de hombres y mujeres. Suponga que se seleccionaron 35 hombres y 35 mujeres. La información se muestra a continuación:

* mujeres

1.54 1.57 1.60 1.60 1.60 1.60 1.61 1.61 1.61 1.61 1.61 1.62

1.62 1.62 1.63 1.63 1.63 1.63 1.63 1.63 1.64 1.64 1.65 1.65

1.65 1.65 1.66 1.66 1.67 1.69 1.70 1.70 1.70 1.70 1.73


* hombres

1.65 1.67 1.67 1.69 1.70 1.70 1.70 1.72 1.72 1.72 1.72 1.73

1.73 1.74 1.74 1.74 1.74 1.75 1.75 1.76 1.76 1.76 1.76 1.76

1.77 1.77 1.78 1.78 1.78 1.78 1.80 1.80 1.80 1.80 1.86


Los cálculos para hacer el intervalo:

1.Calcular los promedios y desviaciones estándar de las muestras ($$\bar{x}_1,\bar{x}_2,s_1~y~s_2$$)

Las mujeres de la muestra tienen un promedio y desviación estándar (valores redondeados a dos décimas):

$$\bar{x}_{1}=1.64 ~y~s_1=0.04$$

Los hombres de la muestra tienen un promedio y desviación estándar:

$$\bar{x}_2=1.75 ~y~s_2=0.04$$

Note que los tamaños de muestra son $$n_1=n_2=35$$


2.Según la confianza el valor de $$Z_{\alpha /2}$$ será cómo sigue:

* 99% --------- 2.58
* 95% --------- 1.96
* 90% --------- 1.65

En este caso si se establece la confianza en 95% el valor de **z** será 1.96.

3.Luego sustituimos en la fórmula del intervalo:

$$(\bar{x}_{1}-\bar{x}_{2})\pm z_{\alpha/2} \sqrt{\frac{s_{1}^2}{n_1}+\frac{s_{2}^2}{n_2}}$$

Primero, el límite inferior del intervalo:

Observe que en el intervalo está la varianza y cómo se había calculado la desviación estándar, solo se eleva al cuadrado.

$$(1.64-1.75) - 1.96* \sqrt{\frac{0.04^2}{35}+\frac{0.04^2}{35}}=-0.13$$


Ahora el límite superior:

$$(1.64-1.75)+ 1.96* \sqrt{\frac{0.04^2}{35}+\frac{0.04^2}{35}}=-0.09$$


4.Finalmente la interpretación será:

El intervalo va de -0.13 m a -0.09 m o de -13 cm hasta -9 cm. Note que el 0 (cero) NO esta contenido en el intervalo y además los límites son negativos, por lo que se puede decir que:

Al 95% de confianza, el promedio de las estaturas de las mujeres ITSON es menor, desde 9 cm hasta 13 cm, que la estatura promedio de los hombres ITSON.

Note que la conclusión fue hecha considerando a la población.


Ejemplo 2. Para saber si el promedio de calificaciones de alumnos de dos universidades son iguales, se seleccionan a 45 alumnos de la universidad A y a 50 alumnos de la universidad B.

Se obtuvo la siguiente información:

$$\bar{x}_{A1}=8.9~~~~~~\bar{x}_{B2}=9$$

$$s_{A1}=0.35~~~~~~s_{B2}=0.40$$


Los cálculos para hacer el intervalo:

1.Según la confianza el valor de $$Z_{\alpha /2}$$ será cómo sigue:

* 99% --------- 2.58
* 95% --------- 1.96
* 90% --------- 1.65

En este caso si se establece la confianza en 95% el valor de **z** será 1.96.

2.Luego sustituimos en la fórmula del intervalo:

$$(\bar{x}_{1}-\bar{x}_{2})\pm z_{\alpha/2} \sqrt{\frac{s_{1}^2}{n_1}+\frac{s_{2}^2}{n_2}}$$

Primero, el límite inferior del intervalo:

$$(8.9-9.0)- 1.96* \sqrt{\frac{0.35^2}{45}+\frac{0.40^2}{50}}=-0.051$$


Ahora el límite superior:

$$(8.9-9.0)+ 1.96* \sqrt{\frac{0.35^2}{45}+\frac{0.40^2}{50}}=0.251$$


3.Finalmente la interpretación será:

El intervalo va de -0.051 puntos a 0.251 puntos. Note que el 0 (cero) esta contenido en el intervalo, por lo que se puede decir que:

Al 95% de confianza, el promedio de las calificaciones de TODOS los alumnos de la universidad A y de TODOS los alumnos de la universidad B son iguales.


ASIGNACION

1.Los siguientes datos son sobre el peso de pollitos alimentados con el alimento A

293.90 295.48 295.64 295.68 295.77 295.97 296.06 296.48 296.53 296.56 297.44 298.67 298.71

298.95 299.08 299.68 300.11 300.49 300.62 300.65 300.66 300.93 301.77 301.93 302.27 302.39

302.52 302.72 303.66 304.07

y éstos otros los pesos de pollitos alimentados con el alimento B.

342.41 344.24 345.35 345.80 346.14 347.37 347.71 347.98 348.47 348.67 349.06 349.20 349.76

349.85 350.26 350.32 350.37 350.38 351.04 351.15 351.30 351.75 351.88 352.25 352.91 353.05

353.16 353.26 354.00 354.27 354.48 354.67

¿Los pesos promedios de los pollos son iguales? si no son iguales ¿cuál alimento es mejor?. Use 95% de confianza.

2.Las ganancias promedio del artículo 1 en una muestra de 100 artículos son 1500 pesos con una desviación estándar de 100 pesos. Mientras que en una muestra de tamaño 120 del artículo 2 el promedio es 1600 pesos con una desviación estándar de 150 pesos.

Use una confianza de 90% para decir con cual artículo las ganancias promedio son mayores.

3.investigue una situación en donde se deba hacer un intervalo para comparar dos promedios. Con datos inventados o investigados en internet. Realice el intervalo al 99% de confianza y haga sus conclusiones.

NOTA. en éste último ejercicio puede buscar en internet: " ejercicios de intervalos de confianza de la diferencia de dos promedios"




Asignación para entregar como máximo mañana lunes 11 de mayo. 

Tareas que se reciban 1 día despues contarán 50%
Tareas que se reciban 2 días despues contarán 25%
Despues de dos diás solo contarán el 10%


Aquí:
[https://forms.gle/nfYMdmv1treF3Tjy7](https://forms.gle/nfYMdmv1treF3Tjy7)


Dudas se atienden en el correo mucio.osorio@itson.edu.mx   Estoy atendiendolas lo mas pronto posible.
