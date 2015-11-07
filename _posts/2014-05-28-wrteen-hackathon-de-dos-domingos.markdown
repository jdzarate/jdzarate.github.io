---
layout: post
title: "Wrteen: un hackathon de dos domingos (casi)"
date:   2014-05-28 12:00:00
excerpt: En el que escribo sobre el proceso de creación de Wrteen - Simple writing for things that might matter.
categories:
- blog
---

En la mañana del miércoles 7 de mayo empecé a escribir en un grupo de WhatsApp un párrafo sobre por qué un fallecido rey en una famosa serie de fantasía estaba loco, pero el párrafo se me hizo corto, necesitaba más historia, necesitaba otro medio para escribir.

Lo primero que se me vino a la mente fue escribir un e-mail pero todavía no me parecía el medio apropiado. Tiendo a relacionar el e-mail con cosas de trabajo, usualmente cosas que no son "cool". 

¿Facebook? de nuevo, quería algo "cool". No. Lo que necesitaba era algo sencillo en lo que pudiera escribir, darle algo de formato, obtener un link, compartirlo y desentenderme. Honestamente, no busqué alternativas, pensé que sería más genial crear una propia.

La noche de ese mismo día, en 1/3 de página, dibujé el layout del website: un editor de [Markdown][lnkMarkdown] + una vista previa + un botón "Guardar" = Link. Diseñé la base de datos, una tabla que almacene título, contenido y fecha de creación. Simple. Estaba listo para el trabajarlo durante el fin de semana.

Quise hacerlo más interesante. Semanas atrás me enteré de un Web Framework basado en Python llamado [Wheezy.Web][lnkWheezy]. Supuestamente liviano y [con un gran rendimiento][lnkToBenchmark]. ¿Por qué no usarlo?

#### Día de las madres

Llegó el sábado 10 de mayo. Trabajo regular por la mañana. Llegué a mi casa a las 12:10pm, encendí la computadora y comencé.

Lo primero que necesitaba era un "nombre código". Uno corto. Es en serio, lo primero que se me vino a la mente fue Wrteen porque suena como "Writing". Suficientemente bueno por el momento.

La siguiente tarea era configurar un ambiente de trabajo virtual e instalar Wheezy.Web. Hecho y hecho. Suficiente trabajo, hora de almorzar.

Lo siguiente en la lista era familiarizarme con Wheezy.Web, me robé una buena porción de líneas de código del [tutorial][lnkTutorial]: Modelo, Repositorio, Vistas, etc. Dieron las 3.30pm y salí a comprar un pastel para la celebración del día de las madres.

Cuando regresé terminé de configurar el proyecto: configuré el enrutamiento para "root" (/) y un template sencillo: "Hola Mundo". Todo funcionó (no a la primera, claro), tomé una siesta y me preparé para la cena familiar. No tenía nada de la lógica de la aplicación, solo una copia del proyecto base en Wheezy.Web pero eso no me preocupaba.

#### El primer domingo

Comencé a las 10 de la mañana. A la 1pm ya tenía el layout de la página principal. Suena fácil y lo fue. Solo programé el "template" base para la aplicación. Lo que me tomó más tiempo fue encontrar [el plugin de jQuery apropiado][lnkCrevasse], lo incorporé al [grid de Skeleton][lnkSkeleton] y en la tarde lo haría funcional.

Después de almorzar trabajé en el flujo del website: definición de rutas y procesamiento de los datos recibidos mediante "requests" HTTP. Ya almacenada la información solamente era necesario preparar el template para mostrar los "posts" y el link para compartir.

A las 6pm ya estaba listo. Podía escribir posts, generaba el link y lo mostraba en la pantalla. Al darle clic al link redirigía a la página del post. Solo me faltaba alojarlo en un servidor pero eso tenía que esperar la cena y un partido de la NBA.

Más o menos a las 9pm comencé a configurarlo en el servidor. Tuve un par de complicaciones. Intenté adaptar una [guía para configurar Flask][lnkFlask] (otro Web Framework basado en Python) y sí aplicaba en la mayor parte. Creo que los problemas más importantes los tuve en la configuración de las rutas de Python en Apache. 

