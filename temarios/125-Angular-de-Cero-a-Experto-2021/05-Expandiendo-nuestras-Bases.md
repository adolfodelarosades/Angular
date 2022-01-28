# 05 Expandiendo nuestras bases - • 17 clases • 1h 54m

* Introducción a la sección 03:00
* Temas puntuales de la sección 00:21
* Continuación del proyecto 02:21
* Módulo DBZ (Dragon Ball Z) 10:39
* Diseño de la pantalla a trabajar 04:39
* FormsModule 08:37
* ngModel 09:03
* Mostrar listado de personajes 06:54
* Crear componentes hijos 05:47
* @Input 06:55
* Tarea con inputs y módulos 12:46
* @Outputs y EventEmitter 10:38
* Bonus: Depuración de aplicación 08:53
* Servicios 08:41
* Centralizar el acceso de los personajes en el servicio 08:34
* Métodos en el servicio 05:33
* Código fuente de la sección 00:12


## Introducción a la sección 03:00

En esta sección vamos a explicar la **Reutilización de Componentes**, vamos a mandar información de un ***Componente Padre*** a un ***Componente Hijo*** y viceversa, incluso a ***Componentes Abuelo*** o ***Componentes Nietos*** etc., la comunicación la vamos a realizar de diferentes maneras por ejemplo mediante  **`@Input`** y **`@Ouput`**, mediante **`EventEmitter`**, vamos a crear nuestros ***Eventos Personalizados***, nuestras ***Propiedades Personalizadas*** y también vamos a tocar el tema de los ***Servicios***.

Los Servicios en Angular es algo muy poderoso que nos permite evitar el uso de **`@Input`** y **`@Ouput`**. un Servicio se define en una Clase y se crea una única instancia de la misma esto lo hace Angular por defecto, los diferentes componentes pueden solicitar al Servicio cierta información sin necesidad de estar pasando información entre los componentes.

Los **`@Input`** y **`@Ouput`** son necesarios por que hay veces donde no necesitamos pasar la información al Servicio pero si entre Componentes, pero no solo nos sirven para hacer este tipo de comunicación entre Componentes, también nos sirven para pasar información hacia Directivas, también nos ayudan a reutilizar Componentes, en la Aplicación de Mapas los **`@Input`** y **`@Ouput`** tendrán un uso fundamental que un Servicio en teoría podría resolver pero es más complejo que hacerlo con un **`@Input`** u **`@Ouput`**.

## Temas puntuales de la sección 00:21

¿Qué veremos en esta sección?

Una vez sentadas las bases de Angular en la sección anterior, vamos a seguir expandiéndolas aquí, con los siguientes temas:

1. Profundizar un poco más en los módulos
2. **`FormsModule`**
2. **`ngModel`**
2. **`@Inputs`**
2. **`@outputs`**
6. Servicios
7. Métodos en servicios
8. Depuraciones

Hay más temas en los videos, pero en forma general esto es lo principal por ahora, tengan presente que aunque todo esto es opcional, la mayor parte de aplicaciones de Angular usan en cierto punto cada uno de los temas que están en esta sección, por lo que hay que asegurarnos de comprender bien cada lección.


## Continuación del proyecto 02:21

En esta lección se ve como descargar el proyecto del repositorio y ejecutarlo, cosa que se explico en la última leccón del módulo anterior.

## Módulo DBZ (Dragon Ball Z) 10:39

En esta lección vamos a trabajar con un nuevo módulo llamado **Módulo DBZ(Dragon Ball Z)**, será una nueva funcionalidad que vamos a añadir a nuestro proyecto con cosas de Dragon Ball Z, esta nueva funcionalidad incluye mostrar un listado, agragar Héroes, personajes de Dragon Ball, jugar con el poder que tienen entre otras cosas, todo esto esta relacionado con Dragon Ball Z por lo que lo lógico es crearnos un módulo que nos agrupe todo lo que tiene que ver con Dragon Ball Z.

