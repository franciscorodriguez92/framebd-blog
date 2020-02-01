---
layout: post
title: Bloques de tipo Print
comments: true
date: 2015-05-06 07:34:25 -0700
categories: general
tags: regular
image: "/assets/images/background_print.png"
published: true
---

En FrameBD puedes representar tus resultados con nuestros bloques para gráficas. En este nuevo post aprenderemos la funcionalidad principal de cada bloque de gráficas. En FrameBD existen **7 tipos de gráfica.**

- **Bloque Print Result:**: para mostrar los resultados almacenados es útil para resultados numéricos que no deseamos pintar en una gráfica.

- **Bloque Print Line Plot:** Permite realizar gráficos de lineas, solo es necesario especificar los ejes X e Y con dos columnas de nuestros datos:
![](/assets/article_images/print_blocks/ejemplo1_2.jpg) 

Por ejemplo, se puede representar en un grafrico la variable X en el eje x y la variable hp en el eje y:

![](/assets/article_images/print_blocks/ejemplo1.png) 

- **Bloque Print Bar Plot:** Sigue la misma filosofía que el bloque anterior pero representado con barras: 
![](/assets/article_images/print_blocks/ejemplo2.png) 

- **Bloque Print Area Plot:** Sigue la misma filosofía que el bloque Print Line Plor pero con distinto diseño:
![](/assets/article_images/print_blocks/ejemplo3.png) 

- **Bloque Print Pie Plot:** Este bloque permite representar un diagrama tipo "pie" o pastel. La entrada label es una columna que especifica los nombres y values la columna numérica. Por ejemplo:
![](/assets/article_images/print_blocks/ejemplo4.png) 

- **Bloque Print Bubble Plot:** Este bloque permite representar un diagrama tipo burbuja. La ventaja de este tipo de representación es que permite representar hasta 4 variables. Las entradas x e y son equivalente a las del resto de bloques. La variable color asigna un color distinto a cada valor diferente de la columna de entrada y la variable size realiza la misma operación con el tamaño de la burbuja. Por ejemplo:
![](/assets/article_images/print_blocks/ejemplo5.png) 

- **Bloque Print Map Plot:** Permite realizar representaciones en el mapa especificando la latitud y la longitud en el formato latitud:longitud.

Esperemos que utilices nuestros bloques, si tienes alguna duda deja tu comentario!

