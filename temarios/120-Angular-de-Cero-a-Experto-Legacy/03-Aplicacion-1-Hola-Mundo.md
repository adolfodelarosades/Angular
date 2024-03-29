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

Y esto nos va  a abrir el navegador por defecto una vez se levante la aplicación en http://localhost:4200/. Vamos a pulsar esta última opción.

![image](https://user-images.githubusercontent.com/23094588/132140521-d9b63a63-c9b5-402a-b9cd-98f8be97b279.png)

Podemos abrir las **Herramientas de Desarrollo** para ver posibles errores mientras desarrollamos.

![image](https://user-images.githubusercontent.com/23094588/132140557-a93921da-4b7b-4403-bcff-e605256a4ff1.png)

### Modificar la Aplicación.

Vamos a ir al archivo **`app.component.html`** y vamos a borrar todo el contenido sustituyendolo por:

![image](https://user-images.githubusercontent.com/23094588/132140612-31a03414-14ac-4627-b958-6aee136ed3fd.png)

Y la APP cambia, gracias al **Live Server**:

![image](https://user-images.githubusercontent.com/23094588/132140623-83649680-5d64-4e26-b71d-3b6d3865f299.png)

Vamos a añadir más código, pero ahora en **`app.component.ts`** que actualmente se encuentra así:

![image](https://user-images.githubusercontent.com/23094588/132140702-f236fe24-75bf-4196-a623-36e1dde60386.png)

Vamos a cambiarla por:

![image](https://user-images.githubusercontent.com/23094588/132140724-7b38fa43-3160-408d-864d-ec0536a93b48.png)

Simplemente estamos colocando dos propiedades a la clase e inicializando su valor, no las hemos tipado ya que TS infiere el tipo de la propiedad.

Ahora en **`app.component.html`** vamos a poner lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/132140828-c9afce23-2fb4-49a4-be6f-5ac13d22c95c.png)

Estamos usando la **Interpolación** para mostrar los valores de la propiedad dentro del HTML. En una Interpolación podemos poner cualquier tipo de código de JS, funciones, operaciones, etc. y lo procesa Angular para que su valor aparezca renderizado en el Navegador.

La APP se actualiza para mostrar:

![image](https://user-images.githubusercontent.com/23094588/132140845-18fe1cc3-1707-4774-96c0-b216f8a82917.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/132140946-bfc458ab-e2f8-4403-9eca-ed60a06a8f66.png)

## Estructura del proyecto 13:12

![image](https://user-images.githubusercontent.com/23094588/132253372-94106dd1-ff0a-4465-9514-e2f4dc094eb7.png)

Video:

![image](https://user-images.githubusercontent.com/23094588/132253385-8f3c4135-d768-46fa-a21e-6f04cbb22f65.png)


En esta lección les voy a explicar cada uno de los archivos y directorios que se encuentran en un proyecto Angular.

Empecemos con la carpeta **`e2e`** que está destinada al manejo de las pruebas de extremo a extremo o ***end to end***. En este curso nosotros no vamos a trabajar con esta carpeta, no es necesaria para crear aplicaciones pero ya la configura de forma automática Angular CLI (Parece que en la versión 12 ya no lo hace).

Si quieres saber más al respecto existe un curso avanzado en el cual hacemos pruebas unitarias y de integración pero básicamente es para correr las pruebas automáticas.

Luego tenemos la carpeta de los módulos de Node **`node_modules`**, esa carpeta es bastante grande y contiene un montón de paquetes.

![image](https://user-images.githubusercontent.com/23094588/132253566-91bea6fc-f5d0-4bc7-83ed-6944fa3c2825.png)

Son más de mil paquetes que se instala Node.

Los módulos de Node en sí nos ayudan a varias cosas, como por ejemplo montar el **`Live Reload Server`**, estar escuchando los cambios en nuestra aplicación, los sockets por ejemplo, en fin muchas cosas que se instalan de forma automática pero únicamente con el fin de desarrollo, cuando ya generemos la aplicación de producción y ya la queremos subir a un servidor corremos un script
que únicamente deja en la aplicación lo básico que necesita para correr, eso por lo general la deja de menos de 500k pero depende de qué tanto código le metamos al programa. Esta carpeta de los módulos de node **`node_modules`**  no la debemos subir a un repositorio, no vamos a hacer un backup de esta carpeta. 

De hecho si ustedes quisieran podrían borrar la carpeta **`node_modules`**  del proyecto y cuando la transfieran o se la pasan a algún compañero simplemente él tendría que ejecutar el comando:

```sh
npm install
```

para recuperar esos módulos de Node y al ejecutar el comando se vuelve a crear la carpeta **`node_modules`** en base a lo que esta definido en el **`package.json`**.

En la carpeta **`src`** es donde esta nuestra aplicación de Angular.

![image](https://user-images.githubusercontent.com/23094588/132254456-62c99b47-1d95-448e-9e4e-a0b2c8ccf5c8.png)

Vamos a dejar la explicación de esta carpeta al final.


Existen varios archivos fuera de la carpeta **`src`**.

![image](https://user-images.githubusercontent.com/23094588/132254512-262ecc39-e8a8-43b6-b586-39dbdce6bc7e.png)

* **`.browserslistrc`**: El sistema de compilación utiliza este archivo para ajustar la salida de CSS y JS para admitir los navegadores especificados.

* **`.editorconfig`**: Son configuraciones del editor por lo regular no lo vamos a tocar.

![image](https://user-images.githubusercontent.com/23094588/132254885-593d8569-f10a-4ac6-9a9a-26fbc55f3a05.png)

* **`.gitignore`**: Archivo que nos sirve para indicar que archivos o directorio no van a subir al repositorio siendo ignoradas.

![image](https://user-images.githubusercontent.com/23094588/132254954-c0d67b0c-05ce-4432-9dff-0b7b17f3519a.png)

* **`angular.json`**; Este archivo sirve para indicar como es nuestra aplicación y como funciona, generalmente vamos a modificar en los **`assets, styles y scripts`**. Cuando hay más de un archivo de estilos los toma todos y los unifica en uno solo, lo mismo pasa con los scripts, los **`assets`** son archivos estáticos.

![image](https://user-images.githubusercontent.com/23094588/132255237-b55512fb-8b68-4642-82b1-fce41f343be1.png)

* **`karma.conf.js`**

![image](https://user-images.githubusercontent.com/23094588/132255272-38c9132a-d8c5-4d72-a08d-1598094b7a65.png)

* **`package-lock.json`**: Este archivo le dice a nuestra aplicación de Node como fue creado el archivo **`package.json`**, ***este archivo NO se toca manualmente***.

![image](https://user-images.githubusercontent.com/23094588/132255326-f2ed0b58-b734-4f00-ae48-c1993d3b8dbf.png)

* **`package.json`**: ***Este archivo es sumamente muy importante***, dependiendo de lo que vayamos instalando este archivo se va modificando, si vamos agregando dependencias aquí se van añadiendo,puede haber dependencias de producción o de desarrollo  

![image](https://user-images.githubusercontent.com/23094588/132255586-35d16b54-480c-40c7-83d2-7fff3a73dbd3.png)

Para comparar con lo que tengo instalado en mi MAC y ver la relación entre ellos.

![image](https://user-images.githubusercontent.com/23094588/132255733-50c54c4b-6214-4a33-a556-68578e4f3da3.png)

* **`README.md`**: Archivo que explica como funciona la aplicación muy util en GitHub.

![image](https://user-images.githubusercontent.com/23094588/132255948-879ec3de-f3c3-43f9-9af0-92659631bedc.png)

* **`tsconfig.app.json`**:

![image](https://user-images.githubusercontent.com/23094588/132256053-8fa3dfa9-48a5-4e48-a52b-cf643b8950dd.png)

* **`tsconfig.json`**: Nos ayuda para indicar en que estandar de JS vamos a trabajar.

![image](https://user-images.githubusercontent.com/23094588/132256085-f6671f15-b871-44b7-9081-5d2a960c03c8.png)

* **`tsconfig.spec.json`**:

![image](https://user-images.githubusercontent.com/23094588/132256107-879821b5-f456-4b26-8bcf-e08b2867ac03.png)

* **`tslint.json`**: Archivo que ayuda a escribir código TS según las reglas establecidas en el.

![image](https://user-images.githubusercontent.com/23094588/132256171-7ca834b4-8a9c-4e31-9ac3-0a2b6414a9cb.png)

### Carperta `src`

![image](https://user-images.githubusercontent.com/23094588/132953008-bd04d1f8-d498-419f-8162-915b4ecfbc67.png)

En la carpeta **`app`** tenemos nuestra primer aplicación de Angular.

![image](https://user-images.githubusercontent.com/23094588/132388025-c12def41-19a2-4682-b7f8-bd4a223d04c3.png)

* **`app`**: Contiene el componente principal el **`app.component`** que se descompone en los siguientes elementtos:
   * **`app.component.css`**: Estilos CSS que se aplican sobre nuestro **`app.component.html`**
   * **`app.component.html`**: Código HTML del componente.
   * **`app.component.spec.ts`**: Archivo de pruebas automáticas 
   * **`app.component.ts`**: Archivo TS donde definimos la clase del componente con su correspondiente decorador y todo el código para añadir funcionalidad al mismo mediante propiedades y métodos.
   * **`app.module.ts`**: Archivo TS que nos permite modularizar nuestro código.
* **`assets`**: Carpeta donde almacenamos todos los recursos estáticos como imágenes, videos, etc.
   * **`.gitkeep`**: Archivo vacío que nos sirve para cuando subamos una carpeta vacia se mantenga en el repositorio. Porque cuando subimos una carpeta vacia a GIT, GIT la ignora y de esta manera mantendríamos nuestra carpeta **`assets`** en el caso de que este "vacia"
* **`enviroments`**: Carpeta que contiene dos archivos:
   * **`environment.prod.ts`**: Variables de ambiente de producción
   * **`environment.ts`**: Variables de ambiente de desarrollo
* **`favicon.ico`**: Archivo de favicon
* **`index.html`**: Página Web inicial que contiene la etiqueta **`<app-root></app-root>`** que hace referencia al **`app.component`** por lo que Angular renderiza ese componente dentro de esta página **`index.html`**
* **`main.ts`**: Archivo TS, este código es el primero que coje Angular para lanzar la aplicación, es como el **`main`** de Java.
* **`polyfills.ts`**: Archivo que ayuda a la compatibilidad con navegadores viejos
* **`styles.css`**: Archivo de estilos globales a la aplicación.
* **`test.ts`**: Este archivo es requerido por **`karma.conf.js`** y carga recursivamente todos los archivos **`.spec`** y **`framework`**.

## Utilizando Bootstrap 10:03

Vamos a aplcar Bootstrap v5.1.1 al proyecto

![image](https://user-images.githubusercontent.com/23094588/132953154-b66a2735-a053-44ac-8748-990415ade3a8.png)

Pulsamos en el botón **Get started** y vamos a copiar lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/132953171-502a60e4-4483-4f46-9af7-8967fadf9fc6.png)

que son los estilos CSS de Bootstrap los cuales los vamos a copiar en el archivo **`index.html`**.

![image](https://user-images.githubusercontent.com/23094588/132953238-e9751851-b4c1-4284-bdf5-4c37906a1662.png)

Al cargar la APP se ve un poco diferente por los estilos que se le estan aplicando.

![image](https://user-images.githubusercontent.com/23094588/132953272-c2c9636a-f6fa-4380-9a5b-a1fa8e67e5d6.png)

### Creación del Componente `header` Manualmente

Dentro de la carpeta **`app`** vamos a crear la carpeta **`components`** y dentro de esta la carpeta **`header`**, dentro de  **`header`** vamos a crear el archivo **`header.component.ts`**

![image](https://user-images.githubusercontent.com/23094588/132953450-cd4b7618-aac6-49bc-a405-80d507cfb79e.png)

Este archivo vacio va a contener la clase **`HeaderComponent`** y para decirle a Angular que es un componente le vamos a poner un decorador de tipo **`@Component`** con su respectivo **`selector`** que llamaremos **`app-header`** e ira acompañado de su **`template`** que es un pequeño código HTML que se desplegara al renderizar este componente . El código completo del componente **`header`** es el siguiente:

![image](https://user-images.githubusercontent.com/23094588/132953709-d41a9247-c1c3-4434-b9c0-2d3451833cb5.png)

#### Incluir el componente **`header`** dentro de **`app.module.ts`**

En el archivo **`app.module.ts`** indicamos a Angular que componentes o servicios tiene, en este caso los componentes se incluyen dentro de **`declarations`** y gracias a que al componente le indicamos que puede ser exportado cono la palabra **`export`**, aquí podemos importarlo para poder incluirlo dentro de **`declarations`** de la siguiente manera:

![image](https://user-images.githubusercontent.com/23094588/132953812-5adbeac7-7165-4700-95b8-007c58d03778.png)

#### Renderizar el componente **`header`**

Finalmente para renderizar el componente **`header`** debemos incluirlo en algún archivo **`html`**, en este caso lo vamos a incluir en **`app.component.html`**:

![image](https://user-images.githubusercontent.com/23094588/132953939-1c52cf35-a4d7-42bc-b076-17f02dd826bd.png)

Al recargar la APP tenemos.

![image](https://user-images.githubusercontent.com/23094588/132953952-776c7d60-f331-4614-8313-2d413e69481a.png)

De esta manera estamos incluyendo el contenido del **`header.component`** dentro del **`app.component`**.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/132954064-4a5136e8-7fd3-4537-81d6-e9664532c515.png)

## TemplateUrl: Separando el HTML del componente 09:32

### Incluir un Navbar de Bootstrap en el `header`

Vamos a buscar en Bootstrap un Navbar y lo copiamos para incluirlo en el `header`.

![image](https://user-images.githubusercontent.com/23094588/132954288-89c0053a-a466-431b-86fb-55be65194633.png)

Y vamos a sustituir el texto que tenemos en **`template`** por lo que hemos copiado:

![image](https://user-images.githubusercontent.com/23094588/132954316-c22a771f-2fc0-4e0e-ba36-0a2c06e7437c.png)

Al cargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/132954342-5f51f1b7-9cd4-488f-828d-f52cb6729b77.png)

Nuestro componente **`header`** ahora lo que renderiza es una barra de navegación, el **`Dropdown`** no funciona por que solo incluimos los estilos de Bootstrap y faltan los JS para que funcionenen, ya lo veremos más adelante.

El estilo blanco del Navbar es gracias a los atributos **`navbar-light bg-light`** del tag **`<nav`** vamos a cambiarlos por **`navbar-dark bg-dark`** y la veremos así:

![image](https://user-images.githubusercontent.com/23094588/132954571-ab81e997-3584-469c-914a-a38ec11b9763.png)

### Separar el Template del Componente

Por ahora nuestro componente **`header`** solo consta del archivo TS donde estamos mezclando código HTML y JS, cuando el código HTML va creciendo como en este caso es mejor manejarlo en un archivo independiente, por lo cual vamos a crear el archivo **`header.component.html`** donde vamos a mover nuestro NavBar.

![image](https://user-images.githubusercontent.com/23094588/132954842-aa5f8859-54d2-490b-b4c5-3eba72606b08.png)

Ahora al componente **`header`** hay que indicarle que use este código en lugar del **`template`** que estaba usando, eso se hace usando el **`templateUrl`** al cual le indicamos la ruta del archivo **`header.component.html`**.

Por lo que al cargar la APP tenemos lo mismo.

![image](https://user-images.githubusercontent.com/23094588/132955479-9eced40d-c13f-4ca3-a4b7-be4ab84c6497.png)

Pero hemos separado el código TS y el código HTML en archivos independientes.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/132955814-87522988-f70a-4dc3-b94c-b63b45517339.png)


### Creación del componente `body`.

De la misma forma que creamos el componente **`header`** vamos a crear el componente **`body`**, siguiendo los siguientes pasos:

1. Crear carpeta **`body`** dentro de la carpeta **`components`**
2. Crear el archivo **`body.components.ts`** con nombre de selector **`app-body`**
3. Crear el archivo **`body.components.html`** para que muestre **`Body Component`**
4. Incluir el componente **`body`** dentro del **`app.module.ts`**
5. Renderizar **`body`** dentro de **`app.component.html`** 

![image](https://user-images.githubusercontent.com/23094588/132955925-1d2dedd7-e36d-43f2-b8a2-8a6cb18f5185.png)

![image](https://user-images.githubusercontent.com/23094588/132955934-8cc005c8-0d25-4d54-b069-e4babbe0615d.png)

![image](https://user-images.githubusercontent.com/23094588/132955949-775e15d7-1842-4b01-a594-192e138e0a02.png)

![image](https://user-images.githubusercontent.com/23094588/132955961-966bc97f-5a73-4a0f-b6da-3823233d8861.png)

![image](https://user-images.githubusercontent.com/23094588/132955971-4d34b659-4afc-430f-a2ab-7baf24f70be3.png)

Para que el Body no este tan pegado al NavBar vamos a meterle una clase a nuestra etiqueta **`<app-body`**

![image](https://user-images.githubusercontent.com/23094588/132956079-638eab2d-5dfc-4e84-9710-5c105fdd66b0.png)

![image](https://user-images.githubusercontent.com/23094588/132956082-822aa91b-32ee-4e10-9cd2-56825112c5ff.png)

Ya se ve un poco mejor.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/132956141-e1996567-a6ab-4599-88ec-bc5154661478.png)

## Creando el **`footer.component`** con Angular CLI 10:32

Vamos a crear el componente **`footer.component`** pero en este caso vamos a usar **Angular CLI** escribiendo el siguiente comando:

```sh
ng generate component components/footer
```

Le estamos diciendo que genere el componente en la carpeta **`components`** y que se va a llamar **`footer`**, el comando anterior lo podemos abreviar como sigue:

```sh
ng g c components/footer
```

![image](https://user-images.githubusercontent.com/23094588/132959361-0165fe78-0f41-4542-9175-c177b2d95801.png)

Al ejecutar este comando se nos han creado los archivos:

* **`footer.component.css`**
* **`footer.component.html`**
* **`footer.component.spec.ts`**
* **`footer.component.ts`**

Y se a actualizado el archivo:

* **`app.module.ts`**

![image](https://user-images.githubusercontent.com/23094588/132959510-f7fb55d6-4d23-444e-8459-d1391b589d8b.png)

Esto que antes lo habíamos creado a mano con este comando se han creado automáticamente aun que con pequeños matices ya que nosotros no ocupabamos los archivos **`footer.component.css`** y **`footer.component.spec.ts`**.

El archivo **`footer.component.spec.ts`** nos ayuda a realizar las prueba pero no lo vamos a cubrir en este curso por lo que lo vamos a eliminar.

El archivo **`footer.component.css`** contiene estilos CSS que solo se van a aplicar sobre el archivo **`footer.component.html`**, por ahora ese archivo esta vacio, para poder utilizarlo se ha declarado dentro de **`footer.component.ts`**:

![image](https://user-images.githubusercontent.com/23094588/132959522-4157e108-9642-4f8b-9b19-71aad7fdb7df.png)

Vemos que en la anotación **`@Component`** hay un nuevo atributo **`styleUrls`** para indicar el archivo de estilos CSS a usar. Ademas de esto tenemos algo nuevo dentro de **`footer.component.spec.ts`** lo que es el **`constructor() { }`** que es el constructor de la clase  y **`ngOnInit(): void {   }`** que es un método del ciclo de vida de las clases, ya veremos más en detalle para que sirven.

En nuestro archivo **`footer.component.html`** solo tenemos:

![image](https://user-images.githubusercontent.com/23094588/132959850-188bd93a-edbe-4a7f-b853-d49c2a98ad13.png)

Mientras que en **`app.module.ts`** vemos como se a incluido automáticamente el componente **`FooterComponent`** para que podamos utilizarlo.

![image](https://user-images.githubusercontent.com/23094588/132959646-6028e34a-9d41-4f01-824a-483a83c769e5.png)

**NOTA**: En caso que por alguna necesidad eliminemos un componente debemos también la referencia hecha de el en el **`app.module.ts`**. 

Vamos a modificar el contenido del **`footer.component.html`** con el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/132959903-ac8ba849-46c9-4aac-bf91-23a282af0f7a.png)

Y vamos a incluirlo en **`app.component.html`** para que sea renderizado.

![image](https://user-images.githubusercontent.com/23094588/132959930-8aa3c6c5-7e59-4711-9f9f-40599e1f24a8.png)

![image](https://user-images.githubusercontent.com/23094588/132959945-2ea3e0a1-33db-4f7e-824c-aa195ff9573c.png)

Vemos que este footer no aparece como esperabamos, vamos a insertar algunos estilos para que luzca mejor, lo podemos a hacer a nivel del componente o a nivel general que es la opción que vamos a usar por lo que vamos a modificar el archivo **`styles.css`**

![image](https://user-images.githubusercontent.com/23094588/132960248-44c05ca0-921c-4ece-8eec-605ef552e6f2.png)

Al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/132960264-6ac1158f-fb44-4889-8df1-8e9fc231021a.png)

Luce mejor pero no del todo, falta centrar el texto pero esto lo haremos dentro del **`footer.component.html`** añadiendo la clase **`text-center`** al tag **`footer`**.

![image](https://user-images.githubusercontent.com/23094588/132960321-c987170b-81f6-4de5-8e09-4e6d583be7cf.png)

Al recargar la APP tenemos que el aspecto a mejorado.

![image](https://user-images.githubusercontent.com/23094588/132960325-fd3e667d-7eea-4ae4-9cea-773a7dac0595.png)

Aun podemos mejorar cosas ya que el año lo tenemos Harcodeado, podemos que esto se calcule automáticamente para que no lo tengamos que cambiar cada que el año cambia, esta lógica la debemos incluir en **`footer.component.ts`**, vamos a iniciar por quitar el **`constructor() { }`** y **`ngOnInit(): void {   }`**, para que la clase quede como la habíamos estado trabajando con los otros componentes.

![image](https://user-images.githubusercontent.com/23094588/132960409-b710e286-3753-4cbd-900c-063d43e6f72b.png)

Lo que vamos a hacer es declarar una propiedad **`anio`*** que contendra el año actual.

![image](https://user-images.githubusercontent.com/23094588/132960443-e5d25092-e4bb-40c2-9efc-74aafe796ac9.png)

Esta es una forma de declarar la propiedad, pero existe otra forma que es un poco más adecuada y consiste en declarar la propiedad y asignarle el valor dentro del constructor como sigue:

![image](https://user-images.githubusercontent.com/23094588/132960487-b0913865-e2f0-4d83-92ae-be3683ff8410.png)

Ya tenemos la propiedad con el valor del año, ahora vamos a usarla dentro de **`footer.component.html`** de la siguiente manera:

![image](https://user-images.githubusercontent.com/23094588/132960554-988edbf9-a63f-447c-a1f7-55eccb4dff48.png)

Al cargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/132960564-7ac6ca62-bbb0-4636-b3e1-203c98ccb85c.png)


#### GIT

![image](https://user-images.githubusercontent.com/23094588/132960664-5a326142-832d-4ece-8269-94a2c87ffcd9.png)

## Estructura del body component 04:56

En esta clase vamos a trabajar un poco en el diseño del Body Component, para lo cual vamos a regresar a la página de Bootstrap y vamos a buscar un elemento llamado **Card**.

![image](https://user-images.githubusercontent.com/23094588/133122402-17e7c3d3-620f-4090-b484-cbf937ea69dd.png)

Esto lo ocuparemos en el diseño de nuestro Body Component, vamos por pasos, vamos a insertar lo siguiente en el **`body.component.html`**.

![image](https://user-images.githubusercontent.com/23094588/133123137-3c477fd0-e767-4d37-a62b-1363a389d81a.png)

![image](https://user-images.githubusercontent.com/23094588/133123214-dbe18816-a4ee-4aaf-a91e-41c453cabf79.png)

Esto aparece un poco pegado a los bordes, vamos a modificar el **`app.component.html`** que actualmente lo tenemos así:

![image](https://user-images.githubusercontent.com/23094588/133123423-b2654014-3acb-4003-95af-8f6be630e2ae.png)

Y vamos a ponerlo como sigue:

![image](https://user-images.githubusercontent.com/23094588/133123621-2b7e0766-b274-49b1-8b0b-cac52dfcdad6.png)

![image](https://user-images.githubusercontent.com/23094588/133123776-f0f2564d-45fa-4211-8e24-cba2acfe4151.png)

Para que no aparezca tan pegado agregamos **`m-5`**:

![image](https://user-images.githubusercontent.com/23094588/133124053-5dbd43db-3f12-4c3b-b9c7-8b093e9d8e82.png)

![image](https://user-images.githubusercontent.com/23094588/133124113-cc764405-e02f-41d2-8c27-891110414c43.png)

Ahora si vamos a ocupar el código de las Card de Bootstrap dentro de **`body.component.html`**

```html
<div class="card text-white bg-primary mb-3" style="max-width: 18rem;">
  <div class="card-header">Header</div>
  <div class="card-body">
    <h5 class="card-title">Primary card title</h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
</div>
```

![image](https://user-images.githubusercontent.com/23094588/133124610-92bcb7df-f2aa-483a-a6a3-915a0ccca403.png)

![image](https://user-images.githubusercontent.com/23094588/133124640-91d3a123-b843-42bb-9cb9-10932b50fae2.png)

Vamos a quitar el **`Header`** por que no lo vamos a ocupar aquí.

![image](https://user-images.githubusercontent.com/23094588/133124791-38cc3024-4276-40c5-a044-71562987befe.png)

Ahora debajo de la Card vamos a añadir un botón.

![image](https://user-images.githubusercontent.com/23094588/133125318-cfd6bccf-ae88-4843-aaf9-e8327950094f.png)

![image](https://user-images.githubusercontent.com/23094588/133125360-ce0a8b38-4f87-4836-87e0-02a70aa46d5a.png)

Por ahora el lado izquierdo correspondiente al **`*ngIf`** ya esta listo, vamos a pasar al lado del **`*ngFor`**, vamos a buscar en Bootstrap las **List**.

![image](https://user-images.githubusercontent.com/23094588/133125704-2cf4629f-5857-4a99-a64e-f3f71b2a71b7.png)

El primer ejemplo que sale nos vale, lo copiamos y lo pegamos debajo del **`*ngFor`**.

![image](https://user-images.githubusercontent.com/23094588/133125853-cb2fc629-ccf5-4ca6-99be-0d50fb5a3910.png)

![image](https://user-images.githubusercontent.com/23094588/133125910-3da2acee-8877-4478-abbc-dcc8ce519d0e.png)

Vamos a hacer que la Card se muestre al 100% y que el botón use también todo el ancho del área donde se pinta, con Bootstrap se usaba la clase **`btn-block`** pero eso a cambiado con Bootstrap 5 que es el que estamos usando.

![image](https://user-images.githubusercontent.com/23094588/133127226-6f032917-c796-472a-93f5-595c14e318f0.png)

![image](https://user-images.githubusercontent.com/23094588/133127267-754204a0-9a2f-44d3-bd6b-90906c97d71b.png)

Cuando nos colocamos sobre el botón cambia su color.

![image](https://user-images.githubusercontent.com/23094588/133127360-f39eb5a4-09d7-4b53-8a8b-158d20aea1c6.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133127733-c8148c70-5733-47bc-8036-66c5174c9dd2.png)


## Directivas estructurales: **`*ngFor`** y el **`*ngIf`** 10:01

Vamos a personalizar los textos que tenemos en Body Component, vamos **`body.component.ts`** y vamos a insertar la propiedad **`frase`**.

![image](https://user-images.githubusercontent.com/23094588/133128709-7c0b6258-910c-45f0-a10a-40ce90be62fc.png)

Vamos a usar este objeto **`frase`** dentro de nuestra Card de la siguiente forma:

![image](https://user-images.githubusercontent.com/23094588/133129057-25e93523-25e6-4ce5-910f-bd1168778eb2.png)

![image](https://user-images.githubusercontent.com/23094588/133129106-3e895f28-bcd5-4773-b98a-abbfd242fa2b.png)

### Directivas estructural **`*ngIf`**

Ahora vamos a darle funcionalidad al Botón cuando lo pulsemos ocultará la Card y cuando lo volvamos a pulsar mostrará la Card nuevamente. Esto se logra con la directivas estructural **`*ngIf`** la cual se coloca en el elemento a Ocultar/Mostrar (el cual es realmente destruido por HTML o construido por HTML según sea el caso), en este caso la Card y debe contener una expresión booleana si es verdadera se mostrara el elemento y si es falsa se ocultara.

Vamos a insertar una nueva propiedad en nuestro **`body.component.ts`** llamada **`mostrar`** inicializada a **`true`**.

![image](https://user-images.githubusercontent.com/23094588/133130350-1c2431cb-cb8f-416b-87e3-cea387daf12a.png)

Y en nuestro **`body.component.html`** vamos a insertar la directiva **`*ngIf`** en nuestra Card, además de esto cada que pulsemos el botón el valor de **`mostrar`** se debe cambiar por su opuesto esto se logra sustituyendo su valor por su negativo, el código nos queda así:

![image](https://user-images.githubusercontent.com/23094588/133130934-96fd5715-6dd4-43c6-8c7d-a15430812bda.png)

![image](https://user-images.githubusercontent.com/23094588/133130977-3dd8f6dc-8acc-4a52-80f3-5b9334cfbc0d.png)

![image](https://user-images.githubusercontent.com/23094588/133131024-8313e603-a8bc-4a94-b7d0-a66cdeee16e7.png)

![image](https://user-images.githubusercontent.com/23094588/133130982-101a4bd7-6e23-4567-bce5-412f901b5b46.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133131222-01a23b7b-43d1-471f-9da6-e9f0800ae01c.png)


### Directivas estructural **`*ngFor`**

El **`*ngFor`** trabaja a base de Arreglos para recorrererlos y hacer algo con ellos por ejemplo pintar sus valores. Para empezar vamos a declarar una nueva propiedad de tipo Array llamado **`personajes`** dentro de **`body.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/133131794-b8fa8250-cc2b-46b6-9f40-832cccdf6022.png)

Como esta es una propiedad de la clase puedo interpolar su valor dentro del HTML de la siguiente forma:

![image](https://user-images.githubusercontent.com/23094588/133131943-bf5ac93b-b47c-46ce-bce4-ec1f2536222c.png)

![image](https://user-images.githubusercontent.com/23094588/133132064-e5b5492b-3a34-46a8-b8a0-c72dc99cf759.png)

Aparecen al final, pero yo quiero que aparezcan como opciones de la lista ordenada que se encuentra debajo del título **`*ngFor`**, eso lo logramos usando precisamente la directivas estructural **`*ngFor`** como sigue:

![image](https://user-images.githubusercontent.com/23094588/133132689-c0ca3950-f3f5-4ee0-89de-afb6a090bdb0.png)

![image](https://user-images.githubusercontent.com/23094588/133132729-d3c59143-188c-463c-b09a-1e818bc5f84a.png)

Como vemos usamos el **`*ngFor`** sobre el elemento a repetir, usamos la propiedad **`personajes`** y por cada iteracción la vamos guardando en **`personaj`** y ese valor es el que interpolamos por eso se van renderizando los nombres.

**`*ngFor`** tiene un atributo llamado **`*index`** el cual podemos usar para saber en que iteracción se encuentra, se usa así:

![image](https://user-images.githubusercontent.com/23094588/133133948-8812b1f6-a3de-412e-aa10-f2aeb50ef45e.png)

![image](https://user-images.githubusercontent.com/23094588/133133881-ef122da5-d342-413d-869e-5cd82cc26775.png)

Podemos sumarle **`1`** a **`i`** para enumerar mejor la lista.

![image](https://user-images.githubusercontent.com/23094588/133134121-662280c2-0c0b-4e9d-9899-9d42e52e1a21.png)

![image](https://user-images.githubusercontent.com/23094588/133134256-35156a67-d6e5-488d-aaf3-3edd4b8f5350.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133134618-97c9c177-3e87-42de-8cf0-7cfa7638dd03.png)

## Examen teórico - de la sección Hola Mundo - 10 preguntas

![image](https://user-images.githubusercontent.com/23094588/133134444-58c1f99f-f56e-4ac0-9cfa-6c0377a15b93.png)

## Código fuente de la sección 00:23
