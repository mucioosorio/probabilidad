0. Uso de R como calculadora
+, -, *, / log() ^  suma, resta, producto, cociente logaritmo, potencia
>, >=, <, <= mayor que, mayor o igual que, menor que, menor o igual que
D(expression(log(x)), "x") Derivada de una función
integrate(function(x) {1/((x+1)*sqrt(x))}, 1, 2) Integral definida


# TALLER DE R PARA ESTADISTICA DESCRIPTIVA.

NOTA. En R, los comentarios se indican con el símbolo de número "#"

Considere que se mide las estaturas de varias personas.Las respuestas son:  

1.82 1.66 1.68 1.74 1.57 1.65 1.65 1.81 1.76 1.70 1.69 1.66 1.80 1.66 1.67 1.63 1.65
1.69 1.76 1.57 1.63 1.62 1.72 1.75 1.77 1.72 1.68 1.69 1.73 1.63 1.66 1.84 1.50 1.71
1.61 1.72 1.63 1.69 1.60 1.77

En Estadística, lo habitual es trabajar con colecciones o muestras de datos.
Para almacenar esas colecciones de datos, la estructura más básica
son los vectores. 
Para definir un vector se usa la función de concatenar "c()"

A continuación se crea un objeto llamado "x" al que se le asignan 
(con el símbolo "<-" ) las estaturas de 40 personas

x <- c(1.50, 1.57, 1.57, 1.60, 1.61, 1.62, 1.63, 1.63, 1.63, 1.63, 1.65, 1.65,
       1.65, 1.66, 1.66, 1.66, 1.66, 1.67, 1.68, 1.68, 1.69, 1.69, 1.69, 1.69,
       1.69, 1.71, 1.72, 1.72, 1.72, 1.73, 1.74, 1.75, 1.76, 1.76, 1.77, 1.80,
       1.81, 1.82, 1.84, 1.91) # para ejecutar este renglón oprima “RUN”

Una vez que se ha almacenado la información ahora realizaremos
el análisis descriptivo.

# 1. Medidas de Posición
¿Cuál es la estatura mínima?
min(x)              

¿Cuál es la estatura máxima?
max(x)           
 
¿Cuál es la media de las estaturas?.
mean(x)         

¿Cuál es la mediana de las estaturas?
median(x)    

¿Cuál es la moda de las estaturas?
table(x)    
la función anterior genera una tabla con los datos y la cantidad
de veces que aparece cada uno. Solo debe elegir cual es el
dato que más veces aparece.

¿Cuáles son los percentiles de las estaturas?
quantile(x)       

# 2. Medidas de Dispersión

¿Cuál es la amplitud de las estaturas?
range(x)

¿Cuál es la desviación estándar de las estaturas?.
sd(x)          

¿Cuál es la varianza?
var(x)     

# 3. Valores extremos
Construya una gráfica de caja y bigote y vea si hay valores extremos
boxplot(x)
boxplot(x,
        notch = T,
        main = 'Estaturas de alumnos')     

# 4. Distribución de frecuencias
Construya un histograma de los datos
hist(x)
hist(x,
     main = 'Estaturas de alumnos',
     xlab = 'm',
     ylab = 'Número de alumnos',
     col = 'pink')

# 5. Correlación entre dosvariables
Los siguientes datos representan los pesos de las 40 personas
y <- c(37.6, 43.1, 44.1, 45.8, 46.5, 47.5, 49.1, 52.1, 52.2, 53.2, 53.9, 55.5,
       55.7, 56.6, 56.7, 57.3, 57.4, 57.6, 58.9, 60.0, 61.2, 61.4, 62.3, 62.9,
       63.1, 63.6, 63.7, 64.5, 64.6, 65.3, 67.9, 68.5, 70.3, 75.0, 75.9, 77.2,
       77.9, 89.9, 92.2, 92.7)

En el siguiente vector 1 representa mujer y 2 hombre

g <- c(1,1,1,1,2,1,2,1,1,2,1,1,1,1,2,2,2,2,2,2,2,1,2,1,1,2,2,2,2,2,2,2,1,2,2,2,2,2,2,2)

Gráfico de barras

barplot(table(g),names.arg = c('Mujeres','Hombres'))
pie(table(g),labels = c('Mujeres','Hombres'))

Diagrama de dispersión
plot(x,y)
plot(x,y,
     main = 'Relación entre estaturas y pesos',
     xlab = 'Estatura (m)', 
     ylab = 'Peso (kg)',
     col = g)

¿Cuál es la correlación entre los pesos y las estaturas?
cor(x,y)

