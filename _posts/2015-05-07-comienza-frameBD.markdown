---
layout: post
title: Comienza a usar FrameBD
comments: true
date: 2015-05-05 07:34:25 -0700
categories: general
tags: featured
image: "http://www.brettullman.com/wp-content/uploads/2014/11/bigstock-Start-Line-55468835.jpg"
published: true
---

En esta entrada aprenderemos como iniciarnos en el uso de la herramienta. Vamos a realizar el análisis muy sencillo de un fichero sobre la gestión del combustible de 38 modelos de automóvil para comprender mejor el funcionamiento de la herramienta. La filosofía de FrameBD es muy simple, compartes tus datos con nuestra plataforma, generas tu topología y ves tus resultados, así de sencillo. **La aplicación FrameBD la puedes encontrar en el siguiente [enlace.](https://franciscorodriguez.shinyapps.io/frameBD_alpha0_3)**

Para realizar este ejemplo puedes descargar los datos del siguiente [enlace.](https://www.dropbox.com/s/ueaaezqhq3wcj8l/mpg.csv?dl=0) No es **estrictamente necesario descargar los datos** ya que estos se encuentran en el servidor de FrameBD **únicamente los descargamos para ver su estructura en el siguiente apartado**.


## Estructura de los datos

Antes de comenzar con el análisis necesitamos conocer los datos y su formato. Para ello podéis cargar los datos en nuestro Data Explorer, señalando la pestaña **Data Explorer** y posteriormente el botón **Choose file**:
![](/assets/article_images/comienza_frameBD/ejemplo1.png)

Este paso nos permite observar la estructura de los datos pero no sube los datos a la aplicación, **únicamente vemos el formato de los datos en nuestro navegador.**
Si nos fijamos en detalle vemos que los datos están compuestos por **12 columnas que tratan sobre características de automóviles.**

- *X: Únicamente indica el numero de la fila.*
- *Manufacturer: Fabricante del automóvil.*
- *model: El modelo concreto del automóvil.*
- *disp: Cilindrada del vehículo.*
- *year: Año de fabricación.*
- *cyl: Número de cilindros.*
- *trans: Transmisión del automóvil (manual o automático).*
- *drv: Tipo de tracción del vehículo (f = tracción delantera, r = tracción trasera, 4 = 4wd).*
- *cty: Indica la distancia (en millas) que puede recorrer el coche por ciudad por cada 3.78 litros de combustible.*
- *hwy: Indica la distancia (en millas) que puede recorrer el coche por autopista por cada 3.78 litros de combustible.*
- *fl: Tipo de motor (e = ethanol, d = diesel, r = regular, p = premium y c = CNG).*
- *class: Tipo de automóvil (compacto, utilitario, etc).*

Por tanto, como hemos comentado, el dataset recoge las características de consumo de combustible de distintos modelos. En el siguiente apartado vamos a proceder al análisis del fichero que acabamos de describir.

## Análisis del fichero con FrameBD


### Lectura del fichero
Para analizar el fichero debemos de plantearnos la información útil que queremos obtener del mismo. Una característica importante que se puede obtener de los datos es **obtener las marcas que mejor gestionan el combustible.** Para eso, debemos crear una topología FrameBD **señalando la pestaña Topology.** El primer elemento que tenemos que crear en nuestra topología debe leer los datos para traerlos al sistema. Comenzamos cargando los datos con el bloque Read file que lo podréis encontrar en la pestaña Read>Read file, para especificar el fichero que queremos cargar necesitamos unir un bloque de texto al bloque Read file, lo podréis encontrar en la **pestaña Text Block** del workspace de FrameBD. Una vez unimos ambos bloques solo hay que escribir el nombre de nuestro fichero, en este caso mpg.csv:
![](/assets/article_images/comienza_frameBD/ejemplo2.png)

Si necesitáis más información sobre los bloques Read, podéis revisar un post de este blog que explica su funcionamiento **visitando este [enlace.](http://franciscorodriguez92.github.io/general/2015/05/07/Bloques%20Read.html)**

###Agrupamiento y creación de nueva columna
Tras cargar el fichero, la idea es obtener lo que consume los vehículos de cada marca. Para ello es necesario agrupar los datos por fabricante mediante el bloque group by que podréis encontrar en la pestaña **Block>Relational>group by:**
![](/assets/article_images/comienza_frameBD/ejemplo3.png)

Y para poder ver el consumo de cada marca necesitamos crear una nueva variable que calcule la media de kilometros de cada modelo. En este caso vamos a calcular la distancia media para los kilometros en autovía. Para ello empleamos el bloque summarise que permite crear una nueva columna y el bloque estadístico para realizar la media. El bloque summarise lo podréis encontrar en **Block>Relational>summarise** y el bloque estadístico en la **pestaña Block>Statistics & Maths>statistical operation:**
![](/assets/article_images/comienza_frameBD/ejemplo4.png)

Si necesitáis más información sobre los bloques Block y para qué sirve cada uno, podéis revisar un post de este blog que explica su funcionamiento **visitando este [enlace.](http://franciscorodriguez92.github.io/general/2015/05/07/Bloques%20Block.html)**

###Representación de los resultados
Finalmente, podemos ver esta nueva variable para cada fabricante con un diagrama de barras. Para representar este tipo de figuras se utiliza el bloque Print bar plot que podréis encontrar en la **pestaña Graphs>Print bar plot.** Si necesitas información acerca del funcionamiento de los bloques Print y sus variables x e y de entrada puedes visitar un post de este blog en el siguiente **[enlace.](http://franciscorodriguez92.github.io/general/2015/05/06/Bloques%20Print.html)** Una vez creada nuestra topología, pulsamos el **botón Run Blocks!** para ejecutarla y ver el resultado:   
![](/assets/article_images/comienza_frameBD/ejemplo5.png)

Como podemos observar, la marca Honda es la fábrica cuyos vehículos gestionan mejor el combustible por autovía, ¿sería lo mismo para ciudad?, vamos a comprobarlo. En este caso tenemos que aplicar la media a los kilometros que se recorren por ciudad (cty). Una vez creamos la nueva topología utilizamos el **botón Run Blocks!** para ejecutarla y ver el resultado:
![](/assets/article_images/comienza_frameBD/ejemplo6.png)

Como se puede comprobar, Honda sigue siendo la mejor marca.

## Un pequeño reto

¿Pudiste completar todo lo explicado? Si tuviste cualquier problema dejanos tu comentario!
![](http://www.madrimasd.org/blogs/emprendedores/files/2014/01/logo-retos.jpg)

Ahora te propongo un reto muy sencillo, **¿serías capaz de realizar una topología para encontrar el coche que peor gestiona el combustible?**

Si te animas, te propongo un segundo reto, **representar en un diagrama de barras la gestión del combustible de los modelos Toyota Corolla únicamente.** Suerte y a practicar!










