---
title: "Tarea para jueves 7 de mayo. Probabilidad y Estadística y Métodos Estadísticos."
output: html_notebook
---


## Intervalos de confianza de la diferencia de dos proporciones poblacionales $$(P_{1}-P_{2})$$

Cuando se requiere saber si las proporciones de éxitos de dos poblaciones $$(P_{1}~y~ P_{2})$$son iguales o no, por ejemplo, la proporción de artículos defectuosos de la máquina 1 ($$P_1$$) y la proporción de artículos defectuosos de la máquina 2 ($$P_2$$), se construirá un intervalo de confianza para la diferencia de éstas proporciones como sigue:


$$(\hat{p}_{1}-\hat{p}_{2})- z_{\alpha/2} \sqrt{\frac{\hat{p}_{1}(1-\hat{p}_{1})}{n_1}+\frac{\hat{p}_{2}(1-\hat{p}_{2})}{n_2}} \leq P_{1}-P_{2}\leq (\hat{p}_{1}-\hat{p}_{2})+ z_{\alpha/2} \sqrt{\frac{\hat{p}_{1}(1-\hat{p}_{1})}{n_1}+\frac{\hat{p}_{2}(1-\hat{p}_{2})}{n_2}} $$

o de manera breve


$$(\hat{p}_{1}-\hat{p}_{2})\pm z_{\alpha/2} \sqrt{\frac{\hat{p}_{1}(1-\hat{p}_{1})}{n_1}+\frac{\hat{p}_{2}(1-\hat{p}_{2})}{n_2}}$$

> Si el intervalo construido contiene al 0 (es decir que un límite sea negativo y el otro positivo) se concluye que las dos proporciones de éxitos poblacionales son iguales.

> Cuando el 0 no este contenido habrá dos maneras de interpretar:

> * Si los dos límites son positivos se dice que la proporción de éxitos en la población 1 es mayor que la proporción de éxitos en la población 2.

> * Si los dos límites son negativos se dice que la proporción de éxitos en la población 1 es menor que la proporción de éxitos en la población 2.


Ejemplo. Se quiere saber si la proporción de varones zurdos en ITSON ($$P_1$$) difiere o no de la proporción de mujeres zurdas en ITSON ($$P_2$$. 
o de forma breve

Para poder responder a ese cuestionamiento deben seleccionarse muestras aleatorias de hombres y mujeres. Suponga que se seleccionaron 200 hombres y 220 mujeres de los cuales 20 hombres y 23 mujeres resultaron ser zurdos.


1. calcular el porcentaje de exitos en las muestras ($$\hat{p}_1~y~\hat{p}_2$$)

Hay un 10.45% de mujeres zurdas en la muestra:

$$\hat{p}_1=\frac{x_1}{n_1}=\frac{23}{220}=0.1045$$
y un 10% de hombres zurdos en la muestra:

$$\hat{p}_2=\frac{x_2}{n_2}=\frac{20}{200}=0.10$$


2. Según la confianza el valor de $$Z_{\alpha /2}$$ será cómo sigue:

* 99% --------- 2.58
* 95% --------- 1.96
* 90% --------- 1.65

En este caso si se establece la confianza en 95% el valor de **z** será 1.96.

3. Luego sustituimos en la fórmula del intervalo:

$$(\hat{p}_{1}-\hat{p}_{2})\pm z_{\alpha/2} \sqrt{\frac{\hat{p}_{1}(1-\hat{p}_{1})}{n_1}+\frac{\hat{p}_{2}(1-\hat{p}_{2})}{n_2}}$$
Primero, el límite inferior del intervalo:

$$(0.1045 - 0.10)-1.96* \sqrt{\frac{0.1045(1-0.1045)}{220}+\frac{0.10(1-0.10)}{200}} = -0.054$$


Ahora el límite superior:

$$(0.1045 - 0.10)+1.96* \sqrt{\frac{0.1045(1-0.1045)}{220}+\frac{0.10(1-0.10)}{200}} = 0.062$$


4. Finalmente la interpretación será:

El intervalo va de -0.054 a 0.062 o de -5.4% hasta 6.2%. Note que el 0 (cero) esta contenido en el intervalo, por lo que se puede decir que:

Al 95% de confianza, la proporción de mujeres zurdas y la proporción de hombres zurdos de ITSON es la misma.

Note que la conclusión fue hecha considerando a la población.



Ejercicios.

1.En una muestra de 100 pacientes sometidos a un cierto tratamiento (A) se obtienen 80 curaciones y en otra muestra de pacientes sometidos a otro tratamiento (B) se obtienen 90 curaciones. 


*Calcular e interpretar el intervalo de confianza del 95% de la diferencia de proporciones de pacientes que mejoran (P). Después de contruir el intervalo diga cuál es el mejor tratamiento.


2.En una muestra de 400 pilas tipo B fabricadas por una empresa, se encontraron 21 defectuosas. Mientras que de 500 pilas tipo C 10 fueron defectuosos. Estime con un intervalo del 99% de confianza la diferencia de proporciones de pilas defectuosas y diga en cuál tipo hay más proporción de pilas defectuosos.


3.En Ciudad Obregón de 250 personas entrevistadas,  100 leen el periodico habitualmente y en Hermosillo 98 de 240 leen el periodico. Al 90% de confianza en que ciudad la  proporción de personas que lee el periodico es mayor?.



Asignación para entregar como máximo mañana jueves 7 de mayo. 

Tareas que se reciban 1 día despues contarán 50%
Tareas que se reciban 2 días despues contarán 25%
Despues de dos diás solo contarán el 10%


Aquí:
[https://forms.gle/k2Y4o6WDixUwAHXx7](https://forms.gle/k2Y4o6WDixUwAHXx7)


Dudas se atienden en el correo mucio.osorio@itson.edu.mx
