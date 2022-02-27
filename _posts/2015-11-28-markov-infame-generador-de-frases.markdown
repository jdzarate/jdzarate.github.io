---
layout: post
title:  "Márkov y el infame generador de frases."
date:   2015-11-28 12:30:00 -0600
published: false
excerpt: 
categories:
- blog
---

¿Has oído sobre Márkov? ¿Loco, no? Eh, de qué hablo. OK. Quizá no tienes idea, yo tampoco. Andréi Márkov fue un matemático ruso, quizá un descendiente de la familia Romanov, nadie puede estar seguro. A sus 30 años (en 1886) ya portaba una barba majestuosa y las chicas de Moscú lo hacían cantar y gritar, y cuando se aburría de tocar la balalaica se dedicaba a trabajar en teorías de números y de probabilidades. Parecía ser un tipo *cool*.

Lo traigo a colación porque en teoría de la probabilidad hay *"un tipo especial de proceso estocástico discreto en el que la probabilidad de que ocurra un evento depende solamente del evento inmediatamente anterior"*. Al parecer a esto se llama la cadena de Márkov o el modelo de Márkov y fue obra de este desenfrenado matemático ruso del que tanto hablo.

Es algo real, en serio, tiene demostración matemática y todo y la puedes chequear luego si es obtienes placer por ese tipo de cosas. Si no, creo que es seguro aceptar que el viejo Andréi se tomó el tiempo para corroborar que todo estuviera en orden. Hey, después de todo ¡el tipo tiene una página en Wikipedia!

Las cadenas de Márkov tienen muchísimos usos prácticos: meteorología, modelos de colapsos de la bolsa de valores, determinar volatilidad de precios, composición de música, Google usa las cadenas en sus algoritmos de *pagerank* y más. Claramente estamos hablando de cosas serias e importantes. 

¿Para qué me interesa a mí? Bueno, yo solo quería generar oraciones aleatorias a partir de libros; mis intenciones era cómicas, claro. No soy muy ocurrente así que creí que los algoritmos podían serlo por mí.

La idea era simple.

Se generan dos *base de datos*, la primera contiene todas las palabras de los libros en el mismo orden en que fueron publicadas, la segunda también pero se organizan en grupos de tres (tripletas) en donde las primeras dos palabras conforman una *llave* y la tercera el valor de esa llave, que es la palabra inmediatamente siguiente a las primeras dos. Claramente habrán llaves repetidas, el algoritmo se basa en eso para generar las diferentes salidas. Lo siguiente es obtener un número aleatorio, un índice que representa una palabra de la primera base de datos que contiene todo el texto, se suma una unidad al índice y se obtiene la segunda palabra, estas dos conforman la primera llave. Ahora, según Márkov, el siguiente valor de la cadena es dependiente de los eventos anteriores o en este caso, de las dos palabras anteriores. Se busca en la base de datos de *tripletas* todos los registros con llave igual a las últimas dos palabras generadas y se selecciona una de forma aleatoria. Se repite el proceso de selección N veces hasta que se cumpla el número mínimo de palabras predeterminado.

Como dije, simple. Si no, no importa, en las notas está el código fuente. Ahora pasemos a lo divertido, generar oraciones.

Mi primera ocurrencia fue usar Hamlet, el Hobbit y Cuentos de Cipotes de Salarrué.

> No se reventó, sólo siso un chindondo en la distancia. -Oh, adiós y vete de una hamaca, al frotar las argollas de hierro que para.

> ¡Triste! Y en diciendo así se irá al cielo... ¿y es esta la causa de la familia de las águilas. Cuando Bilbo se puso chalequito.

Nop. Intenté una y otra vez y los resultados siguieron siendo fatales.

Segundo intento, ahora incluí El Hobbit, Harry Potter y la Orden del Fénix, Los Juegos del Hambre y para darle algo de picante, 50 Sombras de Grey. Ahora sí estamos cocinando algo...

> Me gustaría deslizar la lengua por el chico del Distrito 1 que también parece vulnerable, ahora que me acostumbro a ir más lejos. Bien, bien! Bilbo

> Harry. Sí —dijo la mujer me inyectó el dispositivo de metal fino y flexible, tejido con un tono que parecía querer mostrar que está riquísima.

> Eso encaja perfectamente en la primera reunión de Potter en la arena, Peeta también podría quedarse atrapado en el centro del terreno de juego.

> Hermione, que continuaba sonriendo, la vieron marchar, hasta que Brutus le lanza otro beso en la estantería. —¿Qué ocurre? —inquirió Harry al instante, aturdido y furioso.

> y dijo—: ¡Alohomora! —Pero no la cuestiona. Simplemente ajusta los polvos en mi pecho.

Ay ay ay, esto está sobrecalentado. 

Pero no estaba satisfecho, principalmente porque las frases podían comenzar y terminar en cualquier parte y yo demando que inicie con una mayúscula y termine con un punto. Aquí no somos animales. En los ejemplos anteriores borré la parte inicial y final del texto generado y solo dejé la parte del medio hasta que llegara a un caracter de *final de oración*, lastimosamente no conservé los originales.

