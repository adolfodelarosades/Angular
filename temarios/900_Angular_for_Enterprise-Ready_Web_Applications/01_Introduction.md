# 01. Introduction to Angular and Its Concepts

* A brief history of web frameworks
* Introduction to Angular
   * Angular's philosophy
   * Angular Evergreen
   * TypeScript
   * Basic Angular architecture
* The reactive development paradigm
   * RxJS
   * Reactive data streams
* Advanced Angular architecture
   * The Angular Router
   * Lazy loading
   * State management
      * The Flux pattern
      * NgRx
   * React.js architecture
* Notable Angular features
   * Angular 6
   * Angular 8
   * Angular 9
* Summary
* Further reading
* Questions


# 01. Introducción a Angular y sus Conceptos

Al principio, estaba HTML, luego DHTML. Los tecnólogos inventaron nuevas tecnologías como Java, JavaScript, PHP y muchas otras para ofrecer experiencias interactivas a través del navegador. El santo grial de la programación fue escribir un programa una vez y ejecutarlo en todas partes. En un instante, nació la era de las aplicaciones **Single-Page Applications (SPAs)**. Los SPA engañaron al navegador haciéndole creer que un solo `index.html` podría albergar aplicaciones completas que contienen muchas páginas. ***Backbone.js***, ***Knockout.js*** y ***Angular.js*** iban y venían. Todos los que se tambaleaban por la complejidad no gestionada y el síndrome del marco de la semana de JavaScript buscaban un salvador. Luego vinieron ***React***, ***Angular*** y ***Vue***. Prometieron solucionar todos los problemas, generar componentes web universalmente reutilizables y facilitar el aprendizaje, desarrollo y escalado de aplicaciones web. ¡Y así lo hicieron! Algunos mejores que otros. La historia adolescente de la web nos ha enseñado un par de lecciones esenciales. Primero, el cambio es inevitable, y segundo, la felicidad del desarrollador es un bien preciado que puede hacer o deshacer empresas enteras.

Este capítulo cubre:

* La historia de los frameworks web
* Angular y la filosofía detrás de él
* El paradigma del desarrollo reactivo
* Funciones Angular avanzadas, incluida la gestión del estado
* Principales versiones y características de Angular

Este primer capítulo está destinado a brindarle un trasfondo teórico e histórico para el resto del libro. Siéntase libre de usarlo como referencia a medida que lee el resto del libro. El Capítulo 2, Configuración de su entorno de desarrollo, cubre cómo puede configurar su entorno de desarrollo para una gran experiencia de desarrollo. Con el Capítulo 3, Creación de una aplicación Angular básica, comienza a implementar su primera aplicación Angular. Si ya tiene experiencia con Angular, puede comenzar con el Capítulo 7, Creación de una aplicación de primera línea de negocio de enrutador, para sumergirse en la creación de aplicaciones escalables listas para la empresa.

Cada capítulo del libro le presenta nuevos conceptos y refuerza las mejores prácticas mientras cubre las formas óptimas de trabajar con herramientas de código abierto y ampliamente utilizadas. En el camino, los recuadros de consejos e información cubren las bases para cerrar cualquier brecha de conocimiento que pueda tener sobre los conceptos básicos de desarrollo web y JavaScript moderno. A medida que revisa el contenido, preste atención a los pasos numerados o viñetas, ya que describen las acciones que debe realizar. Si omite una sección o un capítulo, es posible que se pierda cambios sutiles en la configuración o técnicas que pueden confundirlo más adelante.

:blue_book: *Los ejemplos de código que se proporcionan en este libro se han desarrollado utilizando Angular 9, que está previsto que esté en soporte a largo plazo (LTS) hasta agosto de 2021. Es probable que esté leyendo este libro después de que las nuevas versiones hayan reemplazado a Angular 9. Sin embargo, no te preocupes. Este libro adopta el lema imperecedero de Angular de mantener siempre actualizada la versión de Angular con la última versión. Mantenerse actualizado es posible al ceñirse a los fundamentos de la plataforma y evitar bibliotecas de terceros innecesarias. Los proyectos de ejemplo para el libro se escribieron inicialmente para Angular 5 y se actualizaron con el tiempo sin grandes reescrituras siguiendo un programa de actualización de Angular proactivo e incremental. Anticipo que estos proyectos sobrevivirán con modificaciones menores durante los próximos años. Esta confiabilidad es un testimonio del excelente trabajo de compatibilidad realizado por el equipo de Angular*.

El mundo de JavaScript, TypeScript y Angular cambia constantemente. Es normal que haya algunas diferencias entre los ejemplos de código del libro y el código que generan las herramientas que utiliza. Por esta razón, la mayoría de las mejores prácticas y elementos de configuración recomendados por este libro se aplican utilizando herramientas que creé, para que puedan actualizarse. A continuación se muestra una descripción general de alto nivel de la colección de bibliotecas, extensiones y proyectos de código abierto que respaldan el contenido del libro:

![01-01](images/01-01.png)

Figure 1.1: Code developed in support of this book

El diagrama anterior es para darle un vistazo rápido a algunas de las partes móviles. Cada componente se detalla en los próximos capítulos. Las versiones más actualizadas del código de muestra para el libro están en GitHub, en los repositorios vinculados a continuación. Estos repositorios contienen el estado final y completo del código. Para que sea más fácil verificar su progreso al final de un capítulo, la carpeta de proyectos en cada repositorio contiene instantáneas capítulo por capítulo que reflejan el estado actual del código:

* Para los *capítulos 2 a 6 y 12*, LocalCast Weather: https://github.com/duluca/local-weather-app
* Para los *capítulos 7 a 14*, Lemon Mart: https://github.com/duluca/lemon-mart
* Para el *Capítulo 10*, Lemon Mart Server: https://github.com/duluca/lemon-mart-server

:high_brightness: *Puede leer más sobre la actualización de Angular en el Apéndice C, Mantener Angular y Tools Evergreen. Puede encontrar este apéndice en línea en https://static.packt-cdn.com/downloads/9781838648800_Appendix_C_Keeping_Angular_and_Tools_Evergreen.pdf or at https://expertlysimple.io/stay-evergreen.*

