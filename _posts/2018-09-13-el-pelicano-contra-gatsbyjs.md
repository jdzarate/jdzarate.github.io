---


---

<hr>
<p>layout: post<br>
title: “El Pelícano contra el gran Gatsby…js”<br>
date:   2018-09-13 11:50:00 -0600<br>
excerpt: Hace una semana tomé la decisión de cambiar un generador de contenido estático<br>
categories:</p>
<ul>
<li>blog</li>
</ul>
<hr>
<p>Hace una semana tomé la decisión de cambiar el generador de contenido estático de <a href="https://qwirkz.com">qwirkz.com</a>, la agencia de desarrollo de software que intentamos levantar.</p>
<p>Actualmente el sitio está programado con <a href="https://blog.getpelican.com/">Pelican</a>, y elegí esa opción porque tengo cierta predilección por Python y las plantillas Jinja2.</p>
<p>Pelican funciona muy bien y fue sencillo aprender a usarlo. Sin embargo es un tanto porfiado, lo cual es práctico y recomendable cuando no te quieres complicar la vida para resolver algo sencillo. Lamentablemente yo no quedé del todo conforme con su funcionar, específicamente por tres cosas:</p>
<ol>
<li>Carencia de “hot-reload”, por eso me refiero que no cuenta con mecanismos para actualizar el contenido generado de forma automática y en tiempo real luego de modificar el código. A veces cometo errores al escribir código y tener una retroalimentación constante me ayuda, necesito esas silenciosas palmaditas en la espalda cuando hago algo bien y un claro mensaje de error cuando no.</li>
<li>El origen del contenido dinámico se limita a archivos de Markdown (o  formatos similares), lo cual es suficiente si estás programando un blog pero yo lo necesito para dinamizar el ingreso de información de proyectos o aplicaciones Web.  En mi solución actual todo el contenido estaba en el <a href="https://jekyllrb.com/docs/front-matter/"><em>Front Matter</em></a> del archivo Markdown, la sección se escribe en formato YAML, que es más o menos lo que busco pero por alguna razón Pelican no trabaja bien con listas de valores para parámetros personalizados y yo realmente necesitaba eso. Tuve que recurrir a utilizar cadenas de textos con valores separados por puntos y comas para luego separarlas con Python en las plantillas HTML. Me sentí algo sucio por hacer eso.</li>
<li>Los archivos Markdown se almacen en un directorio llamado <em>articles</em> y eso me incomodaba un poco ya que yo incluiría <em>proyectos</em> y no <em>artículos</em>.</li>
</ol>
<p>Quizá pude ser más proactivo y buscar soluciones con Pelican o seleccionar otro software como <a href="https://jekyllrb.com/">Jekyll</a>, con quien me familiaricé al construir este blog y después de un rápido chequeo parecía resolver mis tres problemas. Pero no. Opté por seguir otro camino, uno que resolvía todo pero además me ayudaría a reforzar mis competencias con <a href="https://reactjs.org/">React.js</a> y la creación de <em>Componentes</em>. Me refiero, como ya podrías anticipar, a <a href="https://www.gatsbyjs.org/">Gatsby.js</a></p>
<p>Después de una semana creo que no fue una mala decisión dados los requerimientos de diseño de mi colega <a href="https://www.twitter.com/oscaroarevalo">@oscaroarevalo</a>, sin embargo he tenido que saltar múltiples barreras para lograr los objetivos. Fue más complicado de lo que creí. Ha sido un proceso satisfactorio pero no lo recomendaría a menos que tu blog o página Web requiera de interfaces dinámicas con cierto grado de complejidad.</p>
<p>El nuevo sitio aún no ha sido publicado y cuando esté listo espero poder contar más detalles sobre el proceso.</p>
<p>Eso es todo por esta vez. Ahora, si me disculpan, me pondré mis zapatos casuales de caballero y saldré a dar una vuelta por los alrededores pretendiendo que es el verano de 1922 y tengo que recuperar el amor de una ex debutante.</p>
<p>J.D.</p>

