# 04 Introducción a Angular - • 23 clases • 2h 24m

* Introducción a la sección 03:00
* Temas puntuales de la sección 00:11
* Introducción a Angular 08:18
* Crear un proyecto de Angular 07:21
* Nota de actualización 00:19
* Explicación de cada archivo del proyecto 08:43
* Explicación de los archivos dentro del SRC 07:02
* App Component 07:49
* Contador App 06:54
* Métodos en el componente 05:12
* Tarea con el contador 03:42
* Crear un componente manualmente 09:41
* Componente de Heroe y separación de directorios 08:01
* Cambios en el template del componente 06:51
* Concepto de one way data binding - enlazado en una sola vía 06:21
* Crear componente de forma automática 06:15
* Directiva `*ngFor` 12:36
* Directiva `*ngIf` 04:51
* `ng-Template` y el `ngIf-else` 04:32
* Módulos 10:09
* Módulos - segunda parte 08:16
* Bonus: Hacer respaldo de nuestro proyecto en GitHub 07:35
* Código fuente de la sección 00:17

## Introducción a la sección 03:00

Estamos entrando a la sección 4 del curso, en donde oficialmente vamos a comenzar nuestro camino de Angula. Ya les voy a enseñar a ustedes cómo crear un proyecto de Angular, que significa cada uno de los archivos y directorios y que contiene cada uno de éstos, para que ustedes sepan más o menos o que tengan alguna idea de qué es, para qué me pueden servir, o para qué están orientados.

También les voy a explicar más adelante dónde está la documentación oficial para que ustedes tengan también referencias oficiales o actualizadas de donde se encuentra.

Pero en general, quiero explicarles a Uds. para qué sirve cada uno de los archivos y directorios que se están creando en este momento, son muchos, pero no quiere decir que ustedes necesiten modificarlos. De hecho el 99 por ciento del tiempo ustedes ni siquiera se van a dar cuenta de que existen, ni siquiera los vamos a voltear a ver. Pero va a haber ciertos momentos donde será necesario modificar alguna configuración y es bueno que ustedes sepan para qué sirven cada uno de ellos.

Usualmente vamos a pasar más tiempo trabajando en una carpeta llamada **Source `src`**, ahí es donde está realmente el corazón de nuestra aplicación de Angular. Nosotros vamos a crear componentes, vamos a crear los archivos HTML y sus contrapartes TypeScript para que podamos hacer las interacciones y modificar las vistas como nosotros queremas.

Y si es cierto, estas son las bases para comenzar cualquier aplicación de Angular que vamos a seguir haciendo de aquí en adelante.

Otra cosa es que vamos a llegar hasta el punto de explicar los ***módulos*** en esta sección y muchas personas me han criticado eso, porque estás enseñando módulos desde ahorita en una sección introductoria de Angular, pero a mí me interesa que ustedes miren que los módulos no son complicados y son necesarios de dominar a lo largo del curso. Todo lo vamos a trabajar de manera modularizada, lo cual es algo que les va a ayudar muchísimo a ustedes cuando entren a utilizar paquetes de terceros escritos en Angular que están obviamente basados en módulos o cuando ustedes necesiten reutilizar su código. Y bueno, hay muchas razones por las cuales trabajar en módulos es lo que se recomienda hoy en día.

En fin, eso es todo.


## Temas puntuales de la sección 00:11

¿Qué veremos en esta sección?

Este es un breve listado de los temas fundamentales:

1. Crear proyectos de Angular
2. Explicar cada archivo y directorio de un proyecto
3. Componentes
4. Módulos
5. One way data binding
6. Uso del AngularCLI - ***Angular Command Line Interface***
7. Directivas creadas por Angular
8. **`ngIf`** y **`ngIf-else`**

Y más...

Esta es la sección donde empezaremos nuestro camino de Angular.

## Introducción a Angular 08:18

