# 03 Aplicación #1 Hola Mundo - 14 clases • 1h 26m

* Introducción a la sección 00:43
* ¿Qué aprenderemos en esta sección? 00:21
* Demostración de lo que lograremos en esta sección 01:05
* Introducción a los componentes y directivas estructurales. 03:25
* Nuestra primera interacción en Angular 08:39
* Nota de Actualización del AngularCLI 01:49
* Creando un entorno local de Angular 11:02
* Estructura del proyecto 13:12
* Utilizando Bootstrap 4 10:03
* TemplateUrl: Separando el HTML el componente 09:32
* Creando el **`footer.component`** 10:32
* Estructura del body component 04:56
* Directivas estructurales: **`*ngFor`** y el **`*ngIf`** 10:01
* Examen teórico - de la sección Hola Mundo - 10 preguntas
* Código fuente de la sección 00:23

## Introducción a la sección 00:43

En esta lección vamos vamos a ver muchas cosas interesantes entre las cuales ***los componentes, directivas estructurales, ngIf, ngFor, vamos a poder construir una aplicación***. 

Vamos a ver muchas cosas interesantes así que espero que estén emocionados y ahora si vamos a comenzar con Angula.

## ¿Qué aprenderemos en esta sección? 00:21

Este es un breve resumen de todo lo que veremos a continuación:

1. ¿Qué son los componentes?
2. ¿Qué son las directivas estructurales?
3. Uso de **plunker** para nuestra primera interacción con Angular.
4. Trabajando de forma local un proyecto en Angular.
5. Una breve introducción sobre todos los archivos usados en el QuickStart de Angular.
6. Uso de Bootstrap 4 para nuestros estilos.
7. Crear archivos **`.HTML`** para que se encarguen de la estructura visual de nuestros componentes.
8. Crearemos una aplicación con 3 componentes re-utilizables.
9. **`*ngFor`** y el **`*ngIf`**

Al finalizar tendremos un examen teórico para afianzar los conocimientos.

## Demostración de lo que lograremos en esta sección 01:05