No obstante, a las 11pm el MVP estaba listo. Escribí el [post sobre ese maldito rey][lnkAerys], lo compartí en Facebook y me fui a dormir. Lo había logrado, un website en menos de 24 horas.

#### La mañana siguiente

Por supuesto, a nadie le importó. A pesar de que con orgullo mencioné que había construido el website cuando compartí el post, nadie me dijo nada. Quizá les pareció una porquería y se reservaron los comentarios.

Me pareció buena idea comentarlo en el trabajo. Lo primero que me dijeron fue que estaba bien pero sería mejor si se pudieran editar los posts. La verdad es que era una sugerencia válida. Qué tal si me equivocaba y publicaba algo con muchos errores de ortografía, no sé cómo hubiera podido vivir conmigo mismo.

La idea de editar el post me gustaba pero realmente no quería crear cuentas de usuario porque iba a complicar todo sin necesidad. Me gustaba la simpleza de solo escribir y obtener el link, algo desechable y por qué no, anónimo.

Ese mismo día se me ocurrió una idea. Lo único que necesitaba era asociar una contraseña al post al momento de la creación. Si después se quiere editar, se escribe la contraseña y ya. Sin cuentas de usuario. Simple. Tenía que hacerlo así.


#### El segundo domingo

De nuevo, ya sabía exactamente lo que iba a hacer. Solo necesitaba asignarle un poco de mi precioso tiempo.

El pasado domingo 25 de mayo me levanté a las 8am, desayuné, vi un par de sitcoms (The Office y Hot in Cleveland) y a las 9am comencé a programar. A mediodía ya podía generar contraseñas para posts, encriptarlas y guardarlas en la base de datos. Incorporé la página de edición de posts y la opción para obtener el código del post en formato Markdown.

Después de un nutritivo almuerzo (4 porciones de pizza) reanudé las actividades, solo me faltaba solicitar la contraseña al momento de guardar la modificación al post. A las 3.30pm todo estaba listo y actualizado en el servidor. Leí un poco, configuré un Newsletter, vi a los San Antonio Spurs perder (cara triste) y concluyó el día.

Todavía me falta buscar un nombre de dominio, liberar el código fuente (como material para burlas) y mejorar la experiencia de usuario pero qué importa, ¡hice algo funcional en solo dos domingos!


#### 7 cosas que noté:

1. Cuando construyes aplicaciones lo que crees que es temporal se vuelve permanente antes de que te des cuenta.
2. Todo es más fácil cuando tienes un plan (O el plan A, el B y el que sí funciona).
3. El "no tengo tiempo" es la excusa peor justificada en la historia. Aún tomándome mi dulce tiempo, proscratinando y eso, logré sacar el proyecto en dos domingos (casi).
4. Siempre hay que pensar en la forma más simple de resolver el problema. Usualmente es la mejor forma.
1. Wheezy.Web es medio genial. La documentación no siempre es explícita pero si ya estás familiarizado con otros frameworks de Python todo tiene sentido por su cuenta.
2. No todo es relativo. Estoy hablando de tí "path" en "server" de producción.
3. Unicode es una princesa delicada y sensible.

Por cierto, si quieres chequear la versión beta de Wrteen puedes seguir [este enlace][lnkWrteen].

[lnkWheezy]:http://wheezyweb.readthedocs.org/en/latest/
[lnkToBenchmark]:http://faruk.akgul.org/blog/python-web-frameworks-benchmark/
[lnkTutorial]:http://wheezyweb.readthedocs.org/en/latest/tutorial.html
[lnkCrevasse]:https://github.com/patbenatar/crevasse
[lnkSkeleton]:http://www.getskeleton.com/
[lnkAerys]: http://wrteen.jdzarate.webfactional.com/p/bozJtZFC0A
[lnkFlask]:http://flask.pocoo.org/snippets/65/
[lnkWrteen]: http://wrteen.jdzarate.webfactional.com/
[lnkMarkdown]:http://daringfireball.net/projects/markdown/