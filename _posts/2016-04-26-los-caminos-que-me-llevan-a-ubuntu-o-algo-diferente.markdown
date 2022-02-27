---
layout: post
title:  "Los caminos que me llevan a Ubuntu o a algo diferente"
date:   2016-04-26 22:20:00 -0600
excerpt: No sé si es frustrante o reconfortante que los caminos que tomo en el mundo de Linux siempre me llevan a Ubuntu, el bueno y confiable Plan B.
published: false
categories:
- blog
---

Este sábado pasé todo el día reemplazando el disco duro de mi laptop por un SSD. La clonación de mi partición de Windows tomó 1 hora y funcionó impecablemente. Para mi partición de Linux comenzaría de cero instalando un OS más reciente ya que el que tenía instalado se estaba volviendo obsoleto.

[@corenominal][corenominal] - el desarrollador de mi sistema vigente (Crunchbang OS) - abandonó su proyecto, así que no me quedó más remedio que evaluar otras opciones. Pasé semanas debatiendo internamente y me decanté por [Ubuntu][ubuntu] simplemente por su historial de ofrecer buen soporte y compatibilidad con casi cualquier *hardware*. La última versión se lanzaría el 21 de abril así que esperé hasta ese fin de semana para proceder con la instalación.

Pero ese viernes tuve dudas... cada vez que veía screenshots de Ubuntu y sus variantes me hacían valorar la sencillez de Crunchbang y cuanto me encanta. No era resistencia al cambio sino renuencia a arruinar lo que ya funciona. Lo que necesitaba era Crunchbang pero con el *kernel* de Linux y librerías lo suficientemente recientes como para instalar las últimas versiones de los programas que utilizo.

Y así terminé descargando [Crunchbang++][cbpp], un *spin-off* del original. Me dio paz mental aún sabiendo que estaba repitiendo los mismo errores que me llevaron a este punto. Pero esta vez me hice una promesa: si algún componente no funciona, indicador de batería o lo que sea, instalaría Ubuntu y no perdería mi tiempo intentando resolverlo.

Lo instalé y para mi sorpresa, el indicador de batería que tantos problemas me dio en el pasado funcionaba bien. Sí encontré un problema y uno muy importante: no tenía WiFi. En teoría algo fácil de resolver: instalaría los controladores propietarios del fabricante y listo. 

Descargué los controladores, los instalé, incluso reinicié la laptop y nada... leí en algún lado que el fabricante no soportaba la versión del *kernel* de Linux superior a 3.16 o algo, no sé, me pareció pura porquería. De seguro había solución pero estaba demasiado frustrado para buscarla. Lo más fácil era cumplir mi promesa e instalar Ubuntu.

Y tal como lo supuse todo funcionó a la perfección: batería, WiFi, audífonos, todo. Me odiaba a mí mismo y a mi nueva interfaz gráfica. Eventualmente instalé un [tema visual basado en Material Design][ubuntu-paper], me aprendí unos cuantos shortcuts de teclado y sentí que no era tan malo después de todo.

No sé si es frustrante o reconfortante que los caminos que tomo en el mundo de Linux siempre me llevan a Ubuntu, el bueno y confiable Plan B.

Igual no dejo de pensar que se supone que después de 5 años no debería tener problemas de compatibilidad con mi *hardware*, que francamente, no es tan especial. ¿Qué pasará cuando llegue el día en que me toque comprar una nueva computadora?

No creo que me equivoque suponiendo que tendré que pasar por los mismos problemas de compatibilidad o más. Pues, al menos esta vez no tuve problemas con *drivers* de tarjetas gráficas o el cambio del BIOS por el UEFI Secure Boot, pero quien sabe si me tocaría enfrentarme con algo peor. A eso hay que sumarle el pobre soporte de Software ya que la mayoría de compañías trata a Linux como ciudadano de segunda categoría.

Puede parecer una nimiedad pero es increíble que recién este sábado pude ver Netflix en Linux con Google Chrome (y solamente con ese navegador). Es un ejemplo del tipo de incovenientes que no tendría con Windows u OS X.

A veces me parece que los problemas con Linux son como enfrentarse a [Hydra][hydra], cortas una cabeza y aparecen dos en su lugar.

Solo por curiosidad, al final de mi proceso de instalación y con el estómago lleno, intenté averiguar qué distribución de Linux usa @corenominal. Pues, si abandonó el proyecto debe usar algo mejor. Para mi sorpresa (realmente no me sorprendió) [hace meses que usa OS X][osx]. Muchas veces pienso que yo debería hacer lo mismo.

J.D.

[corenominal]: https://www.twitter.com/corenominal
[ubuntu]: http://www.ubuntu.com/
[cbpp]: https://crunchbangplusplus.org/
[ubuntu-paper]: https://snwh.org/paper/theme
[gnu]: https://es.wikipedia.org/wiki/Proyecto_GNU
[osx]: https://corenominal.org/2015/12/31/new-years-resolutions-2015-the-results/
[hydra]: https://es.wikipedia.org/wiki/Hydra_(c%C3%B3mic)
