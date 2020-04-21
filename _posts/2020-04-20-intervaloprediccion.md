---
title: "Intervalos de predicción para una sola observación. SOLO PARA CLASE DE METODOS ESTADISTICOS"
output: html_notebook
---

Hasta el momento, los intervalos revisados son para el promedio de una población o para la mediana de una población. Hay ocasiones en las que no interesa saber la posición central de los datos, si no que se requiere saber donde se ubicará la siguiente medición (solo una).

Por ejemplo, en el caso del contenido de arsénico, uno pudiera preguntarse lo siguiente:

Si realizamos una sola medición de arsénico en agua subterránea de esa región, ¿en que intervalo caerá esa medición?. Note que este cuestionamiento es diferente al que habiamo hecho con los intervalos sobre medias o medianas. En éste ultimo caso la pregunta a responder era: si realizamos varias mediciones de arsénico de aguas subterráneas de esa región: ¿en que intervalo estará la media o la mediana?.

Otro ejemplo, si usamos la situación de los pollos alimentados con maíz transgenico es: Si se pesa a un pollo alimentado con maíz transgenico ¿en que intervalo estará su peso?. Cosa distinta es lo que nos hemos preguntado antes: si seleccionamos varios pollos alimentados con maíz transgénico ¿ en que intervalo estará el peso promedio de ellos?

Pues bien, para elaborar un intervalo de predicción pueden usarse tambien varios métodos:

1. El primero que revisaremos es cuando los datos son normales:

![Prediccion_Simetrico](/probabilidad/figs/prediccion.PNG)

Ejemplo. Los siguientes datos son sobre las estaturas de alumnos de una universidad.



```{r}
estaturas <- c(1.54, 1.66, 1.60, 1.69, 1.72, 1.76, 1.56, 1.70, 1.68, 1.75, 1.55,1.61, 1.68, 1.59, 1.58, 1.67, 1.70, 1.75, 1.63, 1.76)

```
**El problema planteado es: Si un nuevo alumno se seleccionará de esa universidad, su estatura en que intervalo estará?**

Con la ayuda de un histograma y la prueba de Shapiro primero pruebe si losdatos son normales :

```{r}
hist(estaturas)
shapiro.test(estaturas)

```

El histograma es ligeramente simétrico, pero como hay pocos datos lo mejor es realizar la prueba de Shapiro. Al hacer la prueba se concluye que los datos son normales (pues el valor p es aprox. 0.20).

Por lo que podremos usar el intervalo para hacer el intervalo de predicción. Los siguiente serequiere hacer en R.


```{r}

# el tamaño de muestra

n = 20

# calculamos la media
m <- mean(estaturas)
m

# ahora la desviación estándar
s <-sd(estaturas) 
s

# valor de la distribución t al 95%, recuerde que el tamaño de muestra es 20 y en la formula se establece que  n-1

t <- abs(qt(.025,19))
t

# Ahora los limites del intervalo de predicción
# Límite inferior

li <- m - t*sqrt(s^2+(s^2/n))
li

#Límite superior

ls <- m + t*sqrt(s^2+(s^2/n))
ls
```
POr lo que la conclusión sería: Al 95% de confianza esa persona seleccionada de la universidad mediria entre 1.50m y 1.81 m.

Ejercicios.

1. Un silvicultor calculó la edad de 25 arboles.

104  99 106  99  96  92 115 104 114  97  97  98 101 101 100 101
102 100  96 107 102 101 106 107 102

Si selecciona un siguiente árbol, ¿su edad en que intervalo estará? Al 95 % de confianza



2. Se muestran a continuación los rendimientos (ton/ha) en un cultivo de 22 parcelas de productores: 

9 12  5  9 10  3  9  4  9  7 10 10  8 10  7 10 12  5  9  7  8  9

Si se selecciona una parcela de otro agricultor ¿cual será su rendimiento? con un intervalo del 95%


ENVIAR A MAS TARDAR EL VIERNES 24 DE ABRIL AL CORREO mucio.osorio@gmail.com


Dudas: Atendidas en la semana en el correo mucio.osorio@itson.edu.mx