Echemos un vistazo a los últimos 20 años de historia del desarrollo web, para que pueda contextualizar cómo surgió y evolucionó Angular.

## Una breve historia de los frameworks web

Es esencial considerar por qué usamos frameworks como Angular, React o Vue en primer lugar. Los frameworks web surgieron a medida que JavaScript se hizo más popular y capaz en el navegador. En 2004, la técnica **Asynchronous JavaScript and XML (AJAX)** se volvió muy popular en la creación de sitios web que no tenían que depender de actualizaciones de página completa para crear experiencias dinámicas utilizando tecnologías web estandarizadas como HTML, JavaScript/ECMAScript y CSS. Se supone que los proveedores de navegadores implementan estas tecnologías tal como las define el World Wide Web Consortium (W3C).

**Internet Explorer (IE)** era el navegador en el que confiaba la gran mayoría de los usuarios de Internet en ese momento. Microsoft utilizó su dominio del mercado para impulsar tecnologías patentadas y API para asegurar la ventaja de IE como el navegador de referencia. Las cosas empezaron a ponerse interesantes cuando el Firefox de Mozilla desafió el dominio de IE, seguido del navegador Chrome de Google. A medida que ambos navegadores obtuvieron una participación de mercado significativa, el panorama del desarrollo web se convirtió en un desastre. Las nuevas versiones del navegador aparecieron a una velocidad vertiginosa. Los intereses técnicos y corporativos en competencia llevaron a la implementación divergente de estándares web.

Esta fractura creó un entorno insostenible para que los desarrolladores ofrezcan experiencias consistentes en la web. Las diferentes calidades, versiones y nombres de las implementaciones de varios estándares crearon un desafío enorme, que consistía en escribir con éxito código que pudiera manipular el **Document Object Model (DOM)** de un navegador de manera consistente. Incluso la más mínima diferencia en las API y las capacidades de un navegador sería suficiente para romper un sitio web.

En 2006, jQuery se desarrolló para suavizar las diferencias entre las API y las capacidades de los navegadores. Entonces, en lugar de escribir código repetidamente para verificar las versiones del navegador, puede usar jQuery y ya está listo. Escondió todas las complejidades de las implementaciones específicas del proveedor y llenó con elegancia los vacíos cuando faltaban funciones. Durante unos buenos 5 a 6 años, jQuery se convirtió en el marco de desarrollo web. Era inimaginable escribir un sitio web interactivo sin usar jQuery.

Sin embargo, para crear experiencias de usuario vibrantes, jQuery por sí solo no fue suficiente. Las aplicaciones web nativas ejecutaban todo su código en el navegador, lo que requería computadoras rápidas para ejecutar el JavaScript interpretado dinámicamente y representar páginas web utilizando los complicados gráficos de objetos. En la década de 2000, muchos usuarios utilizaban navegadores obsoletos en computadoras relativamente lentas, por lo que la experiencia del usuario no fue excelente.

Tradicionalmente, la arquitectura de software se describe en tres capas principales, como se muestra en el diagrama siguiente:

![01-02](images/01-02.png)

La capa de presentación contiene código relacionado con la interfaz de usuario (UI), la capa empresarial contiene lógica empresarial y la capa de persistencia contiene código relacionado con el almacenamiento de datos. Es un objetivo general del diseño apuntar a un bajo acoplamiento y alta cohesión entre los componentes de nuestra arquitectura. El acoplamiento bajo significa que los fragmentos de código en estas capas no deben depender entre sí y deben ser reemplazables de forma independiente. Una alta cohesión significa que las piezas de código que están relacionadas entre sí, como el código relacionado con un dominio particular de la lógica empresarial, deben permanecer juntas. Por ejemplo, al crear una aplicación para administrar un restaurante, el código para el sistema de reservas debe estar junto y no extenderse a otros sistemas como el seguimiento de inventario o la administración de usuarios. El desarrollo web moderno tiene más partes móviles que una aplicación básica de tres niveles. El diagrama que sigue muestra capas adicionales que se ajustan a las capas de presentación, negocio y persistencia:

![01-03](images/01-03.png)

En el diagrama anterior, puede ver un diagrama de arquitectura expandido que incluye componentes esenciales del desarrollo web moderno, que incluyen una capa de API que generalmente transforma los datos entre las capas de presentación y de negocios, una capa de herramientas y mejores prácticas que define varias metodologías utilizadas para desarrollar el software y una capa de prueba automatizada que es crucial en los ciclos de desarrollo iterativos y rápidos de hoy.

En la década de 2000, muchas empresas de Internet confiaban en las páginas web renderizadas del lado del servidor. El servidor creó de forma dinámica todo el HTML, CSS y los datos necesarios para representar una página. El navegador actuó como un visor glorificado que mostraría el resultado. El siguiente es un diagrama que muestra una descripción general de la arquitectura de muestra de una aplicación web renderizada del lado del servidor en la pila ASP.NET MVC:

![01-04](images/01-04.png)

**Model-View-Controller (MVC)** es un patrón típico de código que tiene lógica de manipulación de datos en modelos, lógica de negocios en controladores y lógica de presentación en vistas. En el caso de ASP.NET MVC, el controlador y el modelo se codifican mediante C#, y las vistas se crean utilizando una versión con plantilla de HTML, JavaScript y C#. El resultado es que el navegador recibe HTML, JavaScript y los datos necesarios y, a través de jQuery y AJAX magic, las páginas web parecen interactivas. La representación del lado del servidor y los patrones MVC siguen siendo populares y se utilizan en la actualidad. Hay usos de nicho justificados, como Facebook.com. Facebook sirve a miles de millones de dispositivos que van desde los muy lentos hasta los muy rápidos. Sin la representación del lado del servidor, sería imposible para Facebook garantizar una **experiencia de usuario (UX)** consistente en toda su base de usuarios. Encuentro que la combinación de representación del lado del servidor y MVC es un patrón intrincado de ejecutar. Para garantizar el bajo acoplamiento de componentes, todos los miembros del equipo de ingeniería deben tener mucha experiencia. Es difícil encontrar equipos con una alta concentración de desarrolladores senior, y eso sería quedarse corto.

