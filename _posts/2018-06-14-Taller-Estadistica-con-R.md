---
title: 'Taller: Análisis de datos con R Studio <br><br>14/junio/2018.<br><br> Mucio
  Osorio Sánchez. <br><br> Departamento de Matemáticas<br>Cub. 30 CAD Nainari'
output:
  html_notebook: default
  slidy_presentation: default
  pdf_document: default
  html_document: default
  word_document: default
Author: Mucio Osorio Sánchez
---

# Temario

* ¿Por qué usar R?
* Instalar R y Rstudio
* Cálculos, funciones y variables
* Manejo de archivos y gráficas 
* Estadística con R Studio
* Instalación de Paquetes




# ¿Qué es R?

Logo de R|Logo de R Studio
---------|---------------
![Logo R](/probabilidad/figs/Rlogo.png#center)|![R Studio](/probabilidad/figs/RStudio-Logo-Blue-Gray-125.png#right)


## “ R es un lenguaje y ambiente de programación libre para visualización y análisis estadístico de datos”.

![](/probabilidad/figs/mejor.png)

# ¿Por qué R?

## Búsqueda de R en el tiempo

![](/probabilidad/figs/porqR.png)

## Ventajas


* Open Source (Costo nulo), Comunidad dinámica integrada por estadísticos de renombre(Stackoverflow, Comunidad R Hispano, R en español, R Bloggers)
* Multi-plataforma: Disponible para Windows, Mac y Linux 
* Facilidad de enlace con LateX, HTML, RMarkdown y generar reportes dinámicos.
* Amplia bibliografía en la web y libros publicados por editoriales prestigiosas (Springer, Wiley, Chapman & Hall,. . . )

## ¿Quiénes usan R?

![](/probabilidad/figs/companies_r.png)

## Gráficos

![](/probabilidad/figs/porq3.png)

![](/probabilidad/figs/porq4.png)


![](/probabilidad/figs/porq5.png)

# Desventajas

* Poco amigable al inicio
* No hay soporte comercial (en la licencia libre)
* R no posee una interfaz amigable, las tareas se llevan a través de líneas de código, lo cual puede ser incómodo para el usuario.

# Instalación de R y R Studio

En la dirección https://cran.r-project.org/ podrá descargar R para sistemas operativos Linux, Mac OS y Windows.

![](/probabilidad/figs/descarga_r.gif)


R Studio es un ambiente de desarrollo integrado (IDE) que facilita la programación en R. En la dirección https://www.rstudio.com/ se descarga la versión de R Studio, disponible tambien para sistemas operativos linux, OS y windows.

![](/probabilidad/figs/descarga_rstudio.gif)



R Studio esta dividido en 4 partes:

* Editor de código
* Consola
* Espacio de trabajo
* Gráficos, ayuda o archivos

![Pantalla RStudio](/probabilidad/figs/pantallaRstudio.png)

# Directorio de trabajo

R y R Studio tienen como directorio de trabajo la carpeta de **Documentos** de la computadora donde se instalan.

# 1. Uso de R como calculadora


Simbolo            |Operación
-------------------|-------------
+, -, *, / log()  |suma, resta, producto, cociente logaritmo
%%, %/%, ^       |módulo, cociente entero, potencia
==, !=, !        |igual, distinto, no
>, >=, <, <=     |mayor que, mayor o igual que, menor que, menor o igual que
:, seq()         |generar una serie


Alguna operaciones básicas y lógicas:
```{r}
1+6             
2*8             
log(10)         #logaritmo natural si quiere cambiar de base  por ej log10()
9 %% 4          
9%/%4
9==4
9>=4
1:50
seq(1,50,.1)
```

# 2. Asignar valores a variables.

Para asignar valor a variables se usan los simbolos **<-** o **=**

```{r}
x <- 8
y <- 1+6
z = seq(1,50,.5)
```

Si se quiere que se muestren los valores solo debe teclear los nombres y ejecutar (ejecutar desde editor de texto o desde consola)
```{r}
x
y
z
```

# 3. ¿Cómo leer datos?

## c() Concatenar

Una primera opción es haciendo uso de la función concatenar **c()** . Ésta se usa para crear un vector.

La siguiente instrucción crea el objeto q y le asigna un vector
```{r}
q <- c(1,2,3,4,5,6) # vector numérico
s <- c("si","no")   # vector de caracteres

q # para imprimir en pantalla
s
```

Se puede unir vectores con las funciones **cbind() o rbind()**. Por ejemplo, crear tres vectores de 5 elementos y asignar un nombre (edad,altura,nombre).
```{r}
# Se crean los 3 objetos

edad <- c(20,25,31,45,14)
altura <- c(1.60, 1.8,1.7,1.85,1.7)
nombre <- c("Yola","Pedro","Carlos","Maru","Ginger")

# Unir dos vectores rbind(x,y,z) y cbind(x,y,z) y asignar un nombre w

w1<-rbind(nombre,edad,altura)
w2<-cbind(nombre,edad,altura)

# Se muestran los objetos creados

w1
w2
```

## Importar archivo csv

[Aqui los datos del archivo EjemploEstudiantes.csv](https://mucioosorio.github.io/probabilidad/data/EjemploEstudiantesM.csv)



Para leer datos de un documento **csv** se usa la función **read.csv("nombre de archivo")**
```{r}
# El siguiente código asigna al objeto w el archivo de datos EjemploEstudiantes.csv que se encuentra en el directorio "Documentos" y la opción header=T le indican a R que en el primer renglón se ubican los nombres de las variables.

w<-read.csv("EjemploEstudiantesM.csv",header = T)

# opciOnal y posiblemente mejor 

#read.csv(choose.files(),header = T)

```

# 4. Operaciones con vectores + - * / lógicas

Con los vectores se pueden realizar operaciones:

```{r}
edad+2             # Suma a las edades 2
altura^2          # las alturas se elevan al cuadrado
edad==altura      # verifica si edad y altura son identicos 
edad==edad
```

Los **[ ]** se usan para acceder a elementos en un vector, por ejemplo, **x[3:4]** sirve para acceder a la posición 3 y 4 del objeto x. Tambienpodremos usar **x[c(3,4)]**
```{r}
edad[2]                     # accede al elemento 2 de la edad
edad[2:4]                   # accede a los elementos 2,3 y 4
edad[c(2,3,4)]              
edad[edad<40]               # accede a los elementos que cumplela condición  de
                            # ser menores que 40
edad[edad<40 & edad>20]     # elementos que son menores que 40 y mayores que 20
edad[edad<40 | edad>20]     # elementos que son menores que 40 o mayores que 20
```

De la misma manera, para acceder a los elementos de una matriz se usa cualquiera de los siguientes formatos: **x[row,column], x[,"Height"] , x[,2]**

```{r}
w2[1,2]        # accede al lemento 1 de la columna 2
w2[ ,"edad" ]  # accede a la columna edad

```

Para la selección de una columna o de algún elemento de un dataframe tambien se usan los siguientes formatos:

* x[row,column]
* x$edad
* x[,"edad"]
* x[,1]
* x[x$gender == "M", ]

```{r}
w$Matematicas
w[w$genero=="M",]
w[w$Matematicas>6,]
```



# 5. Realizar un análisis descriptivo

Considerando que tenemos un dataframe, para realizar un análisis descriptivo y de inferencia

## 1. Localización de los datos

Deben ubicarse el mínimo y el máximo de los datos, calcularse las medidas de tendencia central y los percentiles.

```{r}
# Para el mínimo y el máximo la función es min() y max()
min(w$Matematicas)
max(w$Matematicas)
# Tres medidas de tendencia central usadas son el promedio, la mediana y la moda. Para la media se usa la función mean(), para la mediana median() y para la moda podemos usar table()
mean(w$Ciencias)
median(w$Matematicas)
table(w$Matematicas)

# Los cuantiles son aquellos valores que dejan por debajo de ellos un determinado porcentaje de los datos
quantile(w$Matematicas)
```
## 2. Variabilidad

Las medidas de localización deben acompañarse con una medida de la variación de los datos. Usualmente se calculan la amplitud,  varianza y desviación estándar.

```{r}
# La amplitud se defime como la diferencia del valor máximo y el mímino

range(w$Matematicas)

# La varianza y la desviación estándar

var(w$Matematicas)
sd(w$Matematicas)
```

## 3. Distribución de las frecuencias

La forma que tiene la distribución de las frecuencias de los datos es importante por ejemplo al seleccionar la medida de tendencia central a usar o la prueba estádistica que aplica para ese tipo de datos.

El gráfico útil para ver la forma de los datos es el histograma, cuya función en R es hist()

```{r}
hist(w$Matematicas)
```

En el caso de variables cualitativas, puede construirse un gráfico de barras o uno de pastel

```{r}
# Primero se hace una tabla con las frecuencias 
frecuencia <- table(w$genero)
barplot(frecuencia, main="Cantidad de hombres y mujeres")
pie(frecuencia, main="Cantidad de hombres y mujeres")

```


## 4. Valores extremos

Los valores muy grandes o muy pequeños afectan a las medidas de localización y a las de variabilidad, por esto, es importante verificar la existencia de éstos valores que en Estadística se denominan "extremos".

Hay varios métodos para detectar valores extremos, uno de ellos son los **boxplot** o **graficos de caja y bigote**.

```{r}
# Si un dato queda fuera de los bigotes de la caja, es extremo
boxplot(w$Matematicas)

# Genera un boxplot para las columnas de la 3 a la 6 del objeto W
boxplot(w[,c(3:6)])

# Genera un boxplot para las calificaciones de Matemáticas y Ciencias
boxplot(w$Matematicas,w$Ciencias)
```

## 5. Relación entre variables.

Es importante en ocasiones estudiar la relación que existe entre las variables de interés. En éstas situaciones el diagrama de dispersión y el coeficiente de correlación son dos herramientas indispensables.

```{r}
# El gráfico de dispersión de las calificaciones de Educación Física y Español
plot(w$EdFisica,w$Ciencias)

# El coeficiente de correlación
cor(w$EdFisica,w$Espanol)

```

La función summary() da un resumen descrptivo de los datos.
```{r}
summary(w)
```

# ¿Qué pasa cuando hay valores faltantes?

En muchas ocasiones (casi siempre :) ) hay datos faltantes. Automaticamente, en R , toda celda con las letras NA es considerada un valor ausente.

Para el uso de algunas funciones se debe informar a R de la existencia de valores extraviados.

```{r}
# Se llama al archivo con valores extraviados y se almacena en ww
ww<-read.csv("EjemploEstudiantesM_NA.csv",header=T)

# Se calcula la media indicando que hay valores extraviados
mean(ww$Matematicas,na.rm=T)
summary(ww)
```



Lugares para aprender
https://www.r-bloggers.com/
http://rpubs.com/
https://www.coursera.org/
https://www.edx.org/
https://www.datacamp.com/

