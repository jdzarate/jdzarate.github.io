---
layout: post
title:  "Considerando memorias microSD para almacenamiento interno"
date:   2015-11-13 08:00:00 -0600
excerpt: Cuando anunciaron la versión de desarrollo de Android 6 o M (por Marshmallow) hubo un feature que me llamó la atención: Android sería capaz de reconocer una memoria SD como almacenamiento interno.
categories:
- blog
---
Cuando anunciaron la versión de desarrollo de Android 6 o M (por Marshmallow) hubo un *feature* que me llamó la atención: Android sería capaz de reconocer una memoria SD como almacenamiento interno.

Eso era algo bueno, muy bueno de hecho, porque podría salirme con la mía y no caer en la estafa que pretende todo fabricante de dispositivos electrónicos: cobrar $50 por cada aumento de capacidad de almacenamiento. De verdad creí que podía comprar cualquier teléfono de 16 GB, conseguir una microSD de 32 GB por unos 12 dólares más y lograría paz mental sabiendo que no recibiría una notificación diciéndome que tengo poco espacio de almacenamiento, al menos por un buen rato.

Mi lógica era esta, la velocidad de escritura/lectura en una microSD es inferior a la memoria flash interna del teléfono pero si compraba una buena tarjeta la diferencia tal vez sería imperceptible. Lo primero que debía saber era cuál es la velocidad de la memoria interna.

OK Google... ¿cuál es la velocidad de lectura/escritura promedio de un teléfono? ... ... ... por favor no intentes hacer esto en casa, no es peligroso pero tampoco funciona. 

La respuesta depende un varias cosas, del SoC, la calidad de la memoria, si está encriptada o no, si es lectura/escritura secuencial o aleatoria, etc. Por diversión instalé una aplicación para que hiciera un *benchmark* en mi viejo, cansado y encriptado Nexus 4. Los resultados (cortesía de [AndroBench](https://play.google.com/store/apps/details?id=com.andromeda.androbench2&hl=en)) fueron algo decepcionantes.

<img src="http://i.imgur.com/ftJdI1W.png">

45 MB/s de lectura secuencial, 6.5 MB/s de escritura. 9.5 MB/s de lectura aleatoria y 1 MB/s de escritura. Está un poco patético en mi opinión, más aún cuando los comparo con el benchmark de los teléfonos Nexus de este año publicado por [indiatoday](http://indiatoday.intoday.in/technology/story/nexus-5x-vs-nexus-6p-checking-the-performance-difference/1/505556.html).

<img src="http://i.imgur.com/w10Gaqv.jpg">

Es irrelevante saber cuál es cuál pero creo que el de la derecha es el Nexus 5x y el de la izquierda el Nexus 6p.

OK. Más de 250 MB/s de lectura secuencial, más de 76 MB/s de escritura, más de 20 MB/s de lectura aleatoria y 11.5 MB/s de escritura. OK, son teléfonos de gama alta pero igual, supongo que podríamos esperar algo un poco más bajo con uno de gama media. O en el mejor de los casos, no me equivoco al creer que en un teléfono no encriptado, fácilmente la velocidad de lectura secuencia debería ser superior a los 100 MB/s y la de escritura más de 50 MB/s.

Ahora, volviendo al tema original. ¿Sería buena idea aprovechar esa nueva característica de Android y comprar una microSD en lugar de una  mejora de almacenamiento interno?

Una MicroSD Sandisk Ultra de 32 GB, clase 10 puede llegar hasta los 90 MB/s de lectura secuencial y 50 MB/s de escritura, más o menos parecido a los valores que sugería para una memoria interna no encriptada. Incluso podría pasarme de listo y gastar un poco más del doble y conseguir una con valores de escritura hasta los 90 MB/s. Sería por gusto, primero porque quizá el SoC del dispositivo no soporta estas velocidades y segundo, porque este valor realmente no me importa.

Si lo que quiero es reemplazar la memoria interna el valor que debería importarme es el de lectura/escritura aleatoria, no me interesa poder leer canciones o videos HD, quisiera utilizarla para aplicaciones y sus datos.

En ningún caso he visto velocidades de lectura/escritura aleatoria superiores a los 10 y 3 MB/s respectivamente. Claramente la microSD no está encriptada, así que habría que tomar eso en consideración. Si se encripta tal como la memoria interna la velocidad se vería reducida en un resto y tres cuartos aunque no tengo datos reales para poder validar esto.

¿Sería suficiente para que funcione como memoria interna? Quizá con un formato de sistema de archivos adecuado, no sé. Los números dicen algo pero al final lo que importa es cómo funciona en la práctica. Puede que en números funcione, pues, mi Nexus 4 era más o menos tolerable.

Igual me quedan otras inquietudes, dado que es un nueva característica de Google y no hay mucha documentación real sobre cómo funciona porque ningún Nexus tiene adaptador para microSD. ¿Sería prudente confiar que el SO operativo trabajará igual? ¿las aplicaciones trabajarán adecuadamente? ¿qué pasaría si la microSD deja de funcionar? Sospecho que debe haber algún *bug* merodiando.

Todavía no tengo ni la más mínima idea de cómo responder esas preguntas pero leyendo Reddit me enteré de algunas particularidades bastante interesantes de este *feature* y la verdad es que no quedé muy convencido de que sería una buena opción poner todos mis malvaviscos en esta canasta.

Más sobre esto en unos días.

J.D.
