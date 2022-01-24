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

Como ya hemos visto actualmente la aplicación se ve así:

![image](https://user-images.githubusercontent.com/23094588/148247872-78e9c3cd-5900-47ba-9dbf-6dbce1798712.png)

Vamos a realizar algunos cambios en el componente inicial que se creo automáticamente para modificar lo que se muestra actualmente. Vamos al archivo **`app.component.html`** vamos a eliminar todo su contenido y vamos a insertar lo siguiente:

```html
<h1>Hola Mundo</h1>
```

En el navegador ahora veremos:

![image](https://user-images.githubusercontent.com/23094588/148248718-525245fb-2db7-4bba-8804-25906d33ec84.png)

Ahora en el archivo **`styles.css`** vamos a insertar el siguiente código:

```css
* {
  font-family: Helvetica, Arial, sans-serif;
  font-weight: 200;
}

html, body {
  
  background: white;
  margin: 20px;
  color: #3e4144;
  -webkit-font-smoothing: antialiased;
}


dd {
  font-weight: bold;
}

button {
  background-color: black;
  border-radius: 5px;
  border: 0px;
  color: white;
  cursor: pointer;
  margin-right: 5px;
  margin-left: 5px;
  padding: 5px 10px;
}

button:hover {
  background-color: #3e4144;
}

button:focus{ 
  outline: none;
}

.p-1 {
  padding: 1px;
}
```

Nuestra página se vera así:

![image](https://user-images.githubusercontent.com/23094588/148249166-242b2302-85fc-4ef9-9abb-ae33a32c6e3f.png)

Si abrimos el archivo **`app.componet.ts`** tenemos lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/148250539-d2c6a79b-613c-4e5f-b473-4072bc457886.png)

Tenemos una importación del decorador **`Component`** que viene de **`@angular/core`**, el decorador **`Component`** tiene varias propiedades internas:

```ts
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
```

Una de las propiedades que tenemos es **`selector`** y sirve para indicar que nombre va a tener este componente, en este caso **`app-root`** por que es la aplicación principal. Si nosotros abrimos el archivo **`index.html`** tenemos:

![image](https://user-images.githubusercontent.com/23094588/148251383-025742fb-b50d-4d24-b495-7d5652325967.png)

dentro del **`<body>`** tenemos **`<app-root></app-root>`** que es el mismo nombre que le dimos al **`selector`** del componente **`app.componet.ts`**, en realidad lo que esta haciedo es que en la página **`index.html`** esta incrustando el componente **`app.componet.ts`**.

Otra propiedad que tenemos en el decorador **`Component`** es **`templateUrl`** en donde vamos a indicar la plantilla HTML asociada al componente en este caso es **`'./app.component.html'`**.

Ademas del **`templateUrl`** existe otra propiedad **`template`** donde podemos insertar directamente el HTML que deseemos sin necesidad de tener un archivo HTML especifico.

![image](https://user-images.githubusercontent.com/23094588/148252834-8754f620-95f9-479c-a1bb-56cbda5b954a.png)

![image](https://user-images.githubusercontent.com/23094588/148252877-df88f340-3e60-4a8c-a515-93a3235a544e.png)

Con **`template`** podemos usar los "Valds Tips" para tener un HTML más complejo.

![image](https://user-images.githubusercontent.com/23094588/148253388-b073742d-0a57-4527-ada1-49ba55e0bce1.png)

![image](https://user-images.githubusercontent.com/23094588/148253441-ac315eb6-dea7-494f-9018-bab2789322cf.png)

Finalmente tenemos la propiedad  **`styleUrls`** que nos sirve para indicar el archivo de estilos para el componente en este caso **`./app.component.css`**, en este caso este archivo esta vacío por lo que podriamos elminar esta propiedad y el archivo **`app.component.css`** o también lo que podríamos haber hecho es meter el código que insertamos en **`style.css`** en este archivo y tendríamos el mismo efecto. 

En este caso vamos a borrar el archivo de Estilos y la propiedad y vamos a usar la plantilla HTML que teniamos inicialmente.

![image](https://user-images.githubusercontent.com/23094588/148254429-19ff8083-6ec8-4351-8a30-6ceb2bbef8ba.png)


### Clase **`AppComponent`**

Dentro de la clase **`AppComponent`** tenemos definida una propiedad llamada **`title`** con valor **`bases`** el cual vamos a cambiar por **`Contador App`**,

![image](https://user-images.githubusercontent.com/23094588/148255103-037f3c3e-b6f2-4767-8265-bbedb5183d84.png)


para mostrar este valor en el HTML vamos a poner el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/148255234-588b6ecb-903c-43dd-9cb7-af3df3ce0e90.png)

![image](https://user-images.githubusercontent.com/23094588/148255337-906034e0-0b88-451c-b608-b0f28879c3dc.png)

De esta forma podemos tener propiedades definidas en la clase e imprimirlas en el HTML para que el usuario vea su valor en el navegador.

El uso de las **`{{ }}`** adems de imprimir propiedades de la clase también sirven para imprimir cualquier valor de una expresión JS como **`{{ 1 + 1 }}`**

![image](https://user-images.githubusercontent.com/23094588/148255892-1ad2e230-ab34-4529-baff-077832a77687.png)

![image](https://user-images.githubusercontent.com/23094588/148255929-eed73aba-5d3b-4d01-8af1-4bba9da832f6.png)

Vamos a eliminar esta última expresión ya que por el momento no nos va a ser útil, además en lugar de llamar a la propiedad **`title`** la llamaremos **`titulo`**

![image](https://user-images.githubusercontent.com/23094588/148256209-fede1bdb-eacb-4ad0-a80d-59c31863d12c.png)

Y si vemos el archivo HTML ya nos marca un error:

![image](https://user-images.githubusercontent.com/23094588/148256350-268db50b-cd8e-4eb5-8727-95953968dd54.png)
 
Esto es por que ya no tenemos esta propiedad, debemos cambiar el nombre:

![image](https://user-images.githubusercontent.com/23094588/148256451-44465639-df13-401e-85bd-e0e5aeb3c533.png)

Cuando definimos una propiedad esta es pública pero podemos indicarlo explicitamente si lo deseamos, además también podemos indicar el tipo de la propiedad aun que en este caso es muy facíl ver que se infiere su tipo.

![image](https://user-images.githubusercontent.com/23094588/148257502-84515f9c-bd7d-46f8-b987-889203b4dfe9.png)

![image](https://user-images.githubusercontent.com/23094588/148257741-1fc8d947-9146-4e83-b6c4-5b344a4eeffc.png)

![image](https://user-images.githubusercontent.com/23094588/148257772-40ac7bf7-1346-4acf-b16b-9b3556d4dde5.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/148258233-adc101da-bec2-4b30-9f2a-36bdcd261a82.png)


## Contador App 06:54

En esta aplicación vamos a desplegar un contador que se va a ir incrementando o decrementando según sea el caso, para mantener el estado de este contador vamos a incluir una propiedad que va a contener su valor. Como ya hemos visto las propiedades por default sion ***públicas*** por lo mismo no lo indicaremos explicitamente, vamos a darle un valor inicial a la propiedad. Por otro lado en el HTML vamos a mostrar dicha propiedad.

![image](https://user-images.githubusercontent.com/23094588/148507361-38db0e77-dafb-4e57-970b-9c902e062166.png)

![image](https://user-images.githubusercontent.com/23094588/148507414-c5c2da22-16bc-4b48-a70b-12d1328d8787.png)

Ahora lo que vamos a incluir son los botones para incrementar y decrementar el contador.

![image](https://user-images.githubusercontent.com/23094588/148507872-c97ba3f1-4d27-40de-a28e-173234cc0e4d.png)

![image](https://user-images.githubusercontent.com/23094588/148507802-0ac0e9c4-19e8-45ef-aa19-32bdd24d38f0.png)

Si pulsamos en los botones por ahora no pasa nada. Estos botones aparecen así por el estilo que incluimos en el archivo **`styles.css`**.

Para darle funcionalidad a los botones vamos a incluir el evento **`click`** del botón. Los eventos en Angular se definen entre paréntisis **`(click)`** y después un **`=`** y entre comillas lo que queremos hacer. En este caso vamos a poner lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/148508611-ceb035e9-0716-45c2-b15e-cb6ce955b27e.png)

En este caso estamos poniendo directamente la instrucción JS que queremos ejecutar.

![image](https://user-images.githubusercontent.com/23094588/148508682-de6f574a-f22e-4395-9d5d-e7b891a453db.png)

![image](https://user-images.githubusercontent.com/23094588/148508721-55cd07ee-5eb1-4fe5-b428-0497a113166b.png)

Al presionar los botones se va incrementando o decrementando el contador. Si vamos a a la pestaña **ELEMENTOS** y presionamos algún botón podemos apreciar en CHROME lo que se vuelve a renderizar al presionar el botón (Se remarca lo que cambia, en la imagen no se aprecia).

![image](https://user-images.githubusercontent.com/23094588/148509495-6739eca7-9b52-4c1c-ad87-50b68253e5d2.png)

![image](https://user-images.githubusercontent.com/23094588/148509332-0a477ea5-474a-4ecc-b338-de36fc922164.png)

En el template HTML hemos puesto la expresión **`(click)="numero = numero + 1;"`** y podríamos pensear ponerla así **`(click)="numero += 1;"`** pero al hacerlo esto nos indica un fallo:

![image](https://user-images.githubusercontent.com/23094588/148510048-649c8ea9-9fdd-4f43-828d-dce6b4efb20a.png)

A pesar de que es una expresión habitual de JS al usarla en el template HTML, generalmente solo se va a poner código JS muy sensillo dentro del template HTML pero generalmente no lo debemos hacer, ya veremos otra alternativa que es mejor.

### GIT

![image](https://user-images.githubusercontent.com/23094588/148510317-fb2cb83a-c13e-4f39-8a99-9a8253afdfa2.png)

![image](https://user-images.githubusercontent.com/23094588/148510791-38923ea3-2e3a-47c6-a657-82ded0b6e75a.png)

![image](https://user-images.githubusercontent.com/23094588/148510661-68f4ea20-f8ea-4392-8823-9327a427b5e9.png)


## Métodos en el componente 05:12

En esta lección vamos a crear dos métodos para sumar y restar uno al contador, y vamos a usar estos métodos en lugar de colocar directamente el código en el template HTML, esto nos va a quedar así:

![image](https://user-images.githubusercontent.com/23094588/148512191-cc24396f-8ef9-4713-a9a6-a304abbbb133.png)

Observe que es necesario colocar la palabra **`this.`** antes de la propiedad que deseemos usar, en el el template HTML no es necesario hacerlo aun que podríamos. Ademas dentro del archivo TypeScript ya podemos usar sin problema la expresión condensada para incrementar o decrementar el contador sin problema.

![image](https://user-images.githubusercontent.com/23094588/148512216-c27e2315-8dc5-444c-ab4e-a3f8bd4f4a5e.png)

![image](https://user-images.githubusercontent.com/23094588/148512243-fcc01cc3-ab13-4aab-b742-0dcce51f2d61.png)

Todo sigue funcionando igual. 

Existe una mejora que podemos usar, usualmente los método **`sumar()`** y **`restar()`** hacen básicamente lo mismo pero al ponerlo por separado estamos de cierta manera duplicando el código. Vamos a crear un solo método el cual recibe un valor que nos servira para incrementar o decrementar el contador, de hecho el valor pasado podría ser uno diferente a 1 o -1.

![image](https://user-images.githubusercontent.com/23094588/148513569-b0daa5a5-44bc-46d4-a8c4-cd0098685ee2.png)

![image](https://user-images.githubusercontent.com/23094588/148513601-9ffdfad1-c070-40e1-bae0-0b9109f7e3e4.png)

![image](https://user-images.githubusercontent.com/23094588/148513621-5525091b-0874-45eb-bf3e-cb0d6f7da2d0.png)

Todo sigue trabajando bien.

### GIT 

![image](https://user-images.githubusercontent.com/23094588/148514370-e23e56b4-2e3f-425d-b12a-4cd38bd1ddcb.png)


## Tarea con el contador 03:42

En esta lección vamos a poner una propiedad para que para parametrizar el valor que vamos a usar como incremento o decremento y que simplemente usando esa propiedad tengamos el valor definido.

![image](https://user-images.githubusercontent.com/23094588/148520357-5cc89750-1cca-4d74-a19a-8226a44bd512.png)

![image](https://user-images.githubusercontent.com/23094588/148520398-ffc1594c-f231-44d4-b4ba-ba0f522770df.png)

![image](https://user-images.githubusercontent.com/23094588/148520431-cbe8cd22-a831-4a45-9acc-394ed2a77f88.png)

![image](https://user-images.githubusercontent.com/23094588/148520489-31cbddc1-130f-4f3d-92d7-7cc5cf548fe5.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/148520685-7a9ea357-958e-4433-9818-beff57467155.png)


## Crear un componente manualmente 09:41

En esta lección vamos a crear un componente manualmente que tenga toda la funcionalidad de nuestro Contador, de esta manera podemos tener varias instancias del contador en una misma página web con su valor independiente sin necesidad de duplicar código.

Vamos a crear el archivo **`contador.component.ts`** dentro de la  carpeta **`app`**, la parte **`.component.`** es una notación que se utiliza para indicar que precisamente se trata de un componente.

El contenido de este archivo es el siguiente:

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-contador',
  template: `



  `
})
export class ContadorComponent {
  
}
```

Es una clase común y corriente tiene la palabla **`export`** para que la podamos utilizar en otros lados. Tiene su correspondiente decorador con su selector y su template. En este caso el template va incrustado dentro del propio archivo TS es decir que no tenemos un HTML independiente. Lo que vamos a hacer es mover el código HTML que tenemos en **`app.component.html`** dentro del template.

![image](https://user-images.githubusercontent.com/23094588/148528718-a365c67e-2e5d-4839-b983-a5962e70ff1a.png)

Como vemos al mover este código nos esta marcando una serie de errores ya que no encuentra las propiedades a las que se hace referencia en el template, nos hace falta mover lo que se encuentra en **`app.component.ts`** dentro de **`contador.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/148529080-06e5cadb-b352-473d-92fa-3fde5f458b86.png)

Si cargamos la aplicación tenemos que se muestra todo en blanco por que ya no existe nada en **`app.component.ts`** y **`app.component.html`**.

![image](https://user-images.githubusercontent.com/23094588/148529168-f89302bb-33bf-41b8-8057-73f216ff2af6.png)

La idea es insertar el componente **`contador.component`** dentro del **`app.component`** para que podamos visualizarlo, recordemos que le hemos dado de nombre **`selector: 'app-contador'`**, por lo que tenemos que colocor en **`app.component.html`** la siguiente etiqueta.

![image](https://user-images.githubusercontent.com/23094588/148529658-ea659f61-d58b-4977-9588-7a3d5c8b74ab.png)

Como vemos ya nos esta marcando un error, si vemos el navegador web vemos un error de compilación

![image](https://user-images.githubusercontent.com/23094588/148529981-ba03b7e1-23c3-4025-8b5a-f09481ed7424.png)

si vemos la consola de Angular nos indica más detalles del error:

![image](https://user-images.githubusercontent.com/23094588/148529839-e52be79f-94e5-4138-a092-4e2b6d57c31b.png)

Lo que nos indica es que el **`app-contador`** no es un elemento conocido, que si es un componente de Angular verificar que es parte del Modulo.

Cada que se cree un Componente es necesario registrarlo en el archivo **`app.module.ts`** en la sección **`declarations`** (Podemos insertar el import automáticamente con **`CTRL + .`**):

![image](https://user-images.githubusercontent.com/23094588/148531104-3cef948d-0550-4d7d-aeaa-fa5397d2ee62.png)

![image](https://user-images.githubusercontent.com/23094588/148531167-f5b332ac-5b08-4a03-8ee7-efbb08083c80.png)

El error a desaparecido en la Consola Angular, si recargamos el navegador tenemos que ya funciona nuevamente pero ahora usando un componente:

![image](https://user-images.githubusercontent.com/23094588/148531432-85c3a51b-ca0c-4cf5-b8fb-f1e9341454d4.png)

Podemos insertar los componentes que deseemos y cada uno de ellos es una instancia diferenente:

![image](https://user-images.githubusercontent.com/23094588/148531691-26fa9fdb-6af3-4701-b72f-00653a49b868.png)

![image](https://user-images.githubusercontent.com/23094588/148531749-1decfe1d-4d43-4708-aa43-e43f77023381.png)

Vamos a dejar solo una instancia por el momento.

### GIT

![image](https://user-images.githubusercontent.com/23094588/148531937-55d0064f-6e10-49e3-9bb3-6484253f6672.png)


## Componente de Heroe y separación de directorios 08:01

Al crear el componente **`contador.component`** lo hicimos en la carpeta **`app`** junto con el en componente **`app.component`** pero lo que se hace generalmente es tener una carpeta por cada uno de los componentes que se vayan creando, por lo que vamos a crear la carpeta **`contador`** dentro de **`app`** y vamos a mover el componente **`contador.component`** en ella.

![image](https://user-images.githubusercontent.com/23094588/148533600-c71e42fd-a769-4c23-9cee-9cbc1600932d.png)

Debemos tener cuidado de modificar **`app.module.ts`** (VSC lo hace automáticamente al mover el componente):

![image](https://user-images.githubusercontent.com/23094588/148533418-807de111-6b3b-45c4-ae27-a6192024b829.png)

![image](https://user-images.githubusercontent.com/23094588/148533468-219b3ad6-56bf-4ff6-b50b-343b88fa831e.png)

Todo funciona igual pero tenemos mejor estructurado nuestro código.

### GIT

![image](https://user-images.githubusercontent.com/23094588/148533784-972e3b6e-802c-44ce-8d0e-bd5f34d65f12.png)

### Componente Heroe

En esta parte de la lección vamos a crear un nuevo componente manual llamado **`heroe.component`** pero como es posible que tengamos una carpeta que haga referencia a todo lo referente sobre los heroes vamos a crear una carpeta **`heroes`**, dentro de esta vamos a crear la carpeta **`heroe`** y dentro de esta crearemos el componete **`heroe.component`**.

![image](https://user-images.githubusercontent.com/23094588/148535089-45f57cb0-d6d5-466a-b7c4-e42cecf90541.png)

El contenido del componente **`heroe.component`** es el siguiente:

![image](https://user-images.githubusercontent.com/23094588/148535487-9a1b8e4a-35f6-44fc-b92a-c035d10862a4.png)

![image](https://user-images.githubusercontent.com/23094588/148535556-0a1cdb5e-f8b1-4229-82ab-072560677f31.png)

Recordemos que además de crear el componente debemos añadirlo en **`app.modules.ts`**:

![image](https://user-images.githubusercontent.com/23094588/148535710-39d3c247-a0b2-46fe-8de2-010de2e35267.png)

Ahora vamos a hacer que en el navegador se despliegue este componente. Recordemos que el **`app.component.html`** es el componente inicial y es aquí donde vamos a insertar lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/148536432-b7840194-ef90-428d-b459-f94707036583.png)

![image](https://user-images.githubusercontent.com/23094588/148536456-cd6ceb16-3b49-4c1e-8b4d-7d3273ac7e42.png)


### GIT

![image](https://user-images.githubusercontent.com/23094588/148536857-7caa2f29-53ff-4bd5-92e6-c31c52b89345.png)


## Cambios en el template del componente 06:51

En esta lección vamos a trabajar sobre el aspecto del componente **`heroe.component`**:

En este caso tenemos definidas dos propiedades que mostramos en el navegador.

![image](https://user-images.githubusercontent.com/23094588/148538944-4bd3a2f1-55d9-4433-b4d8-b185d8e2704e.png)

![image](https://user-images.githubusercontent.com/23094588/148538981-07da53d3-4d99-4fa4-b62e-3f32f9a082a2.png)


También podemos tener un método e invocarlo desde el HTML.

![image](https://user-images.githubusercontent.com/23094588/148539260-5b53c3a9-19f5-471b-902b-77cdbaa699b4.png)

![image](https://user-images.githubusercontent.com/23094588/148539296-b799ccf3-073e-48d5-b6dd-9f99ad6c0c53.png)

Podemos usar los "balds tips" para retornar la cadena de salida:

![image](https://user-images.githubusercontent.com/23094588/148539417-fd8fc285-b624-49ed-9c6f-c54fbc56a287.png)

El resultado es el mismo:

![image](https://user-images.githubusercontent.com/23094588/148539455-bc1e90b3-af55-4eb4-b4ce-fd5eaa2017e1.png)

#### **`get`** y **`set`**

Otra cosa interesante que tiene Angular son los **`get`** y **`set`** dentro de una clase, en este caso vamos a crear un **`get`** que es como tener una propiedad y que se procesa cuando se invoca, observe que al invocarlo el nombre no lleva los paréntesis como en los métodos.

![image](https://user-images.githubusercontent.com/23094588/148540068-b5e7f5a6-1cee-42a1-b669-515b698dcb47.png)

![image](https://user-images.githubusercontent.com/23094588/148540095-d43af02b-e7e1-4943-b53e-0070aaadbb71.png)

Observe como aparecen los **`gets`** a la hora de usarlo, es como una propiedad más pero realmente es un **`getter`**:

![image](https://user-images.githubusercontent.com/23094588/148540283-41fb01af-4cfc-4fde-9ef9-639ab40d3e6a.png)

Finalmente vamos a colocoar dos botones:

![image](https://user-images.githubusercontent.com/23094588/148540671-81ead4bf-5094-437f-81ba-0037de1e2939.png)

![image](https://user-images.githubusercontent.com/23094588/148540700-33bff492-68fe-4556-b119-0edf281b6048.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/148540826-c861c7e1-d6ea-4603-9230-13a28fab69bb.png)

## Concepto de one way data binding - enlazado en una sola vía 06:21

En esta lección vamos a darle funcionalidad a los dos botones que habiamos incluido en la lección anterior, el de **`Cambiar Héroe`** lo que va a hacer cuando lo pulsemos es cambiar en nombre **`Ironman`** por **`Spideman`** en todos los lugares donde aparece, y el  **`Cambiar Edad`** va a cambiar el **`45`** por **`39`** en todos los sitios donde aparezca.

Vamoa a crear el método **`cambiarNombre()`** como este método no retorna nada podemos ponerle **`: void`** que indica que no retorna nada, en la sección anterior no le pusimos nada al método **`get nombreCapitalizado`** podemos ponerle **`: string`** por que en este caso lo que retorna es un **`string`**.

Lo que vamos a hacer en el método **`cambiarNombre()`** es cambiar el valor de la propiedad **`nombre`**, en lugar de **`Ironman`** le vamso a asignar **`Spideman`**.

Ahora en nuestro template HTML vamos a colocar el evento **`(click)`** al botón correspondiente para que llame al método **`cambiarNombre()`**:

![image](https://user-images.githubusercontent.com/23094588/148691138-294aa54b-e622-4e43-a43b-8c91b8a2521c.png)

Si cargamos la aplicación.

![image](https://user-images.githubusercontent.com/23094588/148691190-10126863-e7f6-4ef3-a923-b17ec61b0b49.png)

Al presionar el botón **`Cambiar Héroe`** tenemos:

![image](https://user-images.githubusercontent.com/23094588/148691219-73f918d3-c44e-4211-b19c-81b23179b3e1.png)

Observemos en la pestaña **`Elements`** nos indica donde esta cambiando, donde se redibuja el nuevo nombre del héroe lo demás lo deja tal cual.

![image](https://user-images.githubusercontent.com/23094588/148691260-c0a2740b-4141-4854-804e-26510562459a.png)

Así de facíl estamos cambiando información del DOM.

Ahora vamos a hacer otro método llamado **`cambiarEdad()`** también de tipo **`void`** para cambiar el valor de la propiedad **`edad`**:

![image](https://user-images.githubusercontent.com/23094588/148692357-ebe031e7-c79c-405a-8547-eae377958a25.png)

Al recargar el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/148692245-59d125e0-fcd6-4a8e-b8b1-cd9d84145254.png)

Y al presionar el botón **`Cambiar Edad`** tenemos:

![image](https://user-images.githubusercontent.com/23094588/148692366-750c9bd7-b00d-4088-9780-2204f99a8e75.png)

En la pestaña **`Elements`** vemos claramente lo que se esta renderizando:

![image](https://user-images.githubusercontent.com/23094588/148692321-b2acdf06-aa05-4462-8722-2c65c58bec7a.png)

**NOTA: Si volvemos a pulsar nuevamente alguno de los botones el código se ejecuta pero la información no se reenderiza nuevamete ya que los valores no cambian.**

Esto es parte del concepto **ONE WAY DATA BINDING** o **ENLAZADO EN UNA SOLA VÍA**, es decir si las propiedades cambian en el componente del archivo **TS** se reedibujan en el template HTML, pero no hay manera (hasta el momento) que si cambiamos algo en el template HTML cambie el valor dentro del archivo **TS**.

### GIT

![image](https://user-images.githubusercontent.com/23094588/148692630-13118c0f-5783-4fad-9b8f-415939cfb0e9.png)

## Crear componente de forma automática 06:15

En esta lección vamos a crear un nuevo componente pero vamos a usar **Angular CLI** para su creación, desde la consola vamos a pulsar el siguiente comando:


```sh
ng generate component heroes/listado
```

De una forma abreviada se puede escribir:

```sh
ng g c heroes/listado
```

![image](https://user-images.githubusercontent.com/23094588/148692927-448d24de-9cde-4275-ae83-bd73b8289f09.png)

Como podemos apreciar se crean cuatro archivos y se actualiza un archivo. Creo los archivos CSS, de pruebas, HTML y el TS.

![image](https://user-images.githubusercontent.com/23094588/148692951-8dc40f0d-fd7f-412d-8096-8971faed041a.png)

además actualizo el archivo **`/app.module.ts`** para incluir el nuevo componente. 

![image](https://user-images.githubusercontent.com/23094588/148693067-3d6c7a86-f3bb-4c95-889e-ab082f446c2e.png)

 Todo lo que haciamos antes manualmente lo ha hecho Angular CLI por nosotros.

Para pintar en el navegador el nuevo componente lo que vamos a hacer es modificar el archivo **`app.component.html`**:

![image](https://user-images.githubusercontent.com/23094588/148693166-e13ec4b3-c690-4d54-947b-bc2c7c848a77.png)

Y al recargar el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/148693175-c88041c9-48a3-4e54-a073-56c67d4abaa8.png)

Que es lo que tenemos en el archivo **`listado.component.html`**:

![image](https://user-images.githubusercontent.com/23094588/148693294-16c47c7a-76c9-4bcc-9789-04e5a13e799e.png)

En este caso para el componente Listado no vamos a usar ni el archivo CSS ni el de Pruebas por lo que los eliminamos:

![image](https://user-images.githubusercontent.com/23094588/148693367-0612f773-73dd-42ee-b0ac-d7ed5a4fbbd1.png)

Al hacer esto debemos cambiar algo en **`listado.component.ts`**, como ya no existe el archivo CSS nos esta marcando un error:

![image](https://user-images.githubusercontent.com/23094588/148693397-e83bf05d-730e-4f13-9ea6-0e0dd7d22183.png)

Una vez corregido nos queda así:

![image](https://user-images.githubusercontent.com/23094588/148693455-275f4c10-8021-4524-86f6-414fb1e263fd.png)

Como podemos ver Anglura en la clase esta ***implementando*** **`OnInit`** y para usarlo crea el método **`ngOnInit()`** esto corresponde al ***Ciclo de Vida de Angular***, a su vez también crea un **`constructor`**, tanto el  **`constructor`** como el **`OnInit`** son cosas que dispara Angular de manera automática, solo para ver en que orden se ejecutan estos dos "métodos" vamos a poner un mensaje dentro de ellos:

![image](https://user-images.githubusercontent.com/23094588/148693660-19ceb981-47c4-4a2f-9319-572ff2396835.png)

Al recargar el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/148693671-7621a4fb-b66d-4ae2-a10e-11607ab10922.png)

Como se puede observar se ejecuta primero el **`constructor`** antes que el componente se renderice y posteriormente el **`OnInit`**, usualmente **`OnInit`** se usa para iniciar cosas, por ejemplo un servicio que recupera datos del servidor y son necesarios pintar en una pantalla inicial.

En este ejemplo no vamos a usar ni el **`constructor`** ni el **`OnInit`** por lo que podemos eliminarlos para simplificar nuestro código. Vamos a dejar los archivos como se muestra en la imagen:

![image](https://user-images.githubusercontent.com/23094588/148693878-2ac7c71c-6c77-4420-8ff8-53daadec0b59.png)

![image](https://user-images.githubusercontent.com/23094588/148693885-3ec13ac2-44df-4413-afb6-812b673c72e8.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/148693926-666bd32a-d9a3-4ce3-80f3-0ff9f5e91f5d.png)


## Directiva `*ngFor` 12:36

En el componente **`ListadoComponent`** vamos a definir un listado de héroes es decir un **`array`** de **`string`** los valores los podemos poner entre corchetes:

```js
heroes: string[] = ['Spiderman', 'Ironman', 'Hulk', 'Thor'];
```

En nuestro archivo de Template HTML vamos a pintar algo como lo que sigue:

![image](https://user-images.githubusercontent.com/23094588/148694174-6b74b204-5606-4432-b8c2-98a88da91c80.png)

En el navegador se ve así:

![image](https://user-images.githubusercontent.com/23094588/148694188-1034dc16-efe8-4413-9dc3-93f5f1068c95.png)

Queremos algo así pero que en lugar de **`item 1`** nos pinte cada uno de los nombres de los Héroes. Una forma de hacerlo es así:

![image](https://user-images.githubusercontent.com/23094588/148694267-6aff8ca8-57be-4cec-a1fe-390baea780bf.png)

![image](https://user-images.githubusercontent.com/23094588/148694273-ec9db05b-a9d0-4abd-b1fc-e756260092f1.png)

Esto puede ser valido pero en el caso de que tuviéramos 1000 héroes tendríamos que repetir la sentencia 1000 veces. Gracias a Angular y sus ***Directivas*** podemos escribir el código como sigue para obtener el mismo resutaldo:

![image](https://user-images.githubusercontent.com/23094588/148694467-01d08d61-d284-4f68-b3ae-b3a53d2f79c2.png)

![image](https://user-images.githubusercontent.com/23094588/148694475-10b2fdf1-31af-43e8-9297-4ad72c57920b.png)

Si agregamos un héroe más en el **`array`** no es necesario modificar nada en el template HTML:

![image](https://user-images.githubusercontent.com/23094588/148694517-ed09e80f-caeb-4837-a15c-e8a17a53bee6.png)

![image](https://user-images.githubusercontent.com/23094588/148694525-6130987f-14e1-4b69-b60f-092d3ab7cb48.png)

Incluso podríamos númerar los datos usando el **`index`** del **`*ngFor`** como sigue:

![image](https://user-images.githubusercontent.com/23094588/148694617-36f3e52c-e8c9-4162-be24-b398e0a40490.png)

![image](https://user-images.githubusercontent.com/23094588/148694622-3da604b0-7bf0-4eb7-b195-bfba9bcdd292.png)

Si quisieramos que la lista empezara en uno lo ponemos así:

![image](https://user-images.githubusercontent.com/23094588/148694661-406a3d7b-d85a-4a2a-8d83-ec8ff15eece2.png)

![image](https://user-images.githubusercontent.com/23094588/148694666-eab39367-ef75-4d27-96f3-3ed67c1611c9.png)

### Tarea Borrar un Héroe

Vamos a colocar un botón después del listado que diga **`Borrar Héroe`** y al pulsarlo debe eliminar un héroe del listado.

![image](https://user-images.githubusercontent.com/23094588/148695007-e3539554-1ec8-4303-9e8c-faccc94825cf.png)

![image](https://user-images.githubusercontent.com/23094588/148695023-705fd74e-18c3-42a4-afec-c09b3f15f5a7.png)

![image](https://user-images.githubusercontent.com/23094588/148695029-3e3b1598-1695-4069-830d-05ef658d6d09.png)

![image](https://user-images.githubusercontent.com/23094588/148695034-52aaf9ed-c247-4f2c-9fc1-acf934e84ae4.png)

![image](https://user-images.githubusercontent.com/23094588/148695038-d0de244b-06c8-4512-b3f3-b5a5dfaf76ab.png)

![image](https://user-images.githubusercontent.com/23094588/148695044-b0707dca-649d-483e-8888-60c14583e20a.png)

![image](https://user-images.githubusercontent.com/23094588/148695049-0121d4f8-58d7-4e8f-abb8-9cfc9c99b77f.png)

Con el método **`pop()`** se va eliminando el último elementoo del **`array`**, al hacerlo sucesivamente vamos borrando todos los elmementos del array pero el botón persiste aun ya no haya ningún héroe.

Con el método **`shift()`** se va eliminando el primer elemento del **`array`**.

Tanto el método **`pop()`** como  **`shift()`** devuelven el héroe que se elimino, (devuelve **`string`** o **`undefined`**) por lo que vamos a hacer una mejora a nuestro código cada que pulsemos el botón **`Borrar Héroe`** vamos a pintar el nombre del héroe que estemos borrando, para este ejercicio usemos el método **`shift()`**.


Hemos visto que el método **`shift()`** devuelve **`string`** o **`undefined`** y si lo ponemos simplemente así nos muestra un error: 

![image](https://user-images.githubusercontent.com/23094588/148695567-c940a7cf-dcba-4b05-af84-16dbc099f186.png)

por lo que hay dos posibles soluciones que podemos tener:

![image](https://user-images.githubusercontent.com/23094588/148695591-d911ad04-3fd4-41cd-b361-a2e8c4b52324.png)

O la que vamos a usar:

![image](https://user-images.githubusercontent.com/23094588/148695611-a36598a2-bb51-4f94-9d4d-8357e29c25af.png)

En caso de que no elimine ningún héroe retorna un espacio en blanco.

![image](https://user-images.githubusercontent.com/23094588/148695639-09f3347b-b46e-468b-93ff-f718b33d6661.png)

![image](https://user-images.githubusercontent.com/23094588/148695646-7d9a525a-c7ff-4d98-926d-cc6d5d29939f.png)

![image](https://user-images.githubusercontent.com/23094588/148695649-5fe1a587-67b9-475c-a75c-c76a79047141.png)

![image](https://user-images.githubusercontent.com/23094588/148695653-ea26c24d-066e-44d0-b975-5732ae3d3ddf.png)

![image](https://user-images.githubusercontent.com/23094588/148695657-d3b766b6-c058-406e-b949-17243f84f138.png)

![image](https://user-images.githubusercontent.com/23094588/148695662-b2d2161a-b617-4888-b174-0a133c336184.png)

![image](https://user-images.githubusercontent.com/23094588/148695671-3b0bc438-9e40-4266-9d96-06039fac60d8.png)

Como vemos al eliminar un elemento de la lista el botón se desplaza vamos a hacer un pequeño cambio en el código como sigue:

![image](https://user-images.githubusercontent.com/23094588/148695807-e4476467-60e3-4fb6-b852-cd9b9897f1b5.png)

![image](https://user-images.githubusercontent.com/23094588/148695859-5589cbd1-c0c7-4225-b65d-1910a4bb5293.png)

![image](https://user-images.githubusercontent.com/23094588/148695876-b075d303-1089-4eab-aa79-8b6f1b683227.png)

![image](https://user-images.githubusercontent.com/23094588/148695884-fe4f9c75-1b6d-48d6-a63b-c0e45fb6f55e.png)

![image](https://user-images.githubusercontent.com/23094588/148695887-311b19ab-192d-4f35-98ef-56954bfaba8d.png)

![image](https://user-images.githubusercontent.com/23094588/148695892-86835798-3c6d-460c-b24e-e8302591e3b5.png)

![image](https://user-images.githubusercontent.com/23094588/148695900-d173036c-5f17-445b-92f4-fca09c0e3df5.png)

![image](https://user-images.githubusercontent.com/23094588/148695906-6322a731-8651-4a0e-af6c-4b5a0795fb8d.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/148695932-bf3eeb4e-2907-4974-8690-978ba7ef94a6.png)


## Directiva `*ngIf` 04:51

En esta lección vamos a ver otra directiva que nos va a ayudar a ser selectivos con lo que se muestra en el navegador y con lo que no queremos que se muestre. En nuestra aplicación actual siempre mostramos el texto **`Heroe Borrado`** y realmente esto solo se debería ver una vez que eliminamos a un Héroe, sino lo presionamos el botón no debería mostrar el texto. 

![image](https://user-images.githubusercontent.com/23094588/148799176-22b8edf7-9b37-45c8-8cfd-92a9c22f2474.png)

A la directiva **`*ngIf`** se le asigna una expresión booleana y si esta expresión es **`true`** se mostrará toda la etiqueta donde hayamos colocado la  directiva **`*ngIf`** si la expresión es **`false`** no se mostrará.

Aquí la cuestión es saber cuando un Héroe se borra y esto pasa cuando **`this.heroeBorrado`** es diferente de **`''`** de una cadena vacía y a que cuando borramos el Héreo recuperamos un nombre a menos que no se haya borrado ningún heroe.

El código nos queda así:

![image](https://user-images.githubusercontent.com/23094588/148800673-1188efc4-1fb0-40b8-b99a-c883cf1553d7.png)

Al recargar el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/148801062-83f0a063-3cfe-41d2-a12c-d5147446ee3d.png)

![image](https://user-images.githubusercontent.com/23094588/148801098-d548a42a-a10f-4d43-aaac-bf08b31662dd.png)

![image](https://user-images.githubusercontent.com/23094588/148801116-e5c169fa-bcda-4213-a098-7e64c723c2d9.png)

![image](https://user-images.githubusercontent.com/23094588/148801134-bd2f7afc-bcbb-47f4-9273-57516acaed8a.png)

![image](https://user-images.githubusercontent.com/23094588/148801159-11d668a6-78ee-47b8-a0fa-d9f59ce9f72e.png)

![image](https://user-images.githubusercontent.com/23094588/148801207-8a8b0df9-3755-4958-a366-8cd6c8d8ad5b.png)

Una alternativa interesante es colocor simplemente el código así:

![image](https://user-images.githubusercontent.com/23094588/148801376-2072038f-aa87-41df-8c77-58a6f5e1dff7.png)

El resultado es exactamente el mismo. 

¿Pór qué esto funciona?

Esto funciona por que el **`*ngIf`** es lo suficientemente inteligente para analizar que un **`string`** vacío **`''`** o un **`false`** o un **`null`** o un **`undefined`** representan falta de valor y representan un valor **`false`**.

![image](https://user-images.githubusercontent.com/23094588/148802260-0e13d78f-0689-4bd5-b47f-37c2f6c7b561.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/148802417-a153da9f-7b04-4b15-9aee-9b32105e876b.png)


## `ng-Template` y el `ngIf-else` 04:32

Con la directiva **`*ngIf`** ya vimos que pinta algo cuando la condición es **`true`**, pero también podemos hacer que se pinte algo cuando es **`falso`**, por ejemplo veamos el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/148804112-c8ebd4c7-b9b1-44ff-a89f-d77a6ba3dd70.png)

![image](https://user-images.githubusercontent.com/23094588/148804147-74c0ffb2-8f44-41f8-ad75-c52eddbb1da2.png)

![image](https://user-images.githubusercontent.com/23094588/148804171-6bf8f771-87b3-449f-881f-98a95bf41136.png)

![image](https://user-images.githubusercontent.com/23094588/148804194-467c7773-564d-443f-ae33-811ae369ff64.png)

![image](https://user-images.githubusercontent.com/23094588/148804224-9f53cc61-e7d0-492a-8252-99bf32d7043f.png)

![image](https://user-images.githubusercontent.com/23094588/148804251-974c7b70-ca9e-4457-9a01-04f7e755bf91.png)

![image](https://user-images.githubusercontent.com/23094588/148804294-e08a0d00-34b4-4b2f-b9a5-c5ac96cdd3dd.png)

![image](https://user-images.githubusercontent.com/23094588/148804312-4567a220-332c-4839-bbca-f95537f05dfe.png)

Dependiendo el caso se pinta uno u otro bloque usando la directiva **`*ngIf`**.

Estamos usando una especie de **"else"** usando dos **`*ngIf`** pero existe otra alternativa para cuando tenemos dos casos.

![image](https://user-images.githubusercontent.com/23094588/148806175-fdeaeced-2ef8-47f0-b851-7b3966356fa6.png)

Esmos usando una combinación de un **`else`** una **etiqueta** y un **`*ng-template`**, la **etiqueta** la ponemos en caso de un  **`else`** y en el **`*ng-template`** esta el código que se va a ejecutar en dicho caso.

Los resultados son los mismos:

![image](https://user-images.githubusercontent.com/23094588/148804147-74c0ffb2-8f44-41f8-ad75-c52eddbb1da2.png)

![image](https://user-images.githubusercontent.com/23094588/148804171-6bf8f771-87b3-449f-881f-98a95bf41136.png)

![image](https://user-images.githubusercontent.com/23094588/148804194-467c7773-564d-443f-ae33-811ae369ff64.png)

![image](https://user-images.githubusercontent.com/23094588/148804224-9f53cc61-e7d0-492a-8252-99bf32d7043f.png)

![image](https://user-images.githubusercontent.com/23094588/148804251-974c7b70-ca9e-4457-9a01-04f7e755bf91.png)

![image](https://user-images.githubusercontent.com/23094588/148804294-e08a0d00-34b4-4b2f-b9a5-c5ac96cdd3dd.png)

![image](https://user-images.githubusercontent.com/23094588/148804312-4567a220-332c-4839-bbca-f95537f05dfe.png)

Si vemos la pestaña **Elements** vemos como lo maneja Angular por atrás:

![image](https://user-images.githubusercontent.com/23094588/148808146-88a7436a-bc3d-4d8f-b2d9-5baa2e969c3b.png)

Si borramos cambia el contenido:

![image](https://user-images.githubusercontent.com/23094588/148808223-eaeb5a3e-3e42-40c0-80ac-3c824ebd4a45.png)

![image](https://user-images.githubusercontent.com/23094588/148808264-16102540-cb7a-4257-8e40-0cf2af04798f.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/148808409-c237f6e9-b259-4395-b37a-f7813d474a79.png)


## Módulos 10:09

Actualmente en nuestra aplicación tenemos un solo módulo el cual se encuentra en el archivo **`app.module.ts`** 

![image](https://user-images.githubusercontent.com/23094588/148809335-10f6f855-7104-4b06-8ec1-83473443eb4d.png)

Generalment en este archivo se modifican las secciones **`declarations`** donde se van añadiendo los componente nuevos que vamos creando, si tenemos 100 componentes tendremos que insertar los 100 componentes,  la seccion **`imports`** ya veremos para que sirve, la seccion **`bootstrap`** indica el componente inicial que generalmente no se modifica, la seccion **`providers`** nos va a servir para insertar los servicios de la aplicación.


Este módulo se carga en el archivo **`main.ts`**.

![image](https://user-images.githubusercontent.com/23094588/148809393-fa3b1341-ccb8-42e0-aaa1-62d192dc6a3b.png)

**El objetivo de los Módulos es ayudarnos a agrupar componentes y piezas  de nuestra aplicación  que tienen sentido entre sí. Otro de los objevos de los módulos es Encapsular las cosas, y otro muy importante es ayudarnos con la CARGA PEREZOSA (Lazy load)**. 


### CARGA PEREZOSA o Lazy load

Imaginemos que tenemos un módulo de Productos pero el usuario jamas entra a dicho módulo, entonces no deberíamos cargar toda la información de los componentes y demás referente al módulo de Productos si no lo vamos a usar, es justo lo que hace la **CARGA PEREZOSA** cargarlos bajo demanda.

La idea es que creemos un módulo referente a todo lo relacionado a HEROES por eso lo creamos de esta manera:

![image](https://user-images.githubusercontent.com/23094588/149730734-a00c8256-6a7e-4ffe-a8e7-9447ec43f3aa.png)

En HEROES estamos agrupando un HEROE en particular además de un LISTADO DE HEROES.

Para crear un nuevo modulo referente a los HEROES dentro de la carpeta **`heroes`** vamos a crear el archivo **`heroes.module.ts`**

![image](https://user-images.githubusercontent.com/23094588/149731126-cce6ca66-eb7c-4dfd-b18a-96a70fa2873f.png)

Vamos a meter todo su código manualmente:

```ts
import { CommonModule } from '@angular/common';
import { NgModule } from '@angular/core';
import { HeroeComponent } from './heroe/heroe.component';
import { ListadoComponent } from './listado/listado.component';

@NgModule({
  declarations: [
    HeroeComponent,
    ListadoComponent
  ],
  exports: [
    ListadoComponent
  ],
  imports: [
    CommonModule
  ]
})
export class HeroesModule {}
```

* Un módulo es una clase común y corriente que como la vamos a usar en otros lados le indicamos que la vamos a exportar con **`export`**.
* Un módulo tiene el decorador **`@NgModule`**.
* Dentro de **`declarations`** vamos a definir los dos componentes que tenemos en HEROES.
* Otra cosa importante es indicar las cosas que quiero que sean visibles fuera de este módulo es decir que cosas quiero hacer públicas y esto lo hacemos en la sección **`exports`** en este caso es el **`ListadoComponent`** que es lo que estamos usando en el archivo **`app.component.html`** (**`<app-listado></app-listado>`**).
* Otra sección que podemos crear son los **`imports`** que es donde se definen módulos que se vayan a ocupar en este caso vamos a ocupar el **`CommonModule`** que ya veremos para que sirve.

Ya que tenemos definido el **`heroes.module.ts`** podemos cerrarlo y abrir el archivo **`app.module.ts`** que es el modulo principal y donde vamos a añadir el modulo creado. Pero lo primero que vamos a hacer es que vamos a eliminar los dos componentes de Heroes que tenemos importados dentro de **`app.module.ts`** y lo que tenemos definido en **`declarations`**

![image](https://user-images.githubusercontent.com/23094588/149733717-33ac7bb5-d9a4-463b-b3f5-56601237eec5.png)

![image](https://user-images.githubusercontent.com/23094588/149733889-f5844482-dd39-4676-b267-dc9d6485ed8b.png)

Si grabamos los cambios en la consola y en el navegador nos muestra error:

![image](https://user-images.githubusercontent.com/23094588/149733995-afc9618e-6f5f-46e9-b6de-82e32939a968.png)

![image](https://user-images.githubusercontent.com/23094588/149734053-d7970183-106b-4878-ba1f-a915d50d1d07.png)

![image](https://user-images.githubusercontent.com/23094588/149734135-eba0fabe-893e-4919-9022-1e9dae81411d.png)

Esto esta pasando por que en **`app.component.html`**  estoy usando **`<app-listado></app-listado>`** y como lo he quitado ya no va la aplicación.

![image](https://user-images.githubusercontent.com/23094588/149734289-fd3c5442-4160-4b14-9365-28e4e6222639.png)

El componente **`ListadoComponent`** este definido en el nuevo módulo **`heroes.module.ts`**, entonces lo que nos esta faltando es indicar que se debe usar este nuevo módulo, esto lo vamos a hacer en los **`imports`** dentro de **`app.module.ts`**

![image](https://user-images.githubusercontent.com/23094588/149734886-b2c44637-c5d6-43a5-947f-c413a00b949f.png)

El error desaparece en **`app.component.html`**.

![image](https://user-images.githubusercontent.com/23094588/149734993-2c5fa22c-6709-4128-903c-1bf1052ef82d.png)

Y la aplicación nuevamente funciona.

![image](https://user-images.githubusercontent.com/23094588/149735220-fb26c5bd-af6a-4b3a-8720-0f12dffb0d39.png)

La ventaja es que ya tenemos un módulo independiente **`HeroesModule`** donde vamos a tratar todo sobre los héroes, de esta manera ya no tendríamos que modificar para nada el **`app.module.ts`**, cuando hagamos modificaciones sobre los HEROES se hara en **`heroes.module.ts`** dentro de la carpeta **`heroes`**.

### GIT

![image](https://user-images.githubusercontent.com/23094588/149737090-c8f82822-fcf8-45ea-b132-07d33055ce95.png)


## Módulos - segunda parte 08:16

Los módulos es un tema avanzado, lo estamos viendo muy pronto en este curso ya que tienen mucha importancia ya que si la aplicación va a creecer mucho siempre es importante tenerla modularizada, de esta manera también podemos usar estos módulos en otra aplicación diferente, existen muchas razones por las que trabajar en módulos es muy buena idea.

Recordemos que en la lección anterior en el archivo **`heroes.module.ts`** incluimos la el módulo **`CommonModule`**:

![image](https://user-images.githubusercontent.com/23094588/149793956-f1f54b54-2ee6-4859-98f6-416f122b1cfb.png)

vamos a comentarla para ver que pasa:

![image](https://user-images.githubusercontent.com/23094588/149794056-2f2a2bb4-6117-4cf5-b1c4-c136bce871bd.png)

al comentar esta línea es como si este módulo no existiera, si vamos al navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/149794550-2745d57a-5f9c-47e4-9f11-6e0bd1157832.png)

Nos esta dando errores en las directivas del archivo  **`listado.component.html`**:

![image](https://user-images.githubusercontent.com/23094588/149794818-1fb8c3fa-2cb1-47ea-89ed-f9e1cd8b2f8d.png)

Aunque si entramos en el archivo no nos indica nada (al profe si).

**Siempre que usemos directivas debemos importar el `CommonModule` que ofrece las directivas entre otras cosas** 

En el archivo **`heroe.component.html`** no usamos ninguna directiva por lo tanto en este archivo no deberíamos tener ningún fallo si no hemos incluido el módulo **`CommonModule`** 

![image](https://user-images.githubusercontent.com/23094588/150190281-a4e0d027-1025-4545-864a-6bf240ecf3f0.png)

Vamos a descomentar el **`CommonModule`** para que la aplicación no nos marque errores.

### Crear módulo Contador

Actualmente tenemos el componente Contador como sigue:

![image](https://user-images.githubusercontent.com/23094588/150190957-e8274cc1-30b5-4e76-b158-82dc38365c63.png)

Vamos a cambiarlo para que nos quede de la siguiente forma:

![image](https://user-images.githubusercontent.com/23094588/150191187-e3a47fbf-bad8-4c75-94a4-94e9ddf99ac7.png)

Creamos una carpeta adicional **`contador`** y dentro metimos el archivo **`contador.component.ts`**, esto implica una modificación en el archivo **`app.module.ts`** para indicar la nueva ubicación del componente:

![image](https://user-images.githubusercontent.com/23094588/150191519-2221190c-a976-487f-b154-28af3c95450a.png)

Para usar este componente Contador en lugar del del Héroe vamos a cambiar el archivo **`app.component.html`** 

![image](https://user-images.githubusercontent.com/23094588/150192358-e34722f4-d533-40f7-ba97-bf98fc38a5ba.png)

Por

![image](https://user-images.githubusercontent.com/23094588/150192427-2d9ab060-19c2-4ec5-b8f9-291f0dd04d87.png)

![image](https://user-images.githubusercontent.com/23094588/150192480-80eb0e74-e6e6-4cdb-9e02-da2b37e329ee.png)

Recordemos que en el archivo **`contador.component.ts`** tenemos integrada la plantilla.

![image](https://user-images.githubusercontent.com/23094588/150192631-5f686e0b-86b2-4ae5-a39c-acd433524361.png)

### Tarea Crear Módulo Contador

Esta tarea consta en modificar el archivo **`app.module.ts`** para que no haga referencia al componente **`contador.component`** sino más bien haga referencia a un **`contador.module`** que debemos crear para que la aplicación siga funcionando pero usando un modulo para Contador.


Lo primero que vamos a hacer es crear el archivo **`contador.module.ts`** en la siguiente ubicación

![image](https://user-images.githubusercontent.com/23094588/150198123-85e3b642-e82a-46ec-aec9-cac5badf8820.png)

con el siguiente contenido:

![image](https://user-images.githubusercontent.com/23094588/150197826-25457ed4-085d-4fcf-872a-565aa2ab6b3c.png)

Obsérvese que como en el HTML no usamos directivas no es necesario incluir el **`CommonModule`**.

Ahora vamos a cambiar el archivo **`app.module.ts`** que actualmente lo tenemos así:

![image](https://user-images.githubusercontent.com/23094588/150193537-07c8af18-1b2f-4001-8ba7-c91fcc22155d.png)

Por

![image](https://user-images.githubusercontent.com/23094588/150198304-a5629d34-a1e3-4e68-990e-3eb2dd00e118.png)

La aplicación sigue trabajando perfectamente

![image](https://user-images.githubusercontent.com/23094588/150198427-159a0a58-d02b-45a5-9d48-aec1cea4e7b6.png)

![image](https://user-images.githubusercontent.com/23094588/150198460-581f3e11-9bde-4a3b-b97a-00e16a97a732.png)

Pero ya tenemos una aplicación totalmente **MODULARIZADA**.

### GIT

![image](https://user-images.githubusercontent.com/23094588/150198748-72049b2d-61d5-451c-8833-011151313b6f.png)

## Bonus: Hacer respaldo de nuestro proyecto en GitHub 07:35

En esta lección vamos a subir nuestro proyecto a **GitHub** mediante comandos **Git** por lo que por una parte debemos haber instalado **Git** en nuestro ordenador por un lado y contar con una cuenta de **GitHub** por otro lado.

Hasta el momento hemos ido subiendo a **Git** nuestro código al final de cada lección en un ***repositorio local***, lo que vamos a hacer ahora es subir nuestro código a un ***repositorio remoto*** ubicado en **GitHub**, por lo que tenemos que preparar el espacio en **GitHub** para poder hacerlo.

Accedemos en el navegar a nuestra cuenta de **GitHub**.

![image](https://user-images.githubusercontent.com/23094588/150813214-e0787557-3366-45c1-89eb-058ecdd79892.png)

Y vamos a entrar donde dice **Repositories**

![image](https://user-images.githubusercontent.com/23094588/150813337-32b9cf82-2fad-4b91-8e9d-b6e660a59b79.png)

Vemos un botón verde con la palabra **`New`** que vamos a presionar.

![image](https://user-images.githubusercontent.com/23094588/150813512-d2af28d3-d41f-4c02-9f64-a9979beb5e91.png)

Nos pide un nombre vamos a ponerle el mismo que tiene nuestro proyecto **`125-01-bases`**

Nos pide una descripción donde vamos a poner ****`Primer proyecto Angular del curso 125-Angular-de-Cero-a-Experto-2021`****

Dejamos la opción **`Public`** para que cualquier persona lo pueda ver y damos en el botón **`Create repository`**.

![image](https://user-images.githubusercontent.com/23094588/150814376-4e3686fc-b4a1-41d3-9275-ec6e1bfcf7db.png)

Casi de inmediato nos presenta la siguiente pantalla:

![image](https://user-images.githubusercontent.com/23094588/150814539-0bf49430-690c-4a12-9ebf-702f426636ca.png)

La cual contiene el URL:

```sh
https://github.com/adolfodelarosades/125-01-bases.git
```

Y también tiene una serie de opciones con diferentes comandos **Git** que podemos utilizar.

El primer grupo de comandos incluye algunos comandos para inicializar **Git** en nuestro proyeyecto, pero con la versión actual de Angular ya inicializa **Git** al crear un proyecto. Después estan los comandos para realizar los comados de **`commit`** en nuestro proyecto, cosa que hemos estado haciendo a lo largo de cada fin de lección de este módulo. Enseguida hay un comando para renombrar nuestra rama **`master`** por **`main`**, despúes tenemos el comando **`git remote add origin https://github.com/adolfodelarosades/125-01-bases.git`** que nos va a permitir enlazar el proyecto local con el repositorio remoto y finalmente el comando para hacer un **`push`** del contenedor local al remoto.

```sh
…or create a new repository on the command line
echo "# 125-01-bases" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/adolfodelarosades/125-01-bases.git
git push -u origin main
```

En este segúndo grupo tenemos solo los comandos necesarios para subir nuestro coódigo al repositorio remoto.

```sh
…or push an existing repository from the command line
git remote add origin https://github.com/adolfodelarosades/125-01-bases.git
git branch -M main
git push -u origin main
```

Esta ultima opción nos dice muy claramente lo que hace.

```sh
…or import code from another repository
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.
```

En este caso vamos a ejecutar los comandos del segundo grupo en nuestra consola, los poodemos compiar y ejecutar.

![image](https://user-images.githubusercontent.com/23094588/150817599-372c766d-0068-47fe-b07b-bf83e2d389c7.png)

Si es la primera vez que se ejecuta pide usuario y contraseña de **`GitHub`**, este procedimiento sube el código al repositorio remoto, si retornamos a **`GitHub`** en el navegador y lo refrescamos vamos a tener lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/150818132-21276ef7-788e-46a6-8e7e-45bea391a479.png)

Ya tenemos todo nuestro código en el repositorio de **`GitHub`**.

Es importante notar que la carpeta **`node_modules`** no se sube al repositorio, entre otras cosas, gracias a lo que tenemos incluido en el archivo **`.gitignore`** del proyecto.

![image](https://user-images.githubusercontent.com/23094588/150824068-1b37f288-448e-4161-becc-e174e9742b1a.png)

La carpeta **`node_modules`** es importante para nuestro proyecto pero ocupa mucho espacio para subirlo al repositorio y lo podemos recuperar gracias a lo que tenemos en el archivo **`package.json`**.

![image](https://user-images.githubusercontent.com/23094588/150824767-d0bc9cf0-996e-47fc-9dc4-9535584a7bbb.png)

Si nosotros tenemos la necesidad de pasar este proyecto a alguien más lo descargamos del repositorio y simplemente ejecutamos el comando 

```sh
npm install
```

para que reconstruya todos los módulos de Node, ya lo veremos al final de esta sección.

### Creación de un Tag y Release

Adicionalmente vamos a crear un **Release Tag** que nos permite tener una versión del código que esta en este momento y poder descargarlo. El comando **Git** que vamos a usar es:

```sh
git tag -a v0.1.0 -m "Fin sección 4"
```

Este comando crea un **Tag** el atributo **`-a`** significa que es "anotado" con el texto **`v0.1.0`** que es una forma de nombrar nuestras versiones y con **`-m`** le damos el título de **`Fin sección 4`**

Si después de pulsar el comando anterior pulsamos:

```sh
git tag
```

vamos a tener:

![image](https://user-images.githubusercontent.com/23094588/150819762-52dd80d3-103f-4a6c-acd6-b957151daf2d.png)

Si retornamos al navegar en **GitHub** no vamos a ver ninguna diferencia.

![image](https://user-images.githubusercontent.com/23094588/150819991-b9097fc0-4703-4f03-9d0f-dbb605e85939.png)

Para subir el  **Tag** a **GitHub** lo hacemos con el comando:

```sh
git push --tags
```

![image](https://user-images.githubusercontent.com/23094588/150820305-d3179530-a3da-4088-8bcd-70f1c2966691.png)

Esto simplemente nos sube un **Tag** a **GitHub** no un **Release Tag**.

![image](https://user-images.githubusercontent.com/23094588/150820569-0647ad60-1450-4d49-aba5-0bcffaed259d.png)

Ya podemos ver que nos sale 1 tag si pulsamos en **Releases** vemos los detalles:

![image](https://user-images.githubusercontent.com/23094588/150820905-e3fe364e-cb22-4304-9c5e-b83bd43eeab5.png)

Como podemos ver en **Releases** no tenemos nada y en **Tags** tenemos:

![image](https://user-images.githubusercontent.com/23094588/150821099-2d66a7d9-2b09-4273-a6e6-e02249edf60c.png)

Si pulsamos en el **Tag v0.1.0**  nos lleva a los detalles:

![image](https://user-images.githubusercontent.com/23094588/150821401-efe6c50f-b486-462c-98ce-c2377e3dd5aa.png)

En esta pantalla podemos crear un **Release** a partir de un **Tag** pulsando en el botón **`Create release from tag`**.

![image](https://user-images.githubusercontent.com/23094588/150821786-643962bc-d936-460e-b945-85a41e7399b0.png)

Metemos la información que nos solicita:

![image](https://user-images.githubusercontent.com/23094588/150822068-b4dc1283-3551-4c7b-9983-3ada65d603d9.png)

Y podemos pulsar en el botón verde **`Public release`**

![image](https://user-images.githubusercontent.com/23094588/150822341-0f082087-1c4d-4810-9f03-e208633e88eb.png)

Ahora si ya tenemos un **Release**

Como podemos ver en el **Release** tenemos la sección **Assets** donde podemos descargar el código fuente, vamos a pulsar en **`Source code (zip)`** el código se descarga:

![image](https://user-images.githubusercontent.com/23094588/150823290-1b0711c0-c86a-4a69-8639-4b5c33da1ad0.png)

![image](https://user-images.githubusercontent.com/23094588/150823386-ef432452-2ada-4d79-bb9b-efbc0f5bb98a.png)


### Usar el proyecto Descargado

Vamos a copiar el ZIP descargado dentro de nuestra carpeta de Proyectos Angular y lo descomprimimos.

![image](https://user-images.githubusercontent.com/23094588/150835726-834f4a60-b282-4126-a275-ad60f77c01cd.png)

Observamos que al contrario de nuestro proyecto orignal este no tiene el **`node_modules`**.

![image](https://user-images.githubusercontent.com/23094588/150836031-b7e6fe95-de6b-4520-90d6-a64941f83eea.png)

En la consola vamosa meternos a la carpeta del proyecto descargado y para reconstruir los modulos de Node bastaría pulsar el comando:

```sh
npm install
```

![image](https://user-images.githubusercontent.com/23094588/150836447-2ecdbd08-df81-499d-b3c9-45347667a60f.png)

![image](https://user-images.githubusercontent.com/23094588/150838107-31ffd910-65e8-40ee-9a56-ada902f44726.png)

Si listamos los archivos en la carpeta veremos que ya aparece el **`node_modules`**.

![image](https://user-images.githubusercontent.com/23094588/150838560-34dd92cb-d961-4779-b3fb-1cf5fcb9e1c5.png)

Vamos a levantar el servidor con:


```sh
ng serve -o
```

Como ya tenia el puerto **4200** ocupado me pregunta si quiero abrir la APP en un puerto diferente, respondo **Y** y carga la aplicación en un nuevo puerto.

`http://localhost:64904/`

![image](https://user-images.githubusercontent.com/23094588/150839565-bb5e444b-428e-4f85-add7-db5db7ca8790.png)

La aplicación funciona con lo último que subimos al repositorio.

![image](https://user-images.githubusercontent.com/23094588/150839913-8fc60f19-577c-4764-84ea-3f0122a201b4.png)


Con esto hemos demostrado como descargar una APP del repositorio, la hemos generado o instalado y finalmente la hemos arrancado.


## Código fuente de la sección 00:17

https://github.com/adolfodelarosades/125-01-bases/releases/tag/v0.1.0
