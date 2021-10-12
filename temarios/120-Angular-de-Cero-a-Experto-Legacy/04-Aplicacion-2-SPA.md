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

***De esta misma forma se pueden instalar otras librerías con el NPM***

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133255020-4d780216-c315-4bf3-9d11-989e8cee9112.png)

## Configurando el Navbar y otros componentes 06:34

Este proyecto necesita que nos descarguemos los recursos de la sección que necesitaremos para realizar la sección.

![image](https://user-images.githubusercontent.com/23094588/133235388-66d749ce-fd66-4d80-a627-a01fb1f6a351.png)

Son imagenes de super heroes, un favicon, estilos css y datos de los super heroes.

Dentro de la carpeta **`assets/img`** vamos a copiar todos los archivos **`.png`**. El favicon lo vamos a copiar en la carpeta **`src`** para reemplazar el existente y con esto ya se cargara el favicon.

![image](https://user-images.githubusercontent.com/23094588/133256291-6a1118f5-6a90-4a37-b1d2-b286d29bcd33.png)

### Modificar el Componente `Navbar`.

Vamos a insertar el siguiente código en el archivo **`navbar.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/133258082-223c0c37-f11e-4ebb-9a23-79b5580cba72.png)

Y vamos a cargar este componente en **`app.component.html`** borramos todo lo que tiene y lo reemplazamos por:

![image](https://user-images.githubusercontent.com/23094588/133258306-ddb75c8a-6a48-41d6-97ac-7d0744219c58.png)

La APP se visualiza así:

![image](https://user-images.githubusercontent.com/23094588/133258380-e8a1f8af-e498-4a73-9c7c-e2f86b7bfe6f.png)

### Modificar el Componente `Home`

En el componente **`Home`** vamos a insertar el siguiente código que representa un Jumbotrom de Bootstrap:

![image](https://user-images.githubusercontent.com/23094588/133304346-f6193efa-4668-48b1-92af-fca4f5e70a7f.png)

### Crear el Componente `About`.

Vamos a crear el componente `about` con el comando

```sh
ng g c components/about
```

![image](https://user-images.githubusercontent.com/23094588/133260071-58db27d0-1974-4121-ad2c-6d07131c2be6.png)

Eliminamos el css y el spec y hacemos los ajustes necesarios.

### Crear el Componente `Heroes`.

Vamos a crear el componente `heroes` con el comando

```sh
ng g c components/heroes -is
```

Con **`-is`** no me crea el archivo de estilos.

![image](https://user-images.githubusercontent.com/23094588/133260284-73c8d5ce-023d-4ce5-bae1-4f3297187dac.png)

Eliminamos el spec y hacemos los ajustes necesarios.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133261151-f06c221a-fc67-418a-8e8a-a748bb25277a.png)

![image](https://user-images.githubusercontent.com/23094588/133261365-442940f6-f648-4fb7-870d-fe30694cae3d.png)

## Rutas en Angular 08:23

Las **Rutas** nos permiten navegar a diferentes ***Componentes*** o ***Páginas*** ***sin hacer Refresh del Navegador***, solo se carga lo que se necesita para poder cargar esa página.

En la carpeta **`app`** vamos a crear el archivo **`app.routes.ts`** con el siguiente contenido:

![image](https://user-images.githubusercontent.com/23094588/133301998-10b80711-09b8-4658-8f9a-c11a7cfa34ce.png)

**`APP_ROUTES`** es un arreglo de ruta, cada una de las rutas tiene un **`path`** y tiene un **`component`**, la ruta **`{ path: '**', pathMatch: 'full', redirectTo: '' }`** es una ruta especial por si a caso no hace match con ninguna de las rutas que la preceden.

Vamos a personalizar nuestra primer ruta hacia el componente **`Home`** de la siguiente manera:

![image](https://user-images.githubusercontent.com/23094588/133302559-b78f8abf-5018-4561-bdc2-3def7d8cccd4.png)

Para indicarle a Angular que ya dispone de este sistema de rutas debemos incluirlo en el **`app.module.ts`** de esta forma:

![image](https://user-images.githubusercontent.com/23094588/133303386-b70d054e-6ada-4faf-b0b2-49a2f6b7cd7e.png)

Lo importamos y lo incluimos en la sección de los **`imports`**.

Si cargamos la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/133303602-fd83c813-f074-4bf5-bddd-6e6b0fd55535.png)

Vemos que ya nos carga la ruta **`http://localhost:4200/home`** pero no vemos el contenido del componente **`Home`**, este es por que no le hemos indicado donde lo debe renderizar, nos vamos a **`app.component.html`** y lo incluimos:

![image](https://user-images.githubusercontent.com/23094588/133304750-6ec8c847-a91c-4711-894e-e72b2363b6cc.png)

Al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/133304804-9b42e72b-2c66-4d13-9a26-14cf2b9da4c9.png)

Por ahora solo tenemos una ruta y esta esta asociada al componente **`Home`**.

### Formas en que trabajan las Rutas

Hay varias maneras de manejar las rutas en Angular la primera es la que ya vimos usando un ***Path Relativo*** 

* **`http://localhost:4200/home`**: Esto es como si tuviera un folder home y dentro un **`index.html`**, esto es gracias al HTML 5, esto funciona bien pero cuando ya se mandan parámetros y hacemos refresh perdemos la referencia.

Existe una forma antigua donde se usa el caracter **`#`** que es una manera mas eficiente de manejar las rutas y soportado por la mayoría de los navegadores Web, para poder manejarlo necesitamos indicarselo en el **`app.routes.ts`**:

![image](https://user-images.githubusercontent.com/23094588/133306382-a35f8d78-7622-4f22-8f40-580e26684988.png)

Al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/133306514-5c20193d-bf30-41bf-92a3-b98b35cdbd17.png)

De esta manera la ruta qie se carga es:

* **`http://localhost:4200/#/home`**

***Si no usamos el caracter `#` en las rutas cuando usemos parámetros en las rutas puede fallar y hay que volver a recargar la aplicación por que pierde el estado*** para eso necesitaríamos hacer una pequeña configuración en el servidor para que redireccione siempre al Home y después a la página que debe ir, pero eso es un poco más de trabajo en el Backend que no veremos en este curso.

Otra cosa importante que el Angular CLI hace de forma automática, es que cuando no estamos utilizando el routing con **`#`**, 

![image](https://user-images.githubusercontent.com/23094588/133307516-2a7dc1a8-eac3-4d3f-a28f-b819de33c1ab.png)

el **`index.html`** debe contar con la etiqueta **`<base href="/">`**.

![image](https://user-images.githubusercontent.com/23094588/133307649-415e3fa6-7b6a-401d-8e47-02f30b3aca68.png)

Si no le ponemos esta etiqueta **`<base href="/">`** (comentarla) y no estamos usando el routing con **`#`** la aplicación nos fallará:

![image](https://user-images.githubusercontent.com/23094588/133308007-aa92ff3c-28df-4ad2-9c8b-5fb8b381ffa0.png)

Por ahora lo vamos a dejar sin el **`#`** y ya más adelante veremos donde es donde falla.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133308405-a1e7d89d-b864-4e1c-b317-e0f7056fd393.png)


## RouterLink y RouterLinkActive - Completando las rutas 09:10

Vamos a añadir las dos rutas para los dos componentes adicionales que tenemos **`AboutComponent`** y **`HeroesComponent`**.

![image](https://user-images.githubusercontent.com/23094588/133308986-f3b300f1-3a89-44f6-a718-a84584879e5b.png)

Ya tenemos las rutas a dichos componentes, ahora nos vamos a **`navbar.component.html`** que es donde va estar el cambio entre las diferentes páginas. Primero vamos a insertar las dos opciones para nuestras dos páginas.

![image](https://user-images.githubusercontent.com/23094588/133309603-a8701431-1f9c-4449-92a6-59ed30608e6f.png)

Observese que en la etiqueta **`<a class="nav-link" href="#">`** tenemos el atributo **`href="#"`**, antes se usaba **`<a class="nav-link" href="#/home">`** pero en lugar de eso vamos a usar un elemento llamado **RouterLink** el cual recibe como valor un array y cada elemento del array es como un segmento de la ruta, en nuestro caso solo tenedremos un elemento en la ruta como sigue:

![image](https://user-images.githubusercontent.com/23094588/133312460-ed441c48-b806-44e3-8d5d-f8bced097772.png)

Los nombres que estamos poniendo en los elementos del array son los que asignamos en las rutas **`path`**.

Al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/133312667-025d4e24-e737-48cc-ad50-d1d1f8d5f29b.png)

![image](https://user-images.githubusercontent.com/23094588/133312696-2569d0ce-e7d6-4666-a031-2a0e1eed61e3.png)

![image](https://user-images.githubusercontent.com/23094588/133312722-a23dd77d-7310-417a-b8b8-f5d99ef8b32b.png)

Ya esta trabajando nuestro sistema de rutas llevandonos a nuestros diferentes "páginas".

Vamos a dar un poco de estilo a los componentes empezamos metiendo un margen para que no queden muy pegados el Navbar y los componentes.

![image](https://user-images.githubusercontent.com/23094588/133313349-e93eb708-a6c7-42c0-af8c-a4b7fdc04656.png)

En el Componente About metemos lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/133313879-cf1c5ded-f39b-4077-a51f-bd4b90323c37.png)

En el Componente Heroes metemos lo siguiente:

### Incluir los Estilos de Animación

En el archivo **`styles.css`** vamos a copiar el contenido del archivo **`animate.css`** que nos descargamos en los recursos.

![image](https://user-images.githubusercontent.com/23094588/133314731-5bc9aa51-d915-4d41-bbd3-5ec41b48fb66.png)


### Meter la Animación en el Componente `About` y `Home`

![image](https://user-images.githubusercontent.com/23094588/133315250-2578445a-70f6-4119-9645-9d7b894feed7.png)

![image](https://user-images.githubusercontent.com/23094588/133315406-1bc4aa18-147c-4106-a391-a31ac82f2b1b.png)

Al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/133315591-d240052a-8f57-4c0a-9d06-3b7499ef585b.png)

![image](https://user-images.githubusercontent.com/23094588/133315619-2c3be6ec-693b-42a5-93ee-9ba09152e9b1.png)

En la imagen no se ve pero juro que existe una animación al cargar las páginas.

### Marcar la Página seleccionada como Activa con `routerLinkActive`

Para marcar una página como activa se usa la propiedad **`routerLinkActive`**, vamos al Navbar y vamos a colocar ese atributo:

![image](https://user-images.githubusercontent.com/23094588/133316300-f957b767-823e-40ec-bdc0-e00e314494e3.png)

Al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/133374233-cd04e904-c983-43a6-86dd-292815564e53.png)

![image](https://user-images.githubusercontent.com/23094588/133374258-ab7958f9-3051-421e-83e3-1a8617ae998f.png)

![image](https://user-images.githubusercontent.com/23094588/133313838-1a9cc6b6-a2bc-497e-be4a-1652ecb75e29.png)

En teoría se debería ver más blamco el título de la opción marcada, pero creo que no es del todo así.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133374478-6061efa4-97e2-4895-bcfd-cac7b9c5d9ba.png)


## Componente Heroes - diseño 05:31

Para el diseño de los Heroes vamos a usar las Cards de Bootstrap.

![image](https://user-images.githubusercontent.com/23094588/133374676-2d686f92-a28b-4ff1-b05b-54c86a06707c.png)

En **`heroes.component.ts`** vamos a meter el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/133377620-acac9764-eea2-4f14-b0d7-0e60c910e262.png)

Hemos metido en **`styles.css`** el estilo 

![image](https://user-images.githubusercontent.com/23094588/133377724-5365af17-449f-46e6-b3e2-2272613a728c.png)

para dejar un espacio en la parte de abajo.

Al cargar la APP vemos:

![image](https://user-images.githubusercontent.com/23094588/133377780-beee9c59-cf6a-4094-884f-523c19532c06.png)

Vamos a cambiar el color del botón del Navbar a Azul en lugar de Verde como esta ahora.

![image](https://user-images.githubusercontent.com/23094588/133377950-3487a706-fe40-4088-a201-d7d6d873fba0.png)

La APP final nos queda así:

![image](https://user-images.githubusercontent.com/23094588/133378018-d39fde72-dc11-49e2-ad7f-5718a1efb745.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133378098-129d969f-622c-4461-a816-ade875e4a7c7.png)

## Introducción a los Servicios 02:39

Atualmente nuestra aplicación la tenemos así

![image](https://user-images.githubusercontent.com/23094588/133378178-4cc6e342-34b6-4bac-b737-e4ca2879d527.png)

Estamos en el punto donde ya necesitamos ***Datos*** para manejar la información de nuestros Heroes que se va a desplegar en el Componente de Heroe, pudiera ser que esos ***Datos*** los tuvieramos directamente en el Componente de Heroe, pero que pasa si después tenemos otra pantalla que necesita la información de los heroes, no vamos a duplicar el código, no sería eficiente. Para eso existen los ***Servicios*** nosotros vamos a crear el servicio Heroes que sera el encargado de manejar la información referente a los Heroes de nuestra aplicación.

Los servicios tienen las siguientes características:

![image](https://user-images.githubusercontent.com/23094588/133378717-880be8b2-c1ec-48c2-88d8-b78f06a45164.png)

Los servicios nos permiten compartir la información a todo aquel que se la solicite.

![image](https://user-images.githubusercontent.com/23094588/133379040-dca66316-8503-4bdf-a331-8f2fd6f0e2f5.png)

## Creando nuestro primer servicio - HeroesService 10:55

Vamos a crear manualmente nuestro Servicio de Heroes

Vamos a crear en la carpeta **`app`** la carpeta **`servicios`** y dentro de ella vamos a crear el archivo **`heroes.service.ts`** con el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/133379618-4592a02b-45f9-4fba-9530-4b861577cf38.png)

Los servicios van decorados con **`@Injectable()`**.

Una vez creado el servicio hay que indicarle a Angular que dispone de este servicio en el **`app.module.ts`**.

![image](https://user-images.githubusercontent.com/23094588/133380051-93462e6d-e301-4be6-901a-5588d7cdce4b.png)

Los servicios se deben incluir en la sección de **`providers`**.

Ya lo unico que nos falta es usar ese servicio, esto lo haremos en la clase **`heroes.components.ts`**, el servicio lo tenemos que ***Inyectar*** en el constructor de la clase para poder usarlo

![image](https://user-images.githubusercontent.com/23094588/133380503-59d86c1c-c6a9-461e-9400-67d1975968fc.png)

Tan solo con hacer esto al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/133380625-877b144f-1922-4999-9645-1da13712899b.png)

Al inyectar el Servicio en el Componente Heroes y cargar este ultimo llama al Constructor del Servicio y nos muestra el mensaje que habíamos puesto en la consola.

Ahora en los recursos del proyecto tenemos el archivo **`data.txt`** vamos a copiar su contenido y se lo vamos a asignar a una propiedad del Servicio llamada **`heroes`** el cual es array, el código queda así:

![image](https://user-images.githubusercontent.com/23094588/133382142-82530047-c77c-437b-8c57-962619b503dd.png)

Como la propiedad **`heroes`** es privada no podemos acceder a su contenido, nos vamos a crear un método público **`getHeroes()`** para que nos retorne su valor.

![image](https://user-images.githubusercontent.com/23094588/133382194-e990c0d8-a5ef-4900-be20-4292ad68e63a.png)

Ahora nos vamos a **`heroes.component.ts`** vamos a declarar una propiedad llamada **`heroes`** que será un array y será la encargada de recibir los datos que nos devuelva el servicio, y en el método **`ngOnInit()`** que se ejecuta después de que lo hace el constructor vamos a hacer la asignación de los heroes que recibimos del servicio y los asignamos a la propiedad y los mostramos en la consola.

![image](https://user-images.githubusercontent.com/23094588/133383160-0f136282-6d68-4512-b5a2-d44a4e55de8e.png)

![image](https://user-images.githubusercontent.com/23094588/133383205-8c39675a-3d29-41d5-b066-5bd0342a147f.png)

### Crear la Interfaz de Heroes

Si vemos los Heroes tienen una estructura determinada sería bueno definirla para que todos los heroes que se lleguen a añadir la cumplan, esto lo logramos realizando una Interfaz, la vamos a crear en el servicio.

![image](https://user-images.githubusercontent.com/23094588/133383918-8c0326b3-a627-40c2-9dcf-cbdac4c77c49.png)

Y vamos a indicar que la propiedad **`heroes`** es un array de **`Heroe`** y no de **`any`** como lo teniamos hasta ahora.

![image](https://user-images.githubusercontent.com/23094588/133384127-69a392a0-e124-4fe6-8698-85125683145e.png)

Incluso en la función que regresa los Heroes podemos ser más especificos e indicar que va a regresar un array de **`Heroes`** con:

![image](https://user-images.githubusercontent.com/23094588/133384670-736e2e29-28fb-4dc6-a7a8-4cc30d6be6ff.png)

En **`heroes.component.ts`** también vamos a cambiar la propiedad **`heroes`** de tipo **`Heroe`** (Hay que importar la Interfaz).

![image](https://user-images.githubusercontent.com/23094588/133384402-9526000b-596e-4216-976d-e670809f05b8.png)

Si recargamos la APP tenemos lo mismo

![image](https://user-images.githubusercontent.com/23094588/133385452-0bf8581b-cc13-4c7d-a980-caa14f8c585d.png)


#### GIT

![image](https://user-images.githubusercontent.com/23094588/133385189-5897916b-efe7-440d-a3fc-ede5cc98de51.png)

![image](https://user-images.githubusercontent.com/23094588/133385301-5cd81832-5cc5-4930-b75d-fa1643b01f81.png)


## Página de Heroes - Diseño con **`*ngFor`** 04:57

Vamos a hacer que todos los datos de los Heroes se rendericen el componente Heroes, ya contamos en **`heroes.component.ts`** con la propiedad **`heroes`** que contiene sus valores, vamos a usarla dentro del HTML **`heroes.component.html`** usando la directiva **`*ngFor`**, empecemos por meterla y asignar la imagen.

![image](https://user-images.githubusercontent.com/23094588/133386791-12d57cb6-9a41-45c2-9ba4-19602b11d0b3.png)

Al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/133386851-03d733fc-0f21-445e-8b94-bcc403532b0c.png)

![image](https://user-images.githubusercontent.com/23094588/133386889-20b7c956-fb8f-4a05-b4b7-23785b8b83fc.png)

La interpolación es una forma de poner el valor de la imagen, pero existe otra forma de indicarlo para que lo maneje Angular, como sigue:

![image](https://user-images.githubusercontent.com/23094588/133483745-b0a78bb1-3f3d-445d-b934-c5449a005617.png)

El resultado es el mismo:

![image](https://user-images.githubusercontent.com/23094588/133386851-03d733fc-0f21-445e-8b94-bcc403532b0c.png)

![image](https://user-images.githubusercontent.com/23094588/133386889-20b7c956-fb8f-4a05-b4b7-23785b8b83fc.png)

Vamos a cargar los demás datos, en algunos de ellos no nos queda más que usar la interpolación.

![image](https://user-images.githubusercontent.com/23094588/133484560-dd845c7b-bc97-4f6e-9fe9-1d068a581fcf.png)

El resultado es el siguiente:

![image](https://user-images.githubusercontent.com/23094588/133484627-5146c06e-0d3e-4a30-9f4f-ffabc6d792b7.png)

![image](https://user-images.githubusercontent.com/23094588/133484681-21d2bd00-27db-4a62-a6e4-4f942ecbeb89.png)

![image](https://user-images.githubusercontent.com/23094588/133484728-be963739-521b-4b26-bb45-662fa95639bf.png)

**`NOTA:`** Con Bootstrap v.4 se conseguia un efecto "Pinteres" en las tarjetas, con Bootstrap v.5 no lo he conseguido replicar.

![image](https://user-images.githubusercontent.com/23094588/133485011-1eb32185-2c0e-473a-9090-2a9456de2533.png)

Con la Vista de Móvil se ve así:

![image](https://user-images.githubusercontent.com/23094588/133485371-529aa41f-1f1c-4f85-b26f-14559848d090.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133485837-9d4c15d5-e265-4284-832a-6e7d9a59bdf5.png)


## Rutas con parametros - Router 09:12

En esta lección vamos a hacer que cuando pulsemos el botón de cada Heroe se vaya al detalle.

### Creación del Componente `Heroe`

Vamos a crear el componente que nos va a servir como detalle del Heroe.

![image](https://user-images.githubusercontent.com/23094588/133487072-48abeb3c-9cff-4eaa-9e89-223a6c678c61.png)

### Ruta hacía el Heroe

Debemos añadir una ruta hacia el Heroe que desemos, por lo que para distingirlo necesitamos un parámetro para saber a que Heroe debemos ir, vamos al archivo **`app.routes.ts`**.

![image](https://user-images.githubusercontent.com/23094588/133487959-a12c274e-578b-41d6-80be-0394ae9b948f.png)

Observese que con **`:id`** se pasan el parámetro.

### Invocar la Ruta con Parámetros

Existen dos formas de invocar las Rutas con un botón o con un enlace. Vamos a empezar por ver usando un enlace, por lo cual comentamos el botón que hemos puesto en **`heroes.component.html`** y ponemos el enlace como sigue:

![image](https://user-images.githubusercontent.com/23094588/133491866-411b04bc-b838-419d-872a-72800b67622b.png)

Como podemos observar la ruta que invocamos ya tiene dos partes y como habíamos hablado antes cada parte es un elemento del array que pasamos como parámetros. **`[routerLink]="['heroe', i]"`**, el primero es la ruta que definimos **`heroe`** y el segundo es el elemto a donde nos queremos ir **`i`**, en este caso estamos usando la **`i`** que tiene el valor del **`index`** y nos sirve para indiocar a que elemento deseamos movernos.

En teoría ya debería funcionar, vamos a probarlo.

![image](https://user-images.githubusercontent.com/23094588/133489265-311971b0-c35d-40b1-a2cc-752ac96e4e9f.png)

Al pulsar sobre algún Heroe siempre se va a la página Home.

![image](https://user-images.githubusercontent.com/23094588/133489741-4a164577-8cf1-48b8-aea4-1e96147786eb.png)

**¿Por qué no me redirecciona bien?**

Cuando usamos este tipo de sintaxis **`[routerLink]="['heroe', i]"`** y recordemos que estamos dentro de un **`Router Outlet`**, es decir estamos en una subpagina, ***necesitamos movernos a la raíz***, si yo cargo manualmente la ruta **`http://localhost:4200/heroe/1`** si se carga la página.

![image](https://user-images.githubusercontent.com/23094588/133491959-55e1a693-270e-4c92-b062-838d2b4a649d.png)

Una posible solución es indicar en la ruta toda la ruta completa que sigue para llegar a esta página.

![image](https://user-images.githubusercontent.com/23094588/133492512-704b2f99-a24f-41a0-92d6-b26da2557ba5.png)

![image](https://user-images.githubusercontent.com/23094588/133492599-b089e7e8-94e4-4ba0-a1fe-33accc7a6d4b.png)

Así trabaja pero la ruta nos queda así **`http://localhost:4200/heroes/heroe/0`** por que le esta haciendo un append a la ruta por que ya estamos en ese lugar, existe otra opción que nos permite no movernos a una sub-página, primero dejamos la ruta como la teniamos inicialmente en **`app.routes.ts`** y en **`heroes.component.html`** ponemos la ruta con una barra es decir **`[routerLink]="['/heroe', i]"`**.

![image](https://user-images.githubusercontent.com/23094588/134719124-499c68d1-dc33-4aac-b8db-e93107696d40.png)

Ahora si cargamos http://localhost:4200/heroes vemos la lista de los Heroes donde podemos pulsar el botón de cada uno de ellos:

![image](https://user-images.githubusercontent.com/23094588/134719261-59e70ed6-f1b9-4659-a975-c5d350ebadb4.png)

![image](https://user-images.githubusercontent.com/23094588/134719301-ff4773b7-7b3b-446d-b21d-e98d2054416c.png)

![image](https://user-images.githubusercontent.com/23094588/134719339-2d4524d6-4601-48f6-bb44-806abd4318cb.png)

![image](https://user-images.githubusercontent.com/23094588/134719390-f04001e4-72db-49d5-9494-bd5cc9396f54.png)

Como vemos se desplaza al heroe que pulsemos, falta el diseño de la página Heroe, ***esto lo hemos hecho mediante código de programación pero falta ver como lo hacemos mediante un `routerLink`***. 

Si queremos usar el botón que debería invocar algún método de nuestro Controlador y llamarlo. Vamos a comentar el enlace y descomentar el botón con el siguiente código en **`heroes.component.html`**:

![image](https://user-images.githubusercontent.com/23094588/134720307-0893a6a2-2e9d-4389-ba65-d55e85e81421.png)

Ahora vamos a crear el método **`verHeroe(index)`** en el Componente **`heroes.component.ts`** con el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/134720668-df4bb804-74d5-4e78-9e1a-31db104c5290.png)

Al llamar al Heroe en la consola nos imprime su indice:

![image](https://user-images.githubusercontent.com/23094588/134720817-1f01f298-e3e2-4538-9152-f15bf42bfa8f.png)

He presionado en los tres primeros heroes y vemos como nos indica el indice asociado a cada uno de ellos, lo que realmente tiene que hacer es redireccionar a cada uno de los heroes. Como esto ya tiene que ver con las rutas dentro del Componente **`heroes.component.ts`** debemos primero importar el **`Router`**, el cual para poderlo usar lo inyectamos en el Constructor y en nuestro método **`verHeroe(index)`** vamos a incluir la instrocción **`this.router.navigate( ['/heroe', index] );`**, con la cual estamos indicando que debemos navegar a la dirección que le pongamos como parámetro, recordemos que esta dirección se le indica como array en este caso es **`['/heroe', index]`** que formaran la parte final de la ruta **`http://localhost:4200/heroe/1`** es decir **`/heroe/1`**, recordemos cada elemento del array es una parte de la ruta marcada por la diagonal **`/`**.

![image](https://user-images.githubusercontent.com/23094588/134722028-9a5c9d6a-2220-45e5-a19e-52446ec228a3.png)

Ahora si pulsamos en el botón me redirecciona al Heroe seleccionado:

![image](https://user-images.githubusercontent.com/23094588/134722123-ff94803e-a483-403c-a727-33679307e8eb.png)

![image](https://user-images.githubusercontent.com/23094588/134722159-f9f4a566-b868-44ac-8a08-85a7a1433bf6.png)

#### GIT 

![image](https://user-images.githubusercontent.com/23094588/134722393-5f670b9c-5e37-4fc8-b4c7-a62f7470efd2.png)

## Recibiendo parámetros por URL - ActivatedRoute 06:53

Ahora vamos a trabajar dentro del Componente **`heroe.component.ts`** que es el que debe hacer manejo del parámetro que se esta mandando en la URL. 

Para recuperar el parámetro que viene en el URL necesitamos usar el **`ActivatedRoute`**, el cual importamos e inyectamos en el Constructor, y dentro del mismo constructor vamos a hacer la códificación para recuperar el parámetro usando **`this.activatedRoute.params`**, el cual regresa un **"Observador"**, para usarlo nosotros necesitamos suscribirnos a ese Observador con el método **`this.activatedRoute.params.subscribe`** dentro del cual ya nos regresa los parámetros (le ponemos el nombre que queremos por ejemplo **`params`**) y usamos una función de flecha para manipular los parámetros que recibamos.

![image](https://user-images.githubusercontent.com/23094588/134723733-b014e832-e429-4b98-882a-6cc5ca8dd179.png)

Si recargamos la APP y cargamos el primer Heroe vamos atener:

![image](https://user-images.githubusercontent.com/23094588/134723848-c3be9a92-234c-445b-988c-6c5adc7f5e6d.png)

Esta recuperando un **Objeto** el cual contiene **`{id: '0'}`** es el Cero que se recupera de la URL **`http://localhost:4200/heroe/0`** y el **`id`** aparece por que en el **`app.routes.ts`** pusimos **`{ path: 'heroe/:id', component: HeroeComponent },`**, ***tengan presente que siempre se van a recibir Strings***, para recuperar solo el valor del **`id`**, podemos hacerlo con **`params.id`**, pero como Angular no sabe que realmente el objeto **`params`** tiene un **`id`** una forma más segura es usar **`params['id']`**.

![image](https://user-images.githubusercontent.com/23094588/134724329-337d3948-1661-472f-aeac-e292882df619.png)

![image](https://user-images.githubusercontent.com/23094588/134724372-84c6a712-e9fa-4449-b63d-6636c5d9fb51.png)

De esta manera ya solo recuperamos el valor **`0`** (como String).

### Añadir `getHeroe` en el Servicio

Para recuperar un Heroe por medio de su identificador o indice necesitamos tener un método que lo recupere en el Servicio, vamos a **`heroes.service.ts`** y vamos a añadir el método **`getHeroe`**:

![image](https://user-images.githubusercontent.com/23094588/134725231-5a6d6f9e-d435-44a6-8ef1-3ceed0d839af.png)

Se queja por que en el Array estoy poniendo como indice un tipo String, vamos a dejarlo así de momento, como hay error en la compilación lo he cambiado a:

![image](https://user-images.githubusercontent.com/23094588/134901604-bd0d015c-815f-4067-a0c5-11cd4a371e30.png)

regresamos al Componente **`heroes.component.ts`** , donde vamos a crear un atributo **`heroe`** por el momento de tipo **`any`** que será la variable local para mostrarla en el Template, tenemos que importar el servicio **`HeroesService`** para llamar al método **`getHeroe`** recien creado, lo inyectamos en el Constructor y ya podemos asignar al atributo **`heroe`** lo que nos retorne el método  **`getHeroe`** del Servicio, por ahora simplemente lo vamos a mostrar en la consola.

![image](https://user-images.githubusercontent.com/23094588/134903156-efadad45-90b3-42cb-971b-6d8dea1be1e3.png)

Al cargar alguno de los Heroes tenemos:

![image](https://user-images.githubusercontent.com/23094588/134903409-f021dab1-7ac5-475a-83e8-3389d440b74d.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/134903790-92c17f03-44de-4b97-9298-ae0cab1a21cf.png)

## Tarea práctica #1 - Componente del héroe 02:50

Vamos a crear la página del Heroe donde pinte la información correspondiente a cada Heroe, debemos añadir dos imagenes que nos sirven para identificar la casa a la que pertenece cada heroe **`marvel-logo.png`** y **`dc-logo.jpg`**.

## Resolución de la tarea práctica #1 - Componente del héroe 05:14

Vamos a ir al template del Heroe **`heroe.component.html`** y vamos a añadir el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/135751479-acaccd63-1716-4387-b572-d7b426312626.png)

Estamos obteniendo la información del Heroe con las interpolaciones. Como las imágenes son de diferentes tamaños vamos a añadir un estilo en **`styles.css`**:

![image](https://user-images.githubusercontent.com/23094588/135751541-97303d1b-1433-47cd-8fec-86e05d2cf2be.png)

Al probar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/135751613-ccb498fc-05e7-4589-9289-83816bfac343.png)

![image](https://user-images.githubusercontent.com/23094588/135751623-9ff1c8ae-3efb-4465-9afd-54b6b805f4de.png)

![image](https://user-images.githubusercontent.com/23094588/135751632-fc193d0c-4644-495a-88af-c44d17760f4d.png)

![image](https://user-images.githubusercontent.com/23094588/135751644-ab25bda5-9d23-45bb-a5ab-beb563d1f5e5.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/135751674-b0d695a6-49aa-4df6-b59e-7270e3d5a226.png)


## Pipes: Transformación visual de la data. 03:20

Los **Pipes** nos permiten transformar la forma en que visualizamos los datos, ***no cambian el valor***, simplemente se visualiza de forma diferente, los Pipes disponibles son:

![image](https://user-images.githubusercontent.com/23094588/135751961-562a7650-ab5a-4088-ba13-3b4f02f214bb.png)

Por ejemplo en el template del Heroe estamos mostrando el título así:

![image](https://user-images.githubusercontent.com/23094588/135751814-b7c4da22-da41-4abf-b36b-da8ad9f41acf.png)

Puede ser que queramos que el nombre del Heroe siempre se vea Capitalizado y en la fecha solo mostrar el año, lo realizamos apliacando los Pipes **` uppercase`** y **`date`** como sigue:

![image](https://user-images.githubusercontent.com/23094588/135752140-ebbc171b-c3ab-400a-9b86-0af8dfcf0f27.png)

Al visualizar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/135752157-368d1aec-82f1-4649-85db-50c6969f5c0c.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/135752177-ccbe5bc2-f89e-4c08-8e71-592c4b540913.png)


## Buscador de Héroes 06:14

En esta lección vamos a aplicar la funcionalidad del Search o Buscador que tenemos en la cabecera. Nos vamos al Navbar Component **`navbar.component.html`** que esta dentro de la carpeta **`shared`**, lo primero que vamos a hacer es cambiar **`Search`** por **`Buscar`**.

![image](https://user-images.githubusercontent.com/23094588/135752322-d613c8cd-1ce7-45a3-8744-85a919a06904.png)

Lo que queremos es que cuando escribamos en el campo de texto se dispare un evento que vaya a buscar lo que escribimos a la lista de los Héroes para localizarlos. Como podemos observar el campo de texto y el botón estan dentro de un Formulario, por el momento no vamos a usar el Submit del formulario, solo queremos recuperar el valor de la caja de texto podemos hacer referencia al objeto usando la sintaxis: **`#textoABuscar`** y que cuando pulsemos y soltemos el ***Enter*** se dispare un evento que invoca la función **`buscarHeroe(...)`** en la cual vamos a mandarle el contenido de la caja de texto con **`textoABuscar.value`** todo completo nos queda así: **`(keyup.enter)=buscarHeroe(textoABuscar.value)`**.

El botón lo cambiamos de un **`submit`** a un **`button`** normal para que no haga in submit involuntario.

![image](https://user-images.githubusercontent.com/23094588/136665263-012fb2e4-4b6e-4be9-8e7e-b691651d815b.png)

Ahora vamos a crear la función **`buscarHeroe(...)`** en **`navbar.component.ts`** 

![image](https://user-images.githubusercontent.com/23094588/136665295-b0b65b86-562d-45c1-adbd-49c391a383a5.png)

Si probamos la APP nos vamos a encontrar con ciertos problemas, ya que al pulsar Enter nos sigue submitando la página, hemos tenido que cambiar la **`form`** por una **`div`**, además de invocar el evento **`click`** en el botón para que funcione(esto también se hace si usamos **`form`**), el código nos queda así:

![image](https://user-images.githubusercontent.com/23094588/136929140-856d2570-f6ad-4ff0-8ad6-8c98d8dfca27.png)

Al probar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/136929450-c026e3de-d10f-4242-a419-0cb751c03ecd.png)

Hemos probado dando Enter y después pulsando el botón y todo ha ido bien.

Ahora tenemos que modificar el Servicio **`heroes.service.ts`** para que búsque el Heroe solicitado, tenemos que añadr un nuevo método que llamaremos **`buscarHeroes(...)`** con el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/136933104-7d549647-8506-4509-8bc6-207d286c3d29.png)

Para probar este nuevo método del servicio lo vamos a invocar desde nuestro componente **`navbar.component.ts`**, como sigue:

![image](https://user-images.githubusercontent.com/23094588/136934529-3d333919-0822-408c-bea0-1a650b15955b.png)

Hemos tenido que importar el Servicio **`HeroesService`** y **`Heroe`**, inyectamos **`HeroesService`** en el constructor y apartir de allí ya podemos usar el nuevo método creado **`buscarHeroes(...)`** para el termino que introduzcamos. Al probar la APP tenemos lo siguiente con las diferentes búsquedas que hemos realizado **`a`**, **`spiderman`** y **`spider`**:

![image](https://user-images.githubusercontent.com/23094588/136934888-4b3ee0fe-5601-41fa-852e-da387ca65e05.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/136935144-c1338c6c-62c3-432f-a386-3810f0f1dfc1.png)

## Tarea práctica #2: Crear la pantalla de búsqueda de héroes. 02:02

En esta tarea vamos a crear un nuevo componente que será el encargado de leer el **`termino`** y en su método **`ngOnInit`** vamos a poner la lógica para ejecutar la función **`buscarHeroes(...)`**, es decir en nuestro **`navbar.component.ts`** en su función **`buscarHeroe(...)`** lo único que vamos a hacer es redireccionarlo a ese nuevo componente, por lo que todo el código que hicimos antes para probar el método **`buscarHeroes(...)`** realmente debe ir en el nuevo componente.

## Resolución de la tarea 2 - Buscador de Héroes 07:55

Para crear el nuevo componente vamos a usar el comando:

```sh
ng g c components/buscador -is
```

El **`-is`** me sirve para que no cree el archivo de estilos.

![image](https://user-images.githubusercontent.com/23094588/136936540-847815e9-efdb-4f6f-a992-1b7e9de47642.png)

![image](https://user-images.githubusercontent.com/23094588/136936694-1454d570-f402-424d-b34b-1a3369a039cf.png)

Podemos eliminar el archivo **`buscador.component.spec.ts`**.

### Añadir la Nueva Ruta

En el archivo **`app.routes.ts`** vamos a añadir la nueva ruta:

![image](https://user-images.githubusercontent.com/23094588/136941485-2fac1710-9ef0-4bce-a635-e7b3eefba13a.png)

### Capturar parámetro de la URL

Vamos a nuestro componente **`buscador.component.ts`**, como queremos capturar el parámetro que viaja en la URL necesitamos importar el **`ActivatedRoute`** y lo inyectamos en el constructor, para recuperar su valor lo vamos a hacer dentro del método **`ngOnInit`** suscribiendonos a los parámetros del **`ActivatedRoute`** como sigue:

![image](https://user-images.githubusercontent.com/23094588/136938437-a107e994-9cd2-4c3c-813f-66315aee6198.png)

### Hacer Redirección al Componente `buscador.component.ts`

Vamos a hacer la redirección desde el NavBar al nuevo Componente Buscardor, nos vamos a **`navbar.component.ts`** lo primero que vamos a hacer es quitar todo lo que habíamos puesto para invocar el Servicio de Buscar Heroes ya que esto ira en el nuevo componente Buscador. Una vemos hecho esto debemos importar el **`Router`** para podernos mover entre páginas y lo inyectamos en el Constructor.

En el método **`buscarHeroe`** donde recibimos el termino a buscar vamos a hacer la redirección con **`this.router.navigate`** el cual recibe un arreglo de la ruta relativo a donde estamos por eso vamos a poner **`/`**, recordemos que en la Ruta **`app.routes.ts`** le pusimos **`buscar/:termino`** por lo que el array que tenemos que poner es **`['/buscar', termino]`**, todo completo queda así: **`this.router.navigate( ['/buscar', termino])`**, sería interesante hacer una validación de que el **`termino`** tiene al menos un carácter antes de hacer la redirección, pero esto es suficiente para disparar la búsqueda:

![image](https://user-images.githubusercontent.com/23094588/136940657-53dc7511-3cb6-44e1-ac01-4798148c2088.png)

Si probamos la APP tenemos que al buscar algún termino y pulsar Enter o Click sobre el botón nos redirigue al componente **`buscador`** cuya URL definimos como http://localhost:4200/buscar/Hulk, observar que el termino a buscar viaja en la URL y ese valor lo recuperamos en el componente **`buscador`** y lo imprimimos en la consola.

![image](https://user-images.githubusercontent.com/23094588/136941554-f91b0fc9-4fc8-4ff1-98f9-4c820b34e541.png)

![image](https://user-images.githubusercontent.com/23094588/136941593-f9b45d4b-14ae-485f-b51f-28ef8fb1eec6.png)

### Usar el Servicio para recuperar la Busqueda de Heroes

Vamos a importar el servicio **`HeroesService`** e inyectarlo en el constructor. 

Vamos a crear una variable local **`heroes:any[] = []`** donde almacenemos los Hereos localizados según el termino de busqueda.

![image](https://user-images.githubusercontent.com/23094588/136943105-2a028df5-c785-4bad-b657-fe1b3d199b5e.png)

Al probar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/136943257-66fe3260-8ca8-4c4a-bf06-06cb52143ae1.png)

![image](https://user-images.githubusercontent.com/23094588/136943299-06baea7b-a4ad-4298-9311-c105476632aa.png)

Localiza los Heroes según el termino que introduzcamos.

### Crear el HTML del componente `buscador`

Para crear el template del componente **`buscador`** vamos practicamente a copiar el que tenemos en el componente **`heroes.component.html`**, solo tenemos que hacer pequeños cambios vamos a modificar **`<h1>Héroes <small>Marvel y DC</small></h1>`** por **`<h1>Buscando <small>{{ termino }}</small></h1>`**, por lo cual debemos añadir la propiedad **`termino`** a nuestro comoponente **`buscador.component.ts`**, además de esto nos esta marcando un error en evento **`(click)="verHeroe(i)"`** del botón ya que nosotros no tenemos implementada esa función en **`buscador.component.ts`** así que la copiamos de **`heroes.component.ts`**, por lo que el componente **`buscador.component.ts`** final nos queda así:

![image](https://user-images.githubusercontent.com/23094588/136945526-348e7c66-1f61-49cb-bf0c-2bf04c6a7a73.png)

![image](https://user-images.githubusercontent.com/23094588/136945670-8b9383f8-833a-45c6-a7b4-50c0695b3c3f.png)

Al probar la APP tenemos:


![image](https://user-images.githubusercontent.com/23094588/136945794-59129322-d8f4-483f-9eca-f76e076ec814.png)

![image](https://user-images.githubusercontent.com/23094588/136945861-b29f4589-92fb-45db-ab99-37f4f1986846.png)

![image](https://user-images.githubusercontent.com/23094588/136945944-85b9faca-72f4-4dba-8b40-7774e6e1465d.png)

### Consideraciones

Si no buscamos nada se presentan todos los Heroes.

![image](https://user-images.githubusercontent.com/23094588/136946118-baf38406-aaf3-4e6d-af10-782f5d663a1a.png)

Si buscamos un Heroe en particular y luego pulsamos en su Detalle nos lleva a otro diferente, esto es por que estamos usando los índices para movernos entre ellos y al hacer una búsqueda y recuperar menos heroes que el total los indices ya no coinciden y provoca este error.

![image](https://user-images.githubusercontent.com/23094588/136946439-04052d6e-4fae-451c-88d0-d1b667b02666.png)

![image](https://user-images.githubusercontent.com/23094588/136946504-ee32c7d6-cf6e-48a5-9b25-cf6bfe72af72.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/136946762-878fd4ae-fa53-410d-b2c3-e4a1c7afa744.png)

## Plus: Mostrando un mensaje cuando no hay resultados. 02:01
## `@Input` - Recibir información de un componente padre a un hijo 10:38
## `@Output` - Emitir un evento del hijo hacia el padre 05:40
## Arreglar detalles de la búsqueda 05:50
## Código fuente de la sección 00:24
https://www.comunidad.madrid/servicios/salud/vacunacion-frente-coronavirus-comunidad-madrid
