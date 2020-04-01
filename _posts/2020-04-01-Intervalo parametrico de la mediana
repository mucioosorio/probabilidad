---
title: "Intervalo de confianza parámetrico asimétrico"
output: html_notebook
---

Cuando los datos son asimétricos (con sesgo positivo) un histograma de los logaritmos de los datos originales tiene forma simétrica. Como ejemplo recuerde los datos del arsénico: 


Los datos originales son asimétricos con sesgo positivo.como puede ver
```{r}
a <- c(1.3,8,1.5,9.5,100,580,110,1.8, 2.6, 2.8, 3.5,12, 14, 19, 23,120, 190, 240, 250,4.0,41,300,4.8,80,340)
hist(a)
```

Si se calcula el logaritmo natural de los datos y se realiza la prueba de shapiro puede verse que al 90% de confianza los logaritmos son normales.

```{r}
#log() calcula el logaritmo natural de un número.
y=log(a)

shapiro.test(y)
```

En estas situaciones puede construirse un intervalo de confianza para la mediana de la siguiente manera:



![Statistics](/probabilidad/figs/exponencial.png)


En R, el intervalo se puede calcular así:

```{r}

a <- c(1.3,8,1.5,9.5,100,580,110,1.8, 2.6, 2.8, 3.5,12, 14, 19, 23,120, 190, 240, 250,4.0,41,300,4.8,80,340)


# transformar a logaritmo
y=log(a)

#media de los logaritmos
m <- mean(y)

# desviación estándar de los logaritmos
s <- sd(y)

#valor de la distribución t al 95%, recuerde que el tamaño de muestra es 25 y en la formula dice n-1
t <- abs(qt(.025,24))

#Finalmente los límites de los intervalos
li <- exp(m-t*sqrt(s^2/25))
ls <- exp(m+t*sqrt(s^2/25))
li
ls
```

Finalmente podremos decir que la concentración mediana de arsénico se encuentra entre 10.63 ppb y 53.6 ppb.



EJERCICIO
The following 43 values are annual 7-day minimum flows for 1941−1983 on the Little Mahoning
Creek at McCormick, PA.

```{r}

flujos <- c(0.69,2.90,4.40,0.80,3.00,4.80,9.70, 9.80,1.30,3.10,4.90,10.00,1.40,3.30,5.70,11.00,1.50, 1.50, 1.80, 1.80, 2.10, 2.50,3.70 ,3.80, 3.80, 4.00, 4.10, 4.20,5.80, 5.90, 6.00, 6.10, 7.90, 8.00,11.00 ,12.00, 13.00, 16.00, 20.00, 23.00,2.8,4.2,8)
```
1, Construya un histograma de los datos originales, ¿qué forma tienen?
2. Construya un histograma de los logaritmos de los datos originales,¿qué forma tienen?
3. Realice la prueba de shapiro para los logaritmos de los datos.¿A qué conclusión llega?
4. Construya el intervalo de confianza para mediana usando la fórmula vista en esta sesión.Interprételo.


