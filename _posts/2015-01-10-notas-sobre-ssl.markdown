---
layout: post
title: "Notas sobre SSL (Something Sad and Lame)"
date:   2015-01-10 13:00:00
excerpt: En el que escribo por qué me motivé a instalar certificados SSL en mis web apps y un par de cosas que encontré interesante antes y después.
categories:
- blog
---

Hace seis meses compré dos certificados SSL, uno para crupzi.com, otro para quoffee.com. Me dejé llevar por lo del día la privacidad del Internet y eso, además estaban en promoción a $2 cada uno así que ¿porqué no? La única condición del precio era que debía activarlos antes del 31 de diciembre, suficientemente justo.

No sé porque creí que el proceso de activación iba a ser tedioso. Quizá no era eso sino que ya estaba un poco harto de todo lo que tiene que ver con "startups" y activarlos iba a significar que estaba "trabajando"; o quizá era porque ese precio era para el primer año y para el segundo iba a tener que pagar casi $10 para renovarlos y esos potenciales $20 podrían ser lo que definan mi situación económica y emocional en caso de verme forzado a pagar la tarjeta de crédito con un billete en el que una linda chica que conocí en un almacén escribió su número telefónico y no fui lo suficientemente listo como para haber anotado el número en otro lugar porque soy lo suficientemente estúpido para creer que ella iba a encontrar el mío en una primera edición de un libro de García Márquez. Podría suceder.

En fin. Pasaron los meses, llegó diciembre y yo no había activado los certificados (#QueProblema) y si no hubiera sido por una simple consulta no lo habría hecho.

Alguien de la oficina me preguntó si era seguro comprar en cierto website de procedencia china; le dije que el primer paso era verificar si era un "sitio seguro" y por eso me refería a que la URL comenzara con https y no con http porque si no tiene la "s" no vale la pena continuar verificando, no es seguro. "Ah pero qué hipócrita soy", se dijo así mismo con tono acusador, "demando ese certificando en los demás pero no lo incluyo en mis propios websites". Talvez no sean e-commerce ni manejan datos muy sensibles, pero igual, por $2 es lo menos que se puede hacer, el MDP (Mínimo de Decencia Personal).

El proceso es tan fácil que me da un poco de pena haberme tardado tanto tiempo en decidir hacerlo. No implica más que ejecutar un par de comandos en el "host" para generar el "request" del certificado y solicitar dos activaciones. La primera para generar el verdadero certificado y la segunda para aplicar ese certificado en el "host". Quiero aclarar que es fácil porque la gente del webhosting lo hizo fácil para mí; procuraré leer sobre el proceso y si vale la pena quizá escriba un comentario o dos.

Este post se trata sobre dos cosas que no sabía y que encontré interesantes previo y post instalación de los certificados.


### Indicación de Nombre del Servidor

Es usual que para aplicar un certificado propio en un servicio de alojamiento sea requerido adquirir una dirección IP dedicada, esto se traduce a otro cobro mensual y afecta tanto a servicios de hosting compartido como a servidores virtuales privados. Esta IP dedicada es un requisito del protocolo y no es originado por la avaricia de la gente del web hosting.

Cuando se hace una petición a un sitio web con certificado, es decir, cuando se usa https y no http lo primero es resolver el nombre de dominio a una dirección IP, siendo un request del tipo https, antes de que cargue la página (vía protocolo HTTP) se debe obtener el certificado y verificar si es válido usando el protocolo TLS. 

Lastimosamente en este punto solo se conoce la IP. Esto es un problema al tratarse de un servicio de alojamiento Web ya que una misma dirección IP puede utilizarse para múltiples websites. El detalle de qué dominio se debe utilizar o qué website es el que se debe cargar se envía en los encabezados del protocolo HTTP, y eso es posterior a la verificación del certificado.

El protocolo TLS puede obtener el certificado del servidor y este certificado tiene un nombre (el dominio), pero dado que solo lo puede comparar con la dirección IP no es capaz de validarlo correctamente y por eso en ocasiones vemos "errores" como [este][lnk-to-error]. De allí la necesidad del Server Name Indication (SNI) o Indicación de nombre del servidor.

El SNI, como le dicen los chicos geniales, es una extensión del protocolo TLS que permite que el navegador comunique de una sola vez el nombre del dominio a validar, el servidor busca el certificado por el nombre y ahora sí, el protocolo es capaz de verificarlo.

El SNI debe ser soportado tanto por el navegador como por el servidor. En el caso de los navegadores, si utilizas uno más o menos moderno no deberías de tener ningún problema. Creo que la combinación más difícil de ignorar es si usas Windows XP con Internet Explorer, pero realmente no hay ninguna razón para usar ninguno de esos, Windows XP ya no tiene soporte e Internet Explorer, pues, sin criticar, no es una mejor alternativa a Chrome, Firefox o Safari.

Para crupzi y quoffee me decidí por esta alternativa que al menos me ahorrará $60 al año y si alguien usa XP con IE solo tengo el siguiente consejo: *"get a better browser or suck it!"*.


### Contenido Mezclado

Como dije antes, instalar el certificado fue relativamente sencillo, pero eso no quiere decir que los websites estaban preparados. Cuando la gente del alojamiento me escribió diciéndome que los certificados habían sido instalados en el servidor abrí el navegador, digité https://www.quoffee.com y la página cargó. Me sentí bien, como si hubiera logrado algo importante, hasta que noté que muchos estilos no se habían aplicado y que en la barra de direcciones había un signo de advertencia: la página tenía contenido mezclado (mix content). Sh*t. A los navegadores no les gusta el ese contenido mezclado.

Para ser cortos, eso del contenido mezclado significa que la página base está certificada pero que incluye contenido obtenido de fuentes no certificadas, siendo los más comunes tags con atributos "src" o "href" y no van a cargarse a menos que el cliente lo autorice de forma manual.

En mi caso, pasaba que incluía librerías desde CDNs y hacía las referencias utilizando el protocolo http. Una forma de solucionar esto es utilizando exclusivamente https o hacerlo de forma agnóstica utilizando solamente el doble "slash" (//) sin http ni https, de esa forma asume el protocolo utilizado en el website base. En este último caso hay que garantizar que todas esas referencias funcionen con cualquier protocolo.

No es "rocket science" pero espero al menos me sirva de recordatorio para tener mejores prácticas de programación.

Y esa es mi historia.

Al momento de escribir esto tanto crupzi como quoffee pueden visitarse usando https pero quedo pendiente de trabajar en el redireccionamiento automático de http a https. Otro día, otra historia...

José Daniel

PD: Si eventualmente eres esa chica y encuentras mi número en un libro de Gabo puedes escribirme en [twitter](https://twitter.com/jdzaratem). Es posible que para cuando lo encuentres mi número haya cambiando. Lo siento.

[lnk-to-error]:http://hunterford.me/wp-content/uploads/2010/05/Screen-shot-2010-05-18-at-11.47.48-AM-e1274198216952.png