Para complicar aún más las cosas, C# (o cualquier otro lenguaje del lado del servidor) no se puede ejecutar de forma nativa en el navegador. Por lo tanto, los desarrolladores que trabajan en aplicaciones renderizadas del lado del servidor deben ser igualmente hábiles en el uso de tecnologías frontend y backend. Es fácil para los desarrolladores sin experiencia mezclar la presentación y la lógica empresarial en tales implementaciones sin querer. Cuando esto sucede, la inevitable modernización de la interfaz de usuario de un sistema que de otro modo funcionaría bien se vuelve imposible. En otras palabras, para reemplazar el fregadero de su cocina por uno nuevo, debe renovar toda su cocina. Debido a la arquitectura insuficiente, las organizaciones gastan rutinariamente millones de dólares cada 10 años escribiendo y reescribiendo las mismas aplicaciones.

Durante la década de 2000, fue posible crear aplicaciones web enriquecidas que se desacoplaron de las API de su servidor mediante ***Java Applets***, ***Flash*** o ***Silverlight***. Sin embargo, estas tecnologías dependían de complementos del navegador que necesitaban una instalación separada. La mayoría de las veces, estos complementos estaban desactualizados, creaban vulnerabilidades de seguridad críticas y consumían demasiada energía en las computadoras móviles. Tras la revolución del iPhone en 2008, estaba claro que tales complementos no se ejecutarían en teléfonos móviles, a pesar de los mejores intentos del sistema operativo Android. Además, el desdén del CEO de Apple, Steve Jobs, por soluciones tan poco elegantes marcó el principio del fin del soporte de tales tecnologías en el navegador.

A principios de la década de 2010, comenzaron a aparecer marcos como ***Backbone*** y ***AngularJS***, que demostraban cómo crear aplicaciones web ricas con una sensación y velocidad nativas y hacerlo de una manera aparentemente rentable. El siguiente diagrama muestra un cliente **Model-View-ViewModel (MVVM)** con una **Representational State Transfer (REST)** API de transferencia de estado representacional (REST). Cuando desacoplamos el cliente del servidor a través de una API, entonces podemos aplicar arquitectónicamente la implementación de la presentación y la lógica empresarial por separado. En teoría, este patrón de servicios web RESTful debería permitirnos reemplazar el fregadero de la cocina con la frecuencia que queramos sin tener que remodelar toda la cocina.

![01-05](images/01-05.png)

Observe la casi duplicación de cajas en el diagrama anterior. Solo porque separamos al cliente del servidor, no terminamos simplificando la arquitectura. En todo caso, la arquitectura que rodea a la lógica de presentación se vuelve mucho más complicada. Tanto el cliente como el servidor deben implementar sus capas de presentación/API, negocios y persistencia.

Desafortunadamente, muchos de los primeros esfuerzos de desarrollo que aprovechaban marcos como Backbone y AngularJS colapsaron por su propio peso porque no implementaron correctamente la arquitectura del lado del cliente.

Estos primeros esfuerzos de desarrollo también sufrieron de API web RESTful mal diseñadas. La mayoría de las API no versionaron sus URI, lo que dificulta la introducción de nuevas funcionalidades mientras se da soporte a los clientes existentes. Además, las API a menudo devuelven modelos de datos complicados que exponen sus modelos de datos relacionales internos a aplicaciones web. Esta falla de diseño crea un acoplamiento estrecho entre componentes/vistas aparentemente no relacionados escritos en HTML y modelos creados en SQL. Si no implementa capas adicionales de código para traducir o mapear la estructura de datos, entonces crea un acoplamiento no intencional y no controlado entre capas. Con el tiempo, lidiar con este tipo de acoplamiento se vuelve muy costoso muy rápidamente, en la mayoría de los casos necesita reescrituras significativas.

:blue_book: *Hoy en día, usamos la capa API para aplanar el modelo de datos antes de enviarlo al cliente para evitar tales problemas. Las tecnologías más nuevas como GraphQL van un paso más allá al exponer un modelo de datos bien definido y permitir al consumidor consultar los datos exactos que necesita. Con GraphQL, el número de solicitudes HTTP y la cantidad de datos transferidos por el cable son óptimos sin que los desarrolladores tengan que crear muchas API especializadas.*

Backbone y AngularJS demostraron que era viable crear aplicaciones web que se ejecutaran de forma nativa en el navegador. Todos los marcos de SPA en ese momento se basaban en jQuery para la manipulación de DOM. Mientras tanto, los estándares web continuaron evolucionando y los navegadores permanentes que admiten nuevos estándares comenzaron a convertirse en algo común. Sin embargo, el cambio es constante, y la evolución de las tecnologías web hizo que fuera insostenible evolucionar con gracia esta primera generación de marcos de SPA.

La próxima generación de frameworks web necesitaba resolver muchos problemas; necesitaban hacer cumplir una buena arquitectura; estar diseñado para evolucionar con los estándares web; y ser estable y escalable a las necesidades de la empresa sin colapsar. Además, estos nuevos marcos debían ganar la aceptación de los desarrolladores, que estaban agotados con demasiados cambios rápidos en el ecosistema. Recuerde, los desarrolladores descontentos no crean negocios exitosos. Alcanzar estos objetivos requería una ruptura clara con el pasado, por lo que ***Angular*** y ***React*** surgieron como plataformas para abordar los problemas del pasado de diferentes maneras.

## Introducción a Angular

Angular es un proyecto de código abierto mantenido por Google y una comunidad de desarrolladores. La nueva plataforma Angular es muy diferente del marco heredado que puede haber usado en el pasado. En colaboración con Microsoft, Google convirtió ***TypeScript en el lenguaje predeterminado para Angular***. TypeScript es un superconjunto de JavaScript que permite a los desarrolladores apuntar a navegadores heredados como Internet Explorer 11, mientras les permite escribir código JavaScript moderno que funciona en navegadores como Chrome, Firefox y Edge. Las versiones heredadas de Angular, versiones en el rango 1.x.x, se conocen como AngularJS. La versión 2.0.0 y las versiones superiores se denominan Angular. Donde *AngularJS es un marco SPA de JavaScript monolítico, Angular es una plataforma que es capaz de apuntar a navegadores, marcos híbridos móviles, aplicaciones de escritorio y vistas renderizadas del lado del servidor*.

