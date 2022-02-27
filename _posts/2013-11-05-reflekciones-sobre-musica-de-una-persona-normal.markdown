---
layout: post
title:  "Reflekciones sobre críticas de música de una Persona Normal"
date:   2013-11-06 12:00:00
excerpt: Reflekciones sobre reflekciones sobre reflekciones sobre reflekciones de críticas de música.
published: false
categories:
- blog
---
Tengo una maña. Luego de escuchar varias veces un nuevo álbum de música (nuevo para mí) busco reviews. No los busco porque quiero validar que el álbum es bueno o malo, a este punto ya he formado mi opinión, los busco porque me cuesta expresar con palabras lo que sentí luego de escucharlo. Necesito ayuda (y un tesauro) y espero que tal vez alguno de los expertos pueda describir mis sensaciones con sus palabras.

La última vez que hice esto fue la semana pasada. El martes 30 recibí el correo que estaba lista la descarga de la pre-orden de mi primer compra de un álbum digital: Reflektor de Arcade Fire. 

Después de escucharlo toda la semana recurrí nuevamente a los críticos y por fin caí en la cuenta. No sé si solo soy yo pero me parece que el estado de las críticas musicales es lamentable, es un desastre. Aún cuando leo todo el contenido de la crítica no encuentro razones que fundamenten una calificación ya sea favorable o no.

Básicamente funciona así: el crítico escribe un artículo en el que compara canciones del álbum con otras canciones u otras bandas, artistas, lo que sea, define géneros y después asigna una nota en cualquiera de los sistemas de calificación "estándar": un número entre 1 y 10,  el sistema de 5 estrellas o el sistema de letras en el que la "A" significa "Awesome" o algo parecido.

¿Pero en qué se basa la "calificación"? Esto no es como en Rock Band (el video juego) en el que la canción tiene cierta dificultad y así se asignan la cantidad de estrellas, eso en efecto tiene sentido. No, acá todo es subjetivo y tampoco me refiero a algo como Anthony Kiedis asignándose 10 en “vocals” en el video de Californication (sí, claro); todo depende de la interpretación del crítico y si no existen métricas, simplemente deberían limitarse a redactar el artículo, lo cual no sucederá porque, lastimosamente, siempre buscamos la versión corta de todo y 4/5 estrellas nos dice que algo está por encima del promedio tan rápido como de repente.

Pero quería colocar ejemplos, y por qué no reviews del mismo Reflektor.

##### Drowned In Sound
![Drowned]({{ site.url }}/assets/reflekciones/drowned.png)

4/10 porque las canciones son muy largas y no lo justifican. Hey, bajo esa lógica podría decir que “Hey Jude” apesta porque incluye casi 4 minutos de tipos cantando “Hey Jude, Hey Jude” y sería lo mismo o peor con “I Want You (She’s so Heavy)”. Es más, ¿por qué no quitamos los "coros" de las canciones de una vez por todas? Parece que son redundantes y nos quitan más de nuestro preciado tiempo: di algo una vez, ¿por qué decirlo de nuevo? (Psycho Killer, Qu'est-ce que c'est).

##### Pitchfork Magazine
![Pitchfork]({{ site.url }}/assets/reflekciones/pitchfork.png)

9.2/10 porque sabe escribir combinaciones de palabras que tienen sentido para nadie como "glam-rock earthquake" y notó influencias de discos importantes como "Remain in Light" o "The White Album". Al parecer eso le da la potestad para colocar una nota, no de 9 sino de 9.2. ¡9.2! ¿por qué no 9.1 ó 9.3? Quizá, en su genialidad, significa que es el promedio de las canciones utilizando la fórmula que propone [adamannapolis en el foro de rateyourmusic.com][link-to-rateyourmusic]. 

Código en Python (asumiendo que no utilizan una media ponderada):
{% highlight python %}
'''
Pitchfork Rating Function
Basic Python, Hipster University.
'''
def pitchfork_rating(adict):
	#given a dictionary like adict = { 'song 1': 10, 'song 2': 7, 'song 3': 9}
	return round(sum(adict.values())/len(adict),1)
{% endhighlight %}

Y otra cosa Pitchfork, si alguien de "Drowned In Sound" hiciera un review de tu review podría otorgarle una calificación de 4/10 porque toma casi 10 minutos para leer 1600 palabras cuando pudieron haber reducido todo el artículo a 140 caracteres o menos.

Creo que la única persona que más o menos lo tiene descifrado (que yo sepa) es Robert Christgau. El entiende que no basta con asignar un número o una letra sino que debes decir qué significa. Por eso en su página Web coloca una [guía de referencia para sus calificaciones][link-to-christgau].

![Christgau]({{ site.url }}/assets/reflekciones/christgau.png)

Sí, es un poco aleatoria pero al final todas las reseñas lo son; al menos te está diciendo por qué asignó lo que asignó, por muy personal o subjetivo que sea, hizo el intento de definir una métrica. Pero termina siendo inútil porque puede que muy pocos la lean.

Al final no se resuelve nada. Creo que eso es todo. Es lo que es.

Por cierto, ¿qué tal mi reseña sobre Reflektor?

<img src="{{ site.url }}/assets/reflekciones/loop.png" style="width:auto; vertical-align:middle; margin-right: 10px;">

Basado en mi [sistema alternativo para calificar la música que amas o que desprecias][link-to-system] ... y no, todavía no tengo el código en Python.

Si quieres criticarme, puedes encontrarme en Twitter en [@jdzaratem][link-to-twitter].


[link-to-twitter]: https://www.twitter.com/jdzaratem
[link-to-christgau]: http://www.robertchristgau.com/xg/bk-cg90/grades-90s.php
[link-to-rateyourmusic]: http://rateyourmusic.com/board_message/message_id_is_2684293
[link-to-system]:{{ site.url }}/assets/reflekciones/review-system.png
