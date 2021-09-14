# 04 Aplicación #2: Aplicación de una sola página (SPA) - 26 clases • 2h 24m

* Introducción a la sección 00:55
* ¿Qué veremos en esta sección? 00:30
* Demostración de lo que lograremos en esta sección 01:21
* Iniciar el proyecto - SPA 03:49
* Creando la estructura de nuestro proyecto 06:24
* Instalando el bootstrap cuando usamos el Angular-CLI 14:58
* Configurando el navbar y otros componentes 06:34
* Rutas en Angular 08:23
* RouterLink y RouterLinkActive - Completando las rutas 09:10
* Componente Heroes - diseño 05:31
* Introducción a los Servicios 02:39
* Creando nuestro primer servicio - HeroesService 10:55
* Página de Heroes - Diseño con **`*ngFor`** 04:57
* Rutas con parametros - Router 09:12
* Recibiendo parámetros por URL - ActivatedRoute 06:53
* Tarea práctica #1 - Componente del héroe 02:50
* Resolución de la tarea práctica #1 - Componente del héroe 05:14
* Pipes: Transformación visual de la data. 03:20
* Buscador de Héroes 06:14
* Tarea práctica #2: Crear la pantalla de búsqueda de héroes. 02:02
* Resolución de la tarea 2 - Buscador de Héroes 07:55
* Plus: Mostrando un mensaje cuando no hay resultados. 02:01
* **`@Input`** - Recibir información de un componente padre a un hijo 10:38
* **`@Output`** - Emitir un evento del hijo hacia el padre 05:40
* Arreglar detalles de la búsqueda 05:50
* Código fuente de la sección 00:24

## Introducción a la sección 00:55

En esta sección vamos a trabajar para crear una aplicación de una sola página conocida como **SPA Single Page Aplication**. Trabajaremos con rutas con **Routers links** como se llama ahora, crearemos nuestro primer **servicio** de forma local. Instalaremos Bootstrap, trabajaremos con **Angular CLI** haremos una introducción a los **Pipes**.

## ¿Qué veremos en esta sección? 00:30

A continuación vamos a aprender sobre los siguientes temas:

1. Crearemos una aplicación de una sola página (Single Page Application)
2. Creación de proyectos de Angular usando el CLI (Command Line Interface)
3. Instalando Bootstrap o librerías de terceros usando el Angular-CLI
4. Creación de rutas de nuestra aplicación
5. Uso de RouterLink y RouterLinkActive para movernos de página y colocar clases a los elementos activos.
6. Uso del modulo Router, que nos permite movernos de página mediante código.
7. Obtención de parámetros vía URL.
8. Configuración de nuestro primer servicio en Angular para el manejo de la data.
9. Breve introducción a los Pipes 
10. Uso del buscador del Navbar para realizar una consulta a nuestro arreglo de héroes.

Durante la sección, tendremos una tarea práctica bastante retadora pero servirá de reforzamiento de todo lo que veremos en esta sección.

## Demostración de lo que lograremos en esta sección 01:21

Aplicación de una sola página.