La actualización al nuevo AngularJS fue arriesgada y costosa porque incluso las actualizaciones menores introdujeron nuevos patrones de codificación y características experimentales. Cada actualización introdujo depreciaciones o la refactorización de características antiguas, lo que requirió reescribir grandes porciones de código. Además, las actualizaciones se entregaron en intervalos inciertos, lo que hizo imposible que un equipo planificara los recursos para actualizar a una nueva versión. La metodología de lanzamiento eventualmente condujo a un marco impredecible y en constante evolución que aparentemente no tenía una guía para llevar adelante las bases del código. Si usó AngularJS, probablemente se quedó atascado en una versión en particular, porque la arquitectura específica de su base de código hizo que fuera muy difícil pasar a una nueva versión. *En 2018, el equipo de Angular lanzó la última actualización importante de AngularJS con la versión 1.7*. Esta versión marcó el comienzo del fin del marco heredado, con un fin de vida planificado en julio de 2021.

Angular mejora AngularJS en todas las formas imaginables. La plataforma sigue a semver, como se define en https://semver.org/, donde los incrementos de versiones menores denotan adiciones de nuevas funciones y posibles avisos de depreciación para la segunda próxima versión principal, pero sin cambios importantes. Además, el equipo de Angular en Google se ha comprometido con un calendario de lanzamiento determinista con versiones principales lanzadas cada 6 meses. Después de esta ventana de desarrollo de 6 meses, comenzando con Angular 4, todas las versiones principales reciben LTS con correcciones de errores y parches de seguridad durante 12 meses adicionales. Desde el lanzamiento hasta el final de su vida útil, cada versión principal recibe actualizaciones durante 18 meses. Consulte la siguiente tabla para ver la versión tentativa y el programa de soporte para AngularJS y Angular:

![01-06](images/01-06.png)

¿Entonces que significa esto para usted? Puede estar seguro de que su código Angular es compatible y compatible con versiones anteriores durante un período de tiempo aproximado de 24 meses, incluso si no realiza cambios en él. Por lo tanto, si escribió una aplicación Angular en la versión 9 en febrero de 2020, su código es compatible en tiempo de ejecución con Angular 10 y será compatible hasta octubre de 2021. Para actualizar su código de Angular 9 a Angular 11, debe asegurarse de que no está utilizando cualquiera de las API obsoletas que reciben un aviso de obsolescencia en Angular 10.

En la práctica, la mayoría de las depreciaciones son menores y fáciles de refactorizar. A menos que esté trabajando con API de bajo nivel para experiencias de usuario altamente especializadas, el tiempo y el esfuerzo necesarios para actualizar su base de código deberían ser mínimos. Sin embargo, esta es una promesa hecha por Google y no un contrato. El equipo de Angular tiene un incentivo significativo para garantizar la compatibilidad con versiones anteriores porque Google ejecuta alrededor de 1,000 aplicaciones Angular con una sola versión de Angular active en cualquier momento en toda la organización. Entonces, para cuando lea esto, todas las más de 1,000 aplicaciones de Google se ejecutarán en la última versión de Angular.

Puede pensar que Google tiene recursos infinitos para actualizar miles de aplicaciones con regularidad. Como cualquier organización, Google también tiene recursos limitados y no todas las aplicaciones son mantenidas activamente por un equipo dedicado. Por lo tanto, el equipo de Angular debe garantizar la compatibilidad a través de pruebas automatizadas y hacer que sea lo más sencillo posible avanzar a través de las principales versiones en el futuro. En Angular 6, el proceso de actualización se simplificó mucho con la introducción de `ng update`.

El equipo de Angular mejora continuamente su proceso de lanzamiento con herramientas CLI automatizadas para hacer que las actualizaciones de la funcionalidad obsoleta sean un esfuerzo razonable y en su mayoría automatizado. Los beneficios de esta estrategia fueron demostrados por Air France y KLM al poder reducir sus tiempos de actualización de 30 días en Angular 2 a 1 día en Angular 7.

Un proceso de actualización predecible y bien respaldado es una excelente noticia tanto para los desarrolladores como para las organizaciones. En lugar de quedarse atascado perpetuamente en una versión heredada de Angular, puede planificar y asignar los recursos necesarios para seguir moviendo su aplicación hacia el futuro sin costosas reescrituras. Como escribí en una publicación de blog de 2017, The Best New Feature of Angular 4, en bit.ly/NgBestFeature, el mensaje es claro:

> Para desarrolladores y gerentes: Angular llegó para quedarse, por lo que debería invertir su tiempo, atención y dinero en aprenderlo, incluso si actualmente está enamorado de algún otro marco.

> Para los responsables de la toma de decisiones (CIO, CTO, etc.): planifique comenzar su transición a Angular en los próximos 6 meses. Será una inversión que podrá explicar a las personas con mentalidad empresarial, y su inversión pagará dividendos durante muchos años, mucho después de que expire la ventana LTS inicial, con elegantes rutas de actualización a Angular vNext y más.

Entonces, ¿por qué Google (Angular) y Microsoft (TypeScript y Visual Studio Code) regalan estas tecnologías de forma gratuita? Hay varias razones:

* Un marco sofisticado que facilita el desarrollo de aplicaciones web es una demostración de destreza técnica, que retiene y atrae el talento de los desarrolladores.
* Un marco de código abierto permite probar y depurar nuevas ideas y herramientas con millones de desarrolladores a escala.
* Permitir a los desarrolladores crear excelentes experiencias web con mayor rapidez impulsa en última instancia más negocios para Google y Microsoft.

