---
layout: post
title: "El modelo de la vergüenza"
date:   2014-03-21 12:00:00
excerpt: En el que escribo sobre lo difícil que es cobrar por software y cómo, talvez y solamente talvez, podría ser más sencillo.
published: false
categories:
- blog
---
Desde el lanzamiento de [Crupzi.com][link-to-crupzi] en octubre de 2012 se tenía la idea de que sería un servicio gratuito para los usuarios. Los comercios pagarían mensualmente el uso de la plataforma que les ofrecía la posibilidad administrar sus descuentos y recibir estadísticas anónimas sobre visitas de usuarios. Después de un año y medio, todavía no hemos cobrado un centavo.

Aparte de que recibir pagos por Internet en El Salvador es tan complicado como aprender el nombre del viento, muchas veces no tenemos idea de cuánto podríamos cobrar por un servicio. 

Supongo que sería fácil definir 3 planes y asignarle un valor incremental semi-aleatorio a cada uno: gratis - acceso "mejor que nada", $25 - features algo útiles, $100 - los mismos features del plan de anterior más una cena con los co-fundadores, etc. Pero estaríamos en una situación en la que cobraríamos a partir de las proyecciones de las ganancias que quisieramos obtener en base a la cantidad de clientes que podríamos atraer sin tomar en cuenta lo que realmente cuesta el servicio (lo siento, claramente no soy un hombre de negocios).

#### Un modelo de negocios con solo dos números


En 1997, Derek Sivers fundó cdbaby.com, una tienda de discos en línea para músicos independientes. En su libro ["Anything you Want"][link-to-anything] describió su modelo de negocios:

> Fui a una tienda de discos local en Woodstock y pregunté: ¿cuánto me costaría vender mi CD aquí? La mujer que me atendió me dijo: Tú estableces el precio de venta, cobra lo que quieras, pero nuestra comisión es de $4 por disco. Si era lo suficientemente bueno para ella, estaba bien para mí... Como me tomaba 45 minutos subir el disco al website, decidí cobrar $25 como compensación por mi tiempo (demostrando cuánto valoraba mi tiempo esos días). Un par de días después me di cuenta que $35 era casi lo mismo que $25. Decidí aumentar el precio para tener espacio para descuentos y siempre obtener ganancias. ¡Y eso es todo! 6 años y $10 millones después, esos 2 valores son la fuente de ingresos de la compañía.

Fácil, supongo.

#### Un modelo de negocios basado en la vergüenza

Gina Trapani es la creadora del app [todo.txt][link-to-todo]. El app me pareció interesante por 3 motivos: el contenido está basado en un archivo de texto sincronizado en Dropbox, el precio es $2 y es Open Source, eso quiere decir que el código de la aplicación está disponible públicamente.

Ah qué curioso. Una aplicación "de paga" y Open Source a la vez. El código está allí; específicamente te dicen: puedes descargarlo, compilarlo e instalarlo en tu teléfono (o tablet) pero si crees que tu tiempo es más valioso, puedes descargar el app desde tu tienda favorita por solo 2 dólares (esto último no lo dicen realmente).

No he probado la aplicación pero si realmente la quisiera no dudaría en pagar ese 2 dólares. La vergüenza me obligaría a eso porque sé que aparte del trabajo que tomó hacer el app, el tiempo que me tomaría compilarla vale más que dos dólares.

Hay similitudes con el modelo de Sivers. En ambos casos están cobrando lo que cuesta poner a funcionar el servicio. Sivers no cobró por la construcción de la plataforma, cobró por poner álbumes en el sistema. De manera burda, podría decir que Gina cobra por la instalación de la aplicación y sus actualizaciones.


#### ¿Qué hay de las webapps?

Mi proyecto más reciente es [Quoffee.com][link-to-quoffee], un sitio Web para organizar citas de libros, películas, canciones, blogposts, etc. Cuando comenzó el desarrollo fue pensada como una herramienta de uso estrictamente personal pero creímos que sería más interesante permitir cierta interacción o colaboración entre usuarios.

Fácilmente, si decidiéramos liberar el código y hacerlo Open Source, alguien podría descargarlo, instalarlo en un servidor y utilizar el software de manera privada porque los demás usuarios no son indispensables para que el programa sea funcional. Sin embargo, esta persona se daría cuenta de que su uso no sería gratuito porque tendría que pagar por el alojamiento (hosting) de la aplicación y de la base de datos. 

Siguiendo el modelo de la vergüenza; en lugar de pagar ese hosting de terceros por qué no pagar por el "hosting" que Quoffee ya provee intrínsecamente. Quoffee tendría que ser responsable de cobrar según cuotas (quotas) de uso y/o almacenamiento.

No estoy sugiriendo el modelo de negocios de Quoffee, el problema que pretendía abordar es que es difícil ponerle precio al software y me pareció sencilla la forma de determinar cuánto cobrar en base a lo que toma ponerlo a funcionar y no usar valores casi aleatorios que se preguntan cuánto es lo máximo que alguien pagaría.

[link-to-anything]: http://amzn.to/1nIpXCq
[link-to-todo]:http://todotxt.com/
[link-to-quoffee]: http://www.quoffee.com/
[link-to-crupzi]: http://www.crupzi.com/

