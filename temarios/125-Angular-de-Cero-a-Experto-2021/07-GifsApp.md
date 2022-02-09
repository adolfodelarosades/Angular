# 07 GifsApp - Aplicación para buscar imágenes - • 20 clases • 2h 7m

* Introducción a la sección 02:58
* Temas puntuales de la sección 00:17
* Demostración del objetivo final de la sección 02:01
* Inicio de proyecto - GifsApp 04:59
* Diseño inicial de nuestra aplicación de Gifs 08:04
* Módulo Shared 07:39
* GifsModule y sus componentes 07:17
* **`@ViewChild`** - Obtener referencias a objetos del HTML 11:57
* GifsService 11:09
* Controlar el historial de búsquedas 06:57
* Giphy Api Key - Giphy Developers 07:14
* Realizar una petición HTTP 08:34
* Mostrar los resultados en pantalla 09:15
* Colocando un tipado a las peticiones **`http`** 09:47
* **`LocalStorage`** 10:25
* Cargar imágenes automáticamente 04:42
* Obtener imágenes desde el sidebar 03:31
* **`HttpParams`** 06:40
* Animate.style CSS 03:43
* Código fuente de la sección 00:07

## Introducción a la sección 02:58

En esta sección vamos a desarrollar una APP un poco más compleja, vamos a consumir un Servicio que nos va a regresar unas imágenes que vamos a manipular, tendremos un buscador, vamos a mantener información en el **`LocalStorage`** para mantener información persistente en el **`LocalStorage`**, ver cuales son las diferencias entre el **`LocalStorage`** y el **`SessionStorage`**, trabajaremos en base a módulos, consumiremos el API que es muy utilizado por Facebook, WhatsUp, Instragram, etc que nos retorna unos GIFs para poder usarlas en la aplicación, veremos para que sirve el **`@ViewChild`**, uso del paquete **`http`** y  **`observables`**. 

En la APP que construiremos veremos como consumir información del Servicio, como tomamos esa información y la mostramos, como reutilizamos componentes, como mandamos información a componentes.  

## Temas puntuales de la sección 00:17

#### ¿Qué veremos en esta sección?

La sección contendrá nuestra primera aplicación real de Angular, este es un breve listado de los temas fundamentales:

1. Modularización de la aplicación
2. Estructura de la aplicación de media a gran escapa
3. Componentes
4. **`@ViewChild`**
5. Servicios
6. Historial de búsquedas
7. Uso de Api Keys
8. **`LocalStorage`**
9. Peticiones HTTP
10. Animaciones mediante css

Recuerden que siempre tienen el código fuente al final de la sección para que lo puedan descargar y comparar contra el suyo en caso de que sea necesario.

## Demostración del objetivo final de la sección 02:01