### Creación del Módulo

Para crear este módulo lo vamos a hacer mediante el Angular CLI ya que los módulos anteriores los ccreamos manualmente, ahora lo haremos de una forma más automatizada.

Desde la consola vamos a colocarnos en el directorio que contiene nuestro proyecto y vamos a pulsar el siguiente comando:

```sh
ng g m dbz
```

El anterior comando es la forma simplificada de poner:

```sh
ng generate module dbz
```

Al comando se le pueden agregar otros atributos como **`--flag`** para complementar lo que se va a acrear. 

Al pulsar el comando tenemos:

![image](https://user-images.githubusercontent.com/23094588/150937535-2c573cd0-60f5-4003-a90d-47ac37afde65.png)

![image](https://user-images.githubusercontent.com/23094588/150944546-e22b0cf4-5da6-4afe-8f23-07d6bd090304.png)

Lo que ha hecho es crear el módulo **`dbz.module.ts`** dentro del directorio **`dbz`**.

El contenido de **`dbz.module.ts`** es:

![image](https://user-images.githubusercontent.com/23094588/150944944-3208564c-1144-47ce-a025-ee747b0b3b6f.png)

En el archivo nos a importado los módulos **`NgModule`** y **`CommonModule`** este último se nos a agregado por que usualmente vamos a utilizar las directivas **`*ngIf`** y **`*ngFor`**, en **`declarations`** no tenemos nada por que es un módulo vacío por el momento y en **`imports`** ya incluye el **`CommonModule`**.

Abriendo un pequeño parentesis en este módulo **`dbz.module.ts`** hemos visto que importamos el **`CommonModule`** y si abrimos **`heroes.module.ts`** también importamos el **`CommonModule`**, esto no implica que lo importe dos veces Angular es muy eficiente y solo utiliza el **`CommonModule`** una sola vez.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/151390999-03e484fc-80d3-448b-a633-edf9f0259f44.png)


### Creación del Componente

Vamos a escribir el comando de Angular CLI necesario para crear nuestro primer componente dentro del directorio **`dbz`**.

```sh
ng g c dbz/mainPage --skipTests
```

Estamos generando un nuevo componente dentro del directorio **`dbz`** llamado **`mainPage`**  y para no crear los archivos de prueba ponemos la bandera **`--skipTests`**

![image](https://user-images.githubusercontent.com/23094588/151391427-2a59bb0c-bf98-4568-9679-32f190527187.png)

Nos crea los archivos:

* **`main-page.component.css`**
* **`main-page.component.html`**
* **`main-page.component.ts`**

Y actualiza el archivo 

* **`dbz.module.ts`**


Por que modifico **`dbz.module.ts`** y no el **`app.module.ts`**, por que Angular CLI es lo suficientemente inteligente para saber donde esta ubicado el componente creado y saber a que módulo le corresponde dicho componente.

Nuestro archivo **`dbz.module.ts`** queda así:

![image](https://user-images.githubusercontent.com/23094588/151392322-271da042-a64c-4b70-9319-45dee0ecd6a2.png)

Si abrimos **`main-page.component.html`** tenemos:

![image](https://user-images.githubusercontent.com/23094588/151392533-f80c15de-2191-4fce-93f3-9e18ee546f4f.png)

Vamos a cambiar este contenido por el siguiente:

![image](https://user-images.githubusercontent.com/23094588/151392851-0e4cfc6d-63ac-4e35-b491-9c114e2c7813.png)

### Tarea

Tenemos que hacer que se pinte en pantalla el nuevo componente **`mainPage`** en lugar del que se esta pintando actualmente:

![image](https://user-images.githubusercontent.com/23094588/151393272-8e783601-caab-4f1c-9d94-15d0a0748cd0.png)

Esto lo hace por que actualmente tenemos el siguiente código en el archivo **`app.component.html`**:

![image](https://user-images.githubusercontent.com/23094588/151393731-846ee451-805d-4ad0-9f70-0a2d2928f952.png)

Los pasos que debemos seguir son los siguientes:

* Indicar en **`dbz.module.ts`** que vamos a **exportar** el componente **`MainPageComponent`** para que pueda ser utilizado en otros lugares.
  
  ![image](https://user-images.githubusercontent.com/23094588/151397972-5ae8fc02-02cb-4157-846b-22cf1e52493e.png)


* Añadir el nuevo modulo **`dbz.module.ts`** en **`app.module.ts`**.

  ![image](https://user-images.githubusercontent.com/23094588/151398144-62f0b823-c2d7-43d6-af32-149be7a83c2b.png)
  
* En **`app.component.html`** poner la etiqueta que hace referencia a nuestro componente.

  ![image](https://user-images.githubusercontent.com/23094588/151398278-21d2ae34-eadc-43e9-bc7e-0b21dde8d518.png)
  
Si vemos el resultado en el navegador tendremos lo que estabamos buscando:

![image](https://user-images.githubusercontent.com/23094588/151399619-e52b38bf-1e30-4246-8878-d6e6cfad4e33.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/151401671-5f67b4d3-0200-4af7-a791-773630265fab.png)

## Diseño de la pantalla a trabajar 04:39

En esta lección vamos a crear el diseño del punto inicial de nuestra APP. 

Vamos a añadir el siguiente código en **`main-page.component.html`**.

![image](https://user-images.githubusercontent.com/23094588/151508249-61fc64f3-656d-4fd4-b9cd-0b0fbf5201de.png)

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151508416-6feff351-1a5b-4bc1-8f12-ac3e96a9b92d.png)

Observemos como los espacios que pusimos en el código para alinear los números fueron ignorados.

Vamos añadir otra columna y títulos en ambas:

![image](https://user-images.githubusercontent.com/23094588/151510481-b1d7cace-1db2-4ec7-9d14-53bcbcb8cb69.png)

![image](https://user-images.githubusercontent.com/23094588/151510511-72139211-5e83-4766-b4a5-924f5a9fe669.png)

Para que las columnas salgan una al lado de la otra vamos a introducir algún CSS en el archivo general **`styles.css`** (lo pudemos añadir solo en **`main-page.component.css`** para que solo afecte este componente)


Al añadir solo el siguiente código:

```css
.row {
  display: flex;
}
```

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151511152-f17cffec-dbf8-455a-8d85-ad5875c4cca0.png)

Vamos a añadir algún estilo para la columna:

```css
.col {
  flex-grow: 1;
}
```

En el navegador vemos:

![image](https://user-images.githubusercontent.com/23094588/151511472-9bfcddea-409d-4a26-8b63-a4b56cf2fd0c.png)

Con la propiedad **`flex-grow`** estamos expandiendo las columnas lo más posible pero siguen pegadas, vamos a añadirle un margen derecho para separarlas

```css
.col {
  flex-grow: 1;
  margin-right: 10px;
}
```

![image](https://user-images.githubusercontent.com/23094588/151511776-cd94a7f8-d36a-4d3f-967e-02ced2967539.png)

Observemos que las columnas ya estan separadas pero realmente la segunda columna no esta totalmente alineada con el título principal, por el momento lo vamos a dejar así.

Ya que estamos aquí vamos a incluir un estilo para los **`inputs`**

```css
input {
  display: block;
  margin: 5px;
}
```

Todo el código CSS incluido es:

![image](https://user-images.githubusercontent.com/23094588/151512175-f73e8684-0398-4409-b24c-fb2c2849fddb.png)

**NOTA: Todas los estilos de CSS que hemos ingresado son los estandar de CSS3 ya que aún no hemos incluido Bootstrap en el proyecto.**

Ahora en **`main-page.component.html`** vamos a añadir un formulario.

```html
<form>
  <input type="text" placeholder="Nombre" />
  <input type="number" placeholder="Poder" />
  <button>Agregar</button>
</form>
```

![image](https://user-images.githubusercontent.com/23094588/151513533-44b69b92-357b-44ea-8b82-f999b781a058.png)


Cuando nosotros pulsamos el botón de **`Agregar`** existe un **Full Page Refresh**  (observe la URL generada **`http://localhost:4200/?`**) 

![image](https://user-images.githubusercontent.com/23094588/151514383-85a92bcd-053c-4e18-8a06-7b2f399dfe11.png)

Normalmente cuando trabajamos con Angular no es necesario el **Full Page Refresh** ya veremos como evitarlo.

### GIT

![image](https://user-images.githubusercontent.com/23094588/151518728-a6116ffa-e223-4132-abc4-3d2494b01428.png)


## **`FormsModule`** 08:37

En la lección pasada creamos el diseño de nuestra pantalla, tenemos el problema de que cuando pulsamos el botón de **`Agregar`** existe un **Full Page Refresh** lo que no es optimo tener en la APP.

¿Cómo podemos prevenir el refrescamiento de la pantalla y manejar el Submit del Formulario?

Lo primero que vamos a hacer es que cuando pulsemos el botón Agregar muestre un mensaje en la consola para comprobar que lo estamos pulsando, esto lo hacemos añadiendo el evento **`(click)`** en el botón y que este invoque un método que va  a hacer el que pinte el mensaje en la pantalla.


![image](https://user-images.githubusercontent.com/23094588/151524523-eea14299-1d96-435f-86f3-830c84aa18fa.png)

Nos esta poniendo un error sobre **`agregar()`** ya que no lo hemos definido en **`main-page.component.ts`**, para hacerlo incluimos lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/151524977-17a9cc26-6138-44f3-8c06-d907df3d7aa2.png)

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151525066-02cde6bc-60e1-47eb-9143-c09c557ccb78.png)

Al presionar el botón Agregar aparece el mensaje **`Has presionado el botón Agregado`** pero de inmediato se refresca la pantalla y es dificil capturarlo en la imagen pero si ejecutamos la aplicación lo apreciamos.

![image](https://user-images.githubusercontent.com/23094588/151525465-4ac006ff-10f2-4709-bde6-b46d867f9276.png)

Si seguimos las buenas prácticas de programación el evento no lo debemos invocar en el botón sino en el Submit del Formulario, vamos a hacer los siguientes cambios.

![image](https://user-images.githubusercontent.com/23094588/151526282-54a98212-506d-4523-95e8-32efdc968b55.png)

Aquí lo que estamos haciendo es que al presionar el botón de tipo **`submit`** le indique al Formulario que Poste o haga el Submit del Formulario con **`(submit)="agregar()"`**, estamos invocando al mismo método. ***No es el botón el que dispare todo es el formulario***.

En el navegador pasa lo mismo al presionar el botón Agregar pero lo hemos hecho con mejores prácticas de programación, aun que se sigue refrescando la pantalla y apenas alcanzamos a ver el mensaje **`Has presionado el botón Agregado`**  al ejecutar la aplicación.

![image](https://user-images.githubusercontent.com/23094588/151527361-1ec09845-32ee-48af-8865-5a5af6522b27.png)

El problema del refresco de la pantalla sigue, si tenemos conocimientos de JS podemos enviar como parámetro del método el "evento" que se usa al hacer el **`submit`** del formulario.

Para mandar como parámetro el evento lo hacemos usando **`$event`**:

![image](https://user-images.githubusercontent.com/23094588/151528408-d6d13349-ff98-44c2-96f3-3aefe18f3132.png)

Ahora vamos a modificar el método **`agregar()`** del **`main-page.component.ts`** para que reciba el evento.

![image](https://user-images.githubusercontent.com/23094588/151528772-1efe8d27-e955-423b-a654-88baa8064d40.png)

Tenemos que declararlo explícitamente de tipo **`any`** para evitar que nos arque error.

Dentro del **`event`** tenemos la propiedad **`event.preventDefault()`** que ***Prevee el comportamiento por defecto que tiene el submit de un formulario, que es básicamente hacer el submit o posteo*** por lo que al ponerlo en el método evitaremos el Refresh de la página.

![image](https://user-images.githubusercontent.com/23094588/151529419-0344e26b-6be3-45e9-ac4d-e36c02573eaa.png)

Al probar en el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151529531-d4c9f25a-5565-4454-9ac8-14fb9c5750b2.png)

Ahora al presionar el botón Agregar ya no se refresca la pantalla por que no se esta realizando el Submit del Formulario y podemos apreciar en la consola el mensaje **`Has presionado el botón Agregado`**.

**NOTA: La forma en que hemos evitado que se haga el Submit del formulario es la forma tradicional de JS, pero con Angular la podemos realizar de una forma diferente.**

Podemos sacar en la consola el valor de **`event`**

![image](https://user-images.githubusercontent.com/23094588/151530475-0d148530-c7a9-45c5-9e31-8ef441b2f991.png)

![image](https://user-images.githubusercontent.com/23094588/151530736-21614143-de43-4570-8762-6296077f8e0a.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/151530161-9447a9a2-8e2d-405d-944b-f79d921f2412.png)


Gracias a que Angular es un Framework podemos hacer lo anterior de una forma más simplificada gracias a que cuenta con el módulo **`FormsModule`** que nos permite trabajar con Formularios (Formularios normales por que también existen los Formularios Reactivos).

En el módulo de DBZ **`dbz.module.ts`** vamos a importar el módulo **`FormsModule`**.

![image](https://user-images.githubusercontent.com/23094588/151531674-8dc8ef3f-5a52-46e0-9936-42f1e63d3303.png)

En nuestro archivo **`main-page.component.html`** vamos a cambiar **`(submit)`** por el evento personalizado que nos ofrce el **`FormsModule`** llamado **`ngSubmit`**, además vamos a quitar el parámetro **`$event`**, esta es la ventaja de usar **`FormsModule`** que nos simplifica el código.

![image](https://user-images.githubusercontent.com/23094588/151532220-e83aa53a-9623-40ea-bc06-4c1dd967d2da.png)

Vamos a **`main-page.component.ts`** para eliminar del método **`agregar( event: any ) `** el parámetro **`event: any`** que ya no estamos enviando y la sentencia **`event.preventDefault();`**.

![image](https://user-images.githubusercontent.com/23094588/151532888-a75dd168-3740-4e97-85fd-f096a867d2f8.png)

Si vamos al navegador y presionamos el botón Agregar tenemos:

![image](https://user-images.githubusercontent.com/23094588/151533007-3ceca8f5-0121-4bea-9a98-d88e32584c17.png)

No refresca la pantalla y tenemos un código bastante más simple gracias a usar **`FormsModule`**.

**NOTA: Si por alguna razón el código no hace lo anterior, es posible que tengamos que reiniciar el Servidor ya que modificamos código en los módulos y cuando se hace esto algunas veces si no coge el nuevo código será necesario reiniciar el servidor.**

### GIT

![image](https://user-images.githubusercontent.com/23094588/151533735-b269a4ec-45d4-4fa4-9c0c-d4cee509203f.png)

## **`ngModel`** 09:03

**``**



## Mostrar listado de personajes 06:54
## Crear componentes hijos 05:47
## **`@Input`** 06:55
## Tarea con inputs y módulos 12:46
## **`@Outputs`** y **`EventEmitter`** 10:38
## Bonus: Depuración de aplicación 08:53
## Servicios 08:41
## Centralizar el acceso de los personajes en el servicio 08:34
## Métodos en el servicio 05:33
## Código fuente de la sección 00:12