![image](https://user-images.githubusercontent.com/23094588/132102418-19c39774-b49e-4c67-9a10-4b6231c183b0.png)

![image](https://user-images.githubusercontent.com/23094588/132102526-b116c462-0394-4f1e-832a-2d81f3c9c525.png)

![image](https://user-images.githubusercontent.com/23094588/132102484-b64e867c-33ec-4859-a70b-4b8327b8d1ed.png)

Esto es lo que lograremos al final de la sección, vamos a hablar sobre varios temas muy importantes que es bueno que toda aplicación de Angular tenga, como por ejemplo las directivas estructurales **`*ngFor`** y **`*ngIf`**, más adelante tocaremos otras pero estas son las dos con las cuales vamos a comenzar.

Vamos a hacer esta pequeña aplicación que escucha un evento clic del botón y muestra y oculta la información de los personajes que se encuentran en un arreglo y esto lo vamos a crear en base a la directiva estructural **`*ngFor`**.

Vamos a crearnos también nuestro componente personalizado del ***Header Component***, un ***Body Component*** donde tendremos todo lo que está corriendo de nuestra aplicación y también tendremos un ***Footer Component***.

## Introducción a los componentes y directivas estructurales. 03:25

![image](https://user-images.githubusercontent.com/23094588/132102724-2f7976ce-eea1-4bfc-8f4b-7335ba275341.png)

![image](https://user-images.githubusercontent.com/23094588/132102732-a7a173a9-660c-4d1e-97a3-aa2a4619fe6a.png)

![image](https://user-images.githubusercontent.com/23094588/132102780-9effe766-cb12-462b-bc0f-671dcc80fc84.png)

### Componentes

Cada uno de estos puede ser un componente:

* Menú de Navegación
* Barra Lateral
* Demás páginas y sub-páginas
* Pie de página

La idea es que cada uno de esos componentes debe responder unicamete por su tarea especifica.

![image](https://user-images.githubusercontent.com/23094588/132102840-00782f79-7b20-414c-b381-0e4e5d30dccc.png)

### Directivas Estructurales

![image](https://user-images.githubusercontent.com/23094588/132102900-58479130-647a-48c6-a626-2483523a337b.png)

Las dos Directivas Estructurales que comenzaremos a ver son

* **`*ngIf`**: Cuando su valor es **`true`** muestra el contenido asociado, pero si su valor es **`false`** el contenido asociado no se mostrará.
* **`*ngFor`**: Permite repetir una seríe de contenido asociado.


## Nuestra primera interacción en Angular 08:39

![image](https://user-images.githubusercontent.com/23094588/132103011-c762d56a-e03e-4857-a71c-1424d28a0e7f.png)

### Documentación Oficial

https://angular.io/

![image](https://user-images.githubusercontent.com/23094588/132103135-b715e404-d347-430a-8b9d-c695475fe88e.png)

Podemos buscar cualquier elemento deseado, se muestran una serie de iconos para identificar los diferentes tipos de elementos como ***clases, interfaces, constantes, paquetes, modulos, pipes, etc.***

Si buscamos uno en concreto, nos muestra su documentación.

![image](https://user-images.githubusercontent.com/23094588/132103201-da139dfa-5993-44b6-81e2-e4f5715f3290.png)

Tenemos la posibilidad de indicarle en que versión de Angular nos la muestre.

### Plunker

https://plnkr.co/

![image](https://user-images.githubusercontent.com/23094588/132103290-4a976fd2-ad56-4428-bd03-71cdfaddd0fc.png)

**Plunker** es una página Web donde podemos crear aplicaciones Angular para compartirlas con más gente, en este caso no estaríamos creando nuestra aplicación localmente, sino que la crearíamos en esta aplicación. Inclusive nosotros podemos ver las aplicaciones creadas por otros usuarios que pueden estar en Angular u otro tipo de lenguajes.

Podemos pulsar el botón ***New*** 

![image](https://user-images.githubusercontent.com/23094588/132103374-44c78a85-b22e-49a9-ae3a-f5b9dda7363f.png)

Nos pide que le indiquemos que tipo de aplicación vamos a crear, seleccionamos Angular y nos crea una aplicación inicial.

![image](https://user-images.githubusercontent.com/23094588/132103407-644d636f-8bed-4e01-9023-b3fc96c10947.png)

Que podemos ejecutar pulsando en el botón ***Preview***.

![image](https://user-images.githubusercontent.com/23094588/132103429-405791e5-f33a-4167-9e18-896f8475760b.png)

### StackBlitz

**StackBlitz** Es otra página Web donde podemos crear nuestras aplicaciones Angular.

![image](https://user-images.githubusercontent.com/23094588/132103466-a59f80e0-49b8-40b9-9396-ecdc54be04c9.png)

Al seleccionar Angular nos crea una aplicación inicial que ejecuta inmediatamente.

![image](https://user-images.githubusercontent.com/23094588/132103494-05156f5c-7516-41ac-9f81-a0373ebd0267.png)

Podemos movernos a la página **`index.html`** que es la primera página que Angular carga.

![image](https://user-images.githubusercontent.com/23094588/132103549-67638b29-2ccc-4fcf-b1b0-25daf98f8390.png)

El **`loading`** se debería ver en la ejecución de la aplicación, pero lo hace tan rápido que no se aprecia ya que continua la ejecución y carga todo lo que hay en **`my-app`**. Esto de **`my-app`** se refiere a **`app.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/132103627-5b35cf61-8116-4f9c-aba5-29e703675abf.png)

Podemos ver en el código **`selector: 'my-app',`** precisamente **`my-app`** es lo que tenemos en el **`index.html`**, lo que se le dice con la etiqueta **`<my-app>loading</my-app>`** es que renderice todo lo que se encuentre en la clase **`app.component.ts`**.

Como podemos ver el contenido de **`app.component.ts`** es una clase que podemos importar desde otro lugar y le estamos agregando un decorador **`@Component`** que transforma la clase expandiendo funcionalidades para que Angular sepa que es un coponente que se debe inyectar en el HTML cuyo código HTML a insertar se indicado en **`templateUrl: './app.component.html',`**, y con **`tyleUrls: [ './app.component.css' ]`** indicamos el estilo CSS que debe aplicarse a **`./app.component.html`**. La clase tiene la propiedad **`name = 'Angular ' + VERSION.major;`** si cambiamos su valor por **`name = 'World'`**, la ejecución de la APP se modifica.

![image](https://user-images.githubusercontent.com/23094588/132104138-cb1f03a8-615c-488a-b3b8-6c476917c0ee.png)

Pero donde se le esta diciéndo que ese **`World`** aparezca allí. Vamos al **`app.component.html`**.

![image](https://user-images.githubusercontent.com/23094588/132104166-407af318-fef0-40ef-af83-e5d89c205f91.png)

Al inició del código estamos interpolando la propiedad **`name`**.

Además tenemos el componente **`hello.component.html`**.

![image](https://user-images.githubusercontent.com/23094588/132104242-2e750e65-1572-4258-bd7b-7a6d66b29898.png)

Que es donde realmente se pinta el **`Hello World!`**.

Esta fue solo una pequeña forma de ver como ejecutar código desde aplicaciones Web existentes, nosotros trabajaremos de forma local.

## Nota de Actualización del AngularCLI 01:49

Esa es una pequeña nota de actualización, en la versión 7 de Angular se ha incluido una pequeña pregunta adicional cuando creamos una aplicación y me interesa que antes de que ustedes empiecen a crearlas mediante lo que se conoce como el **Angular CLI** en la próxima lección ustedes van a saber más sobre eso.

Voy a abrir la terminal y les voy a mostrar 

![image](https://user-images.githubusercontent.com/23094588/132104326-7874492c-cdf1-44ec-bc38-8922ebe8f267.png)

Nos realiza dos preguntas:

1. Si deseo integrar el ***routing*** le vamos a indicar que NO, esto lo veremos más adelante desde cero.
2. Luego me va a preguntar si yo deseo utilizar CSS, SCSS, SASS, LESS u otra librería para manejar los estilos, vamos a trabajar solo con CSS por lo que simplemente pulsamos enter para seleccionar la opción por default.

Después de esto empezara a crear toda la aplicación.

## Creando un entorno local de Angular 11:02

El equipo de Angular recomienda usar [**Angular CLI**](https://angular.io/guide/setup-local) para la creación de nuestra APP, **Angular CLI (Command Line Interface)** que es una ***Interfaz de Línea de Comandos*** que nos va a permitir crear cosas de forma automática y nos ahorra mucho tiempo. 

### Creación del Proyecto 

Para crear un nuevo proyecto se usa el comando:

![image](https://user-images.githubusercontent.com/23094588/132104533-42cb42b7-9ba2-4044-80ba-effc18d665e5.png)

Vamos a abrir la terminar y navegar a la carpeta donde vamos a tener todos nuestros proyectos de Angular.

![image](https://user-images.githubusercontent.com/23094588/132104567-a40cf1ce-d8ce-4a31-a632-e8d497e1edbf.png)

Después vamos a escribir el comando **`ng new my-app`** para crear la aplicación **`my-app`** ya le cambiaremos el nombre.

![image](https://user-images.githubusercontent.com/23094588/132104603-663d5f3e-df7a-4ed4-a882-7007e44edfbb.png)

![image](https://user-images.githubusercontent.com/23094588/132104622-986f3c58-312a-4703-a41e-db424d16fe3e.png)

![image](https://user-images.githubusercontent.com/23094588/132104626-6700add9-fc90-432e-bb12-57acf455949d.png)

Esto va a tomar cierto tiempo dependiendo de la conexión de Internet que tengamos.

![image](https://user-images.githubusercontent.com/23094588/132104807-8522081e-cf60-446d-b7d6-1698f4e037f0.png)

Ya nos crea el repositorio GIT.

Dentro dentro de nuestra carpeta **`PROYECTOS-ANGULAR`** vemos la carpeta **`my-app`** que contiene todo el proyecto Angular, la vamos a renombrar por **`01-Hola-Mundo`**.

![image](https://user-images.githubusercontent.com/23094588/132104831-720430c6-840f-4cef-92ff-ca2f39f07513.png)

![image](https://user-images.githubusercontent.com/23094588/132104873-b0f095d9-344b-4148-b626-ba4f4c9250e3.png)

Vamos a abrir nuestro proyecto **`01-Hola-Mundo`** dentro de VSC.

![image](https://user-images.githubusercontent.com/23094588/132104994-5f9d7ace-be40-4a08-9e9d-aa82a5b38af9.png)

### Ejecutar la APP 

En la terminal debemos estar dentro de la carpeta **`01-Hola-Mundo`**, y vamos a escribir el comando:

```sh
ng serve
```

Esto va a levantar un servidor local en el puerto **`4200`** por defecto, también podemos indicar otro puerto como por ejemplo:

```sh
ng serve -p 4201
```

Por si tenemos ocupado el puerto por default.

Podemos también pulsar:

```sh
ng serve -o
```

Y esto nos va  a abrir el navegador por defecto una vez se levante la aplicación. Vamos a pulsar esta última opción.





## Estructura del proyecto 13:12
## Utilizando Bootstrap 4 10:03
## TemplateUrl: Separando el HTML el componente 09:32
## Creando el **`footer.component`** 10:32
## Estructura del body component 04:56
## Directivas estructurales: **`*ngFor`** y el **`*ngIf`** 10:01
## Examen teórico - de la sección Hola Mundo - 10 preguntas
## Código fuente de la sección 00:23