Vamos a crear una APP que nos va permitir conectarnos a [GIPHY Developers](https://developers.giphy.com/)

![image](https://user-images.githubusercontent.com/23094588/153027383-3aaee3f5-6853-43ab-a2aa-2d37cc7c6303.png)

que es muy utilizado por Facebook, WhatsUp, Instragram, etc. para mostrar GIFs en sus aplicaciones.

Nuestra APP va a quedar parecida a la siguiente pantalla.

![image](https://user-images.githubusercontent.com/23094588/153040244-4c1fce7a-f560-4d46-a079-b1fdff8bbeb8.png)

Vemos que tenemos un Buscador y un Historial con las últimas 10 búsquedas, al recargar la página la información es persistente con la última búsqueda o el último historial seleccionado, tenemos limitado hasta 10 los resultados, nuestra APP aunque es sencilla va a ser modularizada con un módulo **`shared`** con un **`sidebar`**, un módulo **`gifs`** con nuestros componentes, servicios e interfaces, 

## Inicio de proyecto - GifsApp 04:59

En esta lección vamos a crear un nuevo proyecto en la ubicación de nuestros proyectos Angular pulsando el siguiente comando:

```sh
ng new gifsApp
```

![image](https://user-images.githubusercontent.com/23094588/153157360-125d1e6b-853d-410d-a7a4-769c40e2790f.png)

Me pregunta si queremos incorporar el Routing le vamos a decir que No.

Luego nos pregunta el CSS que vamos a usar dejamos la opción por defecto CSS.

Comienza la creación del proyecto.

![image](https://user-images.githubusercontent.com/23094588/153159186-e29cc677-1f2d-4639-b6d2-137a6348bc33.png)

Una vez finalizado vamos a renombrar la carpeta **`gifsApp`** por **`125-02-gifsApp`**.

![image](https://user-images.githubusercontent.com/23094588/153160060-e202ed63-95d3-4269-8076-9d2c96df4964.png)

En la consola vamos a entrar al proyecto **`125-02-gifsApp`** y ya vemos que tenemos el primer commit implicito.

![image](https://user-images.githubusercontent.com/23094588/153161702-ea5ed629-7e6c-4633-aff4-14e0cacc39ee.png)

Vamos a arrancar el servidor con:

```sh
ng serve -o
```

Y ya tenemos arrancada nuestra APP

![image](https://user-images.githubusercontent.com/23094588/153162644-411393e1-2f49-4c9d-b8e8-560571168666.png)

### Bootstrap

Abrimos esta carpeta en VSC.

Vamos a usar la versión 5 de Bootstrap, lo vamos a hacer de la forma más sencilla, vamos ir a la página de [Bootstrap](https://getbootstrap.com/)

![image](https://user-images.githubusercontent.com/23094588/153160583-eb5b3d0e-8498-4444-b6f0-fe95afe9ac42.png)

Vamos a pulsar el botón **`Get started`**

![image](https://user-images.githubusercontent.com/23094588/153160805-9dfe4f95-3921-49e8-ae3f-f744d0ab762c.png)

Vamos a copiar el link de CSS

```css
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
```

y lo vamos a insertar en el archivo **`index.html`** 

![image](https://user-images.githubusercontent.com/23094588/153161916-f5d53efa-a0a2-4266-b178-bb0e55fade6e.png)

Vamos a persibir un pequeño cambio en la presentación de la APP.

Antes de Bootstrap

![image](https://user-images.githubusercontent.com/23094588/153162644-411393e1-2f49-4c9d-b8e8-560571168666.png)

Después de Bootstrap

![image](https://user-images.githubusercontent.com/23094588/153162996-efb4de2d-7420-4c99-834b-d82843dc198a.png)

Para persibir mejor Bootstrap vamos a **`app.component.html`** y sustituimos su contenido por:

```html
<h1>Hola Mundo</h1>
```

![image](https://user-images.githubusercontent.com/23094588/153165016-4b120396-81a1-4bdf-ac2b-2ef75a393d34.png)

Es todo lo que vamos a hacer en esta lección.

### GIT

![image](https://user-images.githubusercontent.com/23094588/153165408-3ab5ec72-5171-4bbf-aa3e-f3ce0f6f70a8.png)

## Diseño inicial de nuestra aplicación de Gifs 08:04

En esta lección vamos a crear la estructura del diseño de nuestra APP con HTML clásico, en otras lecciones vamos ya a estructurarlo con Angular con los diferentes módulos y los diferentes componentes, pero en esta lección vamos a comenzar de la manera más básica.

En el **`app.component.html`** vamos a hacer este diseño que va a tener un menú lateral

La clase **`d-flex`** de Bootstrap nos permite usar el Flex Box en el contenedor que tenga esta clase, por ejemplo:

![image](https://user-images.githubusercontent.com/23094588/153170009-46a9a34e-a661-449e-bc3a-08469330f247.png)

![image](https://user-images.githubusercontent.com/23094588/153170119-5cb5ad2b-b6d3-48ad-8bf1-4a37351a439f.png)

Los dos **`<div>`** estan unidos, no tienen el clasico salto en cada sección gracias a la clase **`d-flex`**.

Una alternativa a la clase **`d-flex`** podría ser usar **`row`** y **`col`**.

El primer **`<div class="d-flex">`** va a ser mi menú latera.

### Construcción del SideBar

La clase **`bg-dark`** de Bootstrap nos pone un fondo oscuro.
La clase **`border-right`** de Bootstrap nos pone un borde a la derecha.
La clase **`p-3`** de Bootstrap nos un padding de 3px.
La clase **`text-ligth`** de Bootstrap nos pone el texto en blanco.

En **`app.component.html`** vamos a meter el siguiente código.

![image](https://user-images.githubusercontent.com/23094588/153171777-7b53fb50-9b88-434f-a800-ae66090b2c2a.png)

![image](https://user-images.githubusercontent.com/23094588/153171991-8928a894-d318-42f9-bf4a-e96238d43854.png)

Lo que necesitamos es que nuestro SideBar se extienda hasta el final de la pantalla, eso lo vamos a hacer con CSS en el archivo **`styles.css`**.

![image](https://user-images.githubusercontent.com/23094588/153175454-fc7d949f-ef02-49e6-b233-49c6ac1164a3.png)

Indicamos que el **`html`** y **`body`** van a tener un alto del 100%.

Por otro lado damos un estilo personalizado a la etiqueteta que tenga **`id="sidebar"`** el cual tiene un alto del 100% y el tamaño minimo de alto (vertical) va a ser todo lo que este en la pantalla y también damos un ancho mínimo fijo de 180px (no es responsive).

![image](https://user-images.githubusercontent.com/23094588/153175634-2604ca11-57bf-4bf8-a004-802340b0eabe.png)

En el SideBar vamos a tener el Historial de lo que vayamos buscando, vamos a añadirlo.

La clase **`list-group`** de Bootstrap nos .
La clase **`list-reset`** de Bootstrap elimina los bullepoints.

![image](https://user-images.githubusercontent.com/23094588/153176582-1ff0902e-2e3e-44a5-a206-231983ce7c26.png)

![image](https://user-images.githubusercontent.com/23094588/153176729-3a8bf3ce-7991-4beb-93f8-7778643e0025.png)

Vamos a cambiar la apariencia del enlace añadiendole unas clases.

La clase **`list-group-item`** de Bootstrap nospermite indicar que es un item del grupo.
La clase **`list-group-item-action`** de Bootstrap nos permite hacer click en el elemento.

![image](https://user-images.githubusercontent.com/23094588/153177483-2d660c52-efb2-4096-a2b7-1cf3344759b4.png)

![image](https://user-images.githubusercontent.com/23094588/153177555-273c4f02-7746-4a92-9358-f27ca7b2742f.png)

Vamos a añadir una línea de separación entre el título y los items del SideBar.

La clase **`text-white`** al igual que la clase **`text-ligth`** de Bootstrap nos pone el texto en blanco.

![image](https://user-images.githubusercontent.com/23094588/153177991-5076d7e2-e8a7-412d-b001-264379eec25a.png)

![image](https://user-images.githubusercontent.com/23094588/153178030-c607b073-408c-406c-8c07-e65f69ee6514.png)

La idea es tener varios historiales que hayamos buscado.

![image](https://user-images.githubusercontent.com/23094588/153178455-9eafafae-fa4f-4c45-b91d-4a390393d417.png)

Hasta aquí ya tenemos todo nuestro SideBar.

![image](https://user-images.githubusercontent.com/23094588/153178769-d652be32-764b-4309-aaad-184fa4d23d8a.png)

### Construcción del Contenedor Principal

La clase **`container`** de Bootstrap .
La clase **`row`** de Bootstrap crea una fila.
La clase **`col`** de Bootstrap crea una nueva columna.
La clase **`form-control`** de Bootstrap .

**Short Cut al escribir `.row` + tecla `TAB` nos aparece `<div class="row"></div>`**.

El Contenedor Principal va a tener en la parte superior un Buscador, insertemos en siguiente código.

![image](https://user-images.githubusercontent.com/23094588/153180348-de0af341-6288-4679-8c40-a968776468b9.png)

![image](https://user-images.githubusercontent.com/23094588/153180239-214ab16a-7600-45fc-87b5-acb1fdae81e5.png)

En la parte posterior del Buscador vamos a añadir una línea de separación y después otra fila con un contenido Lorem...

![image](https://user-images.githubusercontent.com/23094588/153181049-5fb3e4ed-4999-4126-8909-9267b4380fb7.png)

![image](https://user-images.githubusercontent.com/23094588/153181122-c73bfeab-e400-492c-bc8a-bf07589c2e1a.png)


Este es el diseño que vamos a manejar en nuestra APP, es un diseño sencillo pero que nos vale para esta APP.

### GIT

![image](https://user-images.githubusercontent.com/23094588/153181521-0d9219f1-206f-4d1e-a5d9-6a509ef6ec7f.png)

## Módulo Shared 07:39

**``**

## GifsModule y sus componentes 07:17
## **`@ViewChild`** - Obtener referencias a objetos del HTML 11:57
## GifsService 11:09
## Controlar el historial de búsquedas 06:57
## Giphy Api Key - Giphy Developers 07:14
## Realizar una petición HTTP 08:34
## Mostrar los resultados en pantalla 09:15
## Colocando un tipado a las peticiones **`http`** 09:47
## **`LocalStorage`** 10:25
## Cargar imágenes automáticamente 04:42
## Obtener imágenes desde el sidebar 03:31
## **`HttpParams`** 06:40
## Animate.style CSS 03:43
## Código fuente de la sección 00:07

