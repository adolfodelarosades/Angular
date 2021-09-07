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

En la carpeta **`app`** tenemos nuestra primer aplicación de Angular.

![image](https://user-images.githubusercontent.com/23094588/132388025-c12def41-19a2-4682-b7f8-bd4a223d04c3.png)

El **`app.component`**



* **``**
* **``**
 



este archivo la verdad simplemente 

Luego tenemos el archivo zip ignoré para las personas que han trabajado con GIT saben que es exactamente

el archivo para las personas que no lo conocen es un archivo que simplemente le dice cuando nosotros

hagamos backups a repositorios de GIT que ignoré todos estos archivos o carpetas es decir que no las

guarden en el repositorio y la Signor y piense que no existen.

Entre esas están los módulos CNOP que por lo general nunca se graban en un repositorio porque se puede

reconstruir con el comando que yo les enseñé anteriormente.

MPM instó.

Pero hay otras cosas como por ejemplo la carpeta de distribución porque eso es un producto de un proceso

que genera entre otras cosas este archivo tampoco lo vamos a manipular mucho nosotros lo voy a cerrar

antes de continuar con el siguiente archivo y que se empiecen a asustar por el montón de cosas que hoy

son muy pocos los archivos que nosotros vamos a manipular de forma directa.

El angular punto Jayson es un archivo que no vamos a hacer grandes modificaciones al mismo pero es un

archivo que le dice a Goulart cómo es nuestra aplicación y cómo funciona.

4U ocupemos yo les voy a enseñar los lugares donde lo vamos a modificar que básicamente es esta es esa

parte de acá.

Cuando nosotros generemos la aplicación de distribución va a tomar todos los estilos y va unificarlos

en un único archivo para tomar todos los scripts personalizados que hagamos y los va a tomar en un único

archivo igual que los assets que estamos diciendo es que estos son estáticos.

Pero en fin estas cosas las vamos a utilizar más adelante pero no se preocupen lo demás no lo tocamos

no lo tocamos manualmente nosotros el package apuntó lospuntos Jayson le dice a nuestra aplicación de

Nott cómo fue creado el paquete Jayson.

No es que este archivo lo vayamos a modificar nosotros este archivo se hace todo automático conforme

nosotros instalamos cosas y nuestra aplicación esto va a ir dejando un rastro de cómo fue que se crea

este archivo de paquete punto.

Este archivo no se toca manualmente.

Luego tenemos el archivo package apuntó Jayson que es sumamente importante es un archivo que ustedes

tienen que cuidar y se manipula con mucho cuidado qué es lo que vamos a tocar acá.

Básicamente nada van a decir bueno entonces para qué lo vamos a manipular.

Es que este archivo del package punto Jayson es para las personas que han trabajado con Nott esto todo

este archivo se va creando de forma automática.

Por ejemplo a quién le va a decir angular cuáles son las dependencias que nuestra aplicación va a necesitar

cuando lo pasemos a producción que en este caso sería todo lo que tenemos acá.

Dependencias de desarrollo como dice el nombre son dependencias que se usan únicamente mientras creamos

la aplicación.

Por ejemplo dice ah bueno esta aplicación fue creada usando el angular Ciela 6.0 6.0.1 el lenguaje que

se está utilizando el 6.0 el Corliss en fin varias cosas que sólo funcionan en desarrollo como por ejemplo

el TS lint que nos va a ayudar a nosotros a que cuando estemos escribiendo código nos detecte dónde

están los problemas antes de que corramos la aplicación.

En fin este archivo no se manipula es muy raro manipularlo manualmente el archivo Redmi punto CMD es

un archivo que normalmente se crea de forma automática y explica cómo funciona la aplicación.

Ustedes pueden cambiar borrar todo esto.

Esta acción no afecta en lo absoluto en su aplicación pero les va a ayudar que cuando los suban a un

repositorio como por ejemplo Guijo se renderiza y aparezca así y les diga a ustedes cómo funciona la

aplicación developer Server developer Server corriendo en el puerto local 4200 es esto de acá básicamente

los archivos con extensión punto de MB es de Mac es como es algo muy parecido al HTML pero mucho más

ligero.

Nosotros no vamos a trabajar mucho con este archivo pero en el momento que lo llegáramos a usar yo les

voy a explicar qué hacer con él.

El TS Koffi apuntó Jayson esto ya lo vimos en la introducción de Skype pero básicamente le dice TACs

scrip cómo trabajar a qué estándar necesitamos trabajar la aplicación.

En este caso queremos que lo transpire o lo convierta a ECMAscript 5 que es el estándar de JavaScript

mayormente soportado por todos los navegadores web.

El Achiote es el punto Jayson.

Eso ha hecho que a veces es un dolor de cabeza pero nos va a forzar a escribir un código más limpio

de escribir cuando notemos que aparece algún error que dice TSE lint es porque están respetando algunas

reglas de este archivo conforme vayamos trabajando.

Yo les voy a explicar qué cosas podemos hacer pero usualmente se deja así como está.

Ahora sí vamos con lo interesante que es la carpeta sours.

Aquí es donde vamos a pasar la mayor parte del tiempo en la carpeta a Pepe tenemos nuestra primera aplicación

de angular que es lo que nosotros vimos en los ejercicios anteriores se acuerdan cuando lo vimos corriendo

en el navegador web component.

Es el primer componente que la aplicación o nuestra aplicación va a cargar.

Déjenme adelantarme un poquito al Index puntuó HTML el Index es una página web común y corriente.

De hecho si no tuviera esta línea si estuviera así sería una página web totalmente plana pero tiene

este app component.

Este app Root este app Rub la definición de todo este archivo o qué hacer con este archivo se encuentra

aquí en la componen .3 ven aquí esta es la brut.

Es este mismo robot entonces angular bar renderizar toda la aplicación aquí adentro eso es básicamente

todo lo que él quería explicar ahorita por el component y por qué hay tantas versiones como por ejemplo

por qué hay un app de puntos CSS HTML puntúe Speck.

Por qué están estos cuatro chicos que se llaman igual.

El CSS es un estilo que se aplica únicamente al HTML que tenemos acá del mismo nombre.

No es que el nombre tiene que ser igual eso está definido acá pero por lo general se llama igual.

Luego tenemos el HTML que es el código HTML de este componente cualquier archivo punto punto T cualquiera

que tenga la palabra expect es un archivo de pruebas automáticas.

Esas pruebas automáticas no las cubren este curso pero tengo el curso de amolar avanzado donde hacemos

todas las pruebas a componentes servicios y demás por si acaso tienen mayor interés en ese tema.

Ahora la parte del PP apuntó módulo este archivo y lo vamos a manipular a veces directamente a veces

de forma automática pero no quiero que se asusten porque tiene una sintaxis rara.

Noten que si yo borro todo esto sigue siendo una simple clase de Suevo de JavaScript pero tiene un decorador

llamado en módulo que lo explicaremos más adelante en el curso y tiene una forma interesante de definir

su decorador o sus propiedades.

Pero eso lo vamos a hablar más adelante.

Luego tenemos la carpeta assets que por lo general aquí vamos a colocar recurso estático como por ejemplo

imágenes y cosas de esas.

El archivo punto es un hecho que absolutamente no tiene nada es un archivo que simplemente se crea para

que cuando subamos a nuestra aplicación a un repositorio aquí se mantenga esta carpeta porque cuando

nosotros subimos una carpeta vacía y simplemente la ignora.

Pero aquí con un pequeño archivo sí lo va a mantener en el repositorio.

La carpeta de environments tiene dos archivos que son el mismo tiene environments como variables de

ambiente de producción que en este caso sería productivo y variable de ambiente de desarrollo.

Esto lo vamos a utilizar más adelante en el Cours ok el browser list es algo que yo absolutamente mi

vida había visto hasta que empecé a generar nuevos archivos con la versión 6 de angula apareció este

archivo pero según esto dice que es usado para el autor fixer.

Jamás lo he usado en mi vida y dice que es para ajustarse a ese deseo o para permitir un mejor soporte

de CSS.

Honestamente no es necesario no les digo que lo borren Déjenlo ahí pero realmente no lo vamos a usar

en el curso de lo que es el.

El Poli Fils el texto son archivos muertos la mayoría de todos los archivos nosotros no lo vamos a tocar

y se manipulan o se manipulan de forma automática.

El archivo es karma apuntó config p.ej. ese es el archivo de configuración de las prueba de karma.

Nosotros no lo vamos a tocar y no se hace nada con él.

En este curso el mail para las personas que han trabajado con Java o echar o aplicaciones que usen ya

un archivo o una función main es el primer código que Angola va a lanzar para correr la aplicación.

Por qué dice Platform Platform Browser Dinamic.

Esta función espanta y la primera vez que yo la vi me asustó un montón.

Pero todo esto se hace de forma automática.

Esta función básicamente lo que hace es configurar todo el ambiente para una aplicación web.

Si nosotros estuviéramos trabajando con Native script para hacer una aplicación nativa de dispositivos

móviles o usar Yony para crear aplicaciones móviles híbridas en nuestros dispositivos móviles que también

funciona con angular aquí Camy un poco angular puede correr en varios entornos y esto lo hace de forma

automática para decir que es una aplicación web.

La parte de los policías simplemente son funciones que ayudan a la compatibilidad entre versiones viejas

de navegadores web.

Este archivo.

Nosotros no lo vamos a tocar de forma automática el mail tampoco así que no se vayan a asustar son muchas

cosas.

Yo sé que asusta pero créanme que cuando ustedes terminen este curso van a ser expertos en manipular

estos archivos.

El estáel es un archivo de estilos globales.

La aplicación aquí ustedes simplemente ponen código de es el texto.

No lo vamos a usar tampoco el TS puntuada.

Son de especificaciones propias de la aplicación de Tixkokob.

Luego tenemos el TS confi que es el punto Jayson es la configuración para hacer las pruebas.

Eso tampoco lo vamos a cubrir acá ni lo tocamos el TC le imputó Jayson.

Son formas para la configuración de nuestra aplicación o para la manera en que nos van a presentar los

errores cuando estamos escribiendo código.

Básicamente esos son todos los archivos y todas las carpetas que tiene un proyecto en este momento.

Yo sé que el contenido es abrumador es exageradamente grande pero créanme se tocan se tocan muy pocos

archivos acá conforme nosotros vayamos creando aplicaciones en angular.

Mi objetivo es que ustedes agarren la confianza para manipular este proyecto.

Ustedes no se preocupen porque a lo largo del curso nosotros cuando hagamos una modificación a un archivo

ustedes van a ver físicamente qué hace para qué lo hicimos y en fin para qué puede servirnos ese cambio

así que vamos a comenzar con nuestra primera aplicación.



## Utilizando Bootstrap 4 10:03
## TemplateUrl: Separando el HTML el componente 09:32
## Creando el **`footer.component`** 10:32
## Estructura del body component 04:56
## Directivas estructurales: **`*ngFor`** y el **`*ngIf`** 10:01
## Examen teórico - de la sección Hola Mundo - 10 preguntas
## Código fuente de la sección 00:23
