---
layout: post
title: Bloques de tipo Read
comments: true
date: 2015-05-07 07:34:25 -0700
categories: general
tags: regular
image: "/assets/images/read_blocks.png"
published: true
---

Como se ha comentado en entradas anteriores en FrameBD existen 4 tipos de bloques: **Read, Block, Write y Print.** En este caso vamos a detallar el primero de los bloques, **el bloque Read**. Por ahora, en FrameBD únicamente se pueden leer archivos en formato .csv, se irá ampliando funcionalidad en este aspecto.


## Leer archivo .csv: Read block
Para leer un fichero en formato .csv necesitamos utilizar el **bloque Read file:**, para encontrar este bloque debemos seleccionar la pestaña Read y arrastrarlo a nuestro workspace. Posteriormente, para especificar el nombre del fichero se utiliza el **bloque de texto** que podemos encontrar en la pestaña Text Block. Por ejemplo, si queremos leer un fichero llamado coches.csv, tendríamos la siguiente estructura:

![](/assets/article_images/read_blocks/ejemplo1.png)


Si queremos ver si el fichero se ha leido correctamente, podemos ver el resultado del bloque Read block mediante el bloque **Print Result** que se encuentra en la pestaña Graphs:

![](/assets/article_images/read_blocks/ejemplo2.png)

Hasta este punto, tendriamos los datos listos para empezar a trabajar con ellos con el resto de bloques.


## Data Explorer
Si deseas observar la estructura de datos del fichero que lees, puedes utilizar nuestro explorardor de datos seleccionando en el sidebar de la izquierda la opción **Data Explorer**. Es una sencilla interfaz que permite mostrar por pantalla los datos. Para subir el fichero, pulsa sobre el botón Choose File y elige tu fichero .csv:

![](/assets/article_images/block_blocks/ejemplo2.png)