![image](https://user-images.githubusercontent.com/23094588/133232010-c9c4dcbc-a22a-4580-b7d2-8ddd445f2ae3.png)

Podemos movernos a través de las diferentes páginas las cuales tienen sus respectivas rutas.

![image](https://user-images.githubusercontent.com/23094588/133232173-782f20bf-04c6-4ff5-8479-465921f93cf4.png)

Podemos consultar la información de cada Heroe

![image](https://user-images.githubusercontent.com/23094588/133232363-27f7a51d-046a-447f-acca-1e954a5fe6d9.png)

![image](https://user-images.githubusercontent.com/23094588/133232062-191ad596-a764-45b0-927e-9149ddf04c41.png)

Podemos hacer búsquedas por medio del buscador.

![image](https://user-images.githubusercontent.com/23094588/133232537-7be58fc0-89f6-4690-9aa6-18db765109c5.png)

Esta diseñado para que se vea bien en los móviles.

![image](https://user-images.githubusercontent.com/23094588/133232690-08e9a7ff-cf80-4586-9bda-382a83bdd24c.png)

Todo esto lo lograremos utilizando Angular, Rutas, Servicios, Pipes y algunas cosas más.

## Iniciar el proyecto - SPA 03:49

Desde la terminal en la carpeta de los Proyectos Angular vamos a escribir el comando:

```sh
ng new spa
```

para crear el nuevo proyeyecto llamado **spa**.

![image](https://user-images.githubusercontent.com/23094588/133233334-f1f91e2c-3085-42bf-9fc4-a9d776db0183.png)

![image](https://user-images.githubusercontent.com/23094588/133234793-f65eb28e-4087-481a-825f-a2a50b399194.png)

![image](https://user-images.githubusercontent.com/23094588/133235830-14515c05-7506-4ff5-ae05-608977f73de3.png)

Una vez que termina vamos a renombrar la carpeta creada **`spa`** por **`02-spa`**.

![image](https://user-images.githubusercontent.com/23094588/133236320-574ddd7c-e08c-456f-9c90-5271e66c2fb2.png)

Vamos a meternos a la carpeta **`02-spa`** y levantamos el servidor con **`ng serve -o`**.

![image](https://user-images.githubusercontent.com/23094588/133236621-bb73b0fc-f090-4498-b56d-a136c9c80516.png)

![image](https://user-images.githubusercontent.com/23094588/133236978-6069ed3f-5a32-4c94-b253-2b440f27563f.png)

![image](https://user-images.githubusercontent.com/23094588/133237088-b61dbeaa-478f-45cc-91c8-1a78ee286d4b.png)


## Creando la estructura de nuestro proyecto 06:24

Vamos a abrir el proyecto **`02-spa`** en VSC.

![image](https://user-images.githubusercontent.com/23094588/133238023-82598a9f-5368-48df-acdc-68e1a2ff4b8d.png)

Dentro de la carpeta **`app`** vamos a crear las siguientes carpetas **`components/shared`** que va a ir conteniendo los nuevos componentes que vayamos creando.

![image](https://user-images.githubusercontent.com/23094588/133238341-a6a819dc-d784-487d-9543-4405cab0ec40.png)

### Crear el Componente `Navbar`

Vamos a crear el componente Navbar con el comando:

```sh
ng g c components/shared/navbar
```

Le estamos indicando que genere el componente en la carpeta **`components/shared`** (la que creamos) y se llamara **`navbar`**.

![image](https://user-images.githubusercontent.com/23094588/133239051-4ce8dc85-2e57-4bdc-a64a-e1620d95e5db.png)

Los crea los 4 archivos y actualiza **`app.module.ts`**.

![image](https://user-images.githubusercontent.com/23094588/133239253-f2dbf3c9-812b-4047-87cc-c06b0e1c625c.png)

Vamos a eliminar **`navbar.component.css`** y **`navbar.component.spec.ts`** que no los vamos a usar en esta APP y hacemos los respectivos ajuestes en **`navbar.component.ts`**.

### Crear el Componente `Home`

Vamos a crear el componente `Home` con el comando:

```sh
ng g c components/home
```

Observese que este componente no va dentro de la carpeta de compartidos **`shared`**, si por equivocación lo crearamos dentro de esa carpeta tendríamos que mover la carpeta **`home`** a **`components`** y editar el **`app.modules.ts`** para indicar la ruta correcta.

De igual manera vamos a eliminar **`home.component.css`** y **`home.component.spec.ts`** y hacemos los ajuestes en **`home.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/133240966-828f49ae-d97f-4836-bb6e-769a0bacbbfd.png)

![image](https://user-images.githubusercontent.com/23094588/133241096-c7cd2195-65f7-4630-9cda-6af1d0a21aaf.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133241241-e2591524-ae5d-4a3a-b97b-4052264f93af.png)

## Instalando Bootstrap cuando usamos el Angular-CLI 14:58

En esta lección vamos a aprender a instalar **Bootstrap** de tres formas diferentes. Esto se aplica para todas las librerías de terceros para que funcionen en su aplicación de Angular.

**NOTA:** En la versión 6 de Angular el archivo **`angular-cli.json`** paso a llamarse **`angular.json`**.

### 1er Forma de Usar Bootstrap con CDN

Vamos a Instalar Bootstrap v4.1.1.

![image](https://user-images.githubusercontent.com/23094588/133242455-16e440d7-c2b5-43ea-8ec5-caea3e330d9d.png)

La forma más sencilla de usar una librería es utilizar el **CDN** o un **Servidor Gestor de Contenidos** 

![image](https://user-images.githubusercontent.com/23094588/133243014-ca52b1ff-bbf2-4d6c-98e2-fde925028321.png)

por lo general esto se recomienda si la aplicación está en Internet, por que esto se almacena en el cache y si ya loo había usado el usuario anteriormente ya no lo volvera a cargar.

Vamos a copiar los CSS y los JS en nuestro **`index.html`**.

![image](https://user-images.githubusercontent.com/23094588/133243594-2a97d457-793b-41de-8cdd-7279a3804323.png)

Movemos el Script de Bootstrap también abajo del todo

![image](https://user-images.githubusercontent.com/23094588/133243733-f2072679-c648-4316-8d42-b7f0c0e78763.png)

Al recargar la APP ya usa los estilos de Bootstrap.

![image](https://user-images.githubusercontent.com/23094588/133244697-932d536e-a550-4d05-abe7-f1eda42645a9.png)

La una restricción de usar el CDN es que siempre debemos estar conectados a Internet.

#### GIT 

![image](https://user-images.githubusercontent.com/23094588/133247245-abd3424f-58b1-48f7-8654-bc0b112c2080.png)

### 2da Forma de Usar Bootstrap Descargandolo.

![image](https://user-images.githubusercontent.com/23094588/133245203-62e4dc11-fd8c-4b41-ba1c-7d7db8c496a9.png)

Otra forma es descargar la librería.

![image](https://user-images.githubusercontent.com/23094588/133245392-bcba712e-d6e2-4fda-a5ab-f324d8b71c5a.png)

Vamos a copiar esta carpeta dentro del proyecto en la carpeta **`assets/libs`** y la renombraremos simplemente como **`bootstrap`**.

![image](https://user-images.githubusercontent.com/23094588/133245922-4a9c72f2-991e-49dc-9031-42877031bf09.png)

Vamos a comentar lo que metimos del CDN y el estilo retorna a su origen.

![image](https://user-images.githubusercontent.com/23094588/133246287-b70b038e-06d9-4859-a892-79bdd0b01cdd.png)

Para usar la librería localmente indicamos la ruta de los archivos descargados:

![image](https://user-images.githubusercontent.com/23094588/133247744-56b37022-13e3-45ef-81a1-0e585d5ab899.png)

![image](https://user-images.githubusercontent.com/23094588/133247785-582adafe-b5de-45d1-8ab5-44bc0292c84d.png)

**NOTA:** Abría que descargarse ademas de la librería de Bootstrap la de JQuery y Popper y meterlos localmente para indicarlos en las rutas de los Scripts localmente. Esta tarea no se ha realizado.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133248151-0e3590ec-dde8-4eab-9f9e-cc9cad07379c.png)


### 3ra Forma de Usar Bootstrap Instalarlo mediante el `npm`

Lo primero que vamos a hacer es eliminar del **`index.html`**, todo lo que habíamos metido con las dos opciones anteriores e inclusive vamos a eliminar lo que habíamos metido en el **`assets`**. Una vez hecho lo anterior vamos a instalar Bootstrap mediante el **`npm`**

![image](https://user-images.githubusercontent.com/23094588/133248420-9c6365f9-758b-4dca-8c2d-1ee3baac3964.png)

Vamos a pulsar el comando 

```sh
npm install bootstrap --save
```

El **`--save`** esto le indica a la APP que es una librería que va a necesitar, esto descarga Boostrap y los coloca en los Modulos de Node.

![image](https://user-images.githubusercontent.com/23094588/133249263-13a91514-a119-424a-8a0d-b947388f998b.png)

Como no hemos indicado que versión de Bootstrap instalar, instalo la más reciente es decir la v5.1, la ventaja de esta versión es que ya no necesita JQuery y Popper que también tendríamos que instalar con:

```sh
npm install jquery --save
npm install popper.js --save
```

Si nos vamos a los Modulos de Node, seguro lo veremos allí.

![image](https://user-images.githubusercontent.com/23094588/133249692-9ccf68be-1cf8-4296-877d-5f01127dae0c.png)

![image](https://user-images.githubusercontent.com/23094588/133252147-ebd4b283-8365-4f4f-afc5-2cf37e40533c.png)

Ahora lo que tenemos que hacer es indicarle a Angular que vamos a trabajar con el Bootstrap que se encuentra en los Modulos de Node

![image](https://user-images.githubusercontent.com/23094588/133251590-caba2a3d-e366-484d-83b1-42f6184dae86.png)

Esto lo vamos a hacer en el archivo **`angular.json`** que actualmente esta así:

![image](https://user-images.githubusercontent.com/23094588/133250970-4a1745a7-d5fd-4302-8612-64bb2bc34217.png)

Vamos a añadir lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/133252248-8a4f26b3-828c-4ccd-80b6-74d0b7981cd7.png)

Hemos elegido esa librería por la documentación de Bootstrap.

![image](https://user-images.githubusercontent.com/23094588/133252712-b31b397a-63d2-4e84-ab05-4a7cc2d64109.png)

Cuando se modifica el archivo **`angular.json`** hay que dar de baja el Servidor y volverlo a cargar para que tome los cambios.

La APP esta tomando Bootstrap del Node Modules.

![image](https://user-images.githubusercontent.com/23094588/133253634-f4f0d024-6a00-44d3-9a46-7abb5f993b3b.png)

La ventaja de usar esta forma es que si creamos otro proyecto simplemente instalamos Bootstrap con el **`npm`** y copiamos lo que hemos insertado en el **`angular.json`** y ya estaría listo Bootstrap para usarse. Pero tiene la desventaja de que todas estas librerías van a formar parte del Bundled y si estas son librerías comunes podría hacer que la aplicación pese algo más.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133255020-4d780216-c315-4bf3-9d11-989e8cee9112.png)

## Configurando el navbar y otros componentes 06:34

Este proyecto necesita que nos descarguemos los recursos de la sección que necesitaremos para realizar la sección.

![image](https://user-images.githubusercontent.com/23094588/133235388-66d749ce-fd66-4d80-a627-a01fb1f6a351.png)

Son imagenes de super heroes, un favicon, estilos css y datos de los super heroes.


## Rutas en Angular 08:23
## RouterLink y RouterLinkActive - Completando las rutas 09:10
## Componente Heroes - diseño 05:31
## Introducción a los Servicios 02:39
## Creando nuestro primer servicio - HeroesService 10:55
## Página de Heroes - Diseño con **`*ngFor`** 04:57
## Rutas con parametros - Router 09:12
## Recibiendo parámetros por URL - ActivatedRoute 06:53
## Tarea práctica #1 - Componente del héroe 02:50
## Resolución de la tarea práctica #1 - Componente del héroe 05:14
## Pipes: Transformación visual de la data. 03:20
## Buscador de Héroes 06:14
## Tarea práctica #2: Crear la pantalla de búsqueda de héroes. 02:02
## Resolución de la tarea 2 - Buscador de Héroes 07:55
## Plus: Mostrando un mensaje cuando no hay resultados. 02:01
## `@Input` - Recibir información de un componente padre a un hijo 10:38
## `@Output` - Emitir un evento del hijo hacia el padre 05:40
## Arreglar detalles de la búsqueda 05:50
## Código fuente de la sección 00:24
