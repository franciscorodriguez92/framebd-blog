---
layout: post
title: Bloques de tipo Block
comments: true
date: 2015-05-07 07:34:25 -0700
categories: general
tags: regular
image: "/assets/images/blocks.png"
published: true
---

En este post vamos a hablar de los bloques más importantes que existen en FrameBD los bloques **tipo Block**. Dentro de este tipo de bloque existen 4 subcategarorías:

> - Maths & Statistics: Tenemos 3 tipos de bloques que permiten realizar operaciones estadísticas básicas, aritméticas y el sumatorio de datos.
> - Relational: Distintos tipos de bloques para realizar las operaciones más comunes en un análisis de datos como, agrupar, filtrar o crear nuevas columnas.
> - Algorithms: Actualmente está disponible un algoritmo de agrupación de datos.
> - Custom blocks: Este bloque permite realizar tus propios diseños con tu código R o importar los bloques que comparten el resto de usuarios.


## Maths & Statistics

En esta categoría disponemos de **3 bloques** que se pueden ver a continuación: 

![](/assets/article_images/block_blocks/ejemplo1_blocks.png)

- **Bloque estadístico:** Permite aplicar una operación estadística a cualquier columna o variable de nuestros datos. Se permiten la operación media, mediana, mínimo, máximo, desviación estandar y varianza. El siguiente ejemplo calcula la media de la variable hp del fichero de datos coches.csv:

![](/assets/article_images/block_blocks/ejemplo3.png)

- **Bloque de operaciones aritméticas:** Permite realizar operaciones aritmética básica sobre nuestras columnas. 

- **Bloque suma:** Realiza el sumatorio de todos los valores de la columna indicada. Por ejemplo, la suma de todos los valores de la variable hp de nuestro archivo coches.csv:

![](/assets/article_images/block_blocks/ejemplo4.png)

## Relational

En esta categoría disponemos de **6 bloques** que se pueden ver a continuación: 

![](/assets/article_images/block_blocks/ejemplo5.png)

- **Bloque profiling:** Permite realizar un profiling de tus datos. Arroja información de las características del fichero y sus variables.

- **Bloque filter:** Permite filtrar los datos con una determinada condición. Por ejemplo, vamos a seleccionar aquellas entradas de nuestro conjunto de datos en los que la columna hp es igual a 110: 
![](/assets/article_images/block_blocks/ejemplo6.png)

- **Bloque distinct:** Elimina todas las filas duplicadas de nuestros datos.

- **Bloque mutate:** Permite crear nuevas columnas en nuestro conjunto de datos. Debemos especificar el nombre de nuestra nueva columna en el campo var name. En este bloque podemos incluir operaciones de los bloques de Maths & Satistics. Por ejemplo, vamos a crear una nueva columna llamada "suma" sumando las columnas hp y mpg de nuestros datos:
![](/assets/article_images/block_blocks/ejemplo7.png)

- **Bloque group by:** Permite agrupar los datos por alguna variable. Este bloque se suele utilizar junto con el **bloque summarise** para crear una nueva columna con la variable agrupada. 

- **Bloque summarise:** Permite crear una variable al igual que el bloque mutate pero con los datos agrupados. **Se suele utilizar tras el bloque group by.** Típicamente los datos iniciales son agrupados y se crea una nueva columna manipulando las variables agrupadas:
![](/assets/article_images/block_blocks/ejemplo8.png)

## Algorithms

Actualmente disponemos del bloque kmeans que aplica en algoritmo de agrupamiento a nuestros datos de entrada. Únicamente es necesario especificar el numero de agrupaciones que deseamos:
![](/assets/article_images/block_blocks/ejemplo9.png)

## Custom blocks

En este apartado, se pueden crear bloques propios con código R o algoritmos concretos que quieras ejecutar sobre tus datos. Con el bloque **Code Block** puedes escribir el código R que deseas ejecutar:
![](/assets/article_images/block_blocks/ejemplo10.png)


Si tienes alguna duda dejanos tu comentario!