No veo ninguna intención nefasta aquí y doy la bienvenida a herramientas abiertas, maduras y de alta calidad que, si es necesario, puedo modificar y doblar a mi propia voluntad. No tener que pagar un contrato de soporte para una pieza de tecnología patentada es un bono de bienvenida.

:blue_book: *Cuidado, buscar ayuda de Angular en la web puede ser complicado. Observará que a veces se hace referencia a Angular como Angular 2 o Angular 4. En ocasiones, tanto Angular como AngularJS se conocen como AngularJS. Esto es incorrecto. La documentación de Angular está en angular.io. Si aterriza en angularjs.org, estará leyendo sobre el marco heredado de AngularJS.*

:high_brightness: *Para obtener las últimas actualizaciones sobre los próximos lanzamientos de Angular, consulte el calendario de lanzamientos oficial en https://angular.io/guide/releases.*

### Filosofía de Angular

Su tiempo es valioso y su felicidad es primordial, por lo que debe tener cuidado al elegir las tecnologías en las que invertir su tiempo. Con esto en mente, debemos responder a la pregunta de por qué aprender Angular, pero no React, Vue o algunos otro marco? Angular es un gran marco para comenzar a aprender. El marco y las herramientas lo ayudan a despegar rápidamente y continuar teniendo éxito con una comunidad vibrante y bibliotecas de IU de alta calidad que puede utilizar para ofrecer aplicaciones web excepcionales. React y Vue son excelentes marcos, con sus fortalezas y debilidades. Cada herramienta tiene su lugar y propósito.

En algunos casos, React es la opción correcta para un proyecto, y en otros casos, Vue es la correcta. Independientemente, llegar a ser algo competente en otros marcos web solo puede ayudarlo a comprender mejor Angular y convertirlo en un mejor desarrollador en general. Las SPA como Backbone y AngularJS captaron toda mi atención en 2012 cuando me di cuenta de la importancia de disociar las preocupaciones de frontend y backend. Las plantillas renderizadas del lado del servidor son casi imposibles de mantener y son la causa principal de muchas reescrituras costosas de los sistemas de software. Si le interesa crear software que se pueda mantener, debe cumplir con la directiva principal; Mantenga la lógica empresarial implementada detrás de la API desacoplada de la lógica de presentación implementada en la interfaz de usuario.

Angular encaja perfectamente con ***el principio de Pareto o la regla 80-20***. Se ha convertido en una plataforma madura y en evolución, lo que le ***permite lograr el 80% de las tareas con el 20% del esfuerzo***. Como se mencionó en la sección anterior, todas las versiones principales son compatibles durante 18 meses, lo que crea un continuo de aprendizaje, se mantiene actualizado y se desaprovechan las funciones antiguas. Desde la perspectiva de un desarrollador de pila completa, este continuo es invaluable, ya que sus habilidades y capacitación seguirán siendo relevantes y frescas durante muchos años.

La filosofía detrás de Angular es errar por el lado de la configuración sobre la convención. Los marcos basados en convenciones, aunque pueden parecer elegantes desde el exterior, dificultan que los recién llegados adopten el marco. Los marcos basados en configuración, sin embargo, tienen como objetivo exponer su funcionamiento interno a través de configuraciones y enlaces explícitos, donde puede adjuntar su comportamiento personalizado al marco. En esencia, donde AngularJS tenía toneladas de magia, que puede ser confusa, impredecible y desafiante de depurar, Angular intenta no ser mágico.

La configuración sobre la convención da como resultado una codificación detallada. La verbosidad es algo bueno. El código conciso es enemigo de la mantenibilidad y solo beneficia al autor original. Como lo expresaron Andy Hunt y David Thomas en The Pragmatic Programmer:

> Recuerde que usted (y otros después de usted) leerán el código cientos de veces, pero solo lo escribirán unas pocas veces.

Además, la Ley de diseño de Andy Hunt dicta:

> Si no puedes arrancar todas las piezas fácilmente, entonces el diseño apesta.

El código detallado, desacoplado, cohesivo y encapsulado es la clave para preparar su código para el futuro. Angular, a través de sus diversos mecanismos, permite la correcta ejecución de estos conceptos. Elimina muchas convenciones personalizadas inventadas en AngularJS, como `ng-click`, e introduce un lenguaje más natural que se basa en los elementos y propiedades HTML existentes. Como resultado, `ng-click` se convierte en `(click)`, extendiendo HTML en lugar de reemplazarlo.

A continuación, repasaremos la mentalidad imperecedera de Angular y el paradigma de programación reactiva, que son las últimas extensiones de la filosofía inicial de Angular.

### Angular Evergreen

Cuando está aprendiendo Angular, no está aprendiendo una versión específica de Angular, sino una plataforma que evoluciona continuamente. Desde los primeros borradores, diseñé este libro con la idea de restar importancia a la versión específica de Angular que estás usando. El equipo de Angular defiende esta idea. A lo largo de los años, he tenido muchas conversaciones con el equipo de Angular y los líderes de opinión dentro de la comunidad y he escuchado muchas presentaciones. Como resultado, puedo afirmar que puede confiar en Angular como una plataforma de desarrollo web madura. Angular recibe actualizaciones con frecuencia con gran atención a la compatibilidad con versiones anteriores. Además, cualquier código que sea incompatible con una nueva versión se presenta con la ayuda de herramientas automatizadas o una guía explícita sobre cómo actualizar su código a través de update.angular.io, por lo que nunca tendrá que adivinar o buscar respuestas en Internet. El equipo de Angular se compromete a garantizar que usted, el desarrollador, tenga la mejor experiencia de desarrollo web posible.

Para llevar esta idea al frente y al centro de los desarrolladores, varios colegas y yo hemos desarrollado y publicado una extensión de Visual Studio Code llamada Angular Evergreen.

![01-07](images/01-07.png)

Esta extensión detecta su versión actual de Angular y la compara con las últimas y próximas versiones de Angular. Las versiones que están etiquetadas a continuación están destinadas a los primeros usuarios y para probar la compatibilidad de su código con una próxima versión de Angular. No utilice las siguientes versiones etiquetadas para implementaciones de producción.