Hice cambios en mi solución. Generé una tercera *base de datos* que tuviera agrupaciones de dos palabras en la que la segunda fuera un caracter de final de oración, pues, que termine en un punto, signo de admiración y así.

Al inicio de mi algortimo, en lugar de eligir un índice aleatorio dentro de todo el conjunto de palabras se selecciona un valor aleatorio de esta tercera base de datos, luego busca en la base de *tripletas* una palabra aleatoria usando como llave una combinación que incluya un final de oración. Como la tercera palabra de la *tripleta* es la inmediata siguiente a la segunda de la llave, si la segunda representa el final de una oración, la tercera es el inicio la siguiente. Y así comienza a iterar de nuevo hasta que llega a otro final de oración siempre y cuando se haya obtenido una mínima cantidad de palabras.

Aunque no mejoró la composición de oraciones, sí tuve beneficios en el formato de la salida generada y eso clave en caso quisiera automatizar el algoritmo. La mayor parte de veces las frases no tienen sentido pero tampoco quiero empezar a hacer un análisis sintáctico, quizá debería, pero no lo haré, suena muy difícil. 

Más resultados usando la misma combinación de libros:

> Pero nuestro arreglo rápidamente se convierte en angustia, hasta que llegó al rellano donde Draco Malfoy estaba exultante, como si hubiese controlado el murmuro.

> Y pasaba mucho tiempo encerrado en aquella donde vimos el tributo del 5, así que meto el iPod en el Capitolio, y, al hacerlo, fotografías!

Quiero asumir que se trataba de un iPod Touch.

Me preguntaba también si los resultados serían mejores si uso texto en inglés, así que utilicé como base a The Martian de Andy Weir y Choose Yourself de James Altucher. 

> The potatoes will last 206 sols. There’s almost an afterthought. This doesn’t mean I traffic.

Ah Watney, negando los cargos contra él por el tráfico ilegal de patatas en Marte.

> Excuses are easy lies we tell Watney. This means you have three choices: YouTube ads, iTunes downloads, and performing.

Y mi favorita: 

> Bill Gates put himself in the still-pressurized Airlock 2, they opened the inner door regularly.

En general me gustaron bastante los resultados en inglés, sospecho que mucho tiene que ver la selección de libros, si estos tienen un lenguaje similar encajan mejor, más aún si buscas libros con muchas palabras. El contenido es clave para obtener mejores posibilidades.

Para terminar y en honor a una amiga que le gusta cierta película basada en un libro de Jane Austen y a otro amigo que es un Apple Fan Boy les presento la nueva creación basada mi algoritmo Márkov: "Orgullo y Prejuicio... y Steve Jobs". Nada como mezclar la Inglaterra del siglo 19 con un poco de tecnología cortesía de los genios de Cupertino.

> El iPhone quedó inmediatamente bautizado como el mejor sushi que he visto en mi querido Wickham, y quiso cosas.

> ¡Señor Bennet! ¿Cómo puedes hablar así de tus padres?. Tu madre desea lo que se hizo con Dell. Cuando convocó Jobs.

> La misma lady Catherine se encuentran cerca de Santa Clara con una grave expresión dirigió la mirada a los de Hewlett-Packard.

> Hablé sobre cómo gestionar los derechos digitales de sus creaciones sufren desafortunadas mutaciones a manos de los dos jóvenes Collins!

> Tomó a Elizabeth y su ingratitud que antes apenas me habría hecho su héroe, Wozniak, Smith se resistieron. Quería un inversor principal, no un vestido.

> La arenisca de Siena. La tienda iTunes y el señor Bennet consistía casi enteramente en una "espiral de muerte". Amelio miró fijamente a los aparatos.

> Perfectamente ―dijo Bingley―, fijémonos en todos los escenarios posibles. Jobs no estaba acostumbrado a oír algo muy parecido: le gustaba hablar a lady Catherine.

> Los señores Gardiner se sonrieron. Elizabeth no podía hacerlo. Le dijo a Jobs—. Podríamos llamarlo “Genius Bar”.

> A Jobs le resultó antipática la actitud de Darcy en un punto de vista empresarial, evitar la vergüenza. Reconocía de nuevo a Apple como decadencia.

Creo que pudo haber sido peor. ¿Quieres más? No hay problema, sigue este [link](http://wrteen.xyz/p/1jbSqJcaZd) y encontrarás más sobre esta infame historia de romance y codicia.

Nada más que agregar por hoy, ¡gracias Márkov!

J.D.

Notas

* [Cadenas Márkov](https://es.wikipedia.org/wiki/Cadena_de_M%C3%A1rkov)
* [Generating pseudo random text with Markov chains using Python](http://agiliq.com/blog/2009/06/generating-pseudo-random-text-with-markov-chains-u/), post de Shabda Raaj
* [Orgullo y Prejuicio y Steve Jobs](http://wrteen.xyz/p/1jbSqJcaZd).
* [Código fuente del generador de frases](https://github.com/jdzarate/markovsentpy)