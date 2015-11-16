---
layout: post
title:  "Detalles del formato de memoria interna de una microSD con Android M"
date:   2015-11-15 22:00:00 -0600
excerpt: Puntos claves a tomar en cuenta antes de formatear una microSD como memoria interna para un dispositivo Android, solo es posible *ver* la capacidad de almacenimiento de la MicroSD y otros detalles.
categories:
- blog
---

En mi [post anterior](http://www.jdzarate.com/blog/2015/11/13/considerando-memorias-microsd-para-almacenamiento-interno.html) escribí sobre mis problemas para decidir si sería una buena idea utilizar una micro SD para expandir el almacenamiento interno de un dispositivo.

El feature de Android M me parece genial pero a corto plazo, con las bajas velocidades de lectura/escritura de las microSD del mercano y lo poco probada que está esta característica no me parecía buena idea depender de esta solución, mucho menos si pensaba invertir más de $400 dólares en un teléfono de 16GB que esperaba conservar al menos 2 años.
 
Hace tres semanas leí un *post* en reddit escrito por /u/stereomatch. Este es el enlace: [Guidelines for Marshmallow users - formatting options for external SD cards (Portable vs. Internal modes)](https://www.reddit.com/r/Android/comments/3oz7eu/guidelines_for_marshmallow_users_formatting/). Está muy completo y se le recomiendo a cualquiera que esté interesado en cómo funciona este nuevo formato para las tarjetas SD de Android M.

Los puntos clave son los siguientes:

* Al usar la SD como memoria interna esta adquiere el formato ext4 y se encripta, la velocidad original se reduce aún si ext4 fuese más rápido que fat32, no tengo datos pero tampoco creería que hay mucha diferencia entre los formatos.

* Después de la conversión a memoria interna solo es posible *ver* la capacidad de almacenimiento de la MicroSD. La memoria interna original está allí pero no puede ser accedida por apps como ES File Explorer. Esto también aplica cuando se conecta el dispositivo a una computadora. Así, si tienes un teléfono de 32GB y una SD de 16GB a la que le das este formato, cuando conectes el teléfono a la computadora solo podrías ver los 16GB de la tarjeta externa.

* El almacenamiento interno original no desaparece pero sí se pierde el control sobre este. Los archivos de sistema y aplicaciones preinstaladas estarán aquí y no se pueden mover, sí se podrá mover otras aplicaciones entre las dos memorias pero queda a criterio del usuario decidir qué tipo de memoria conviene para cada aplicación. 

* Otros tipos de acceso se pierden, por ejemplo, ya no puedes copiar archivos, fotos o canciones directamente a la memoria interna.

Si alguien compra un dispositivo 32GB o más, o aún de 16GB estaría haciendo un *gran* compromiso al optar por darle formato de memoria interna a una tarjeta SD. Invertir en esa cantidad de memoria para luego perder control sobre esta para darle prioridad a una memoria de velocidad más baja es contraproducente. Además de la poco óptima organización del espacio se corre el riesgo de tener problemas de *performance* y es justo lo que quieres evitar cuando compras un teléfono *caro*.

De momento me parece que sirve como una medida desesperada para darle un poco más de vida a dispositivos viejos con poco espacio de almacenamiento (8GB o menos). Para el resto no creo que sea apropiado, es solo algo experimental que puede que mejore en un futuro.

Es mejor esperar, puede que a corto plazo la memoria interna se vuelva más barata o que los fabricantes corten por lo sano y no vendan teléfono o tablets con espacio insuficiente. O si esto no sucede puede que las microSD logren velocidades aceptables para este propósito y Google talvez ha mejorado los detalles en la implementación del *feature*. Solo especulo.

Mi recomendación sería hacer un análisis de la cantidad de espacio interno que necesitas y hacer proyecciones de cuánto aumentaría durante el tiempo que piensas conservar el teléfono y considerar una SD Card como un bono. Pero como eso no va a suceder mejor haz lo mismo que yo: comprar un dispositivo de al menos 32 GB y olvidarte del asunto.

J.D.