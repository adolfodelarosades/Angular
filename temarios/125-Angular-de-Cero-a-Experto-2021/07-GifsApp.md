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

En esta lección vamos a realizar un historial de las busquedas que vamos haciendo e ir pintando ese historial en forma de listado en el SideBar de la pantalla. Esto nos permite ver que necesitamos crear un Servicio centralizado para almacenar todo lo referente a los GIFs.

Actualmente tenemos esta estructura en el proyecto.

![image](https://user-images.githubusercontent.com/23094588/154261921-754d0b7b-7db0-4a9a-aa90-79e49790cb01.png)

Dentro de la carpeta **`gifs`** vamos a tener otra carpeta llamada **`services`** y dentro vamos a tener nuestro **`GifsService`**. Vamos a crear el Servicio usando el Angular CLI, con el comando:

```sh
ng g s gifs/services/gifs --skipTests
```

o 

```sh
ng generate service gifs/services/gifs --skipTests
```

![image](https://user-images.githubusercontent.com/23094588/154264410-8f38ad18-bfa7-425b-9e19-f09737f00b13.png)

![image](https://user-images.githubusercontent.com/23094588/154314315-c0b35069-7710-44f4-906a-3417d6c6182f.png)

Observemos que solo se creo el archivo **`src/app/gifs/services/gifs.service.ts`** y no se ha actualizado ningún módulo ni algún otro archivo que indique que se va a utilizar este Servicio. Si abrimos el archivo tenemos:

![image](https://user-images.githubusercontent.com/23094588/154314822-014f6cdf-e463-4900-b64d-b75ce2d4a019.png)

A diferencia de Servicios que creamos anteriormente donde solo teniamos la anotación:

```js
@Injectable()
```

En este Servicio tenemos:

```js
@Injectable({
  providedIn: 'root'
})
```

El bloque de código **`providedIn: 'root'`** fue una característica añadido en Angular 4 lo cual permite que los Servicios puedan estar definidos en el momento que se construye el Bundle de la aplicación, al especificar el **`providedIn: 'root'`** en el decorador **`@Injectable()`** le dice a Angular que no importa en que parte de la aplicación estemos el Servicio va a estar disponible, esto es genial por que evita que yo tenga que especificar en **`gifs.module.ts`** en la sección de **`providers[]`** como se hacia en versiones anteriores de Angular. Si lo llegaramos a especificar en los **`providers[]`** de **`gifs.module.ts`** el Servicio solo estara disponible en este módulo. Pero al especificar el **`providedIn: 'root'`** en el decorador **`@Injectable()`** el Servicio esta disponible Globalmente, usualmente así usaremos los Servicio Globalmente.

Hecho lo anterior vamos a manejar un listado que nos permita ir almacenando la información que vayamos introduciendo en el Buscador. Cada una de las entradas en el Buscador la vamos ir almacenando, estas entradas son **`strings`**, por lo que en el Servicio nos vamos a crear una propiedad privada para almacenar la lista de **`strings`** que llamaremos **`_historial`**.

![image](https://user-images.githubusercontent.com/23094588/154317914-54ef23e4-9a7e-4362-9c0d-8ba9fc16ea05.png)

Vamos a querer exponer una propiedad para poder obtener el **`historial`** por lo que vamos a realizar un GETTER, donde vamos a romper la relación con el objeto original **`_historial`** para que no podamos manipularlo fuera del servicio, esto lo hacemos con:

![image](https://user-images.githubusercontent.com/23094588/154318723-743f7cd5-26f2-44d6-82a3-567f0f447371.png)

Recordar que rompemos la referencia con el operador spread **`...`** y regresando un nuevo arreglo, si simplemente retornamos **`this._historial`** estaríamos enviando el objeto original y podríamos modificarlo fuera del Servicio.

Además de lo anterior vamos a crear un método para ir insertando los terminos que estemos buscando en el historial, el termino lo vamos a ir insertando al inicio del array esto lo logramos usando el método **`unshift()`**, el método es el siguiente:

![image](https://user-images.githubusercontent.com/23094588/154319898-3e9229d0-52c9-4bb4-bfd7-048f8e34ed89.png)

![image](https://user-images.githubusercontent.com/23094588/154320044-708cdb20-0cd0-462a-a671-292a2a509fd0.png)

Este método recien creado en el servicio debemos invocarlo en el componente **`busqueda.component`**, para usar el Servicio debemos inyectarlo en el **`constructor()`** y hecho esto ya tenemos acceso a todas las propiedades y métodos del Servicio inyectado, usemos el método **`buscarGifs`** para ir almacenando los terminos de busqueda.

![image](https://user-images.githubusercontent.com/23094588/154320980-4ab78eb0-631d-4cac-b380-1028648b1fce.png)

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/154321143-24bb8057-becc-496a-9135-35adeea2b099.png)

![image](https://user-images.githubusercontent.com/23094588/154321233-b92b4004-e121-4ab3-86e8-f01f13f320de.png)

![image](https://user-images.githubusercontent.com/23094588/154321455-9a7f2710-368c-4914-b710-1d3c823849f3.png)

![image](https://user-images.githubusercontent.com/23094588/154321506-7e601357-4f78-46a4-8e58-d02f0299de82.png)

Ahora lo que necesitamos es consumir el **`historial`** para construir Items en el SideBar, por lo tanto en el componente **`sidebar.component`** en la parte del HTML vamos a usar la directiva **`*ngFor`** para repetir el Item por cada valor en el listado, y en el TS necesitamos recuperar el historial a partir del Servicio.

![image](https://user-images.githubusercontent.com/23094588/154323850-8c00f026-e8ed-41a5-a050-4d1c4b85b93d.png)

Observemos que el **`get historial()`** esta declarado antes del **`constructor`** ya que el **`get historial()`** no es un método sino una propiedad del Componente.

![image](https://user-images.githubusercontent.com/23094588/154324158-37950929-938a-42b2-a4c6-7ed632f39633.png)

En el HTML estamos usando la directiva  **`*ngFor`** para repetir el Item y estamos renderizando su valor.

Una vez que ejecutamos la APP en el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/154324425-64d17be9-60c0-4462-96c6-349b44daa571.png)

¿Qué pasa si metemos un valor ya introducido anteriormente?

![image](https://user-images.githubusercontent.com/23094588/154324790-d4a152c5-f2ea-44b3-988c-87b474e8f8c0.png)

Acepta valores repetidos, ya controlaremos esto en la siguiente lección.

### GIT

![image](https://user-images.githubusercontent.com/23094588/154325054-5bd334df-5180-4a5d-a315-8cf446d61b05.png)

## Controlar el historial de búsquedas 06:57

En esta lección vamos a controlar varias cosas, la primera es la cantidad de elementos que se pueden insertar en el historial, el segundo no meter busquedas duplicadas, el tercero es que no acepte valores vacios, el cuarto controlar mayúsculas y minúsculas.

![image](https://user-images.githubusercontent.com/23094588/154434656-1b248e5f-f703-464d-a124-77bdf517538c.png)

Para validar que no acepte vacios lo podemos hacer desde el Componente aun que también lo podemos hacer en el Servicio, vamos a meter el siguiente código para validar que no acepte blancos en **`busqueda.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/154443954-046cc6e4-188e-4f03-9cf8-19a2ed863104.png)

Para limitar el número de inserciones que se pueden hacer en el historial existen varias formas de hacerlo, vamos a ver una forma sencilla en la cual más que limitar la inserción a 10 items en el historial vamos a recuperar las 10 primeras en la lista. Esto lo vamos a hacer en el GETTER del **`GifsService`**.

![image](https://user-images.githubusercontent.com/23094588/154445284-571d063a-666c-4d44-ab63-c136a22fa074.png)

Con **`this._historial = this._historial.splice(0,10);`** lo que estamos haciendo es cortar el array para recuperar los primeros 10 elementos.

Si lo dejamos aquí cuando recuperamos el historial se va a estar haciendo el corte del array

![image](https://user-images.githubusercontent.com/23094588/154445943-6c3d3d9a-33be-4e4e-a58d-98a28b7c6aa3.png)

Cada vez que pase por el GETTER se corta el array y se vuelve a redibujar, esto funciona pero tal vez no es el mejor sitio donde ponerlo. Vamos a cambiarlo a la siguiente posición:

![image](https://user-images.githubusercontent.com/23094588/154446497-0fed4092-8020-489e-9611-69c760c124e5.png)

Si lo ubicamos en este sitio lo que estamos haciendo es que primero insertamos la busqueda en el historial y luego lo cortamos, de esta manera evitamos que estar cortando el array cada vez que se recupera.

![image](https://user-images.githubusercontent.com/23094588/154446839-92d2c323-43a8-4fe0-9867-5013a4a7dbea.png)

Ahora lo que vamos a hacer es evitar valores duplicados, vamos a usar lógica de JS para hacerlo usando una función nueva **`includes`** incorporado en ES6 que nos indica si existe en el array lo que pasemos como parámetro, en este caso lo que vamos a hacer es que si el array no lo incluye lo insertamos.

![image](https://user-images.githubusercontent.com/23094588/154447823-40e81f35-3843-4cad-bf33-a9bb87ab1365.png)

En el navegador podemos ver que cuando pulsamos valores repetidos ya no se insertan.

![image](https://user-images.githubusercontent.com/23094588/154448208-9e5cff7d-91a1-43bf-ae91-5529ccebab15.png)

Incluso podemos hacer el corte del array solo si se inserta una nueva busqueda.

![image](https://user-images.githubusercontent.com/23094588/154448566-6136d611-8665-4495-8b4e-be660202da50.png)

![image](https://user-images.githubusercontent.com/23094588/154448722-4cd44fbd-408b-4e62-8477-a51f0b4d716f.png)

Ahora vamos a ver que pasa si meto una búsqueda en mayúsculas y la misma en minúsculas.

![image](https://user-images.githubusercontent.com/23094588/154451768-3f24343c-ba69-4c6f-a376-85b51296907a.png)

Acepta ambos valores, vamos a hacer algo para procesar la manera en que la grabamos, ya sea que en el historial alacenemos todo en mayúsculas o todo en minúsculas, vamos a almacenarlo en minúsculas.

![image](https://user-images.githubusercontent.com/23094588/154472351-ee74034d-5dec-424c-aa31-4156aae1cc94.png)

Podemos obligar a que siempre tenga un valor asignandolo en el parámetro que llega.

![image](https://user-images.githubusercontent.com/23094588/154472636-481171d0-bea7-47a5-8d33-020f29b63f77.png)

Vamos a meter el mismo valor en minúscula y mayúscula.

![image](https://user-images.githubusercontent.com/23094588/154472846-2cdbf728-c4a5-46d6-870a-b5979b1f7295.png)

Ya solo acepta un solo valor.

Ahora lo que no nos gusta es que los Items salgan en minúscula, los podemos capitalizar para que se muestre la primer letra en mayúscula, aunque todo se este almacenando en minúsculas. Para hacer esto nos vamos al SideBar que es donde se estan reenderizando los Items y usaremos un PIPE para darle formato solo vizualmente, no cambia los datos almacenados.

![image](https://user-images.githubusercontent.com/23094588/154473644-eae17fb5-fa5d-4671-868f-e6abf8ad9f60.png)

![image](https://user-images.githubusercontent.com/23094588/154473786-1b431600-e25b-489e-8eaf-ef07eb5b1bba.png)

![image](https://user-images.githubusercontent.com/23094588/154473881-919c79b6-c47e-4948-b757-3490b3c5b1b5.png)

![image](https://user-images.githubusercontent.com/23094588/154474135-c54b437e-a733-4ee8-9d6e-2d5ad733bb03.png)

![image](https://user-images.githubusercontent.com/23094588/154474202-8cbcee51-047e-42a6-8f1c-1d71061effb6.png)

No importa como introduzcamos la búsqueda se almacena en minúscula y se muestra capitalizado.


### GIT

![image](https://user-images.githubusercontent.com/23094588/154474682-479709fc-3bce-4aa6-99c5-5d811b4dd73a.png)


## Giphy Api Key - Giphy Developers 07:14

En esta lección vamos a acceder al API KEY de [GIPHY Developers](https://developers.giphy.com/).

![image](https://user-images.githubusercontent.com/23094588/154682165-34143de0-ad53-4304-abc0-231c337e045b.png)

Este es API que utilizan muchas compañias como Snapchat, Twitter, Facebook, etc. para acceder a diferentes GIFs y compartirlos en las Redes Sociales. 

La idea es consumir esta API en su parte de consumo gratuito es excelente para practicar, vamos a recuperar las imágenes que coincidan con el termino de búsqueda.

Para comenzar dentro de la página [GIPHY Developers](https://developers.giphy.com/) tenemos varias opciones a las que podemos acceder.

![image](https://user-images.githubusercontent.com/23094588/154683138-ba3db598-0986-4585-9896-c7ee3a8f4df5.png)

### Crear Cuenta

Pero lo primero que debemos es crear una cuenta presionando el botón **Create Account**.

![image](https://user-images.githubusercontent.com/23094588/154683376-f9e1396f-5646-4806-9b56-fc0ff95a2849.png)

![image](https://user-images.githubusercontent.com/23094588/154683457-f0ef1b1e-d41a-421e-9b3c-474a4f7e6de3.png)

Vamos a meter nuestros datos para darnos de alta.

Una vez que nos hemos dado de alta en la página podemos acceder a nuestra cuenta.

![image](https://user-images.githubusercontent.com/23094588/154683988-fa9523c2-bc02-44e2-820e-39feb7eb1d27.png)

Una vez logeados podemos ir a [API Quickstart Guide](https://developers.giphy.com/docs/api/#quick-start-guide).

![image](https://user-images.githubusercontent.com/23094588/154685734-9c8c5917-f083-46d5-b5af-2eec078a75cc.png)

![image](https://user-images.githubusercontent.com/23094588/154685797-68b49960-711f-442d-aee4-dd888ba094df.png)

Podemos presionar el botón **Create an APP**.

![image](https://user-images.githubusercontent.com/23094588/154685993-5ce8f094-448a-4c66-a7d2-5a837ae91e5e.png)

Nos muestra dos opciones el **SDK** que nos permite crear ya todo el componente pero nosotros vamos a seleccionar la opción **API** que es una opción más limitada pero que nos va a permitir crear lo que queremos.

![image](https://user-images.githubusercontent.com/23094588/154686336-5b6d8452-b0ac-4287-abc0-d980439a0cf6.png)

Precionamos en **Next Step**.

![image](https://user-images.githubusercontent.com/23094588/154686564-886673fb-f243-4428-9b11-69db29821e21.png)

Se nos pide un nombre de la APP y su descripción, vamos a insertar lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/154686833-07339c59-fed1-4389-bea8-681b7fb489cf.png)

Presionamos en **Create App**.

![image](https://user-images.githubusercontent.com/23094588/154686977-820f4e96-ee2c-4717-8d9a-7cda5e622e9a.png)

Lo importante es el API Key que se genera y que vamos a usar dentro de nuestra aplicación Angular.

**`3sZBfqeXrIArY6K1eq7xwISx6nb4B2V8`**

Nos podemos ayudar de la documentación de GIPHY para ver como usar el [API Quickstart Guide](https://developers.giphy.com/docs/api/endpoint).

![image](https://user-images.githubusercontent.com/23094588/154687822-1d16989d-eea6-4b12-b536-8fadf5a96e46.png)

Especificamente nos vamos a la sección **Search Endpoint**.

![image](https://user-images.githubusercontent.com/23094588/154688021-4b4dbf57-09f0-4950-815c-e901132e27c0.png)

Tenemos varios enlaces, en particular el primero de ellos nos permite recuperar GIFs o Sticker(Una forma de personalizar los chats de Whatsapp de forma única es mediante los stickers, que son dibujos, ilustraciones y fotos que puedes añadir a tus mensajes. ) 

![image](https://user-images.githubusercontent.com/23094588/154689411-3b20d424-6b15-41f4-b2dd-2004bec0f24f.png)

**`api.giphy.com/v1/gifs/search`**	**`api.giphy.com/v1/stickers/search`**

, tenemos el URL que necesitamos, y más abajo tenemos todos los argumentos que podemos mandar, por ejemplo el **api_key** es ***requerido*** por eso lo generamos en los pasos anteriores, otro argumento requerido es el **query (q)**, podemos tener un argumento para limitar los resultaddos **limit**, el **offset** nos permite tener una páginación, **rating** nos permite indicar que recuperemos solo GIFs de cierto rango, podemos mandar el idioma con **lang**, y otras más opciones.

![image](https://user-images.githubusercontent.com/23094588/154689693-eab796c0-82fa-4efe-8e31-27c32073afec.png)

Antes de códificar en Angular debemos tener claro como funciona el API y sus EndPoints, podemos probar los EndPoints en PostMan.

![image](https://user-images.githubusercontent.com/23094588/154690494-be9710df-67d3-4b0e-bcd4-fd15ad004a3e.png)

Vamos a poner como URL el enlace del **GifURL**

![image](https://user-images.githubusercontent.com/23094588/154690657-983e9801-c869-41cd-be25-87963d09ef14.png)

Si lanzamos la petición nos muestra el mensaje **`No API key found in request`** que indica que no hemos introducido nuestra API KEY, podemos añadirlo en la URL de la siguiente forma:

![image](https://user-images.githubusercontent.com/23094588/154691138-1e89a3d8-6d74-4788-b2ca-68e7312b8d00.png)

Al lanzar esta petición ya obtenemos una respuesta, nos regresa **`data[]`** un array de resultados vacío que lo indica en **`"total_count": 0,`**, esto es porque no hemos mandado el **`query`** de busqueda, el cual lo podemos añadir en la URL al que hicimos con el **`api_key`** o usar la pestaña de **Params** para añadirlo de una forma más comoda.

![image](https://user-images.githubusercontent.com/23094588/154691836-65f3cc9c-5c28-4420-9f7b-6a3cc2a11e1f.png)

![image](https://user-images.githubusercontent.com/23094588/154691932-7afc37ae-e817-4dbd-848d-a87d0e93e561.png)

Podemos ver que tenemos un resultado de **444*** Gifs localizados. Podemos limitar los resultados para solo recuperar 10 resultados usando el argumento **`limit`**.

![image](https://user-images.githubusercontent.com/23094588/154692274-9c64b20b-eb90-4f4b-8e4a-d634c42f2886.png)

Si vemos el detalle de **`data`** vamos a ver la información que retorna el API, entre ellas una URL que accede a GIPHY con los resultados encontrados.

https://giphy.com/gifs/TOEIAnimationUK-dbz-dragon-ball-z-977YesTjNfQC7vQiph

![image](https://user-images.githubusercontent.com/23094588/154693394-c9d95848-9915-4e53-bc6e-c1f4da41f5a4.png)

![image](https://user-images.githubusercontent.com/23094588/154692612-14820cc0-cd72-46d4-8ef2-e782b1b79fe3.png)

Si bajamos tenemos un objeto **`images`** con los diferentes tamaños de las imagenes que tenemos y las URLs donde se encuentran dichas imagenes:

https://media4.giphy.com/media/977YesTjNfQC7vQiph/giphy.gif?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=giphy.gif&ct=g

![image](https://user-images.githubusercontent.com/23094588/154693137-d8dec90a-54e7-4f0f-9a8a-5fa2548e3c1a.png)

https://media4.giphy.com/media/977YesTjNfQC7vQiph/giphy.mp4?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=giphy.mp4&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/giphy.webp?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=giphy.webp&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/200.gif?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=200.gif&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/200.mp4?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=200.mp4&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/200.webp?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=200.webp&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/200_d.gif?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=200_d.gif&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/200_d.webp?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=200_d.webp&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/100.gif?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=100.gif&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/100.mp4?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=100.mp4&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/100.webp?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=100.webp&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/100_s.gif?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=100_s.gif&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/200_s.gif?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=200_s.gif&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/200w.gif?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=200w.gif&ct=g",
https://media4.giphy.com/media/977YesTjNfQC7vQiph/200w.mp4?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=200w.mp4&ct=g
https://media4.giphy.com/media/977YesTjNfQC7vQiph/200w.webp?cid=94c348a7xcfl3awvr3ry7s3g7tnbqpomsltdxne5py0hd625&rid=200w.webp&ct=g

Dependiendo de la imagen que queramos usar usaremos un valor u otro.

Vamos a cambiar el URL para recuperar los STICKERS en lugar de los GIFs, tenemos lo siguiente:

api.giphy.com/v1/stickers/search?api_key=3sZBfqeXrIArY6K1eq7xwISx6nb4B2V8&q=Dragon Ball Z&limit=10

![image](https://user-images.githubusercontent.com/23094588/154696188-476bcbbf-3f81-4e42-9be2-66cc6aa43385.png)

![image](https://user-images.githubusercontent.com/23094588/154696327-78fc93c7-a8d2-4f1c-a69b-e2accfafb838.png)

![image](https://user-images.githubusercontent.com/23094588/154696428-6eaa60cc-b23f-48c9-a099-8873d230ed73.png)

Con Postman podemos ir almacenando los Request que hagamos en una colección.

![image](https://user-images.githubusercontent.com/23094588/154696583-b917e822-72a2-45ae-99b1-d77df6c65378.png)

También podemos cargar la URL que estamos poniendo en Postman directamente en el Navegador.

![image](https://user-images.githubusercontent.com/23094588/154696854-b5054df3-42d4-436b-b681-56d0517c6107.png)

Una vez que ya tenemos idea de como trabaja el API podemos seguir con la codificación en Angular.


## Realizar una petición HTTP 08:34

En esta lección vamos a ver como utilizar el URL que usamos en Postman y en el Navegador dentro de Angular.

### Usando **`Promesas`**

Vamos a nuestro servicio **`gifs.service.ts`** y vamos a ver una primera forma de usar el URL usando la forma tradicional de JS con Promesas.

**`https://api.giphy.com/v1/stickers/search?api_key=3sZBfqeXrIArY6K1eq7xwISx6nb4B2V8&q=Dragon%20Ball%20Z&limit=10`**

![image](https://user-images.githubusercontent.com/23094588/154913003-44e1edb1-654c-4def-b90c-5351c5fe9eb1.png)

Si lo probamos en el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/154913086-907df010-7de0-4738-9b9c-658528332f18.png)

### Usando **`async`**

Nos devuelve los mismos datos que en Postman, podríamos hacerlo también usando el método como **`async`** como sigue:

![image](https://user-images.githubusercontent.com/23094588/154913712-c6279beb-e5e3-4ee8-8954-b6ae32843015.png)

En el navegador vamos a obtener el mismo resultado:

![image](https://user-images.githubusercontent.com/23094588/154913984-604da8b0-a2d8-40f2-b725-9d8281c8ba7d.png)

Esta última forma es más limpia pero seguimos usando la forma en la que trabaja JS.

Pero al usar el **`fetch`** siempre se hace más "carpinteria" ya que si existe un error hay que encerrarlo en un **`try - catch`**, si ocupamos el tipado hay que especificarlo en otro lugar, etc.

### Usando el módulo **`HttpClientModule`**

Angular nos ofrece un objeto para hacer peticiones HTTP, para usar este objeto debemos importar un módulo lo vamos a hacer de una manera global por lo que lo vamos a importar en **`app.module.ts`** pero de igual modo lo podríamos importar en un módulo particular para que solo se use allí.

Vamos a añadir lo siguiente en **`app.module.ts`**.

![image](https://user-images.githubusercontent.com/23094588/154915409-30c5ab57-5eee-413f-ab85-96ede544ea47.png)

Observese como en el **`imports`** colocamos primero los módulos creados por Angular y luego los módulos hecho por nosotros, si tuvieramos módulos de terceros irian en medio de ambos.

**`HttpClientModule`** nos ofrece un monton de servicios entre ellos ***algo que puedo inyectar en mi propio servicio***.

Vamos a inyectar en nuestro servicio **`gifs.service`** el servicio **`HttpClient`** en nuestro constructor.

![image](https://user-images.githubusercontent.com/23094588/154916757-60318288-648f-4222-96cc-ecc960d1423f.png)

Con este **`HttpClient`** ya podemos hacer peticiones HTTP GET, POST, PUT, etc. pero la diferencia es que vamos a trabajar en base a **`Observables`** los cuales son más poderosos que las **`Promesas`**. Ambos tienes sus usos pero el **`Observables`** tiene más control que las **`Promesas`**.

Para usarlo vamos a utilizar el servicio inyectado como sigue:

![image](https://user-images.githubusercontent.com/23094588/154920766-bc255f41-a14c-46a1-a16f-e679644f2fe9.png)

En el navegador seguimos recuperando los mismos datos.

![image](https://user-images.githubusercontent.com/23094588/154920944-12ae31a0-a602-4ec9-8fff-83af70c29bed.png)

Tenemos toda la respuesta:

![image](https://user-images.githubusercontent.com/23094588/154921230-349a00b7-4e1a-4ae9-8380-875ed023ea8e.png)

La **`data`**, la **`meta`** y la **`pagination`** podemos recuperar solo la **`data`** con:

![image](https://user-images.githubusercontent.com/23094588/154922364-fbabf5b2-a8ec-4c75-9b11-7a5db8108e63.png)

Pero el **`data`** nos esta marcando un error.

![image](https://user-images.githubusercontent.com/23094588/154922544-4f1a062a-ecc1-441a-b3e5-d13f7df079ab.png)

Si dejamos el cursor encima nos indica que es de tipo **`any`**, lo que esta pasando que TS no es capaz de saber que es **`resp`** nos esta retornando lo que ya vimos en el navegador que son **`data`**, **`meta`** y **`pagination`**. Hasta que ejecuto la URL podemos saber el tipado, entonces de alguna manera necesitamos especificare a TS el tipado que viene en la respuesta **`resp`**. Una forma simple para salir del paso es especificar que **`resp`** es de tipo **`any`**.

![image](https://user-images.githubusercontent.com/23094588/154923451-0d6e144b-782e-410b-b35d-1b949abc1c78.png)

Y de esta manera se va el error, esto le dice a TS que nos vale camote el tipo que sea esa respuesta, yo se que en la respuesta tengo la **`data`** y eso es todo lo que me importa. Si vemos la salida en el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/154923939-f4616540-1c89-47f0-ab07-7e1230e6bfa2.png)

Ya solo estamos pintando la **`data`** en la consola que es lo que realmente nos interesa.

La ventaja de utilizar el módulo **`HttpClientModule`** nos ofrece muchas cosas interesantes entre ellas son que las peticiones HTTP que hagamos nos retornan **`Observables`** a los cuales les puedo añadir funcionalidades a la hora de hacer la petición, puedo mapear la respuesta, puedo concatenar otras cosas, puedo hacer muchas manipulaciones en la petición, esto incluye también poder disparar otra petición simultaneamente, todo esto nos ofrese más ventajas sobre la forma en que trabaja JS.

### GIT

![image](https://user-images.githubusercontent.com/23094588/154925154-17cf0690-8be1-4ea6-bb88-d7642d9feee7.png)


## Mostrar los resultados en pantalla 09:15

En esta lección vamos a mostrar las imágenes en nuestra aplicación, actualmente estamos usando el URL de los Stickers, vamos a seguir usandolos y en un futuro los cambiaremos por los GIFs. 


Actualmente todas las busquedas que se hacen son de Dragon Ball Z ya que hemos pegado en el URL el parámetro **`q`** query que indica lo que queremos buscar,

```js
https://api.giphy.com/v1/stickers/search?api_key=3sZBfqeXrIArY6K1eq7xwISx6nb4B2V8&q=Dragon%20Ball%20Z&limit=10
```

vamos a hacer unos pequeños cambios para que la búsqueda sea dinamica en **`gifs.service.ts`**

Cambiaremos 

![image](https://user-images.githubusercontent.com/23094588/155114074-063315ea-f1e1-43ab-923a-da4d7dafdfc0.png)

Por

![image](https://user-images.githubusercontent.com/23094588/155114341-2b82cfef-6635-41dd-9998-649aa3c1c322.png)

De esta manera lo que recibamos 

![image](https://user-images.githubusercontent.com/23094588/155114533-da90876a-a78b-49dc-8ea1-1162a0096e3d.png)

Ademas de hacer esto nosotros tenemos que almacenar el **`resp.data`** en algún lugar, vamos a crear una propiedad pública en el Servicio llamada **`resultados`** que será un array de **`any`**.

![image](https://user-images.githubusercontent.com/23094588/155115385-123c03b1-47c5-4c58-a70f-610c9a24623a.png)

Observeces que TS acepta asignar **`resp.data`** a **`resultados`** por que no sabe a ciencia cierta si la **`data`** es un arreglo, con ponerle **`any`** ya nos deja hacer la asignación confiando en que nosotros sepamos lo que estamos haciendo.

Cuando se haga la petición del Servicio, los datos estan almacenados en **`resultados`**, vamos a inyectar nuestro Servicio en el componente **`resultados.component`** y vamos a crear un GETTER para retornar los resultados a partir del Servicio inyectado.

![image](https://user-images.githubusercontent.com/23094588/155116598-186e3328-ea46-4d8a-849c-e95e7980d39e.png)

Los GETTER facilitan mucho el acceso en la parte del HTML. También podríamos poner público el Servicio y acceder a el desde el HTML. Pero nosotros lo haremos a través del GETTER por que queda más limpio el código.

En **`resultados.component.html`** vamos a poner el siguiente código.

![image](https://user-images.githubusercontent.com/23094588/155117568-a85baa6e-53a1-4a45-bc45-63d910c1659f.png)

La desventaja de haber declarado a **`resultados`** como **`any`** no tenemos la posibilidad de ver las propiedades de **`gif.`**, por el momento la única forma que tenemos para conocer las propiedades es que escribamos algo en el navegador y que en la consola veamos las propiedades, es como normalmente se trabaja en JS:

![image](https://user-images.githubusercontent.com/23094588/155118502-053f7cea-5244-45b4-b3c5-23ef3f9dc4c6.png)

Por ejemplo tenemos una propiedad llamada **`title`** y lo colocamos en el HTML.

![image](https://user-images.githubusercontent.com/23094588/155118746-82dd4e81-a92f-48cc-aacc-791dfcce30a5.png)

![image](https://user-images.githubusercontent.com/23094588/155118958-a07b5b3a-a70c-42f8-ac32-0b99b3d7caf1.png)

![image](https://user-images.githubusercontent.com/23094588/155119073-6e925bd9-06c3-4b6d-9d29-e8aef00d21a3.png)

Ya vemos como estamos recuperando la información, vamos a darle un mejor diseño.

![image](https://user-images.githubusercontent.com/23094588/155119974-20b4e709-0d7e-4c38-828a-347dd885cd15.png)

![image](https://user-images.githubusercontent.com/23094588/155120089-873f31e9-dbc2-4a57-94c8-c5fc546370db.png)

Ahora vamos a pintar la imagen, usando la propiedad que esta dentro de las **`images`** y vamos a tomar la que se llama **`downsized_medium`** 

![image](https://user-images.githubusercontent.com/23094588/155120440-e7409fdc-a0c7-4422-b8f6-b7bb20737a30.png)

y a su vez tenemos que tomar la que se llama **`url`**.

![image](https://user-images.githubusercontent.com/23094588/155120568-91a91a1d-8e1f-4b52-a6ce-1e94fb87f2ff.png)

La desventaja de no tener el tipado es que tenemos que asegurarnos de ver las propiedades en la consola.

Para mostrar la imagen vamos a usar la propiedad **`gif.images.downsized_medium.url`** que usaremos en un elemento **`img`**.

![image](https://user-images.githubusercontent.com/23094588/155121488-d4db34c6-c4f8-482a-a387-160a4762e7dd.png)

Observese que en el navegador vamos a tener un error

![image](https://user-images.githubusercontent.com/23094588/155121618-1d1b7a4f-5ce9-474f-8c3c-3fbbac7fb126.png)

Esto pasa por que en **`<img src="gif.images.downsized_medium.url" alt="gif.title">`** estamos asignando al **`src`** un string con el valor **`gif.images.downsized_medium.url`** que realmente no es ningún URL a ninguna imagen, tenemos que indicarle a Angular que realmente ese valor hace referencia a un valor de una propiedad que contiene el URL esto lo hacemos poniendo corchetes en **`src`** y **`alt`**.

![image](https://user-images.githubusercontent.com/23094588/155122015-537cf7ad-452f-4429-bd8a-25137b07fa3a.png)

En el navegador ahora se podran ver las imágenes.

![image](https://user-images.githubusercontent.com/23094588/155122165-d6c1bce8-d2d8-4e0c-8f3c-e84488b8c8dc.png)

Vamos añadir una clase al elemento **`img`**.

![image](https://user-images.githubusercontent.com/23094588/155122819-54996e6f-b681-4214-a157-ee5a59ea1f88.png)

![image](https://user-images.githubusercontent.com/23094588/155122895-47ba246e-17c8-4841-a9fc-826afc7f416b.png)

Hasta aquí con el diseño de nuestra APP, en donde estamos los Stickers, vamos a cambiar el URL en el servicio para recuperar los GIFs.

![image](https://user-images.githubusercontent.com/23094588/155123203-b303cdba-643b-4669-ba9b-60eab34d4a6f.png)

En el navegador tenemos.

![image](https://user-images.githubusercontent.com/23094588/155123273-c80b43cb-1f5b-42e4-874a-a4678d2704d0.png)

![image](https://user-images.githubusercontent.com/23094588/155123410-b6d7c22e-0daa-4b1c-a454-c91a16094c51.png)


### GIT

![image](https://user-images.githubusercontent.com/23094588/155123763-199d2a74-0b78-4c24-9bc0-5ec012fb1e53.png)


## Colocando un tipado a las peticiones **`http`** 09:47

En esta lección vamos a poner el tipado a la **`respuesta`** que obtengamos del Servicio. El poner un tipado no es algo obligatorio podríamos mantener el tipado **`any`** sin más, pero tiene la desventaja de que no conocemos los nombres de las propiedades, podemos poner propiedades con nombres equivocados sin darnos cuenta hasta que se ejecute la APP, por ejemplo si pusieramos **`daata`** en lugar de **`data`**, TS no nos indica ningun fallo.

![image](https://user-images.githubusercontent.com/23094588/155124862-5781c338-05ca-410d-8b95-4fb807e250db.png)

En el navegador si hacemos una búsqueda.

![image](https://user-images.githubusercontent.com/23094588/155125019-31973e9b-d8b8-4332-b7ae-be5ba9f5f60b.png)

Encuentra los resultados pero estos no son asignados a **`resultados`** por que estamos asignando **`daata`** y no **`data`** TS no tiene manera de saber que dentro de **`resp`** viene **`daata`** por eso no nos marca error, este tipo de errores son dificiles de detectar, por lo que no es buena práctica declarar a **`resp`** como **`any`**, debemos ponerle un tipado ¿pero cúal? Si nosotros analizamos la respuesta en POSTMAN de lo que nos esta retornando el API de GIPSY

![image](https://user-images.githubusercontent.com/23094588/155126418-b259b432-264d-48c2-91fe-2373dad4b8b4.png)

![image](https://user-images.githubusercontent.com/23094588/155126200-73ed1269-859d-4e07-b5ef-68155e4019be.png)

![image](https://user-images.githubusercontent.com/23094588/155126786-ef413fdf-92b4-4347-92b3-e662dd11c6d2.png)

esto nos puede sacar canas por que en primera instancia viene un **`data`**, **`pagination`** y **`meta`**, dentro de **`data`** tenemos varias propiedades y a su vez dentro de cada propiedad existen más valores como en **`imagenes`**. Podríamos crear un tipado que tenga **`data`**, **`pagination`** y **`meta`**, o crear un tipado que tenga solo la **`data`** con todas sus propiedades o por lo menos la información mínima necesario que usemos pero toda esta carpintería lleva tiempo hacerla.

### Uso de [quicktype](https://quicktype.io/) para crear una Interfaz rápidamente.

Vamos a usar una herramienta que nos va a permitir crear las Interfaces para el tipado de una forma casí instantanea, vamos a copiar la respuesta completa que nos esta retornando Postman.

![image](https://user-images.githubusercontent.com/23094588/155127502-a7159f9c-48b1-4d53-af80-0d5d894eacb9.png)

Y vamos a ir a [quicktype](https://quicktype.io/) 

![image](https://user-images.githubusercontent.com/23094588/155127760-3544f581-ff3e-4f98-ab74-26aac7d3df93.png)

[quicktype](https://quicktype.io/) tiene extensiones para incorporarlo dentro de VSC en este caso usaremos su Web, presionamos en el botón rosa **`OPEN QUICKTYPE`** 

![image](https://user-images.githubusercontent.com/23094588/155128083-2a2fdf5f-e664-4579-996d-ca5d993211cb.png)

En el estado izquierdo vamos a copiar lo que obtuvimos en POSTMAN, le vamos a poner el nombre **`SearchGifsResponse`**.

![image](https://user-images.githubusercontent.com/23094588/155128469-c32f5fe7-c0fc-45b2-983b-491531d0fb3c.png)

En **Options** vamos a cambiar el lenguaje a **TypeScript**.

![image](https://user-images.githubusercontent.com/23094588/155128683-35521b95-8a5f-4611-a9ae-3faed17ddf25.png)

Esto nos crea la Interfaz necesaria, incluso enumeraciones y todo el código necesario para mapear la respuesta del API de GIPSY, simplemente copiamos todo el código generado presionando el botón **COPY CODE**.

Vamos a VSC y vamos a crear una Interface, en la carpeta **`gifs`** vamos a crear la carpeta **`interfaces`** y dentro de esta carpeta creamos el archivo **`gifs.interface.ts`** donde copiamos el código generado en [quicktype](https://quicktype.io/).

![image](https://user-images.githubusercontent.com/23094588/155130223-68e2d040-c742-456d-947b-f538679eb748.png)

Si observamos el código generado podemos ver que se han generado varias interfaces no solo una, si vemos la primer parte:

![image](https://user-images.githubusercontent.com/23094588/155130774-cbd4554a-542f-44db-a1ca-9a531d60d7cd.png)

Los datos se estar retornando en **`Datum`** vamos a cambiar este nombre por **`Gif`** para que tenga más sentido para nosotros.

![image](https://user-images.githubusercontent.com/23094588/155131250-bbf692a6-8c32-4fa7-ba94-cba10e92f3c9.png)

ya podemos trabajar con el **`SearchGifsResponse`**, vamos a regresar al **`gifs.service.ts`** y vamos a cambiar el **`any`** por esta Interfaz.

![image](https://user-images.githubusercontent.com/23094588/155131795-ddf8b726-107c-41dc-803d-8a77d426d4a0.png)

![image](https://user-images.githubusercontent.com/23094588/155131973-acd3ed8a-90d4-434c-a559-94da265921dc.png)


En teoría así debería funcionar pero ahora lo que se recomienda es que en logar de colocarlo donde lo pusimos se coloque en el método **`get`** ya que es de tipo GENERICO, esto significa que el **`get`** va a traerr una información y esa información tiene la forma de **`SearchGifsResponse`** luce de esta forma (no esta haciendo ningún mapeo).

![image](https://user-images.githubusercontent.com/23094588/155132616-ecc887bb-e894-4bca-8d3e-ca2396f0c963.png)

![image](https://user-images.githubusercontent.com/23094588/155132890-efeff58e-74a6-4cd1-97f6-da9832a95ee3.png)

![image](https://user-images.githubusercontent.com/23094588/155133130-6f572c99-1e83-464e-8586-1d23c61e5738.png)

De esta forma con la ayuda ya nos va poniendo las propiedades válidas que podemos usar gracias al tipado. Recordemos que la **`data`** es un arreglo por eso estamos indicando el acceso al primer elemento.

Ya hemos tipado la respuesta del servicio, pero nuestra propiedad **`resultados`** sigue estando tipada como **`any`**.

![image](https://user-images.githubusercontent.com/23094588/155133765-0ee458a4-8464-42c0-86de-0ddf222bfac0.png)

Debemos cambiar su tipo, recordemos que en **`resultados`** solo estamos almacenando la **`data`** de **`SearchGifsResponse`** a la cual llamamos **`Gif`** en nuestro archivo **`**`SearchGifsResponse`**`** por lo que el tipado de **`resultados`** nos queda así:

![image](https://user-images.githubusercontent.com/23094588/155134588-714da966-d136-4139-94e9-52fcd735a96e.png)

Si retornamos al navegador todo sigue funcionando igual.

![image](https://user-images.githubusercontent.com/23094588/155134770-773c03ac-ab32-44da-8847-92583d98660c.png)

La Interfaz no a añadido ninguna funcionalidad a la aplicación, simplemente es para ayudarnos a la hora de la codificación y evitar posibles errores y agilizar la programación.

Si vamos a **`resultados.component.ts`** podemos ver que en el GETTER ya infiere que **`resultados`** es de tipo **`Gif`**.

![image](https://user-images.githubusercontent.com/23094588/155135510-9d6925a1-19eb-4bd4-a515-c4fa6e91eeeb.png)

Incluso podríamos tiparla explicitamente:

![image](https://user-images.githubusercontent.com/23094588/155135694-6556097f-a92f-4321-92d6-b095db500978.png)

Aun que podríamos dejarla sin el tipo por que lo infiere.

En la parte del **`resultados.component.html`** también ya nos va presentando las propiedades válidas, ya no tengo que memorizarlas ni buscarlas en la consola gracias a TS.

![image](https://user-images.githubusercontent.com/23094588/155136115-0824e049-34fb-40c0-b93e-621d6535971e.png)

También nos marca los posibles errores que tengamos si escribimos mal una propiedad.

![image](https://user-images.githubusercontent.com/23094588/155136517-6e77d4c4-0104-4505-93ea-81f43bd5a953.png)


### GIT

![image](https://user-images.githubusercontent.com/23094588/155136896-65beb110-29df-4af3-b993-3674f8f546cf.png)

## **`LocalStorage`** 10:25

En esta lección vamos a hacer que el historial de búsquedas persista si nosotros refrescamos la página, actualmente podemos buscar varias terminos pero si refrescamos la página estos se pierden.

![image](https://user-images.githubusercontent.com/23094588/155138335-b7194c7a-5dec-4653-80e1-e8c42932b30f.png)

![image](https://user-images.githubusercontent.com/23094588/155138372-6f17b3ac-1ce0-4e77-b1a8-9749db99c924.png)

Al refrescar todo se pierde por que todo esta en memoria y al recargar se reinicia todo creando una nueva instancia del array donde teniamos el historial. 

Para almacenar esta información nos vamos a apoyar en el **Storage** del navegador si abrimos las herramientas del desarrollador en la pestaña **Application** podemos ver los diferentes tipos de almacenamiento con los que contamos.

![image](https://user-images.githubusercontent.com/23094588/155139027-f4f2bc2c-1821-4dcd-997d-479b2ee775ce.png)

Básicamente tenemos el **Local Storage** y el **Session Storage** ambas nos sirven para almacenar información de forma persistente en el navegador Web, la diferencia es que mientras que en el **Session Storage** almacenemos información esta se perdera al cerrar el navegador mientras que en el **Local Storage**  la información se mantendra persistente la información aun cerrando el navegador. Aun que en ocaciones el navegador podría tomar la decisión de eliminarlo bajo algunas condiciones como falta de espacio, también nosotros podemos eliminar estos datos manualmente pulsando en la X que se muestra sobre la lista de Key/Value que se muestra.

El **Local Storage** no es un sitio seguro para almacenar información sencible como tarjetas de crédito, password, etc., podemos almacenar información sin mucha importancia como podría ser el historial de la información que ha buscado en la APP.

Para almacenar en el **Local Storage** lo vamos a hacer dentro de nuestro Servicio **`gifs.service.ts`** usando **`localStorage`** que es un objeto de JS por lo que no necesitamos importar nada, este objeto tiene el método **`setItem()`** el cual necesita dos parámetros una clave y un valor expresado estrictamente como un string.

![image](https://user-images.githubusercontent.com/23094588/155141613-cde944ae-f872-48b4-aa4a-ba07769c9cbb.png)

Si hago una busqueda ya se almacena en el **Local Storage** el termino usado.

![image](https://user-images.githubusercontent.com/23094588/155141674-8923be68-cb49-47a8-8e6b-a24bc8135d4d.png)

Si realizo otra busqueda tenemos:

![image](https://user-images.githubusercontent.com/23094588/155141857-a140a032-0f7d-4c9e-b197-7440830624b8.png)

El valor del **`historial`** almaceno solo la última búsqueda pero la primera se perdio.

La idea que no solo almacenemos el termino buscado **`query`** sino todo el **`historial`** pero este es un array(objeto) y solo se pueden almacenar **`strings`**. Afortunadamente contamos con otro objeto de JS llamado **`JSON`** el cual tiene un método **`stringify`** el cual convirte a **`string`** cualquier objeto que se le pase como parámetro, por lo tanto podemos hacer lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/155142852-029ef8cc-19e5-4212-aaca-d6b101b96870.png)

Realizamos dos búsquedas y estas ya se almacenan en el **Local Storage** 

![image](https://user-images.githubusercontent.com/23094588/155143150-4b1ac009-23dc-4f99-9951-b623a557171e.png)
![image](https://user-images.githubusercontent.com/23094588/155143276-729dd484-b13f-4344-86c5-6c43f51efd30.png)

Si recargamos en navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/155143409-90801be9-43e6-4bf4-b9f4-eeaa1fd1ab4a.png)

la información renderizada se pierde pero la que almacenamos en el **Local Storage** sigue almacenada. 

Para que la información se siga renderizando cuando se refresca el navegador se debería tomar la información del **Local Storage**, ¿Cómo lo hacemos?

Podríamos usar el **`constructor`** del Servicio **`gifs.service.ts`** que ***se ejecuta solo una vez cuando el Servicio es creado***, por lo que es el lugar ideal para cargar la información del **Local Storage** por que solo se ejecuta una vez. Para recuperar la información del **Local Storage** nuevamente usamos el objeto **`localStorage`** pero en este caso vamos a usar el método **`getItem`** al cual le tenemos que indicar como parámetro que es lo que queremos recuperar en este caso es el **`hitorial`**, por lo que la instrucción completa es **`localStorage.getItem('hitorial');`**, 

![image](https://user-images.githubusercontent.com/23094588/155842584-c5e3d0c3-0d74-4133-a29e-5b1e0b890354.png)

pero hay un pequeño detalle lo que se recupera es un **`string`** o un su defecto un nulo en caso de que lo que queramos recuperar en el **Local Storage** no exista.

![image](https://user-images.githubusercontent.com/23094588/155842593-7d2e0a34-e7f7-43f1-be9b-b10cdd7c80bf.png)

Si intentamos almacenar lo recuperado del **`localStorage`** con:

![image](https://user-images.githubusercontent.com/23094588/155842692-1021b2b5-7ed1-41b2-ba9b-c01fcefbfe92.png)

¿Cómo resolvemos este inconveniente? Hay varias maneras, vamos a ver una tradicional que es facil de comprender.

Lo primero que vamos a hacer es validar que lo que se retorne del **`localStorage`** sea diferente de **`null`** y si esta condicion se cumple vamos a asignar a **`this._historial`** lo recuperado, recordemos que **`this._historial`** es un **`[] string`** arreglo de **`string`**, y lo que estamos recuperando del **`localStorage`** es un **`string`**,  pues contamos con el metodo **`JSON.parse()`** que es el inverso del **`JSON.stringify()`**, lo que hace **`JSON.parse()`** es convertir un **`string`** a dos posibles cosas ***un Objeto literal*** o un ***array de string o primitivos*** por lo que el código nos queda así:

![image](https://user-images.githubusercontent.com/23094588/155843058-5de7fa96-01b2-495d-a477-2f28a978243d.png)

Pero nos sigue marcando un error 

![image](https://user-images.githubusercontent.com/23094588/155843091-924f8644-bcd4-473c-a8f4-2c941d363916.png)

Ya que insiste que lo que se va a recuperar puede ser **`string`** o **`null`**, podríamos pensar en poner lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/155843299-3b654b50-0ff0-4638-b048-f70a8ea829f3.png)

Pero esto no anula el error, pero hay una cosa interesante que podemos hacer, yo le puedo decir a TS que confie en mi por que se lo que estoy haciendo ya que acabamos de validar de que el valor retornado por **`localStorage`** no sea **`null`** por lo que podríamos hacer la línea dentro del **`if`** sin ningún problema, **ESTO ANTES NO DABA ERROR PERO AHORA SI POR QUE ESTAMOS EN EL MODO SUPER ESTRICTO, SIMPLEMENTE LE VAMOS A DECIR A TS QUE CONFIE EN MI USANDO EL OPERADOR ! AL FINAL**.

![image](https://user-images.githubusercontent.com/23094588/155843323-cc4b4bbd-25cd-417d-bdad-2f0f44323f5f.png)

Si regresamos al Navegador Web

![image](https://user-images.githubusercontent.com/23094588/155843483-cecb8c52-5f0d-45ed-9891-d7c389ba38ea.png)

Ya vemos que sin hacer nada, magicamente se han puesto los valores en el SideBar, si hacemos unas nuevas búsquedas estas se almacenan en el **`localStorage`**.

![image](https://user-images.githubusercontent.com/23094588/155843544-34c46bce-1058-40b7-b2b4-065ff4887bde.png)

Si refrescamos la pantalla:

![image](https://user-images.githubusercontent.com/23094588/155843562-b3ac745b-0bdd-44d3-99d9-85b7c2cfb1f2.png)

Recupera los cuatro valores del **`localStorage`** y los podemos ver en el SideBar.  Nuestro código funciona, pero si lo queremos tener un poco más condensado podemos escribirlo de la siguiente forma:

![image](https://user-images.githubusercontent.com/23094588/155843757-3a44f06d-9967-4ab9-8617-73de9e974540.png)

Si recargamos la aplicación tenemos nuestro listado

![image](https://user-images.githubusercontent.com/23094588/155843871-69c8be8a-f30c-4299-a550-7b1fd7018ae7.png)

![image](https://user-images.githubusercontent.com/23094588/155843936-eba2fae2-3e5c-4a0e-a9af-d31611f5a56e.png)

Y sigue funcionando correctamente.

Si en el navegador borramos el **`localStorage`** 

![image](https://user-images.githubusercontent.com/23094588/155843990-1d0fd05a-cf30-4865-b40b-d0b6999d743b.png)

![image](https://user-images.githubusercontent.com/23094588/155844004-edeb279b-49dc-4c84-b765-9bb2cde3f159.png)

y recargamos la APP no revienta ya que le estamos colocando un arreglo vacío al **`_historial`**.

![image](https://user-images.githubusercontent.com/23094588/155844014-059e1b23-b9b6-4c38-bc44-fd18bde24872.png)

Con esto ya sabemos como hacer persistente la información.

### GIT

![image](https://user-images.githubusercontent.com/23094588/155844090-4e742f4a-f2f3-4fae-ae8a-d169dbb9c177.png)

![image](https://user-images.githubusercontent.com/23094588/155844101-2b3b5ef0-8a51-47fb-a356-ce78d71277c6.png)


## Cargar imágenes automáticamente 04:42

**``**

## Obtener imágenes desde el sidebar 03:31
## **`HttpParams`** 06:40
## Animate.style CSS 03:43
## Código fuente de la sección 00:07

