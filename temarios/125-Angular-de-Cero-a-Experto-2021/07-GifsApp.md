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

![image](https://user-images.githubusercontent.com/23094588/153181860-f138497f-bb85-4903-a16f-30ed23add9b7.png)

![image](https://user-images.githubusercontent.com/23094588/153181955-9528d382-8761-43ae-9046-af5d00f085f5.png)

![image](https://user-images.githubusercontent.com/23094588/153181521-0d9219f1-206f-4d1e-a5d9-6a509ef6ec7f.png)

## Módulo Shared 07:39

En la lección anterior metimos todo nuestro diseño en el **`app.component.html`**, pero una aplicación Angular deberíamos tenerla segmentada en componentes que realicen pequeñas tareas, por ejemplo el SideBar que tiene como objetivo único mostrar el Historial de búsquedas, otra parte importante de nuestra aplicación puede ser el Buscador que va a recuperar las imágenes que se podrían mostrar en una tercera sección que se encuentra debajo del Buscador.

Podríamos tener dos módulos, uno con todos aquellos Componentes que son compartidos por la APP usualmente llamado **`Shared`** o **`Compartido`** el cual puede contener un SideBar, un NavBar, un Footer, un contenido que se puede usar a través de toda la APP. El segundo módulo tendría todo lo referente a los GIFs.

### Tarea

Vamos a realizar las siguientes actividades.

1. Crear el módulo **`shared.module.ts`**.
2. Crear el Componente **`sidebar.component.ts`**.
3. Exportar el Componente en el Módulo.
4. Importar el **`shared.module`** dentro de **`app.module.ts`**.
5. Usar el componente **`sidebar.component`** dentro del **`app.component.html`**.
6. Mostrar resultado en el Navegador.

1. Para crear el módulo **`shared.module.ts`**

```sh
ng g m shared
```

![image](https://user-images.githubusercontent.com/23094588/153188896-9c726431-101d-4181-a913-818c95dd58af.png)

![image](https://user-images.githubusercontent.com/23094588/153189353-4b332db0-af0c-423b-a274-c179f7322bcc.png)


2. Para crear el Componente **`sidebar.component.ts`**.

```sh
ng g c shared/sidebar
```

Con el siguiente comando no nos crea el archivo de pruebas y el CSS (is inline style).

```sh
ng g c shared/sidebar --skipTests -is
```

![image](https://user-images.githubusercontent.com/23094588/153189670-a5f223d9-e4c4-4fe4-a13e-ef4326f6ccc3.png)

![image](https://user-images.githubusercontent.com/23094588/153189782-207c012c-282e-4cfe-b4b9-48aac7135973.png)


3. Exportar el Componente **`sidebar.component.ts`** en el Módulo **`shared.module.ts`**.

Exportamos el componente para poder usarlo fuera del Módulo **`shared.module.ts`**.

![image](https://user-images.githubusercontent.com/23094588/153190168-b9816fec-ac42-49a3-8c71-c4734d396b51.png)

4. Importar el **`shared.module`** dentro de **`app.module.ts`**.

![image](https://user-images.githubusercontent.com/23094588/153190450-59fbfa82-bd0f-48de-bf9d-43acd317182a.png)

5. Usar el componente **`sidebar.component`** dentro del **`app.component.html`**.

En **`app.component.html`** vamos a mover el código que renderiza el SideBar a **`sidebar.component.html`** y lo reemplazaremos para usar el componente **`sidebar.component`**.

![image](https://user-images.githubusercontent.com/23094588/153191134-2a3c76a0-adf7-495b-b285-d23ac5c53345.png)

![image](https://user-images.githubusercontent.com/23094588/153191075-23786a2b-4d50-47f4-9402-12f7d6a48d28.png)

6. Mostrar resultado en el Navegador.

![image](https://user-images.githubusercontent.com/23094588/153191275-6bc4ef29-bb06-4c63-bbff-82ab71b314b3.png)

La aplicación luce exactamente igual que antes pero con la ventaja de que ya tenemos un módulo independiente en el cual puedo colocar cualquier cosa que sea compartida en toda la APP.

### GIT

![image](https://user-images.githubusercontent.com/23094588/153192357-9b217b9d-a5d3-4ab3-8b7b-50bbb9554a3b.png)

## GifsModule y sus componentes 07:17

En esta lección vamos a crear el módulo que va a contener todo lo referente a los GIFs desde la búsqueda hasta su renderización. Vamos a pulsar el siguiente comando para crear el módulo **`gifs.module.ts`**.

```sh
ng g m gifs
```

![image](https://user-images.githubusercontent.com/23094588/153193256-3e620938-e018-4b3a-907d-aaa1a6de9501.png)

![image](https://user-images.githubusercontent.com/23094588/153193330-6b63435e-c3d6-48d2-8bad-863ce56a621c.png)

Para no olvidarlo vamos a importar este nuevo módulo en el **`app.module.ts`**.

![image](https://user-images.githubusercontent.com/23094588/153193569-6d43bfa5-12ac-4bbd-ab44-6271d4c0e7f7.png)

Dentro del módulo **`gifs`** vamos a tener un primer componente que será el **`gifsPage`** el cual contendra todos los demás componentes que necesitemos como el Buscador y la sección donde se van a renderizar las imágenes. Para crear el componente vamos a pulsar el siguiente comando:

```sh
ng g c gifs/gifsPage --skipTests -is
```

![image](https://user-images.githubusercontent.com/23094588/153194336-35d14f3f-56b3-4534-8d8c-e73411ab26a4.png)

![image](https://user-images.githubusercontent.com/23094588/153194426-1d81ac74-1c5e-41b2-bf6b-81081f503a3e.png)

Como el componente **`gifs.component`** lo vamos a usar en el **`app.component.html`** es decir fuera del módulo **`gifs.module.ts`**, necesitamos incluirlo en los  **`exports`** del propio módulo **`gifs.module.ts`**.

![image](https://user-images.githubusercontent.com/23094588/153196071-9faed515-daba-4daf-8d62-8bfb8004873d.png)

En el **`app.component.html`** vamos a cortar todo el código que pinta el contenedor 

![image](https://user-images.githubusercontent.com/23094588/153196310-833c2338-fdc8-450d-8116-614a5c864bba.png)

Y lo vamos a mover al **`gifs-page.component.html`**.

![image](https://user-images.githubusercontent.com/23094588/153196665-56525235-700d-430e-9c72-ec25c183cc2d.png)

En el **`app.component.html`** vamos a sustituir lo cortado por el uso del **`gifs-page.component`**.

![image](https://user-images.githubusercontent.com/23094588/153196909-f67cdb26-dadb-4a3e-a2ca-ff5ef8d028f1.png)

Si abrimos el navegador vemos el mismo resultado.

![image](https://user-images.githubusercontent.com/23094588/153197060-72207174-0df9-440b-b7da-1a58258158ef.png)

Si nos ponemos exigentes podemos abrir las Herramientas de Desarrollador en la pestaña **Elements**.

![image](https://user-images.githubusercontent.com/23094588/153197426-47984f01-7368-48b4-b612-8e3faa0a0bcc.png)

Podemos ver que el **`<div class="container">`** puede estar sobrando ya que tiene como padre el contenedor **`<app-gifs-page>`**.

Vamos a **`gifs-page.component.html`**.

![image](https://user-images.githubusercontent.com/23094588/153197788-9d16d025-13f1-4242-8b32-26651a96bc1d.png)

Y vamos a eliminar el  **`<div class="container">`**.

![image](https://user-images.githubusercontent.com/23094588/153197897-1e0afa24-b7db-4625-b985-6207018810c7.png)

Al quitar la **`class="container"`** nuestra pantalla se ha descompuesto.

![image](https://user-images.githubusercontent.com/23094588/153197960-a9c7370c-e388-4239-b349-e680dfbd82c2.png)

Para mantener el diseño como lo teniamos podemos aplicarle la **`class="container"`** al **`<app-gifs-page>`** en el **`app.component.html`**.

![image](https://user-images.githubusercontent.com/23094588/153198287-769c9f23-579c-4b57-8097-af6c66182ccc.png)

![image](https://user-images.githubusercontent.com/23094588/153198405-4200fef8-5280-4fb1-8e61-4ade2407a57e.png)

Y en la consola ya vemos que no esta el **`div`** que teniamos de más:

![image](https://user-images.githubusercontent.com/23094588/153198726-f4e23513-02ce-4bb8-9697-5b1aebb7e0e5.png)

### Crear los Componentes Busqueda y Resultados.

Vamos a crear el componente **`busqueda`** dentro del módulo **`gifs`** con el siguiente comando:

```sh
ng g c gifs/busqueda --skipTests -is
```

![image](https://user-images.githubusercontent.com/23094588/153199163-8b0d6b1c-d3f7-485a-93de-f522286d3c99.png)

![image](https://user-images.githubusercontent.com/23094588/153199202-97786ab3-691e-417b-a0a2-23847532b6d1.png)

**NOTA: Como este componente no lo vamos a usar fuera de este módulo no lo debemos exportar en el **`gifs.module.ts`**.

Vamos a crear el componente **`resultados`** dentro del módulo **`gifs`** con el siguiente comando:

```sh
ng g c gifs/resultados --skipTests -is
```

![image](https://user-images.githubusercontent.com/23094588/153199648-d35f7932-0dd9-4d73-bd64-c6188cf2f46d.png)

![image](https://user-images.githubusercontent.com/23094588/153199712-f1ae687a-1c01-4d4e-8da2-28ec96bc8900.png)

**NOTA: Como este componente no lo vamos a usar fuera de este módulo no lo debemos exportar en el **`gifs.module.ts`**.

Vamos a mover el código de **`gifs-page.component.html`** a los componentes recien creados respectivamente y sustituirlo por el uso de los componentes.

![image](https://user-images.githubusercontent.com/23094588/153199999-329db7d9-6ed7-4157-950f-dbce67f3293c.png)

![image](https://user-images.githubusercontent.com/23094588/153200440-d0a31b89-1f4b-438a-80ec-9990816d4c72.png)

![image](https://user-images.githubusercontent.com/23094588/153200512-aefc937b-ae30-4df3-b8a6-2a8f4b873fcb.png)

![image](https://user-images.githubusercontent.com/23094588/153200587-6402ddbd-fbf1-4ad1-adbf-b2496ac32f24.png)

La aplicación se ve exactamente igual pero ya la hemos implemnentado con dos módulos independientes y sus respectivos componentes, hemos cambiado un diseño HTML a una estructura Angular.

![image](https://user-images.githubusercontent.com/23094588/153200941-9d7782ec-3df6-4816-8928-d7bd48015a8a.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/153201094-adcdfb32-0b24-4946-8034-ad5264ee5a42.png)


## **`@ViewChild`** - Obtener referencias a objetos del HTML 11:57

En esta lección nos vamos a dedicar a obtener la información de la caja de texto del Buscador, es decir cuando presionemos Enter podamos ver su valor en Consola y a su vez borrar su contenido.

![image](https://user-images.githubusercontent.com/23094588/153839216-42b66daa-541e-4e81-ac34-59cb1d04f410.png)

Hay muchas maneras de hacerlo una es usando el **`FormModule`** podríamos usar el **`NgModel`** y gracias al **Two wait DataBinding** poder establecer y borrar el contenido de la caja de texto facilmente. Pero no quiero importar el **`FormModule`** solo para una caja de texto aun que se puede hacer y es más sencillo usando el **`FormModule`**. 

Vamos a usar otras técnicas para recuperar el valor de la caja de texto sin utilizar el **`FormModule`**  y **`NgModel`**, vamos a concentrarnos en el componente **`busqueda.component`**, lo primero que vamos a hacer es en **`busqueda.component.html`** en el elemento **`input`** vamos a poner el evento **`keyup`** el cual se dispara cada que liberamos la presión en cualquier tecla y vamos a invocar al método **`buscar()`**.

![image](https://user-images.githubusercontent.com/23094588/154226172-30b46e95-bb9d-4df0-af79-f41fa1f1588f.png)

Vamos a implementar el método **`buscar()`** en **`busqueda.component.ts`** simplemente para empezar y que no nos marque error vamos a mandar un mensaje a la consola.

![image](https://user-images.githubusercontent.com/23094588/154226908-48547efa-d794-4094-94d4-ecc5fcfd55fa.png)

Cada que pulsamos y liberamos una tecla se escribe el mensaje en la consola.

![image](https://user-images.githubusercontent.com/23094588/154227021-e75138a1-42f7-4914-8620-c20e9a38cc4a.png)

Podríamos no estar mandando el mensaje cada que se presione cualquier tecla, podríamos hacerlo hasta que se pulse la tecla **`Enter`** para lo cual vamos a pasar como parámetro el **`$event`** 

![image](https://user-images.githubusercontent.com/23094588/154228300-01c1e4fd-2812-41d7-93f7-8aaa3f52bdf1.png)

y que sea recibido por **`buscar(evento)`** tenemos que tipar el **`evento`** como no sabemos exactamente su tipo lo tipamos como **`any`** es decir **`buscar(evento: any)`** y podemos sacar a consola el valor de **`evento`**.

![image](https://user-images.githubusercontent.com/23094588/154229013-9a0e4626-3d2a-42a2-b298-1c4f660c4a82.png)

![image](https://user-images.githubusercontent.com/23094588/154229299-50b5e6c1-3155-4835-9063-47d0e64993d6.png)

![image](https://user-images.githubusercontent.com/23094588/154229417-b268acdc-a7eb-4455-a6f9-38b753ae6411.png)

Como podemos ver en la consola nos indica que se ha disparado el evento **`KeyboardEvent`** y podemos sustituir el tipo **`any`** por **`KeyboardEvent`**.

![image](https://user-images.githubusercontent.com/23094588/154230275-4eb5a851-e8f9-422d-9d0a-9a2c30dc6959.png)

![image](https://user-images.githubusercontent.com/23094588/154230406-ec3950c4-0495-4026-8a42-41cee228d646.png)

Con esto ya podemos ver todos los métodos y propiedades de **`event`** gracias a que lo hemos tipado.

En el navegador podemos presionar varias teclas y presionar un **`Enter`**.

![image](https://user-images.githubusercontent.com/23094588/154231331-ebc0251e-5501-49b3-a85d-643d71e72d56.png)

En **`event`** tenemos la propiedad **`code`** que para la tecla **`e`** su valor es **`KeyE`** y para **`Enter`** su valor es **`NumpadEnter`**. Pero realmente nada de esto nos interesa en este caso solo queremos conocer el valor de la caja de texto. Por lo que en el método **`buscar`** no vamos a recibir el **`evento`**. En **`busqueda.component.html`** vamos a hacer lo siguientes cambios, el evento que vamos a capturar es **`keyup.enter`** que detecta cuando pulsamos y liberamos el **`Enter`**, vamos a poner un identificador a la caja de texto con **`#txtBuscar`** y en **`buscar()`** vamos a mandar el valor de la caja de texto con **`buscar(txtBuscar.value)`**.

![image](https://user-images.githubusercontent.com/23094588/154246306-5041d55f-196d-4a2e-a892-83b1ea3b80a2.png)

En **`busqueda.component.ts`** en el método **`buscar`** vamos a recibir el termino que queremos buscar.

![image](https://user-images.githubusercontent.com/23094588/154246655-0959f34d-d9be-405f-9931-e8dd99cc3171.png)

Lo que recibimos ya es una cadena de texto por eso la tipamos con **`string`**.

Al buscar un texto en el navegador y pulsar **`Enter`** aparecera el texto en la consola.

![image](https://user-images.githubusercontent.com/23094588/154247063-1dc6263e-6d17-4140-9fe6-8eaa59e3b52a.png)

Todo perfecto, ya tenemos el valor de la caja de texto, pero todo esto tiene un posible inconveniente si queremos limpiar la caja de texto una vez recuperado su valor, cosa que sería sencilla si usaramos **`FormModule`** y **`NgForm`**. Podríamos pensar en asignar a **`termino`** un valor vacío.

![image](https://user-images.githubusercontent.com/23094588/154247915-33e17c02-4a1f-46fc-a917-a7a3c64ac590.png)

Si ejecutamos el navegador 

![image](https://user-images.githubusercontent.com/23094588/154247978-03e36c1a-5029-474b-b52b-69be4b48c837.png)

Vemos que se limpia el **`termino`** en la consola pero no la caja de texto en el navegador.

**¿Cómo hacemos para tomar la caja de texto y mantener su referencia?**

En JS clásico podemos recuperar la referencia al único **`input`** que tenemos con:

![image](https://user-images.githubusercontent.com/23094588/154248505-47883fcc-0110-4943-b1d7-bd0b368bca76.png)

Pero TypeScript me marca un error al ejecutarlo.

![image](https://user-images.githubusercontent.com/23094588/154248938-81867fcb-593c-4a95-a438-4dca4cbf04a2.png)

Vamos a ver como hacerlo con Angular para lo cual vamos a usar el decorador **`@ViewChild`** este decorador recibe un parámetro el cual se refiere al elemento que queremos hacer referencia en el HTML, podemos buscar por nombre del Tag, por clases pero en nuestro caso vamos a usar el identificador con el que nombramos a la caja de texto, es decir **`@ViewChild(txtBuscar)`** esto es como el tipo de la propiedad y ahora lo que tenemos que definir es el nombre de la propiedad  **`@ViewChild(txtBuscar) txtBuscar;`**

![image](https://user-images.githubusercontent.com/23094588/154251019-30b4a503-8da4-4361-a87f-3fffab392cea.png)

Esto nos marca un error por que tiene un tipo **`any`** implicito, 

![image](https://user-images.githubusercontent.com/23094588/154251425-63318031-c41d-491d-aec9-c3dc8416c196.png)

como no conocemos el tipo exacto vamos a poner el tipo **`any`** explicitamente.

![image](https://user-images.githubusercontent.com/23094588/154251570-5fd43936-68a5-4ab0-abc7-892af9bbc6c4.png)

Ahora vamos a imprimir en consola el valor de la propiedad **`txtBuscar`**.

![image](https://user-images.githubusercontent.com/23094588/154251917-4855a9cd-ac4d-4588-9bd9-90e7bee4da32.png)

Lo que nos esta haciendo el **`@ViewChild`** es ir a buscar en el HTML el elemento que tenga la referencia que pasamos como parámetro y lo asigna a la propiedad definida, con esto ya podemos manipular ese elemento en nuestro archivo TS.

En el navegador tenemos lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/154252627-ce4f3c18-670a-4280-ac0b-70256e9072dc.png)

En la consola se imprime el **`nativeElement`** el cual es el elemento HTML el cual contiene muchas propiedades con mucha información para hacer referencia a el. Podemos ver también que el elemento **`input`** es de tipo **`ElementRef`** por lo que podemos cambiar el tipo de **`any`** a **`ElementRef`**.

![image](https://user-images.githubusercontent.com/23094588/154253425-973a22b3-29d0-45a4-a755-889877fd53cd.png)

Pero nos esta mandando un error, de que el elemento no esta inicializado.

![image](https://user-images.githubusercontent.com/23094588/154253495-ef055802-3d58-4a33-b904-84e5b5fc3908.png)

**Esto es algo que esta apareciendo en las versiones nuevas de Angular por que estamos trabajando en un modo Super Estricto** lo cual esta bien, la cosa es que nosotros estamos 100% seguros que el elemento **`txtBuscar`** siempre va a existir, es parte del HTML. Lo que me dice VSC es que puede ser que **`txtBuscar`** no exista es decir que puede ser que sea **`null`** pero como nosotros sabemos que existe se lo hacemos saber a Angular poniendo el operador **`!`**, como sigue:

```js
@ViewChild('txtBuscar') txtBuscar!: ElementRef;
```

El operador **`!`** se conoce como [Non-null assertion operator](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-2-0.html#non-null-assertion-operator) u Operador para asegurarse de que el operador no es nulo. Este operador es propio de TypeScrip no de JavaScript. 

Podemos entonces usar las propiedades del elemento **`txtBuscar`** dentro del TS para imprimir su valor en la consola.

![image](https://user-images.githubusercontent.com/23094588/154255407-28c8d57b-c20d-48bb-a6b1-0018626d212b.png)

Con esto podemos recuperar el valor de la caja de texto e imprimirlo en la consola.

![image](https://user-images.githubusercontent.com/23094588/154255620-a89fb252-28f1-431d-a88e-a7ddc6a22346.png)

Por lo tanto ya no necesitamos ni mandar ni recibir el **`termino`** a buscar por que ya podemos recuperar el valor directamente del elemento.

![image](https://user-images.githubusercontent.com/23094588/154255921-7d50276a-a7dc-40d6-ac77-24db2da16542.png)

![image](https://user-images.githubusercontent.com/23094588/154256008-e5578377-7d3e-4a37-9a3d-d3fc46cdf817.png)

![image](https://user-images.githubusercontent.com/23094588/154256087-95cb45b4-8c9e-492b-add0-918971f3537e.png)

Solo hay un detalle, VSC no nos muestra ayuda del **`nativeElement`**.

![image](https://user-images.githubusercontent.com/23094588/154256372-f8684108-553d-413d-a86e-c7d5348750fd.png)

Y eso es por que como podemos observar **`ElementRef`** es de tipo Generico y por defecto su valor es **`any`**.

![image](https://user-images.githubusercontent.com/23094588/154256593-007c3f81-a5a6-4c8f-b3f7-0035d3df6425.png)

Si queremos especificar que es del tipo **`Input`** ¿Cómo lo hacemos?.

Usamos el tipo **`HTMLInputElement`**, no es necesario importarlo por que ya TS los incorpora automáticamente por que son cosas relacionadas con JS directamente. De esta manera ya tenemos todas las propiedades del elemnto en la ayuda del VSC para usarlas. Esto en el navegador no cambia nada, lo hicimos más para ayuda en la códificación.

![image](https://user-images.githubusercontent.com/23094588/154257538-9b7e3bce-8947-4901-b58b-f99edba446fb.png)

Como ya tenemos la referencia del elemento ya tenemos la posibilidad de borrar el contenido de la caja de texto asignandole una cadena vacia como valor.

![image](https://user-images.githubusercontent.com/23094588/154257921-12de888f-f848-4e72-9208-3b8bb79513b2.png)

![image](https://user-images.githubusercontent.com/23094588/154258030-424d2496-f09e-419c-9e74-ea7c5bd07ae4.png)

Al presionar **`Enter`** se imprime el valor de la caja de texto en la consola y se limpia la caja de texto que era nuestro objetivo.

![image](https://user-images.githubusercontent.com/23094588/154257224-4f58373d-38de-4f28-86bc-ec0b29df1345.png)

Gracias a usar **`@ViewChild`** tenemos acceso a todo el elemento HTML en este caso al **`Input`** y podemos manipularlo a nuestro antojo a diferencia de cuando usamos el **`NgModel`** que solo manipulo su valor, con **`@ViewChild`** puedo manipular todo lo que desee del elemento HTML. 

### GIF

![image](https://user-images.githubusercontent.com/23094588/154259112-f80aee79-b9ee-4339-bba8-7d7156055003.png)


## GifsService 11:09

**``**

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

