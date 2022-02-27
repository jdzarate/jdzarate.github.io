---
layout: post
title: "Mis frustaciones con Linux"
date:   2015-06-20 15:00:00
excerpt: En el que escribo sobre las complicaciones de la adopción de Linux y mi reciente incapacidad de recomendar este sistema operativo.
published: false
categories:
- blog
---
Mis primeros pasos con Linux los di hace diez años en la clase de Programación Estructurada y lo empecé a usar a tiempo completo hace cinco. El sistema operativo me encanta y tiene mucho potencial pero me avergüenza admitir que soy incapaz de recomendárselo a alguien y me da más vergüenza el hecho que estoy considerando abandonar su uso en mi computadora personal.

De verdad que cualquiera puede usar Linux, no es tan tan complicado pero sí tiene sus peculiaridades. Ya pasaron años de aquellos días en los que tenías que escribir varios comandos para *montar* un *flash drive* pero todavía puedes sufrir complicaciones para instalar un programa si no manejas bien las dependencias de paquetes.

La verdad es que al principio Linux me pareció *cool* pero pero solo lo utilizaba si era necesario, fue hasta que me harté de Windows, sus virus, la fragmentación del disco, las actualizaciones inoportunas, los fatales ambientes de desarrollo de software y el horrible rendimiento de mi humilde procesador i3 de primera generación que me decidí a migrarme a Linux a tiempo completo. Eso es algo genial de Linux, es super óptimo y puedes encontrar un distribución que se ajuste a tu hardware.

Y todo estuvo bien hasta que sufrí incomodidades. Por ejemplo. Toshiba incluye dos sets de data de arranque y Linux no lee la correcta de modo que se requiere una modificación del kernel con una tabla DSDT ajustada, era un problema para mí porque Linux no me reconocía el nivel de carga de la batería. Intenté e intenté y no pude hacer nada para resolver esto en Salix OS (la distribución que usaba en ese momento). Me harté e instalé Ubuntu, que es - digamos - la distribución más popular. No reconocía el nivel de carga de inmediato pero alguien ya había resuelto el problema, un par de comandos aquí y allá y funcionó, lástima que eventualmente me di cuenta que odiaba Ubuntu, especialmente la ineficiencia de su entorno gráfico Unity. Me vi forzado a buscar una mejor opción. Y la encontré en el nombre de CrunchBang.

Nunca había estado tan a gusto con una distribución como lo estoy con CrunchBang. Demanda pocos recursos de hardware, tiene un entorno gráfico con diseño monocromático y minimalista, con *shortcuts* que optimizaban mi trabajo, compatibilidad completa con Debian (se traduce en estabilidad y buen soporte), la comunidad era excelente y amena, tanto que se prestaba a discutir incluso libros de fantasía. Resolví el problema de la batería en una tarde, tuve que modificar la tabla DSDT y recompilar el kernel pero solo fueron un par de horas de trabajo y todo era perfecto, hasta que no lo fue...

La última versión de CrunchBang se lanzó en mayo de 2013 y desde el año pasado he sufrido problemas de librerías viejas, eso me ha impedido instalar algunas aplicaciones como un plugin de Google Hangouts, Netflix o Spotify, realmente no es algo grave pero son cosas que quisiera tener en mi computadora, y estoy en todo mi derecho de tenerlas ¿por qué tendría que limitarme? 

OK. No hay problema, Solamente esperaré la nueva versión de CrunchBang y ya... pero qué suerte la mía, el creador decidió abandonar el proyecto, no más CrunchBang y me vida se derrumbaba...

¿Qué tengo que hacer? ¿Buscar otra distribución? pero es que son tantas... ¿instalar Vanilla Debian y tratar de replicar CrunchBang por mi propia cuenta? Sí, claro, [ni siquiera podria escribir un comando *tar* válido](https://xkcd.com/1168/). ¿instalar uno de esos *forks* de CrunchBang? Probablemente sería la mejor opción pero nada me garantiza que en un par de años me vea en esta situación de nuevo. Lo otro sería decidirme por distros populares con soporte de compañías pero no lo sé, ya lo he intentado y no me ha resultado.

Mi queja tiene un punto, ves lo que he tenido que sufrir con Linux siendo un informático, si yo que sé una cosa o dos no estoy del todo conforme, ¿cómo podría estarlo alguien con menos conocimientos en este tema? No es intuitivo para muchos abrir una consola de comandos y digitar "xrandr --auto" cada vez que quieres proyectar tu pantalla, o modificar el archivo .conf de Alsa en ModProbe si no te funcionan los audífonos. No todos tienen interés en aprender esto, no a todos les parece *cool* saberlo o no pueden llevar a un *experto* en Linux cada vez que salen de sus casas o sus trabajos a otros lugares u oficinas, gracioso que he visto cómo sucede esto último.

Si la gente quiere usar Excel, AutoCAD o Photoshop no debería limitarse con usar la *versión pobre* o la *copia* multiplataforma. A veces es mejor pagar un poco más y evitarse problemas de compatibilidad con el resto del mundo que sí está utilizando esos programas. El software para Linux es muy bueno y me es más que suficiente en el 90% de los casos pero es difícil recomendárselo a alguien cuando su productividad y trabajo pueden verse comprometidos.

Sé que no estoy aportando nada con este post, que solo estoy manifestando mis frustraciones y despechos. Probablemente cuando me toque comprar computadora me decidiré por la opción barata y le instalaré Lubuntu o algo. No lo sé. Sé que odio KDE, Gnome y Unity. Me gusta Xfce y OpenBox + Tint2. Quizá mi computadora ideal sería una Raspberry Pi.

Esto tiene Linux, hay opciones pero eso mismo también le juega en su contra, aun así no sugeriría una unificación ya que eso dañaría la filosofía que representa.

Bueno, todavía le queda vida a mi laptop pero ya dentro de poco cumplirá su quinto aniversario y es hora de ahorrar y eventualmente tomar decisiones pero no estoy tan seguro de que el uso de Linux (más no Unix) sea el factor decisivo para estas decisiones.

J.D.