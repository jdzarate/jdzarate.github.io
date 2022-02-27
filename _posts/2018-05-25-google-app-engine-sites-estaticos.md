---
layout: post
title: "Google App Engine ama los websites estáticos"
date:   2018-05-25 15:30:00 -0600
excerpt:
published: false
categories:
- blog
---

Creo que no hace falta recalcar qué tan geniales son los generadores de websites estáticos pero igual lo haré.

Cuando tu site o aplicación solamente requiere de tecnologías que se ejecutan en el navegador (HTML, JS, CSS) no vale la pena complicarse con más. ¿Para qué un sitio de Wordpress? ¿para qué crear un propio CMS con Python, Ruby o Node? ¿para qué diseñar una base de datos? Si solo necesito generar el código HTML, escribir artículos en Markdown con mi editor de texto y dirigirme a la Terminal para publicar contenido, eso es lo que haré.

Hace casi 4 años, cuando escribí sobre [herramientas para bloguear][lnk-herramientas], mencioné que este blog había sido creado con Jekyll y Github Pages como servidor. Github Pages ofrece alojamiento gratuito y me basta con digitar un "git push" para publicar un nuevo artículo.

Todo eso aún es cierto, pero en los últimos dos meses he trabajado en un par de sitios Web sencillos y una [Aplicación Web Progresiva][lnk-pwa] hecha con ReactJS utilizando Google App Engine como mi servidor y debo admitir que, aunque no he hecho una búsqueda exhaustiva, no sé si podría encontrar una mejor opción.

Las razones son simples:

* que esté alojada en la granja de Google significa un alto porcentaje de disponibilidad y buen rendimiento.
* puedes asociar tus propios dominios y subdominios vía Cloud Console.
* automáticamente instala un certificado SSL con Let's Encrypt.
* ¡es gratis!

Lo único que necesitas es la cuenta de Google/Gmail que probablemente ya tienes.

No entraré en detalles sobre el procedimiento porque todo lo puedes encontrar en [este enlace][lnk-gcloud] y si después de leerlo te sorprendes de lo fácil que es, créelo, lo es.

Así que ve, construye cosas geniales con Jekyll, Pelican, React, Vue, Gatsby o alguna alternativa en tu lenguaje favorito, genera el código HTML y despreocupate de cómo alojarlo en la Web.

[lnk-pwa]: https://www.jdzarate.com/blog/2016/04/03/aplicaciones-web-progresivas.html
[lnk-herramientas]: https://www.jdzarate.com/blog/2014/03/23/herramientas-para-bloguear.html
[lnk-gcloud]: https://cloud.google.com/appengine/docs/standard/python/getting-started/hosting-a-static-website.

J.D.