![image](https://user-images.githubusercontent.com/23094588/144288489-5475a292-a7e5-423e-8e0f-1e5e3273761c.png)

Antes de comenzar a escribir nuestro código en Angular quiero hacer una introducción. Si nosotros vemos el sitio web de [Angular](https://angular.io/), que es Angular, podemos ver rápidamente que habla de que con Angular nosotros podemos desarrollar para un montón de plataformas y eso es totalmente cierto.

Nosotros podemos desarrollar para la web, para el móvil, para móvil de forma nativa y aplicaciones nativas de escritorios para aplicaciones de Windows, Linux y Mac.

Podemos hacer todo eso con Angular, con el mismo código de Angular. Claro, aquí ya intervienen otros factores, como por ejemplo para la web podemos hacerlo directamente con Angular o utilizar Angular y **Universal** para hacer un service de rendering.

Para los dispositivos móviles tenemos dos tipos podemos utilizar **Native Script** que lo compila directo a **Swift** o **Android**. También tenemos móvil web qué podríamos usar el mismo código de Angular o bien utilizar otros frameworks de terceros, como por ejemplo **Ionic**, que es uno de los exponentes más fuertes en ese ámbito para hacer aplicaciones híbridas.

Y también podemos hacer **PWAs** directamente con Angular o con Ionic.

Podemos hacer aplicaciones de escritorio gracias a **Electron**, pero siempre todo con el mismo código de Angular.

Eso sonara bastante complicado, pero realmente es el mismo código de Angular que se aplica en diferentes tecnologías, lo cual si tú aprendes Angular, es muy fácil entrar a cualquier otra de esas tecnologías.

![image](https://user-images.githubusercontent.com/23094588/144290593-2970fa62-ebb7-49e4-93f9-4dc2bfeaf0d0.png)

**¿Qué es Angular?**

Angular es un **framework**, eso significa que es un marco de trabajo estandarizado. ¿A qué nos referimos con esto? Pues muy probablemente sitú ves el código de Angular de otra persona va a ser muy parecido al código de Angular que tú estás desarrollando, porque aquí vamos a seguir ciertos estándares que recomienda el mismo equipo de Angular para desarrollar aplicaciones.

Vas a ver que los ***componentes*** se llaman igual o tienen nombres parecidos. Vas a ver que los ***servicios*** se llaman parecido, las directivas y otro montón de cosas.

Otro punto es que Angular viene con todo lo que tú necesitas para trabajar. Es raro que tú digas Ok, necesito incorporar otro paquete de terceros. No digo que no pasa, pero usualmente con una aplicación de Angular ya tienes todo lo que necesitas para 
comenzar. Obviamente, si ocupas **Google Maps**, obviamente se ocupás **Map Box**, obviamente si ocupas algo especializado de alguna otra librería con la cual quieras trabajar, probablemente si necesitas algo extra, pero por lo general ya viene bien completo con todo lo que vas a ocupar para trabajar.

Las aplicaciones de Angular son modulares. ¿A qué nos referimos con esto?, pues básicamente nosotros vamos a crear módulos, estos módulos van a servir o van a tener objetivos específicos.

Y también, por si te lo preguntas, **Google** es quien mantiene hoy en día el framework de Angular.


![image](https://user-images.githubusercontent.com/23094588/144290667-b5f821d8-eaed-440d-b8c3-4d78e487aac0.png)

Por otro lado, quiero hablar sobre los bloques fundamentales de Angular.

Angular se compone de 5 bloques o pilares fundamentales que son:

* Los componentes
* Las rutas 
* Las directivas
* Los servicios 
* Los módulos.


![image](https://user-images.githubusercontent.com/23094588/144291116-d1af6eda-db4f-4e97-b2a5-d93b93b731f8.png)

Los componentes podrían verse como un bloque de código que tiene su segmento HTML y tiene una contraparte de TypeScript que usualmente es una clase. Esa clase de TypeScript es como las que vimos nosotros en la introducción, nada sorprendente. Una clase común y corriente que tiene un decorador, eso es todo.

La parte del HTML es el HTML que tú estás acostumbrado, tiene divs, puede tener botones, puede tener span, puede tener textos en negrita, el código HTML que tú ya conoces, eso es básicamente un componente. 

También se busca que los componentes sean bloques pequeños de código y lo más simples posibles.

![image](https://user-images.githubusercontent.com/23094588/144291381-c0766b4a-5434-41b0-b558-84c49b70727b.png)

Luego tenemos los servicios, los servicios son bastante interesantes porque es bastante fuerte lo que los servicios pueden hacer en Angular. Esto ha hecho de que la verdad no sea tan necesario que tú necesites entrar en **Redux**, no te preocupes si no sabes qué es eso, para las personas que conocen más de Redux, pues sabrán de lo que hablo.

Pero para las personas que ya conocen un poco de Angular, sabrán que los servicios pueden utilizarse de tal manera que tú no vas a ocupar trabajar con Redux, **Blog** u otro tipo de ***Gestor de Estado*** claro, son opcionales.

Siempre hay muchas alternativas y hay unos beneficios en cada uno de ellos.

Usualmente los servicios de Angular son ***singleton*** bastante fuertes que te van a permitir trabajar toda la aplicación con uno, bueno, con la información centralizada.

***Podríamos decir que los servicios son lugares centralizados de información.***

![image](https://user-images.githubusercontent.com/23094588/144292070-92f818a8-d631-4bf1-99bb-aad9226735c4.png)

Usualmente ustedes van a tener un componente, su componente puede tener un botón HTML, ese botón es el que va a llamar al servicio para que grabe en base de datos, para que traiga información o cualquier otra cosa.

***Pero usualmente los servicios son los lugares centrales de información.***


![image](https://user-images.githubusercontent.com/23094588/144292790-6c3e0eca-1beb-4dcd-b0b3-07250dcbd41c.png)

Luego tenemos las **directivas**, hay tres tipos de directivas:

* Directivas de componentes 
* Directivas estructurales 
* Directivas de atributos.

Las ***directivas de componentes*** básicamente son muy parecidas a un componente, sólo que tiene un pedazo de código HTML reutilizable, el cual ya viene como conectado. Es decir, tú colocas la directiva y ya crea ese HTML con cierta funcionalidad integrada y eso es bien útil.

Luego tenemos las ***directivas estructurales*** que lo que hacen es modificar el **DOM** o el **HTML**, ya sea añadiendo elementos o removiendo elementos.

Luego tenemos las ***directivas de atributos*** que básicamente cambian la apariencia o el comportamiento de un elemento, otro componente o bien una directiva. Sé que esto sonará raro, pero no se preocupen, ya lo terminaremos viendo.


![image](https://user-images.githubusercontent.com/23094588/144293417-16a60a5f-013f-449d-afdb-7d9e627b7afb.png)

Luego tenemos las **rutas**, las rutas son básicamente diferentes componentes que ustedes pueden mostrar pasados en la URL del navegador web o el URL en el cual se encuentra el cliente.


![image](https://user-images.githubusercontent.com/23094588/144293855-b94f3ef5-87e7-4e65-9c69-5687cf00f16a.png)

Y por último, el último bloque que tenemos aquí para hablar son los **módulos**. Los módulos son geniales porque permiten agrupar todo lo que nosotros hemos hablado, inclusive otros módulos.

Podemos tener un módulo de productos en el cual va a estar todo lo relacionado a productos, por ejemplo, las formas de las pantallas para mostrar los productos, las pantallas para agregar productos, editar productos o servicios que estén relacionados a los productos. Todo puede estar ahí, en el mismo módulo.

Lo mismo con módulos de autenticación. Quiere decir que ahí estaría todo lo relacionado a la autenticación de mi aplicación o módulo de proveedores, módulo de clientes. Imagino que eso ya tiene un poco más de sentido. Obviamente todo esto es muy abstracto. Todavía no lo vemos en código, pero así funciona.


![image](https://user-images.githubusercontent.com/23094588/144294136-bb2a2850-a377-481b-a1da-a7e5b5578d3a.png)

Otra cosa interesante de los módulos es que si nosotros ocupáramos, por ejemplo, crear este calendario, cómo lo haríamos?

Bueno, probablemente alguien que tenga un conocimiento técnico bastante avanzado va a poder decir bueno, yo me voy a poner a crear este calendario de cero, pero muy probablemente ese es el caso del calendario, ya hay componentes hechos para que ustedes simplemente los descarguen y los utilicen en su proyecto.

Eso es todo. Si lo que ustedes necesitan ya existe en Angular, muy probablemente va a ser un módulo lo que ustedes van a descargar, ese módulo lo van a incorporar a otros módulos de su aplicación y ya tienen toda la funcionalidad lista.

Recuerden que no necesariamente el código de Angular es el que ustedes van a poder utilizar de terceros. Pueden utilizar librerías propias de JavaScript que no están escritas en Angular, porque realmente Angular es el mismo JavaScript, se va a poder hacer. Pero lo genial de esto es que si ustedes se encuentran el paquete y el paquete está soportado por Angular, van a ver un gran potencial ya incorporándome en sus aplicaciones.

## Crear un proyecto de Angular 07:21

Vamos a crear nuestro primer proyecto usando **Angular CLI**, para ver la versión que tenemos instalada podemos pulsar el comando **`ng --version`**.



## Nota de actualización 00:19
## Explicación de cada archivo del proyecto 08:43
## Explicación de los archivos dentro del SRC 07:02
## App Component 07:49
## Contador App 06:54
## Métodos en el componente 05:12
## Tarea con el contador 03:42
## Crear un componente manualmente 09:41
## Componente de Heroe y separación de directorios 08:01
## Cambios en el template del componente 06:51
## Concepto de one way data binding - enlazado en una sola vía 06:21
## Crear componente de forma automática 06:15
## Directiva `*ngFor` 12:36
## Directiva `*ngIf` 04:51
## `ng-Template` y el `ngIf-else` 04:32
## Módulos 10:09
## Módulos - segunda parte 08:16
## Bonus: Hacer respaldo de nuestro proyecto en GitHub 07:35
## Código fuente de la sección 00:17
