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

Vas a ver que los ***componentes*** se llaman igual o tienen nombres parecidos. Vas a ver que los ***servicios*** se llaman parecido, las ***directivas*** y otro montón de cosas.

Otro punto es que Angular viene con todo lo que tú necesitas para trabajar. Es raro que tú digas Ok, necesito incorporar otro paquete de terceros. No digo que no pasa, pero usualmente con una aplicación de Angular ya tienes todo lo que necesitas para comenzar. Obviamente, si ocupas **Google Maps**, obviamente se ocupás **Map Box**, obviamente si ocupas algo especializado de alguna otra librería con la cual quieras trabajar, probablemente si necesitas algo extra, pero por lo general ya viene bien completo con todo lo que vas a ocupar para trabajar.

Las aplicaciones de Angular son ***modulares***. ¿A qué nos referimos con esto?, pues básicamente nosotros vamos a crear módulos, estos módulos van a servir o van a tener objetivos específicos.

Y también, por si te lo preguntas, **Google** es quien mantiene hoy en día el framework de Angular.


![image](https://user-images.githubusercontent.com/23094588/144290667-b5f821d8-eaed-440d-b8c3-4d78e487aac0.png)

Por otro lado, quiero hablar sobre los bloques fundamentales de Angular.

Angular se compone de ***5 bloques o pilares fundamentales*** que son:

* Los componentes
* Las rutas 
* Las directivas
* Los servicios 
* Los módulos.


![image](https://user-images.githubusercontent.com/23094588/144291116-d1af6eda-db4f-4e97-b2a5-d93b93b731f8.png)

***Los componentes*** podrían verse como un bloque de código que tiene su segmento HTML y tiene una contraparte de TypeScript que usualmente es una clase. Esa clase de TypeScript es como las que vimos nosotros en la introducción, nada sorprendente. Una clase común y corriente que tiene un decorador, eso es todo.

La parte del HTML es el HTML que tú estás acostumbrado, tiene divs, puede tener botones, puede tener span, puede tener textos en negrita, el código HTML que tú ya conoces, eso es básicamente un componente. 

También se busca que los componentes sean bloques pequeños de código y lo más simples posibles.

![image](https://user-images.githubusercontent.com/23094588/144291381-c0766b4a-5434-41b0-b558-84c49b70727b.png)

Luego tenemos ***los servicios***, los servicios son bastante interesantes porque es bastante fuerte lo que los servicios pueden hacer en Angular. Esto ha hecho de que la verdad no sea tan necesario que tú necesites entrar en **Redux**, no te preocupes si no sabes qué es eso, para las personas que conocen más de Redux, pues sabrán de lo que hablo.

Pero para las personas que ya conocen un poco de Angular, sabrán que los servicios pueden utilizarse de tal manera que tú no vas a ocupar trabajar con Redux, **Blog** u otro tipo de ***Gestor de Estado*** claro, son opcionales, siempre hay muchas alternativas y hay unos beneficios en cada uno de ellos.

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

Luego tenemos las ***rutas***, las rutas son básicamente diferentes componentes que ustedes pueden mostrar pasados en la URL del navegador web o el URL en el cual se encuentra el cliente.


![image](https://user-images.githubusercontent.com/23094588/144293855-b94f3ef5-87e7-4e65-9c69-5687cf00f16a.png)

Y por último, el último bloque que tenemos aquí para hablar son los ***módulos***. Los módulos son geniales porque permiten agrupar todo lo que nosotros hemos hablado, inclusive otros módulos.

Podemos tener un módulo de productos en el cual va a estar todo lo relacionado a productos, por ejemplo, las formas de las pantallas para mostrar los productos, las pantallas para agregar productos, editar productos o servicios que estén relacionados a los productos. Todo puede estar ahí, en el mismo módulo.

Lo mismo con módulos de autenticación. Quiere decir que ahí estaría todo lo relacionado a la autenticación de mi aplicación o módulo de proveedores, módulo de clientes. Imagino que eso ya tiene un poco más de sentido. Obviamente todo esto es muy abstracto. Todavía no lo vemos en código, pero así funciona.


![image](https://user-images.githubusercontent.com/23094588/144294136-bb2a2850-a377-481b-a1da-a7e5b5578d3a.png)

Otra cosa interesante de los módulos es que si nosotros ocupáramos, por ejemplo, crear este calendario, cómo lo haríamos?

Bueno, probablemente alguien que tenga un conocimiento técnico bastante avanzado va a poder decir bueno, yo me voy a poner a crear este calendario de cero, pero muy probablemente ese es el caso del calendario, ya hay componentes hechos para que ustedes simplemente los descarguen y los utilicen en su proyecto.

Eso es todo. Si lo que ustedes necesitan ya existe en Angular, muy probablemente va a ser un módulo lo que ustedes van a descargar, ese módulo lo van a incorporar a otros módulos de su aplicación y ya tienen toda la funcionalidad lista.

Recuerden que no necesariamente el código de Angular es el que ustedes van a poder utilizar de terceros. Pueden utilizar librerías propias de JavaScript que no están escritas en Angular, porque realmente Angular es el mismo JavaScript, se va a poder hacer. Pero lo genial de esto es que si ustedes se encuentran el paquete y el paquete está soportado por Angular, van a ver un gran potencial ya incorporándome en sus aplicaciones.

## Crear un proyecto de Angular 07:21

Vamos a crear nuestro primer proyecto usando **Angular CLI**, para ver la versión que tenemos instalada podemos pulsar el comando **`ng --version`**.

![image](https://user-images.githubusercontent.com/23094588/148211026-7ac74991-6d6e-4abf-9b44-68c881b899ef.png)

Vamos a trabajar con la versión 12.2.1 de Angular. El paquete **`@schematics/update`** nos va a permitir actualizar de manera automática a versiones posteriores de Angular.

Para crear nuestros proyectos de Angular lo vamos a hacer dentro de un directorio que contenga todos nuestros proyectos Angular en mi caso lo llamaré **`PROYECTOS-ANGULAR`**.

![image](https://user-images.githubusercontent.com/23094588/148211812-e53faeb4-3592-4b29-8013-9a9e109c80bc.png)

En la consola nos posicionamos en dicho directorio y vamos a pulsar el siguiente comando que nos permite **crear un nuevo proyecto Angular**:

```sh
ng new bases
```

Cuando damos Enter nos hace una serie de preguntas:

![image](https://user-images.githubusercontent.com/23094588/148212205-0969803e-57c0-4db0-92d9-d5e3092bd734.png)

Nos pregunta si deseamos incorporar el ***Angular routing*** es decir si crea de manera automática el archivo de rutas por nosotros, como estamos aprendiendo le vamos a indicar que NO.

![image](https://user-images.githubusercontent.com/23094588/148212471-912883fb-fd6e-4b7d-981f-d4534c9871b6.png)

Lo siguiente que me pregunta es que tipo estilo vamos a manejar, en este caso vamos a seleccionar CSS, basta presionar Enter para seleccionar la opción por defecto.

![image](https://user-images.githubusercontent.com/23094588/148212646-4b13be97-0af2-4c64-bca8-b511ac92983c.png)

Al presionar Enter se comienza a crear el proyecto Angular, esto puede llevar algunos minutos.

![image](https://user-images.githubusercontent.com/23094588/148213296-29ae46dd-8344-43da-8a1c-91266a296e52.png)

Una vez que termina de crear el proyecto podemos ver todo lo que ha descargado entre ellos la carpeta **NODE_MODULES**.

![image](https://user-images.githubusercontent.com/23094588/148213415-494990cf-2300-4587-be15-66ceb39e1db0.png)

Vamos a cambiar el nombre de la carpeta **bases** por **125-01-bases** para tener una notación de acuerdo al Curso y numero de proyecto que vamos creando. 

![image](https://user-images.githubusercontent.com/23094588/148213493-bf19221c-5d7e-4e90-a7b4-b8a9affd215d.png)

Una vez hecho esto lo abrimos dentro de VSC.

![image](https://user-images.githubusercontent.com/23094588/148213761-1bd7e4b2-072c-45fb-9939-6589ab245b5a.png)

#### Ejecutar la APP

Para ejecutar la aplicación nos metemos dentro de la carpeta del proyecto y pulsamos el siguiente comando:

```sh
ng serve -o
```

Este comando toma todo el código, lo transpila a JS monta un servidor mediante WebPack y con **`-o`** lo abre tan pronto este disponible.

![image](https://user-images.githubusercontent.com/23094588/148214394-cbf8562f-0599-45a3-9279-77c9113734b4.png)

![image](https://user-images.githubusercontent.com/23094588/148214821-18bd2c8d-f49a-43ac-9592-e525002a91af.png)

Una vez que se levanta el servidor se abre el navegador con la APP.

![image](https://user-images.githubusercontent.com/23094588/148214766-4acd5abd-28db-4638-a803-81aa02c14426.png)


## Nota de actualización 00:19

En la siguiente clase vemos la estructura del proyecto de Angular, en las últimas versiones tenemos dos cambios:

- Ya no trae TSLint, este fue deprecado. Si quieren usar un linter, actualmente pueden usar ESLint.

- Actualmente la carpeta e2e no viene por defecto, ya que se está discutiendo el futuro de Protractor. Pueden leer más sobre esto en el blog: https://blog.angular.io/angular-v12-is-now-available-32ed51fbfd49.

Ninguno de estos dos cambios afecta a la funcionalidad del curso, pueden seguirlo sin pasos adicionales.


## Explicación de cada archivo del proyecto 08:43

Vamos a explicar los diferentes archivos creados dentro del proyecto.

![image](https://user-images.githubusercontent.com/23094588/148215464-a57740ad-741c-4e0e-9ae4-6ab316ae074d.png)


* ***`e2e`***: ***Deprecado en la versión 12 de Angular***. Nos permite hacer la configuración para las pruebas Unitarias End To End.

* **`node_modules`**: Contiene una gran cantidad de Modulos, para ayudar a desarrollar la aplicación y otros necesarios para la APP en producción.

   ![image](https://user-images.githubusercontent.com/23094588/148221138-89d08234-dbce-483d-a387-f8304fe2ec2d.png)


* **`src`**: Carpeta SRC que contiene varios archivos y que se expliaca en la siguiente sección.

   ![image](https://user-images.githubusercontent.com/23094588/148220831-720a6e1e-fb86-4def-824f-99a94a03bf6c.png)


* **`.browserslistrc`**: El sistema de compilación utiliza este archivo para ajustar la salida de CSS y JS para admitir los navegadores especificados.

   ![image](https://user-images.githubusercontent.com/23094588/148220660-901520eb-b3db-47c4-9842-798ac1a8579b.png)

* **`.editorconfig`**: Son configuraciones del Editor.

   ![image](https://user-images.githubusercontent.com/23094588/148220442-25679845-57e2-4de3-860d-ea30fd691c52.png)


* **`.gitignore`**: Archivo para indicar que archivos no debe darle seguimiento GIT.

   ![image](https://user-images.githubusercontent.com/23094588/148220291-d14d87f3-f4d6-42ab-854d-6a4e6427b382.png)

* **`angular.json`**: Este es un archivo importante para nuestra APP, contiene configuraciones importantes para la APP como el favicon de la APP, indica donde estan los assets de la aplicación, indica el archivo general de estilos CSS,  

   ![image](https://user-images.githubusercontent.com/23094588/148219785-f31628a2-0377-4bff-89fd-1e40eae12854.png)

   
* **`karma.conf.js`**: Son las configuraciones para las pruebas unitarias e integración basadas en Karma. Esto se cubre en el Curso avanzadlo de Angular.

   ![image](https://user-images.githubusercontent.com/23094588/148219630-4aa87fb9-5e65-4e48-a1aa-478f49724155.png)

* **`package-lock.json`**: Este archivo indica como se construyeron los modulos de node entre otras cosas, su contenido es enorme.

   ![image](https://user-images.githubusercontent.com/23094588/148219324-5f5097c9-f9bb-424f-9d27-2a9073a4b521.png)

* **`package.json`**: Este archivo es algo delicado y no deberíamos hacer modificaciones en el y se si necesita modificar generalmete esto se hace mediante comandos. Contiene las dependencias de producción y las de desarrollo, comandos 

   ![image](https://user-images.githubusercontent.com/23094588/148217936-fa832288-3d01-42b7-a533-2be6f17e23f1.png)


* **`README.md`**: Archivo Mark Down para documentar la APP. En VSC podemos ver estos archivos formateados con la opción de menú Vista - Paleta de Comandos.

   ![image](https://user-images.githubusercontent.com/23094588/148217415-5fa29607-49e3-487a-8464-2392d75a85a2.png)

   ![image](https://user-images.githubusercontent.com/23094588/148217475-35c0d319-77eb-4712-a38e-c218771e637a.png)

   ![image](https://user-images.githubusercontent.com/23094588/148217538-5e6b0f69-b76a-4e80-a1b6-35d351553c1c.png)

* **`tsconfig.app.json`**: Este archivo "extiende" del **`tsconfig.json`**. Esta enfocado más a la aplicación pero rara vez se modifica.

   ![image](https://user-images.githubusercontent.com/23094588/148218010-2d7bce09-7645-40d2-9cb0-bf46990e54c5.png)

* **`tsconfig.json`**: Archivo de configuración de TypeScript, básicamente indica como se va a traducir el TypeScript a JavaScript o como quieren que funcione TypeScript en este proyecto. Por lo general este archivo no se modifica.

   ![image](https://user-images.githubusercontent.com/23094588/148218124-c977ad03-7ebf-468d-8362-9634f326975d.png)

* **`tsconfig.spec.json`**: Este archivo "extiende" del **`tsconfig.json`** y añade características adicionales. Generarlmente los archivos `.spec` estan relacionados con las pruebas o test.

   ![image](https://user-images.githubusercontent.com/23094588/148218164-081b9bc8-7bba-4fca-a32f-1865ab1cd6ae.png)

* ***`tslint.json`***: ***Deprecado en la versión 12 de Angular***. Todos los archivos con extensión **`.json`** son archivos de configuración. El **`tslint.json`** contiene reglas de TypeScript que nos ayudan a programar de cierta manera 


## Explicación de los archivos dentro del SRC 07:02

![image](https://user-images.githubusercontent.com/23094588/148240071-687334eb-ee28-485b-b1fa-d0f5a4350c11.png)

Dentro de la carpeta **`src`** tenemos otra carpeta llamada **`app`**, dentro de esta carpeta tenemos nuestro componente inicial el cual consiste en 4 archivos:

* **`app.component.css`**: Archivo de estilos del componente, inicialmente esta vacío.

   ![image](https://user-images.githubusercontent.com/23094588/148241517-ac0b1ce5-a4e1-4b27-b979-51f092174098.png)

* **`app.component.html`**: Archivo de plantilla del componente.

   ![image](https://user-images.githubusercontent.com/23094588/148241626-1ce4cb0d-60fc-4a9b-80d1-b320f9605ad2.png)

   Esta plantilla es la que pinta la aplicación.
   
   ![image](https://user-images.githubusercontent.com/23094588/148241768-272a9bb0-339a-49a3-b8cd-4b2a6e0d95a1.png)

* **`app.component.spec.ts`**: Archivo de pruebas del componente.

   ![image](https://user-images.githubusercontent.com/23094588/148241890-f2147f89-f0d1-4ac6-87dd-619b8ae89325.png)
   
* **`app.component.ts`**: Archivo TypeScript del componente. Es una clase común y corriente.

   ![image](https://user-images.githubusercontent.com/23094588/148241993-2bf8294b-f8d5-4425-b27a-db71e51c3464.png)

Además dentro de esta carpeta contamos con el archivo:

* **`app.module.ts`**: Archivo donde se definen los modulos de la aplicación. Es una clase común y corriente con un decorador especial **`@NgModule`**

   ![image](https://user-images.githubusercontent.com/23094588/148242073-970eb8fe-5d8f-4415-9844-4834947fd931.png)


Dentro de la carpeta **`src`** también tenemos la carpeta llamada **`assets`**, donde colocamos recursos estáticos, usualmente son imágenes, videos, sonidos, etc. Actualmente esta carpeta solo contiene el archivo:

* **`.gitkeep`**: Este archivo se coloca en una carpeta que esta vacía y para que GIT no la ignore se coloca este archivo.


Dentro de la carpeta **`src`** también tenemos la carpeta llamada **`environments`**, donde tenemos dos archivos donde podemos tener nuestras variables de entorno de desarrollo y producción:

* **`environment.prod.ts`**: Variables de entorno de producción.

   ![image](https://user-images.githubusercontent.com/23094588/148244238-fa30b82d-b2c1-4ff3-950d-3f68707a4060.png)

* **`environment.ts`**: Variables de entorno de desarrollo.

   ![image](https://user-images.githubusercontent.com/23094588/148244319-95c68beb-3028-4077-bf01-19709a73f09d.png)

Además de las carpetas anteriores, la carpeta **`src`** contiene los siguientes archivos:

* **`favicon.ico`**: Favicon de la aplicación.
 
   ![image](https://user-images.githubusercontent.com/23094588/148244981-4b366734-ac07-49c1-af4d-38e6e1587879.png)

* **`index.html`**: Página inicial de la aplicación.

   ![image](https://user-images.githubusercontent.com/23094588/148245055-c14023d2-b302-4a3a-8188-890895528562.png)

* **`main.ts`**: Este archivo usualmente no se toca, sirve para indicarle a Angular el ambiente donde se esta ejecutando la aplicación. 

   ![image](https://user-images.githubusercontent.com/23094588/148245365-e8fef523-381a-4f85-a26a-8d0e7778ffe6.png)

* **`polyfill.ts`**: Archivo que ayuda tener compatibilidad con otros navegadores web.

   ![image](https://user-images.githubusercontent.com/23094588/148245859-4bfb16a7-4352-46ab-86cf-ab092bd4a3c6.png)

* **`styles.css`**: Archivo de estilos CSS global para toda la aplicación.

   ![image](https://user-images.githubusercontent.com/23094588/148245981-c6ff99c1-bc6a-4fcb-8d92-1d42e5334160.png)

* **`test.ts`**: Configuración del ambiente de pruebas.

   ![image](https://user-images.githubusercontent.com/23094588/148246349-34239386-c8b9-4c11-bea3-d904550d3af8.png)


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