:high_brightness: *Encuentre más información, solicitudes de funciones e informes de errores sobre la extensión Angular Evergreen en https://AngularEvergreen.com.*

Uno de los componentes críticos de Angular que permite que la plataforma permanezca siempre verde (evergreen) es **TypeScript**. TypeScript permite implementar nuevas funciones de manera eficiente al mismo tiempo que brinda soporte para navegadores más antiguos, de modo que su código pueda llegar a la audiencia más amplia posible.

### TypeScript

Angular está codificado con TypeScript. TypeScript fue creado por Anders Hejlsberg de Microsoft para abordar varios problemas importantes con la aplicación de JavaScript a escala empresarial.

Anders Hejlsberg es el creador de Turbo Pascal y C#, y es el arquitecto principal de Delphi. Anders diseñó C# para ser un lenguaje amigable para desarrolladores construido sobre la sintaxis familiar de C y C++. Como resultado, C# se convirtió en el lenguaje detrás del popular .NET Framework de Microsoft. TypeScript comparte un pedigrí similar con Turbo Pascal y C# y sus ideales, lo que los convirtió en un gran éxito.

JavaScript es un lenguaje interpretado dinámicamente, donde el código que escribe es analizado y entendido por el navegador en tiempo de ejecución. Los lenguajes de tipado estático como Java o C# tienen un paso de compilación adicional, donde el compilador puede detectar errores de programación y lógica durante el tiempo de compilación. Es mucho más económico detectar y corregir errores en tiempo de compilación que en tiempo de ejecución. TypeScript aporta los beneficios de los lenguajes de tipado estático a JavaScript al introducir tipos y genéricos al lenguaje. Sin embargo, TypeScript no incluye un paso de compilación, sino un **paso de transpilación**. Un compilador crea código en lenguaje de máquina con C/C++ o lenguaje intermedio (IL) con Java o C#. ***Un transpilador, sin embargo, simplemente traduce el código de un dialecto a otro***. Entonces, cuando se crea, compila o transpila código TypeScript, el resultado es JavaScript puro.

:blue_book: *El nombre oficial de JavaScript es ECMAScript. El conjunto de características y la sintaxis del lenguaje son mantenidos por el Comité Técnico 39 de ECMA o TC39 para abreviar.*

La transpilación tiene otro beneficio significativo. La misma herramienta que convierte TypeScript a JavaScript se puede utilizar para reescribir JavaScript con una nueva sintaxis a una versión anterior que los navegadores más antiguos pueden analizar y ejecutar. Entre 1999 y 2009, el lenguaje JavaScript no vio ninguna característica nueva. ECMAScript abandonó la versión 4 debido a varias razones técnicas y políticas. Comenzando con la introducción de ES5 y luego ES2015 (también conocido como ES6), los proveedores de navegadores han tenido problemas para implementar nuevas funciones de JavaScript en sus navegadores. Como resultado, la adopción de estas nuevas funciones por parte de los usuarios se ha mantenido baja. Sin embargo, estas nuevas características significaron que los desarrolladores podían escribir código de manera más productiva. Esto creó una brecha conocida como la brecha de características de JavaScript, como lo demuestra el gráfico siguiente:

![01-08](images/01-08.png)

La brecha de funciones de JavaScript es variable, ya que TC39 se ha comprometido a actualizar JavaScript cada año en el futuro. Como resultado, TypeScript representa el pasado, presente y futuro de JavaScript. Puede utilizar las funciones futuras de JavaScript hoy y seguir siendo capaz de orientar sus anuncios a los navegadores del pasado para maximizar la audiencia a la que puede llegar.

Ahora, repasemos la arquitectura subyacente de Angular.



### Arquitectura angular básica

Angular sigue el patrón `MV*`, que es un híbrido de los patrones MVC y MVVM. Anteriormente, repasamos el patrón MVC. En un nivel alto, la arquitectura de ambos patrones es relativamente similar, como se muestra en el diagrama siguiente:

![01-09](images/01-09.png)

El nuevo concepto aquí es ViewModel, que representa el código de pegamento que conecta su vista con su modelo o servicio. En Angular, este pegamento se conoce como encuadernación (binding). Mientras que los frameworks MVC como Backbone o React tienen que llamar a un método de renderizado para procesar sus plantillas HTML, en Angular, este proceso es fluido y transparente para el desarrollador. La vinculación es lo que diferencia una aplicación MVC de una MVVM.

La unidad más básica de una aplicación Angular es un componente. Un componente es la combinación de una clase de JavaScript escrita en TypeScript y una plantilla angular escrita en HTML, CSS y TypeScript. La clase y la plantilla encajan como un rompecabezas a través de enlaces, de modo que puedan comunicarse entre sí, como se muestra en el diagrama siguiente:

![01-10](images/01-10.png)

Las clases son una construcción de **programación orientada a objetos (OOP) Object-Oriented Programming (OOP)**. Si invierte tiempo en profundizar en el paradigma OOP, mejorará enormemente su comprensión de cómo funciona Angular. El paradigma OOP permite la inyección de dependencia (DI) de servicios dependientes en sus componentes, por lo que puede realizar llamadas HTTP o activar un mensaje de brindis (toast message) para que se muestre al usuario sin introducir esa lógica en su componente o duplicar su código. DI facilita que los desarrolladores utilicen muchos servicios interdependientes sin tener que preocuparse por el orden de creación de instancias, inicialización o destrucción de dichos objetos de la memoria.

Las plantillas Angular también permiten una reutilización similar de código a través de directivas, pipes(tuberías), controles de usuario y otros componentes. Estos son fragmentos de código que encapsulan el código de usuario final altamente interactivo. Este tipo de código de interactividad a menudo es complicado y enrevesado y debe mantenerse aislado de la lógica de negocios o la lógica de presentación para que su código se pueda mantener.

Todos los componentes, servicios, directivas, pipes y controles de usuario de Angular están organizados en módulos. Cada aplicación de Angular es iniciada por un módulo raíz que procesa su primer componente e inyecta cualquier servicio y prepara las dependencias que pueda requerir. Puede introducir módulos secundarios para habilitar capacidades como la carga diferida, de modo que no tenga que entregar todos los componentes de su aplicación web al navegador de una vez. Por ejemplo, no sirve de nada enviar código para el panel de administración a un usuario sin privilegios de administrador.

