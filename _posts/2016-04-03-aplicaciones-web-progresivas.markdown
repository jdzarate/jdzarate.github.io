---
layout: post
title:  "Aplicaciones Web Progresivas"
date:   2016-04-03 12:00:00 -0600
excerpt: 
categories:
- blog
---

La semana pasada encontré un artículo de [@henrikjoreteg](https://twitter.com/henrikjoreteg) que me llamó la atención. El título de la publicación fue inequívocamente un anzuelo para clics: [“Me cambié a Android después de 7 años de iOS”][lnk-joreteg]. Como dije, fue un anzuelo, y uno que no suelo tomar. Pero me dio una sensación que debía hacerlo (tenía más de 700 votos en Hacker News), estaba seguro de que no se trataba de otra queja más sobre alguna nimiedad del sistema operativo, debía tratarse de algo más profundo. 

El post no es una crítica dirigida a iOS ni una glorificación de Android. Es una introducción a una serie de conceptos y utilidades para el desarrollo de aplicaciones Web y cómo Android las está adoptando y así enriqueciendo la ejecución de estas aplicaciones en su sistema operativo y como el autor, siendo un programador Web, sentía el compromiso moral de apoyar a la plataforma que trabaja en proveer las mejores herramientas para hacer su trabajo. 

El post gira en torno al concepto de las Aplicaciones Web Progresivas (Progressive Web Apps)

> Las Aplicaciones Web Progresivas son experiencias que combinan lo mejor de la Web y las Aplicaciones Nativas. No requieren instalación. El usuario construye, progresivamente, una relación con la aplicación a través del tiempo, cada vez se convierte más y más potentes. Cargan más rápido y envían notificaciones relevantes. Proveen íconos en la Pantalla de Inicio y te sumergen en modo Pantalla Completa. - [Google][lnk-google].

Esa es la definición de Google. Suena bien pero no dice mucho. 

Repasemos: 

* No requiere instalación.
* Iconos en Pantalla de Inicio (Home Screen)
* Pantalla Completa (sin UI del navegador)

Nada nuevo. iOS y Android proveen esas funcionalidad desde hace ratos. ¿Cuál es la diferencia a cualquier otro sitio Web?

Cuando trabajaba en Crupzi y Quoffee habían dos cosas que realmente deseaba que fueran posibles en ambos websites: (1) envío de notificaciones en dispositivos móviles y (2) uso *offline*. 

Buenas noticias: con las Aplicaciones Web Progresivas puedo obtener ambas. ¿Qué tan genial es esto?

##### Uso Offline

Por motivos de rendimiento, la posibilidad de tener parte de la aplicación *offline* es una ventaja. Si los archivos del UI residen en el dispositivo, la conexión a Internet solo se requeriría para descargar el contenido dinámico. Incluso existen websites cuyo contenido no cambia mucho con el tiempo y pueden funcionar completamente offline casi para siempre.

Sobre lo último se me viene a la mente la primera Aplicación Web Progresiva que vi: [Pokedex.org](http://pokedex.org). Si eres un fan de Pokemon o si simplemente quieres apreciar una buena aplicación Web te recomiendo que le des una visita. Además, el [post introductorio del creador][lnk-pokedex] es de los artículos más interesantes sobre programación Web que he leído en mucho tiempo.


##### Notificaciones

Todos tenemos una relación de amor y odio con las notificaciones de nuestros teléfonos pero al final del día sabemos que las necesitamos por eso estaba muy interesado en la implementación de esta característica. A través de Service Workers y la plataforma de Google Cloud Messaging esto es posible.

Facebook las implementó en la versión Web de Chrome para Android y mucha gente optó por usar únicamente la Web App y desinstalar la aplicación nativa, más aún cuando [experimentos han mostrado que hacer esto incrementa la duración la batería en un 20%][lnk-facebook]. 

Y eso no es todo, según el post de @henrikjoreteg, desarrolladores en Google están trabajando por incorporar más funcionalidades como WebBluetooth y WebNFC. Super interesante.

##### La Pantalla de Inicio

No puedo dejar de pensar en que todo esto puede ser una causa perdida, las aplicaciones nativas ya cuentan con todo esto, ¿para qué intentar ir al paso?

Hace un año [escribí sobre mi percepción de que la gente no quería aplicaciones Web sino App Nativas][lnk-jdzarate]. Estaba resentido porque nadie parecía tomar en serio mis websites y 2 de cada 3 personas me preguntaban cuándo estaría lista la aplicación para descargarla en la Tienda. De verdad entendía el punto pero aún así me molestaba y estaba perdiendo fe en las aplicaciones Web.

Viendo ejemplos como el que mencioné de Facebook y otros casos como la publicación [“Nadie quiere tu App”][lnk-nobody] pueden ser muestra de que la gente tal vez no está tan interesada en Apps sino en Servicios.

El desarrollo de Apps nativas es costoso. Requieren de licenciamiento, de aprobación de la aplicación, desprenderse del 30% de tus ganancias como tributo a Apple o Google, además del tiempo de desarrollo y uno o varios programadores para crear una aplicación multiplataforma si así lo quieres. Tendría que corroborar el dato pero me pareció haber leído que los costos podrían ser hasta 10 veces más que una Aplicación Web. Te pone a pensar en si es un método viable cuando solo quieres probar una idea.

No se tú, pero yo considero que mi teléfono es mi dispositivo más personal. Instalar una aplicación significa invitarla que sea parte de mi día a día. Últimamente me vuelto muy *picky* con esto. No me gusta instalar cualquier app, aún cuando sea de servicios que uso casi a diario, mucho menos cuando se trata de servicios a los que acudo sin mucha recurrencia. Mi regla es, “si no es algo que quiero ver en mi Pantalla de Inicio no lo instalo”.

Y por eso creo que sí hay espacio para las Aplicaciones Web Progresivas. No necesitamos ver una aplicación X en una Tienda, necesitamos una forma fácil de “instalarlas” o más bien tener acceso rápido cuando las necesitemos y que sean intuitivas en su uso.

Si construyes una Aplicación Web Progresiva y logras que la gente presione el botón “Agregar a la Pantalla de Inicio” buena parte del trabajo ya está hecho, y si el funcionamiento y rendimiento no difieren de una aplicación nativa dudo mucho que al usuario le importe que no lo sea.

##### Hay un largo camino hacia la cima

Android está haciendo su parte y espero que Apple y los demás también la hagan en un corto plazo. Si no, me temo que el resultado quedaría incompleto siendo válido para una sola plataforma.

No todos harán el cambio de iOS a Android ni deberían hacerlo porque cada plataforma tiene sus fortalezas y el balance mejora la competencia. El desarrollo Web no es una razón atractiva para hacerlo el cambio, quizá solo para esos idealistas de la Web Abierta, y ni siquiera serían todos.

Igual es alentador y una buena iniciativa de Google/Android. Alguien tiene que empezar, si no, nadie podría seguirlos.

J.D.

[lnk-joreteg]:https://joreteg.com/blog/why-i-switched-to-android#so-why-android-isnt-it-just-more-of-the-same
[lnk-jdzarate]: http://www.jdzarate.com/blog/2015/01/29/mi-hipocresia-it-webapps.html
[lnk-google]: https://developers.google.com/web/progressive-web-apps?hl=en
[lnk-pokedex]: http://www.pocketjavascript.com/blog/2015/11/23/introducing-pokedex-org
[lnk-facebook]:http://www.theguardian.com/technology/2016/feb/01/uninstalling-facebook-app-saves-up-to-20-of-android-battery-life
[lnk-nobody]: https://medium.com/swlh/nobody-wants-your-app-6af1f7f69cb7#.r5n2npibw