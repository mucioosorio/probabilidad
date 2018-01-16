## Instalación de R, R Studio y Jupyter.


Las tres herramientas que deben instalarse para el curso son **R**, **RStudio** y **Jupyter** (a éstos  dos últimos se puede acceder desde la plataforma de ANACONDA)

![r_rstudio_jupyter](/probabilidad/figs/00_r-jupyter-rstudio.PNG)

## 1. Instalación de R. 

En el curso se usará el lenguaje de programación para análisis y visualización de datos **R**. Para más detalles vea ["https://www.r-project.org/"](https://www.r-project.org/) 

![pagina_r](/probabilidad/figs/03_pagina-r.PNG)

Debe descargar e instalar la versión que corresponda a su sistema operativo desde la página ["https://cran.itam.mx/"](https://cran.itam.mx/) 

![instalacion_r](/probabilidad/figs/04_instalacion-r.PNG)

## 2. Instalación de Anaconda y RStudio. 

Para la instalación de Jupyter descargue la plataforma **Anaconda** (para el sistema operativo que use) del sitio ["https://www.anaconda.com/download/"](https://www.anaconda.com/download/) 

En el cursos se usará la versión que contiene Python 3.6

![web_anaconda](/probabilidad/figs/01_sitio-anaconda.PNG)

Una vez instalada la plataforma de Anaconda, inicie **Anaconda Navigator** e instale RStudio desde allí.

![navigator_anaconda](/probabilidad/figs/02_anaconda-navigator.PNG)

Ahora, inicie **R Studio** y ejecute en la consola lo siguiente. Hasta que no ejecutes esto no tendrás disponible R en Jupyter. (ver ["https://irkernel.github.io/installation/"](https://irkernel.github.io/installation/)


```R
install.packages(c('repr', 'IRdisplay', 'evaluate', 'crayon', 'pbdZMQ', 'devtools', 'uuid', 'digest'))
devtools::install_github('IRkernel/IRkernel')

IRkernel::installspec()
```

![kernel_r](/probabilidad/figs/05_instalacion-kernelr.PNG)

Finalmente, para poder trabajar en **Jupyter**, abrá la aplicación desde **Anaconda Navigator** o desde el menú de inicio de windows.