Angular hace un uso intensivo de la biblioteca RxJS, que introduce patrones de desarrollo reactivos en Angular, a diferencia de los patrones de desarrollo imperativos más tradicionales.

## El paradigma del desarrollo reactivo

Angular admite múltiples estilos de programación. La pluralidad de estilos de codificación es una de las grandes razones por las que es accesible para programadores con diferentes antecedentes. Ya sea que tenga experiencia en programación orientada a objetos o sea un firme creyente de la programación funcional, puede crear aplicaciones viables con Angular. En el Capítulo 3, Creación de una aplicación angular básica, comenzará a aprovechar los conceptos de programación reactiva para crear la aplicación LocalCast Weather.

Como programador, lo más probable es que esté acostumbrado a la programación imperativa. La programación imperativa es cuando usted, como programador, escribe un código secuencial que describe todo lo que debe hacerse en el orden en que lo ha definido y el estado de su aplicación dependiendo de las variables correctas que se configurarán para funcionar correctamente. Escribe bucles, condicionales y funciones de llamada; usted dispara eventos y espera que sean manejados. La lógica imperativa y secuencial es la forma en que está acostumbrado a codificar.

La programación reactiva es un subconjunto de la programación funcional. En la programación funcional, no puede confiar en las variables que ha establecido anteriormente. Cada función que escriba debe sostenerse por sí sola, recibir su propio conjunto de entradas y devolver un resultado sin verse influenciado por el estado de una función o clase externa. ***La programación funcional es muy compatible con el desarrollo basado en pruebas (TDD)*** porque cada función es una unidad que se puede probar de forma aislada. Como tal, cada función que escribe se vuelve componible. Por lo tanto, puede mezclar, combinar y combinar cualquier función que escriba con cualquier otra y construir una serie de llamadas que produzcan el resultado que espera.

***La programación reactiva agrega un giro a la programación funcional. Ya no se trata de lógica pura, sino de un flujo de datos asincrónico que transforma y moldea en cualquier forma que necesite con un conjunto de funciones componibles***. Entonces, cuando se suscribe a un evento en un flujo reactivo, entonces está cambiando su paradigma de codificación de la programación reactiva a la programación imperativa.

:blue_book: *Más adelante en el libro, cuando implemente la aplicación LocalCast Weather, aprovechará la suscripción en acción en dos lugares, en los componentes CurrentWeather y CitySearch.*

Considere el siguiente ejemplo, acertadamente expresado por Mike Pearson en su presentación

***Pensar de manera reactiva***: lo más difícil es proporcionar instrucciones para obtener agua caliente del grifo para ayudar a comprender las diferencias entre la programación imperativa y reactiva:

Instrucciones para sacar agua caliente del grifo.

Paso | Imperativo | Reactivo
-----|------------|---------
0    | Estado inicial: el agua está apagada | Estado inicial: el agua está apagada
1    | Agarra una manguera | Abra el grifo de agua caliente
2    | Rocíe agua en el calentador | 
3    | Abra el grifo de agua caliente | 
4    | Envíe un mensaje de texto a la empresa de servicios públicos para obtener gas |
5    | Espera agua caliente
6    | Deshaga sus pasos para restaurar el estado inicial | Deshaga sus pasos para restaurar el estado inicial

Como puede ver, con la programación imperativa, debe definir cada paso de la ejecución del código. Cada paso depende del paso anterior, lo que significa que debe considerar el estado del medio ambiente para garantizar una operación exitosa. En un entorno así, es fácil olvidar un paso y muy difícil comprobar la exactitud de cada paso individual. En la programación reactiva funcional, se trabaja con flujos de datos asíncronos que dan como resultado un flujo de trabajo sin estado que es fácil de componer con otras acciones.

RxJS es la biblioteca que permite implementar su código en el paradigma reactivo.

### RxJS

RxJS son las siglas de Reactive Extensions, que es una biblioteca modular que permite la programación reactiva, que en sí misma es un paradigma de programación asincrónica y permite la manipulación de flujos de datos a través de funciones de transformación, filtrado y control. Puede pensar en la programación reactiva como una evolución de la programación basada en eventos.

### Reactive data streams

En la programación dirigida por eventos, debe definir un controlador de eventos y adjuntarlo a una fuente de eventos. En términos más concretos, si tuviera un botón **Save**, que expone un evento **onClick**, implementaría una función `confirmSave` que, cuando se activa, mostraría una ventana emergente para preguntarle al usuario **¿Está seguro?**. Mire el siguiente diagrama para ver una visualización de este proceso.

![01-11](images/01-11.png)

En resumen, tendría un evento que se activará una vez por acción del usuario. Si el usuario hace clic en el botón Guardar muchas veces, este patrón representará con gusto tantas ventanas emergentes como clics, lo que no tiene mucho sentido.

El patrón de publicación-suscripción (pub/sub) es un tipo diferente de programación impulsada por eventos. En este caso, podemos escribir múltiples manejadores para que todos actúen sobre el resultado de un evento dado simultáneamente. Digamos que su aplicación acaba de recibir algunos datos actualizados. El editor revisa su lista de suscriptores y transmite los datos actualizados a cada uno de ellos.

Consulte el siguiente diagrama sobre cómo el evento de datos actualizado activa múltiples funciones:

* Una función `updateCache` actualiza su caché local con nuevos datos
* Una función `fetchDetails` recupera más detalles sobre los datos del servidor
* Una función `showToastMessage` informa al usuario que la aplicación acaba de recibir nuevos datos

![01-12](images/01-12.png)

Todos estos eventos pueden ocurrir de forma asincrónica; sin embargo, las funciones `fetchDetails` y `showToastMessage` recibirán más datos de los que necesitan y puede resultar complicado intentar componer estos eventos de diferentes formas para modificar el comportamiento de la aplicación.

