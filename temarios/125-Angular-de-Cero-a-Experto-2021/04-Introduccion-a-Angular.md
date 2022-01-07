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

![image](https://user-images.githubusercontent.com/23094588/148509332-0a477ea5-474a-4ecc-b338-de36fc922164.png)

![image](https://user-images.githubusercontent.com/23094588/148509495-6739eca7-9b52-4c1c-ad87-50b68253e5d2.png)

En el template HTML hemos puesto la expresión **`(click)="numero = numero + 1;"`** y podríamos pensear ponerla así **`(click)="numero += 1;"`** pero al hacerlo esto nos indica un fallo:

![image](https://user-images.githubusercontent.com/23094588/148510048-649c8ea9-9fdd-4f43-828d-dce6b4efb20a.png)

A pesar de que es una expresión habitual de JS al usarla en el template HTML, generalmente solo se va a poner código JS muy sensillo dentro del template HTML pero generalmente no lo debemos hacer, ya veremos otra alternativa que es mejor.

### GIT

![image](https://user-images.githubusercontent.com/23094588/148510317-fb2cb83a-c13e-4f39-8a99-9a8253afdfa2.png)

![image](https://user-images.githubusercontent.com/23094588/148510791-38923ea3-2e3a-47c6-a657-82ded0b6e75a.png)

![image](https://user-images.githubusercontent.com/23094588/148510661-68f4ea20-f8ea-4392-8823-9327a427b5e9.png)


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