En la programación reactiva, todo se trata como un flujo. Una transmisión contendrá eventos que suceden con el tiempo y estos eventos pueden contener algunos datos o ningún dato. El siguiente diagrama visualiza un escenario en el que su aplicación está escuchando los clics del mouse del usuario. Los flujos incontrolados de clics de los usuarios no tienen sentido. Usted ejerce cierto control sobre esta secuencia aplicándole la función de aceleración, por lo que solo obtiene actualizaciones cada 250 milisegundos(ms). Si se suscribe a este nuevo evento, cada 250 ms, recibirá una lista de eventos de clic. Puede intentar extraer algunos datos de cada evento de clic, pero en este caso, solo le interesa la cantidad de eventos de clic que ocurrieron. Podemos dar forma a los datos del evento sin procesar en varios clics utilizando la función `map`.

Más adelante, es posible que solo estemos interesados en escuchar eventos con dos o más clics, por lo que podemos usar la función `filter` para actuar solo en lo que es esencialmente un evento de doble clic. Cada vez que se activa nuestro evento de filtro, significa que el usuario tenía la intención de hacer doble clic, y usted puede actuar sobre esa información mostrando una alerta.

El verdadero poder de las transmisiones proviene del hecho de que puede elegir actuar sobre el evento en cualquier momento a medida que pasa por varias funciones de control, transformación y filtro. Puede elegir mostrar los datos de clic en una lista HTML usando `*ngFor` y la `async` pipe de Angular, para que el usuario pueda monitorear los tipos de datos de clic que se capturan cada 250 ms.

![01-13](images/01-13.png)

Ahora consideremos algunos patrones arquitectónicos Angular más avanzados.

## Arquitectura Angular Avanzada

Como se mencionó anteriormente, en la sección Arquitectura básica Angular, los componentes, servicios y dependencias de Angular se organizan en módulos. Las aplicaciones Angular se inician a través de su módulo raíz, como se muestra en el siguiente diagrama:

![01-14](images/01-14.png)

El módulo root puede importar otros módulos y también declarar componentes y proporcionar servicios. A medida que su aplicación crece, necesita crear submódulos que contengan sus componentes y servicios. Organizar su aplicación de esta manera le permite implementar la carga diferida, lo que le permite controlar qué partes de su aplicación se envían al navegador y cuándo. A medida que agrega más funciones a su aplicación, importa módulos de otras bibliotecas, como Angular Material o NgRx. Implementa el enrutador para permitir experiencias de navegación enriquecidas entre sus componentes, lo que permite que su configuración de enrutamiento orquesta la creación de componentes.

:high_brightness: *El Capítulo 7, Creación de una aplicación de primera línea de negocio de enrutador, presenta la arquitectura de enrutador primero, donde le animo a comenzar el desarrollo de su aplicación creando todas sus rutas con anticipación.*

En Angular, los servicios se proporcionan como singleton a un módulo de forma predeterminada. Te acostumbrarás rápidamente a este comportamiento. Sin embargo, debe tener en cuenta que si proporciona el mismo servicio en varios módulos, cada módulo tiene su propia instancia del servicio proporcionado. En el caso de un servicio de autenticación, donde deseamos tener solo una instancia en toda nuestra aplicación, debe tener cuidado de proporcionar solo esa instancia del servicio de autenticación en el nivel del módulo raíz. Cualquier servicio, componente o módulo proporcionado en el nivel raíz de su aplicación estará disponible en el módulo de funciones.

Más allá de los módulos, el router es la siguiente tecnología más poderosa que debe dominar en Angular.

### El Angular Router

El Router Angular, incluido en el paquete `@angular/router`, es una parte central y crítica de la creación de aplicaciones **single-page applications (SPAs)** que actúan y se comportan como sitios web normales que son fáciles de navegar mediante los controles del navegador o los controles de zoom o micro zoom. .

El enrutador angular tiene características avanzadas como carga diferida (lazy loading), salidas de enrutador (router outlets), rutas auxiliares, seguimiento de enlace activo inteligente(smart active link tracking) y la capacidad de expresarse como un `href`, lo que permite una arquitectura Router-first app altamente flexible que aprovecha los componentes controlados por datos sin estado utilizando RxJS `BehaviorSubject`.

Los equipos grandes pueden trabajar con una única base de código, y cada equipo es responsable del desarrollo de un módulo, sin pisar los dedos de los demás, al tiempo que permite una fácil integración continua. Google, con sus miles de millones de líneas de código, trabaja con una única base de código por una muy buena razón: la integración a posteriori es muy cara.

Los equipos pequeños pueden remezclar sus diseños de IU sobre la marcha para responder rápidamente a los cambios sin tener que volver a diseñar su código. Es fácil subestimar la cantidad de tiempo perdido debido a cambios tardíos en el diseño o la navegación del juego. Estos cambios son más fáciles de absorber por equipos más grandes, pero un esfuerzo costoso para equipos pequeños.

Considere el diagrama que sigue, donde `app.ts` contiene el módulo. Tiene un `rootRouter`; componentes `a`, `master`, `detail` y `c`; `services`; `pipes`; y `directives` proporcionadas y declaradas para ello. Todos estos componentes serán analizados y cargados con entusiasmo por el navegador cuando un usuario navegue por primera vez a su aplicación.

![01-15](images/01-15.png)

Si tuviera que implementar una ruta `/b` con carga diferida, necesitaría crear un módulo de funciones llamado `b`, que tendría su propio `childRouter`; componentes `d`, `e` y `f`; `services`; `pipes`; y `directives` proporcionadas y declaradas para ello. Durante el transpile-time, Angular empaquetará estos componentes en un archivo o paquete separado y este paquete solo se descargará, analizará y cargará si el usuario alguna vez navega a una ruta en `/b`.

Analicemos la carga diferida con más detalle.

### Lazy loading


### State management
#### The Flux pattern
#### NgRx
### React.js architecture
## Notable Angular features
### Angular 6
### Angular 8
### Angular 9
## Summary
## Further reading
## Questions



![01-16](images/01-16.png)
![01-17](images/01-17.png)
![01-18](images/01-18.png)
![01-19](images/01-19.png)
