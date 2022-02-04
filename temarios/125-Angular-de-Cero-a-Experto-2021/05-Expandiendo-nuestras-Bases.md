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

### Uso de JS Tradicional

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

#### GIT

![image](https://user-images.githubusercontent.com/23094588/151530161-9447a9a2-8e2d-405d-944b-f79d921f2412.png)

### Uso de **`FormsModule`**

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

#### GIT

![image](https://user-images.githubusercontent.com/23094588/151533735-b269a4ec-45d4-4fa4-9c0c-d4cee509203f.png)

## **`ngModel`** 09:03

En esta lección vamos a ver como podemos recuperar la información de las cajas de texto (**`inputs`**) de una forma sencilla.

En nuestro archivo **`main-page.component.ts`** vamos a definir una propiedad **`nuevo`** que será un objeto que contiene dos propiedades **`nombre`** y **`poder`**

```js
nuevo = {
    nombre: '',
    poder: 0
}
```

Siempre será recomendable que en lugar de crear un simple objeto tengamos una Interface que nos describa como se debe construir el objeto, como el objeto representa un Personaje así llamaremos a la Interface.

```js
interface Personaje {
  nombre: string;
  poder: number;
}
```

Al tener la Interface definida podemos indicar el tipo del objeto **`nuevo`*:

![image](https://user-images.githubusercontent.com/23094588/151535761-f88476cb-e263-4cf1-9e29-49d5f6dfdfbf.png)

Si en el objeto no definimos todo lo que tengamos en la Interface nos indicará un error:

![image](https://user-images.githubusercontent.com/23094588/151536143-5afa3411-e505-4bf3-bdcf-74e6f17b0626.png)

**Esa es la importancia de tener definida la Interface, nos ayuda a controlar errores. En este caso hemos definido la Interface dentro del código de la Clase pero podría estar en un archivo independiente.**

Vamos a descomentar la propiedad **`poder`** para eliminar el error.

### Asignar Valores Iniciales a los **`Inputs`** en el HTML

En **`main-page.component.html`** podemos asignar un valor inicial a los **`inputs`** con la propiedad **`value`** de la siguiente forma:

![image](https://user-images.githubusercontent.com/23094588/151546233-d5f7072a-e7a3-43aa-be15-9c977b5dddc4.png)

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151546305-0ccd1591-93a3-4a32-8a44-9864ff80ea69.png)

### Asignar Valores Iniciales a los **`Inputs`** en el HTML con valores de Propiedades en el TS

Ahora lo que vamos a hacer es inicializar las propiedades del objeto **`nuevo`** como sigue:

![image](https://user-images.githubusercontent.com/23094588/151546706-b31e3f50-032a-4641-8eb2-decd6b9b7530.png)

En el HTML en lugar de Hardcodear el valor al Input vamos a indicarle que lo lea los valores de la Propiedad **`nuevo`** como sigue:

![image](https://user-images.githubusercontent.com/23094588/151547080-7ec29acb-9211-46ca-9a64-8c2f26e4fff0.png)

Lo que estamos haciendo con los corchetes en **`value`**, es decir **`[value]`** estamos indicandole que en nuestro componente hay alguna propiedad que queremos enlazar al valor del Input, si no ponemos el valor de la propiedad sino un valor cualquiera como teniamos antes nos marcara un error.

![image](https://user-images.githubusercontent.com/23094588/151547835-c7c3d9e3-a0e3-4f45-83ea-0d860eca2f7b.png)

Es necesario poner alguna propiedad definida en la clase.

En el navegador tendremos:

![image](https://user-images.githubusercontent.com/23094588/151548055-31f24e6b-01b4-41f9-ae70-864ab070709b.png)

Ahora lo que vamos a hacer es que al pulsar el botón Agregar muestre en la consola el objeto **`nuevo`**.

![image](https://user-images.githubusercontent.com/23094588/151548802-5938b1fc-448f-4265-9949-d0518cac5e7b.png)

![image](https://user-images.githubusercontent.com/23094588/151548842-fcfee937-daa0-4531-b8c9-50afd63bc16e.png)

Si nosotros añadimos algo en los Inputs y presionamos el botón Agregar, en la consola se sigue mostrando el objeto **`nuevo`** definido en la clase, ignora lo que pusimos en los Inputs.

![image](https://user-images.githubusercontent.com/23094588/151549110-231b282d-0b21-46b3-815b-24c8ddf2664b.png)

![image](https://user-images.githubusercontent.com/23094588/151547174-433cf1bc-2942-436e-8b1f-66c84347429c.png)

Este es el concepto de **One Way Data Mining**, del TS al HTML pero no a la inversa.

### Cambiar Valor de la Propiedad a través de los Inputs

Para cambiar el valor de la propiedad de acuerdo a lo que ingresemos en los Inputs lo vamos a hacer de una forma muy elemental invocando un evento cuando cambie el valor del Input.

![image](https://user-images.githubusercontent.com/23094588/151550024-8051672f-269d-4b56-b312-6fa62c7ce281.png)

Con el evento **`(input)`** estamos detectando cambios en el Input y dispara el método **`cambiarNombre( $event )`** que aún no hemos definido.

Vamos a definir el método **`cambiarNombre`**.

![image](https://user-images.githubusercontent.com/23094588/151550594-5908b705-aa51-45f6-a9b3-d7be2046f892.png)

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151550703-98d8e36e-c88e-4988-bae3-60d5c431a9a2.png)

Vemos que por cada caracter que ingresamos se invoca el el método **`cambiarNombre( $event )`**, y la salida aparece en la consola.

Dentro de todas las propiedad que tiene **`event`** tenemos una que nos interesa **`target`**. 

![image](https://user-images.githubusercontent.com/23094588/151551125-a317d686-d962-4f94-92cb-3edbe6b1ffa9.png)

Dentro de **`target`** (hay que dar en **`...`** para ver más propiedades) tenemos **`value`** que contiene el valor del Input **`Trucks123`**

![image](https://user-images.githubusercontent.com/23094588/151551497-563f6c45-08b2-43b4-ad51-e7527a271a0b.png)

Por lo que podemos mostrar en la consola solo esta propiedad con:

![image](https://user-images.githubusercontent.com/23094588/151551766-8e90c2d9-bf9c-4f5b-b099-cd0ccce49ad7.png)

![image](https://user-images.githubusercontent.com/23094588/151551872-d1458339-ec7d-413e-85a0-501321486180.png)

Como podemos ver estamos recuperando el valor del Input de Nombre, si queremos recuperar el valor del Input de Valor, tendríamos que hacer algo similar, invocar y definir un método y si tuvieramos más Inputs lo mismo, lo que se vuelve tedioso.

### Uso de **`ngModel`**

Si usamos **`ngModel`** podemos elimanar las siguiente propiedades del Input

```js
  ...
  [value]= "nuevo.nombre"
  (input)="cambiarNombre( $event )"
  ...
```

y sustituila por:

```js
  ...
  name="nombre"
  [(ngModel)]= "nuevo.nombre"
  ...
```

Incluso podemos eliminar el método **`cambiarNombre( event: any )`** del **`main-page.component.ts`** ya que no lo vamos a invocar más.

Cuando usemos **`ngModel`** es requisito usar el atributo **`name`**, si no nos marcara un error.

![image](https://user-images.githubusercontent.com/23094588/151596945-96512439-d9bd-4068-b9d4-d8aafc2a3f73.png)

Observese que estamos usando **`[(ngModel)]`** los corchetes son para que podamos ***establecer el valor***, podríamos tener solamente **`[ngModel]`** para asignarle el valor,  pero si además queremos que escuche el evento (que actualice el valor de **`nuevo.nombre`**) son necesarios los parentesis es decir **`[(ngModel)]`**. Si simplemente ponemos **`(ngModel)= "nuevo.nombre"`** no marca error, no asigna valor inicial, ni cambia el valor de la propiedad, no hace nada, no sirve de nada.

Este es el concepto de **Two Way Data Mining** tanto "Emite" o "Recibe" valores para las propiedades.

El código para el Input de Nombre nos queda así:

![image](https://user-images.githubusercontent.com/23094588/151597082-0c3b1b1a-ecef-45af-bed1-4efd8ef909ec.png)

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151597186-f16a5f76-a7ec-4a36-a94a-34107ef9b810.png)

Al insertar texto en el Input de Nombre y pulsar el botón Agregar vamos a tener lo siguiente en la consola:

![image](https://user-images.githubusercontent.com/23094588/151597303-dbde890e-5f4c-4710-8ad2-e4dd95825863.png)

Observese que ya no se esta invocando ningún evento cada que cambia el contenido del Input Nombre, pero el valor de la propiedad se esta cambiando cada que modificamos el valor del Input, solo que hasta que no presionamos el botón Agregar que es el que hace que se Submita el Formulario e invoque el método que pinta en Consola el valor no vemos el cambio. Para comprobar que el cambio se hace en tiempo real vamos a hacer que pinte el valor de la propiedad en el título de la columna:

![image](https://user-images.githubusercontent.com/23094588/151599834-2aee8954-5b4a-4921-8791-5d2df952976a.png)

En el navegador vemos el cambio en tiempo real:

![image](https://user-images.githubusercontent.com/23094588/151599971-8a0c9086-a9b2-444a-be3b-9b3fad71f79e.png)

![image](https://user-images.githubusercontent.com/23094588/151600009-2b80e005-431a-4418-929c-77e250924c93.png)

![image](https://user-images.githubusercontent.com/23094588/151600231-e5aa21c0-83b0-42ac-9109-af9481ff03d0.png)

![image](https://user-images.githubusercontent.com/23094588/151600267-374431dc-390b-4d84-9912-0070b2699261.png)

Y al presionar el botón Agregar:

![image](https://user-images.githubusercontent.com/23094588/151600356-c1098dd5-1aae-4a12-a487-5712a2154a2f.png)

se invoca al método que muestra el mensaje en la consola.

Vamos a hacer lo mismo en el Input del Poder.

![image](https://user-images.githubusercontent.com/23094588/151600744-7b6c8969-3b07-44b5-90cc-659b0394b2e5.png)

En el navegador:

![image](https://user-images.githubusercontent.com/23094588/151600860-694dc7e7-4346-4627-8aef-9b686776401f.png)

![image](https://user-images.githubusercontent.com/23094588/151600920-87ed482b-c118-4ee4-8faf-494f5ad098f9.png)

El código final de nuestros archivos quedo así:

![image](https://user-images.githubusercontent.com/23094588/151601538-5640a3f6-54b1-45ef-919a-573eb1c1794d.png)

![image](https://user-images.githubusercontent.com/23094588/151601661-20c69233-b635-43ac-9ef8-49d4a841e2db.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/151601801-a8dc9de4-51bf-455b-8d12-a71c40de41da.png)


## Mostrar listado de personajes 06:54

Una vez que hemos visto como recuperar los valores introducidos en los Inputs, en esta lección vamos a añadir el Personaje introducido al listado de Personajes existentes.

Lo primero que vamos a hacer es tener inicializado a nuestro nuevo personaje como sigue:

![image](https://user-images.githubusercontent.com/23094588/151602391-84f0f1a1-5859-4116-ad99-bbefeae66e19.png)

Ahora lo que vamos hacer es añadir una validación por medio de código (existen validaciones automáticas) para validar que lo introducido en el Input de Nombre tiene algún valor, el método **`agregar()`** nos va a quedar así:

![image](https://user-images.githubusercontent.com/23094588/151603311-694cb67c-f10a-477d-af39-ec80a1ea5823.png)

Estamos validando que si el Nombre no tenemos nada salga del método.

Si en el navegador presionamos el botón Agregar sin colocar nada el nombre no pasa nada.

![image](https://user-images.githubusercontent.com/23094588/151603572-a61440d9-4502-4c3c-9e6b-39d0e2099ea5.png)

Pero si ingresamos algo en Nombre y presionamos el botón Agregar se imprime en la Consola lo que hayamos insertado.

![image](https://user-images.githubusercontent.com/23094588/151603682-1def0a1d-4a97-4f4c-ac92-4f0060ba01e9.png)

### Uso de Array de Personajes

Actualmente en la pantalla tenemos en nuestro archivo **`main-page.component.html`**  "Harcodeados" los Personajes que se estan renderizando en la pantalla.

![image](https://user-images.githubusercontent.com/23094588/151604151-fd6839c9-56aa-4d42-b375-212813b72dfa.png)

![image](https://user-images.githubusercontent.com/23094588/151604311-ec1d55ea-dbe5-498e-af70-b796e55be9c8.png)

Vamos a hacer un cambio que va a consistir en declarar un array **`personajes`** de tipo **`Personaje`** (nuestra Interface) inicializado con los mismos personajes que tenemos "Harcodeados" en el HTML.

![image](https://user-images.githubusercontent.com/23094588/151605107-d3d947e0-3b10-4f10-ab75-af8c4166ea47.png)

Vamos a usar el array **`personajes`** para que renderice los Personajes en el **`main-page.component.html`** en lugar del código "Harcodeado":

![image](https://user-images.githubusercontent.com/23094588/151605896-929c1568-a051-433e-8ccb-5a5f20474b13.png)

![image](https://user-images.githubusercontent.com/23094588/151605915-0e339d85-0db3-4a30-a747-fa25a49d6f4e.png)

Si observamos los números ya no nos salen formateados, para conseguir el formateo vamos a usar un **Pipe** llamado **`number`**:

![image](https://user-images.githubusercontent.com/23094588/151607985-1e724595-4858-4c8f-8758-80e3bafa8277.png)

De esta manera nuestros números salen formateados:

![image](https://user-images.githubusercontent.com/23094588/151608058-81d9e487-2eb2-4055-9176-f878a1a29a32.png)


### Añadir Personaje al Listado de Personajes

Ahora lo que necesitamos hacer es que al presionar el botón Agregar se añada el Personaje que vayamos ingresando y una vez hecho esto limpiar los Inputs para una futura alta.

Una primer solución es la siguiente:

![image](https://user-images.githubusercontent.com/23094588/151608216-8e90d1e0-2913-48ac-9467-0db1e9139018.png)

Pero comparandola con la del profesor no es necesario crear un **`nuevoPersonaje`** ya que todo lo tenemos en **`nuevo`** por lo que la solución final es:

![image](https://user-images.githubusercontent.com/23094588/151608480-7cfaf5cf-bf7f-4ce4-bfae-4f683957f53e.png)

Probando la APP en el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151608579-5f0890e1-668b-455f-b85d-27dee9b354e8.png)

![image](https://user-images.githubusercontent.com/23094588/151608733-7b9b9799-a1ff-494e-bb6b-3aeea76989bf.png)

![image](https://user-images.githubusercontent.com/23094588/151608745-f16be7ed-bd9a-4dee-8cc0-e8ec106acce0.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/151609085-665e5af4-e6e6-49ef-bb4b-341f674095c7.png)


## Crear componentes hijos 05:47

Actualmente tenemos nuestra aplicación funcionando pero si vemos el archivo **`main-page.component.html`**:

![image](https://user-images.githubusercontent.com/23094588/151932598-6fcad396-4999-4ff0-bd72-7769fe841186.png)

Observamos que tenemos todo el código en este archivo, tanto el que pinta el listado de Personajes, como el código que permite añadir Personajes. El código podría seguir creciendo para que muestre más cosas.

Se recomienda separar nuestra aplicación en pequeños bloques reutilizables, en este caso el listado y el añadir personajes podrían ser componentes independientes.

### Crear componente Listado

Dentro del módulo de DBZ vamos a crear el componente **`personajes`** con el comando:

```sh
ng g c dbz/personajes -skipTests
```

![image](https://user-images.githubusercontent.com/23094588/151933761-edcc21da-819c-41e7-89a3-c98df34cb096.png)

![image](https://user-images.githubusercontent.com/23094588/151933962-6ad50d14-2593-4c7e-a6c2-49dbf71a7ba9.png)

Observese que usamos la bandera **`-skipTests`** para no crear el archivo de pruebas que si se creo, lo que no se creo el archivo css.

Si vemos el archivo **`dbz.module.ts`** tenemos:

![image](https://user-images.githubusercontent.com/23094588/151934345-e75061a9-1a32-4399-9774-2de4c305617f.png)

Vemos como se añadido el componente **`PersonajesComponent`** en **`declarations`**, pero no en **`exports`** recordemos que lo que ponemos en **`exports`** para que sea posible usarlo en otros módulos, en este caso el listado solo lo vamos a usar dentro del módulo DBZ especificamente en la clase **`main-page.component.html`** por eso no lo vamos a incluir en **`exports`**.

Ya tenemos nuestro componente **`personajes`** vamos a usarlo en **`main-page.component.html`** comentamos lo que renderizaba la lista y usamos el nuevo componente:

![image](https://user-images.githubusercontent.com/23094588/151935127-d5d2c46c-ca7d-4050-8d4f-bcb47858e6ae.png)

Al recargar el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151935171-1a719e1a-667b-4ddd-9fa3-ae9f0b49bb25.png)

Vemos que se esta renderizando el contenido del componente **`personajes.component.html`**

![image](https://user-images.githubusercontent.com/23094588/151935385-ab291041-b31f-434e-a0d3-8f07cd0b2965.png)

Vamos a sustituir este código moviendo el código que habíamos comentado en **`main-page.component.html`**, nos queda así:

![image](https://user-images.githubusercontent.com/23094588/151935637-df1395b4-cdf3-4df3-b726-a0336ce6fbf0.png)

![image](https://user-images.githubusercontent.com/23094588/151936867-ef1bae32-cc82-4cfd-8d41-ba33c73d0eb9.png)

Nos esta marcando un error en **`personajes`** ya que esto no existe en **`personajes.component.ts`**, existe en **`main-page.component.ts`** pero no en **`personajes.component.ts`**. Deberíamos pasar los **`personajes`** desde el **`main-page.component.ts`** al personaje "Hijo" **`personajes.component.ts`** pero eso lo vamos a hacer en la siguiente lección por ahora solo vamos a declarar una propiedad **`personajes`** en **`personajes.component.ts`** para evitar el error.

Actualmente nuestra clase **`personajes.component.ts`** la tenemos así:

![image](https://user-images.githubusercontent.com/23094588/151937007-ce0db7a1-50f9-4803-8f13-c90be1a00964.png)

Cabe hacer notar que en la clase tenemos el método **`ngOnInit()`** que corresponde al ciclo de vida de las clases y también tenemos un **`constructor()`**, como esta clase es muy simple y no vamos a utilizarlos podemos quitar toda esta parte del código quedandonos así:

![image](https://user-images.githubusercontent.com/23094588/151938609-449c723d-dc0a-4aec-87ae-30769494406e.png)

Ahora si añadimos la propiedad **`personajes`**.

![image](https://user-images.githubusercontent.com/23094588/151938798-5c089d29-499c-42ee-ad5e-389a41897d6c.png)

El error desaparece en **`personajes.component.html`** y podemos ver la pantalla no con el listado pero ya sin errores.

![image](https://user-images.githubusercontent.com/23094588/151939081-cbc54e73-8fd6-4855-a6b1-858fd61be0eb.png)

En la próxima lección vamos a ver como pasar información del componente Padre al Hijo, con eso resolveriamos el problema para que se renderice nuevamente el listado de Personajes.

### GIT

![image](https://user-images.githubusercontent.com/23094588/151939459-74d31d14-762a-443d-abd9-3241521fb5fd.png)


## **`@Input`** 06:55

En esta lección vamos a ver como pasar información del componente Padre al Hijo, especifícamente la lista de Personajes.

Lo primero que vamos a hacer es que en **`personajes.component.ts`** vamos a añador el decorador **`@Input()`** a la propiedad **`personajes`**, puede ir en dos líneas o en la misma.

![image](https://user-images.githubusercontent.com/23094588/151940360-e19c8ab7-26be-4523-a98b-31b87589477a.png)

Con **`@Input()`** le estamos indicando a Angular que quien utilice la propiedad **`personajes`** puede a su vez enviarle valores que serán recibidos en la propiedad.

Ahora en el archivo **`main-page.component.html`** que es donde estamos usando el componente **`personajes`** vamos a hacer el siguiente cambio.

![image](https://user-images.githubusercontent.com/23094588/151940926-ea366903-a19d-426f-900a-15e17a9a712a.png)

El **`[personajes]`** se refiere a la propiedad en el componente Hijo y **`"personajes"`** se refiere a la propiedad del componente Padre.

Si vemos el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151941198-d6f4731c-c75d-4030-8723-6906711b2ffc.png)

Podemos cambiar el nombre de la propiedad **`personajes`** en el Hijo para que no sea muy redundante (implíca cambiarlo tambien en el HTML) o podemos usar un nombre "virtual" como sigue:

![image](https://user-images.githubusercontent.com/23094588/151941707-d6083d89-2146-4ec6-9b6e-a6f4f19097df.png)

No es necesario cambiar el HTML.

![image](https://user-images.githubusercontent.com/23094588/151941898-71290d3d-aa84-45bf-9c77-77099d50df37.png)

Cuando asignamos el valor tenemos que usar **`data`**

![image](https://user-images.githubusercontent.com/23094588/151941802-d3c443c1-ff7e-4a7c-80b9-06cd1ddfdfd0.png)

![image](https://user-images.githubusercontent.com/23094588/151942729-f4f716e7-bbd6-4d0a-84c9-a3abcefe3a15.png)

Vamos a dejar el nombre **`personajes`**, incluso puedo ponerlo como sigue pero es redundante y no es neesario.

![image](https://user-images.githubusercontent.com/23094588/151943021-4d4bb7b8-f964-49d7-9264-f9ee71dee336.png)

![image](https://user-images.githubusercontent.com/23094588/151943173-65784f54-a078-48a1-995b-79c6b2d3807c.png)

Actualmente tenemos definida la propiedad **`personajes`** como un array de **`any`** con lo cual no se que propiedades tiene **`personajes`** sería bueno mantener el tipado.

Una podible opción es quitarle el tipado y ya va a depender de los datos que reciba el tipo que va  a adoptar.

![image](https://user-images.githubusercontent.com/23094588/151943563-16442976-33b6-4040-ab69-c3a4d0a4a45d.png)

Aun que nos indica que es de tipo **`never`**, esta opción no es la mejor, lo ideal es usar nuestra Interface **`Personaje`** que actualmente tenemos definida en **`main-page.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/151956665-9c20657c-e63d-47d0-a6ba-7b010a0e74df.png)

Lo que vamos a hacer es definir la Interface **`Personaje`** en un archivo independiente, dentro de la carpeta **`dbz`** vamos a crear la carpeta **`interfaces`** y dentro de esta carpeta vamos a crear el archivo **`dbz.interface.ts`**, en este archivo vamos a mover la Interface **`Personaje`** que tenemos en **`main-page.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/151957543-d6771550-f6e0-47e3-bf07-e47d86f9ef0a.png)

Como vamos a utilizar esta Interface fuera del archivo **`dbz.interface.ts`** tenemos que ponerle **`export`**.

![image](https://user-images.githubusercontent.com/23094588/151958686-f002f03d-b596-4028-9ea5-2c85fdd7565c.png)

Como hemos quitado la Interface de **`main-page.component.ts`** debemos importarla del nuevo sitio para que no nos indique error.

![image](https://user-images.githubusercontent.com/23094588/151959061-a62a4126-23b0-4b0f-a5aa-631de39fbb40.png)

**Recuerden que las Interfaces no tienen una contraparte de JS por lo que lo que escribamos en las Interfaces no existira en el Boundel final de la aplicación. Tampoco se importan en ningún mmódulo solo se importa en el archivo donde se vaya a usar.**

Ahora ya podemos tipar nuestro array **`personajes`** en **`personajes.component.ts`**:

![image](https://user-images.githubusercontent.com/23094588/151960151-82d4426b-a6b3-4a2e-b283-f45f3f08c0ad.png)

Y en el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/151960205-4f59d8f0-88f3-4bfc-855c-1aaeca68608e.png)

Incluso podemos insertar un nuevo personaje y este se listara en la lista.

![image](https://user-images.githubusercontent.com/23094588/151960620-846405ed-cfc2-4a02-8751-301d95fde3b4.png)

![image](https://user-images.githubusercontent.com/23094588/151960655-45b7bbea-bf4a-4348-9eda-2a75ebf8e14f.png)

Esto sigue funcionando como antes ¿Por qué?

Cuando en el componente Padre tocamos el botón Agregar se dispara el Submit, que llama al método **`agregar()`** que añade el personaje al listado y el ciclo de vida de Angular detecta un cambio y desde el componente Padre se le vuelve a mandar al Hijo los valores de los **`personajes`**, el Hijo lo renderiza y por eso podemos ver como se añade a la lista. Estas son las ventajas de usar Angular.

### GIT

![image](https://user-images.githubusercontent.com/23094588/151961896-7f1b9677-eb9c-48de-96df-5c94270de481.png)


## Tarea con inputs y módulos 12:46

En esta lección vamos a crear un nuevo componente que va a contener todo lo referente a Agregar un nuevo Personaje.

Vamos a comenzar creando el nuevo componente con el siguiente comando:

```sh
ng g c dbz/agregar --skipTests
```

![image](https://user-images.githubusercontent.com/23094588/151963594-9700e4c0-98e6-46d1-a701-bb766d8f5947.png)

Nos suguiere que usemos **`Use '--skip-tests' instead of '--skipTests'`**

Vamos a mover el código referente a Agregar de **`main-page.component.html`** a **`agregar.component.html`**

Nos marca una serie de errores ya que no tenemos el método **`agregar()`** ni la propiedad **`nuevo`** en este componente nuevo, debemos moverlo desde el **`main-page.component.ts`** a **`agregar.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/152115214-d9850b72-ddbb-4bae-95f5-b1ce63208e88.png)

Ahora lo que tenemos un error en **`this.personajes`** ya que hace referencia a una propiedad que no esta definida en esta clase, por lo que la tenemos que definir y además debemos anotarla con **`@Input`** para que reciba los valores en esta propiedad.

![image](https://user-images.githubusercontent.com/23094588/152115512-2bfbcd39-54d9-4ea0-b016-19cfe6cef0bf.png)

Lo siguiente es incluir en **`main-page.component.ts`** la etiqueta que hace referencia a **`agregar.component.ts`** y pasarle los **`personajes`**.

![image](https://user-images.githubusercontent.com/23094588/152115697-db098fca-904a-4e1c-8064-864a33408af5.png)

Ya no tenemos ningún fallo, si vemos el navegador podemos ver nuestra aplicación.

![image](https://user-images.githubusercontent.com/23094588/152115835-f30866c9-32d9-4139-9cd5-08d3e8c42f19.png)

![image](https://user-images.githubusercontent.com/23094588/152115855-1be9319a-a166-450d-b62d-860dd0b2e1a3.png)

![image](https://user-images.githubusercontent.com/23094588/152115871-7ced6c88-4c19-4063-b043-29f334a43657.png)

Aun que la APP funciona bien realmente el componente Agregar no debeía ser el encargado de insertar el Personaje sino que solo debería "Emitir" ese nuevo cambio, "Emitir" la información procesada del formulario, se inserta por que el Objeto **`personajes`** se esta pasando por ***referencia***, en la siguiente lección vamos a ver como evitar esto.

Antes de terminar desde **`main-page.component.ts`** vamos a pasar un objeto **`nuevo`** con valores que va a recibir **`agregar`** por lo que el formulario se va a rellenar con dichos valores ya no  va a aparecer en blanco como hasta ahora.

En **`main-page.component.ts`** añadimos el objeto **`nuevo`**.

![image](https://user-images.githubusercontent.com/23094588/152118601-02cfe293-f333-4169-8ae2-43933def8803.png)

En **`main-page.component.html`** mandamos también el valor del objeto **`nuevo`**.

![image](https://user-images.githubusercontent.com/23094588/152119383-6d66bcf9-15d2-452a-9b44-865fbaa40ca3.png)

Y en **`agregar.component.ts`** tenemos que apuntar a la propiedad **`nuevo`** con  **`@Input`**.

![image](https://user-images.githubusercontent.com/23094588/152119663-6caf968c-44f9-45d3-affa-e44410a751c7.png)

En la aplicación ya vemos como se pasa el valor de la propiedad **`nuevo`**.

![image](https://user-images.githubusercontent.com/23094588/152119727-2949991d-ad49-402c-9697-ae58a495caf8.png)

![image](https://user-images.githubusercontent.com/23094588/152119769-c728cd13-948b-4eca-89d1-85a1f38df2e9.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/152120038-b8ce814a-b475-4c84-8f3b-dbe56161b31e.png)

## **`@Outputs`** y **`EventEmitter`** 10:38

En esta lección vamos a ver como desde el componente Agregar "Emita" el nuevo personaje pero no lo inserte, por lo cual en **`main-page.component.html`** no vamos a mandar a los **`personajes`** como lo estamos haciendo actualmente:

![image](https://user-images.githubusercontent.com/23094588/152181768-8fe9b15a-da5d-4e61-af54-cac18d8888cc.png)

Lo vamos a dejar así:

![image](https://user-images.githubusercontent.com/23094588/152181843-a2341111-2c00-4859-9ee3-ab40e484a6b4.png)

Como ya no enviamos los **`personajes`** tenemos que modificar **`agregar.component.ts`**

![image](https://user-images.githubusercontent.com/23094588/152182328-3f3ed7c7-2f9c-4465-b497-3ebffa74ac6a.png)

Vamos a quitar los **`personajes`** y que añada el Personaje al Array.

![image](https://user-images.githubusercontent.com/23094588/152182572-d0f81236-96c6-4eba-8866-f7a0d42bbc39.png)

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/152182792-03ae2c16-a055-4b3b-a9b5-43a94f25ac8b.png)

![image](https://user-images.githubusercontent.com/23094588/152182894-784a42ed-b130-42e1-94c5-1eb6857c2bd4.png)

ya no se esta añadiendo el personaje al array.

### **`@Output`**

El decorador **`@Output`** es utilizado cuando tenemos un componente Hijo y necesita "Emitir" un valor al Padre. Se usa para emitir eventos 

En el momento que yo ya tengo la información que quiero enviar es el momento en que yo necesito "Emitir" la información al Padre, es como cualquier otro evento, cuando suceda en el componente Hijo sea capaz de reaccionar en base a ese evento. En este caso cuando en el método **`agregar()`** después de comprobar que se cumplen las validaciones del elemento **`nuevo`** es un buen momento para "Emitir" el valor. Para hacerlo tenemos que crear una propiedad(evento) con el decorador **`@Output`** y que es del tipo especial **`EventEmitter`** lo que me genera un **`Observable`**.

![image](https://user-images.githubusercontent.com/23094588/152185392-fcff7bb2-ddc8-4146-a998-76ed349b48a1.png)

Pero si observamos bien nos esta marcando un error:

![image](https://user-images.githubusercontent.com/23094588/152185521-2234f027-75c6-4335-b5c9-ab29cecd03ee.png)

Nos indica que **`EventEmitter`** es un **Generico** lo que quiere decir que puede ser cualquier cosa que nosotros queramos. Por ejemplo si es un **`string`** lo puedo poner así:

![image](https://user-images.githubusercontent.com/23094588/152185973-c9268a0c-fdc4-43bb-a40c-f68a930f16bd.png)

O incluso para no ser tan redundantes así:

![image](https://user-images.githubusercontent.com/23094588/152186084-ef97cb5c-7c0f-439d-b1ff-55fb4a253658.png)

Pero en nuestro caso no estamos emitiendo un **`string`** vamos a emitir un **`Personaje`**.

![image](https://user-images.githubusercontent.com/23094588/152186324-5716cfbd-fd6a-4d62-afcb-61445805551d.png)

Ahora vamos a usar la propiedad en el lugar donde queremos emitir el valor. Esta propiedad tiene muchos métodos entre ellos el **`suscribe`** por que es un **`Observable`**, pero en este caso vamos a usar la método **`emit()`** que como parametro le vamos a mandar **`this.nuevo`**

![image](https://user-images.githubusercontent.com/23094588/152187436-8634f41c-3e02-4822-9cf7-b9722ca876fb.png)

Si yo intemto mandar como parámetro un **`string`** me va a marcar error por que no cumple con la Interface que indique en el Generico que iba a usar.

Esto es todo por parte del componente Hijo.

Vamos a regresar al componente Padre **`main-page.component.html`** y tenemos que hacer que en el componente **`<app-agregar>`** detecte el evento que se dispará.

![image](https://user-images.githubusercontent.com/23094588/152188572-80266dc4-45c8-4940-b1c0-b87d0016c482.png)

En **`main-page.component.ts`** debemos crearnos el método **`agregarNuevoPersonaje()`**

![image](https://user-images.githubusercontent.com/23094588/152189409-2e71a295-8693-4be5-8453-29221628cf17.png)

Si cargamos el Navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/152189609-6e02437c-a525-4c76-8a01-a7ab78a59d45.png)

Al presionar el botón Agregar

![image](https://user-images.githubusercontent.com/23094588/152189633-1314ef4b-cffd-4ff3-a1a5-4e437fefbce5.png)

El evento se emitio del componente Hijo, lo recibio el Padre y el Padre lo interpreto.

Ahora lo que nos interesa es recibir la información mutada por parte del componente Hijo. Cuando se emite un evento y necesitamos las características de donde se hizo click, los valores del target, etc., todo ese contenido lo tenemos en **`$event`** por lo que será necesario enviarlo como parámetro del método:

![image](https://user-images.githubusercontent.com/23094588/152190369-f536927a-503f-4342-8052-1699fda6a6f1.png)

![image](https://user-images.githubusercontent.com/23094588/152190461-4f902194-e189-4bcf-95fe-57758f0055c0.png)

**`$event`** es de tipo **`Personaje`** por que así lo definimos en el componente Hijo.

En **`main-page.component.ts`** debemos recibir el argumento en el método **`agregarNuevoPersonaje()`**

![image](https://user-images.githubusercontent.com/23094588/152190890-442fdf3f-42e5-4f69-9534-5cbd60de912b.png)

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/152190955-8d3b5933-08ee-4100-8e12-b1235e044a6e.png)

![image](https://user-images.githubusercontent.com/23094588/152191035-af519d89-97b0-44de-9126-a6785b86ae6f.png)

Como podemos observar ya recibimos el Nuevo Personaje, por lo cual si ya lo recibimos lo podemos añadir en el array de los personajes.

![image](https://user-images.githubusercontent.com/23094588/152191328-7a1c148c-d9a3-4c93-89b0-a62f031439fb.png)

En el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/152191362-5be8358e-0c54-4c73-870b-ff7c10007005.png)

![image](https://user-images.githubusercontent.com/23094588/152191410-7786a3b6-33d6-45ab-b2c3-44e585a947de.png)

Podemos observar como al añadirlo a la lista este ya se renderiza en la lista de Personajes.

### GIT

![image](https://user-images.githubusercontent.com/23094588/152192079-df89e9fa-6f29-4789-b27f-0f41a48af347.png)

## Bonus: Depuración de aplicación 08:53

Hasta el momento lo que hemos utilizado para "Depurar" nuestra aplicación es usar los **`console.logs()`** 

![image](https://user-images.githubusercontent.com/23094588/152192896-4fff43a9-7624-4356-b84a-5af4595c9f5c.png)

Podemos abrir el Prototype del objeto y ver más características.

Tambien podemos pinchar en el enlace que esta al lado **`main-page.component.ts`** y se abre lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/152193673-1c4feff4-a19e-4646-a245-da6523d1ffcb.png)

Nos lleva al archivo fuente donde esta la sentencia que muestra el mensaje en la consola. En estos archivos fuentes podemos poner BreakPoints para que se vaya parando la aplicación y ver los valores de las variables que use.

![image](https://user-images.githubusercontent.com/23094588/152194108-3dd1c98d-c47d-4ad1-8cbc-f5a339a2ef5f.png)

Aquí podemos usar F5, F6, fecha Azul para ir recondiendo el código.

Otra forma de establecer BreakPoints es directamente en el código escribir la palabra **`debugger`** 

![image](https://user-images.githubusercontent.com/23094588/152194663-0bb89246-c994-48f2-89b3-74207adb68be.png)

Y cuando en la ejecución se llegue en donde se localiza esa instrucción se va a detener la ejecución.

![image](https://user-images.githubusercontent.com/23094588/152194774-6f6c0b00-ee30-4789-9c5e-14ca21d0e3a2.png)

La forma más potente y util para depurar es hacerlo dentro del propio VSC, lo primero que vamos a hacer es presionar F5 en VSC para seleccionar el entorno.

![image](https://user-images.githubusercontent.com/23094588/152195534-ceadb260-10b6-4ee7-bacd-4287f4b27f5f.png)

Vamos a seleccionar **`Chrome`** y esto nos va a crear el archivo de configuración **`launch.json`**.

![image](https://user-images.githubusercontent.com/23094588/152195843-4357337e-5de7-41d1-b078-649a73aed1e4.png)

Esto nos crea la carpeta **`.vscode`** con el archivo **`launch.json`** dentro.

![image](https://user-images.githubusercontent.com/23094588/152196139-d0058846-b0e1-4cd3-9322-9778cf05aa9b.png)

Podemos borrar la carpeta **`.vscode`** para generarla en el mismo entorno u otro diferente.

El único inconveniente que tenemos es que el URL creado lo hizo en **`http://localhost:8080`** lo podemos cambiar al **`http://localhost:4200`** que es el que nosotros estamos usando, una vez hecho el cambio salvamos y cerramos el archivo.

Nosotros tenemos arrancado nuestra consola y levantado el servidor, si en VSC presiono F5 se va a abrir un nuevo navegador y la APP se va ejecutar en modo DEBUGGER.

![image](https://user-images.githubusercontent.com/23094588/152199475-929bb3dc-8513-4d7e-8176-e3226775b4a5.png)

Podemos poner BreakPoints en los archivos de VSC y la aplicación se irá deteniendo cada que se encuentre uno de ellos.

![image](https://user-images.githubusercontent.com/23094588/152199997-ae419ceb-27bb-41dd-b135-f731403ec431.png)

![image](https://user-images.githubusercontent.com/23094588/152200120-2882424c-26ec-46c2-9baf-0b93c4b50f8d.png)

Podemos usar los botones para ir avanzando en el código y colocarnos en las propiedades para ir viendo sus valores, pasar de unos métodos a otros, etc.

Tenemos la sección de la izquiera donde podemos inspeccionar los valores de las variables.

![image](https://user-images.githubusercontent.com/23094588/152201086-13006c5e-a352-4c84-9566-a275c34063b0.png)

![image](https://user-images.githubusercontent.com/23094588/152201257-105c29d4-ef13-40a0-8981-bc649660927a.png)

Incluso podemos cambiar los valores en medio de la Ejecución

![image](https://user-images.githubusercontent.com/23094588/152201553-07fa1787-f8ca-4535-ab04-b09980c90751.png)

Y que los tome en cuenta.

![image](https://user-images.githubusercontent.com/23094588/152201653-f43b0703-d93b-4fa9-9dfe-587abd262589.png)

Para cerrar la Depuración es suficiente cerrar la ventana del navegador que abrio VSC. Incluso podemos borrar la carpeta **`.vscode`**.

Aun que me sigue conservando los botones superiores.

![image](https://user-images.githubusercontent.com/23094588/152202416-16a64033-e73b-4397-8a7f-1fe39798b3ee.png)

## Servicios 08:41

El concepto de los Servicios en Angular es una de las cosas más fuertes que tiene y ha hecho de que cuando estén trabajando en Angular, no sea tan necesario implementar patrones como **Redux**, **Blog**, entre otros.

Porque el hecho es que los Servicios en Angular son manejados de una manera muy eficiente, muy parecido a trabajar con un **Singleton**. **Singleton** digamos que sería que ustedes tuvieran una clase que es instancia de manera global en su aplicación.

Cuando ustedes quieran obtener información, se van al servicio y el servicio mantiene la información actualizada sin importar donde ustedes están.

### Crear el Servicio de Forma Manual.

Dentro de la carpeta **`dbz`** vamos a crear una carpeta llamada **`services`** por que vamos a hacer un servicio que solo se usara en el módulo de DBZ por eso lo colocamos en este sitio.

Dentro de la carpeta **`services`** vamos a crear el archivo **`dbz.service.ts`**.

Un Servicio también es una clase la diferencia con respecto a los Componentes es que el servicio se va a anotar con **`@Injectable()`** esto básicamente le esta diciendo a Angular que esta es una clase que se puede ***Inyectar***. Vamos a añadir el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/152205494-9a19b0a0-3ce3-4b72-833b-a57c01affe81.png)

Hasta aquí solo hemos creado el Servicio pero no hemos indicado en ningún sitio que lo use.

Los servicios se deben añadir dentro del módulo en un apartado adicional llamado **`providers`** donde se van añadiendo todos los servicios, añadamoslo en el módulo **`dbz.module.ts`**.

Los servicios sirven como Singlentons, es decir una sola vamos a tener una solo instancia que sirva a todo el módulo.

![image](https://user-images.githubusercontent.com/23094588/152304091-c4bacc54-a0f2-413c-8890-06f46774e725.png)

El servicio se va a ejecutar hasta que alguien lo requiera, en este momento no esta creada la primera instancia del Servicio.

Vamos al archivo **`main-page.component.ts`** donde tenemos lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/152305028-60632869-3ef7-4243-81d4-69f4b634328d.png)

En el Constructor vamos a Inyectar el Servicio creado como un parámetro.

![image](https://user-images.githubusercontent.com/23094588/152306045-eca378dc-fcc9-414b-8aa9-7a98a17b9768.png)

Si cargamos el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/152307167-c8380aaa-fe02-471c-8d77-c0c316c2941d.png)

Ya nos muestra en consola **`Servicio inicializado`** lo que significa que el servicio ya ha sido inicializado y esta listo para usarse.

Este mismo servicio lo podemos Inyectar en otro componente por ejemplo **`personajes.component.ts`**

![image](https://user-images.githubusercontent.com/23094588/152308466-21cf5dfc-61a7-41c1-8998-f123614d81bd.png)

Y al cargar el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/152308557-6de39cf1-52ae-4c28-8298-43d662c4c586.png)

Observece que el mensaje en consola **`Servicio inicializado`** solo aparece una vez a pesar de que estamos invocando el Servicio en dos Componentes diferentes, el servicio se crea primero en el **`main-page.component.ts`** y cuando se invoca en **`personajes.component.ts`** ya tenemos el Servicio inicializado y no crea una nueva instancia más bien usa la existente. 

Si en el **`main-page.component.ts`** se hicieran modificaciones al servicio (la información) se reflejaria en los demás componentes que usen el servicio.

Actualmente en el **`main-page.component.ts`** tenemos declarados todos los datos y el método para agregar un Personaje, esta lógica realmente no debería ir dentro del Componente, lo deberíamos tener en el Servicio esto lo hacemos para poderla centralizar la información y pueda ser usada por todos los componentes y no solo en donde se encuentra declarada la información como en este caso. Toda está lógica debería estar en el Servicio que es como una clase Abstracta donde vamos a poner toda la información y los métodos para interactuar con fuentes externas y poder manipular la información. **Esto es lo genial de los Servicios que tenemos la información centralizada donde tenemos la información.**

### GIT

![image](https://user-images.githubusercontent.com/23094588/152310753-5e15247b-8091-4945-99b8-29fc97e1533b.png)

## Centralizar el acceso de los personajes en el servicio 08:34

En esta lección vamos a centralizar la información de los Personajes en el Servicio, actualmente la información de los Personajes la tenemos en el **`main-page.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/152374961-dae1fecb-edcd-4c7b-857b-78efd9f0afe6.png)

Vamos a cortar el array de **`personajes`** y lo vamos a mover a **`dbz.service.ts`**.

![image](https://user-images.githubusercontent.com/23094588/152375558-2c8b4ebd-2e79-423b-b9ae-06cb24a1653e.png)

Al quitar los **`personajes`** de **`main-page.component.ts`** nos esta marcando un error.

![image](https://user-images.githubusercontent.com/23094588/152375961-31442a7f-c726-4a9d-9d22-0ecb7c97af00.png)

Vamos a crear nuevamente el arreglo de **`personajes`** y lo vamos a inicializar vacio.

![image](https://user-images.githubusercontent.com/23094588/152376288-2042fe89-b2ee-4cb2-bc3a-d888dd884598.png)

Si cargamos el navegador tenemos lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/152376753-84f91d06-ef15-4567-9133-f359f47931d8.png)

Como hemos declarado un array vacio no tenemos lista de personajes, pero si empezamos a añadir Personajes estos aparecen en la lista.

![image](https://user-images.githubusercontent.com/23094588/152377008-ee7c1718-96b0-4d87-a4ed-2c9771e14c2c.png)

En **`main-page.component.ts`** podemos recuperar la lista de los Personajes y asignarlos a la propiedad **`personajes`** recien creada, esto lo vamos a realizar en el Constructor.

![image](https://user-images.githubusercontent.com/23094588/152377597-c561701b-6d72-4137-ac0a-765b8ba855c2.png)

Si recargamos el navegador ya tenemos nuevamente la lista de Personajes por que la estamos recuperando del Servicio.

![image](https://user-images.githubusercontent.com/23094588/152377754-045cf26f-73b5-49f4-bf0c-6a8d0d611e53.png)

![image](https://user-images.githubusercontent.com/23094588/152377863-3c5f7039-5467-4632-bfde-2f9f6c4de532.png)

La aplicación funciona correctamente pero de alguna manera dentro del componente estamos nuevamente procesando la lista de **`personajes`** al tener la propiedad **`personajes`** declarada dentro del componente y asignarle los valores desde el Servicio o añadiendo valores a la lista en el método **`agregarNuevoPersonaje( personaje: Personaje)`**. ***Toda la manipulación de los datos debería hacerse dentro del Servicio y no dentro de los Componentes***.

Vamos a hacer una refactorización em el archivo **`main-page.component.ts`** eliminando la propiedad **`personajes`** y la asignación en el constructor.

![image](https://user-images.githubusercontent.com/23094588/152379603-8071ea47-b9b3-4a2c-bd70-2dc882314af2.png)

Vamos a incluir un **GETTER** para recuperar los datos desde el servicio.

![image](https://user-images.githubusercontent.com/23094588/152380524-35b23459-075d-4b3a-af5e-c74feca1ddd0.png)

Si cargamos la APP en el navegador sigue funcionando correctamente.

![image](https://user-images.githubusercontent.com/23094588/152380647-224e6269-3c6a-48ad-8d00-a93da3e49bf3.png)

![image](https://user-images.githubusercontent.com/23094588/152380693-b6a85ee1-8882-4dfa-a19e-a6fca8e24399.png)

Todo correcto hasta aquí.

Pero si pensamos un poco en el componente **`main-page.component.ts`** este no debería usar para nada los personajes, solo debería renderizar los Componentes Hijos **`personajes.component`** y **`agregar.component`**, vamos a eliminar del **`main-page.component.ts`** todo rastro de los **`personajes`**.

![image](https://user-images.githubusercontent.com/23094588/152394248-ec9ce7e2-cf02-43c0-9ed1-44440218057f.png)

Si cargamos la APP en el navegador tenemos errores que se muestran en la consola de Angular:

![image](https://user-images.githubusercontent.com/23094588/152394858-cb0749b7-7681-4313-92fa-389d3a75e600.png)

Esto es por que en el **`main-page.component.html`** estamos haciendo referencia a cosas que ya eliminamos en el TS.

![image](https://user-images.githubusercontent.com/23094588/152395078-d092c652-0fec-4ac6-83be-1729a14912d7.png)

Eliminamos todo el código que hace referencia a las propiedades o métodos que hemos eliminado.

![image](https://user-images.githubusercontent.com/23094588/152395287-eb9547ef-ea66-49f9-93f9-bef0f1ed052f.png)

Si cargamos la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/152395488-876edec6-15cf-4c98-b228-2b252bc7760b.png)

Si presionamos el botón Agregar ya no pasa nada ya que hemos eliminado el evento al que se invocaba y que llamaba al método **`agregar()`** encargado de insertar un nuevo Personaje.

### Encapsular los Personajes

Una cosa que deberíamos hacer es hacer el acceso más seguro a los **`personajes`** que tenemos en el Servicio, es decir no debemos permitir que en ningún lado nos manipulen el array de **`personajes`**, **NO DEBEMOS PERMITIR ESA MANIPULACIÓN** el único lugar donde se debe modificar el array de **`personajes`** es dentro del Servicio. Actualmente en el servicio tenemos el array de **`personajes`** público:

![image](https://user-images.githubusercontent.com/23094588/152396477-b35791cb-1eb3-4268-a0db-4cc78ffb0c50.png)

Vamos a ponerlo como privado, cuando se hace esto se le suele poner un **`_`** al nombre de la propiedad como convención para indicar que es una propiedad privada, pero lo que hace que la propiedad realmente sea privada es la palabra **`private`** que ponemos antes de la declaración de la propiedad.

![image](https://user-images.githubusercontent.com/23094588/152396980-bec5850d-27ad-4dee-8c57-9c4337e20d7e.png)

Al tener la propiedad privada ya no se puede utilizar fuera de la clase donde se declaro, en este caso el servicio **`dbz.service.ts`**, si algún componente que utiliza el servicio intenta usar esta propiedad no le será posible acceder a ella que es el caso de **`personajes.component.ts`**:

![image](https://user-images.githubusercontent.com/23094588/152489634-cad5a2e5-004d-4c2e-86cd-461f3b6ca58a.png)

Si la propiedad fuera pública sin el **`private`** si podríamos acceder a la propiedad.

Al ser **`private`** la propiedad **`_personajes`** no podremos manipular el array **`_personajes`** fuera de **`dbz.service.ts`**. Pero de alguna manera tengo que tener acceso a la lista de Personajes para poder renderizar la lista de personajes, en **`dbz.service.ts`** debemos crear un método que lo retorne, en este caso vamos a  hacer un GETTER.

![image](https://user-images.githubusercontent.com/23094588/152490474-c6c4e70c-2f67-4108-b1d4-54133b82b3fd.png)

```js
get personajes() {
   return this._personajes;
}
```

Estoy mandando **`this._personajes`** por que dentro del **`dbz.service.ts`** si tenemos el acceso a la propiedad, pero nuestro GETTER tiene un inconveniente **por que en JS  todos los Objetos son mandados por Referencia** y entonces desde donde se reciba **`personajes`** podemos manipular la lista con lo que estaríamos manipulando nuestra lista **`_personajes`** que es lo que queríamos evitar. Para romper esta relación se debe hacer de la siguiente manera, vamos a usar es operador [Spread](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Spread_syntax) **`...`**, el cual separa los elementos individuales del array de una manera individual y vuelve a crear otro array, con esto rompemos la Referencia con el objeto original **`_personajes`**.

**La sintaxis extendida o spread syntax** permite a un elemento iterable tal como un arreglo o cadena ser expandido en lugares donde cero o más argumentos (para llamadas de  función) o elementos (para Array literales) son esperados, o a un objeto ser expandido en lugares donde cero o más pares de valores clave (para literales Tipo Objeto) son esperados.

![image](https://user-images.githubusercontent.com/23094588/152492374-d4e51c27-cd73-4eeb-8c75-ef41d5f5a707.png)

Esto no es obligatorio de Angular es una ***buena práctica de JS***.

Regresemos a **`personajes.component.ts`** que actualmente lo tenemos así:

![image](https://user-images.githubusercontent.com/23094588/152492717-30394dff-c692-4f71-9ffd-712bed73adcf.png)

Vamos a comentar la propiedad **`personajes`** por que ya no la vamos a recibir a través de **`@Input`**, y lo vamos a sustituir por un GETTER retornando los **`personajes`** del servicio.

![image](https://user-images.githubusercontent.com/23094588/152493165-3cee5d0a-7b51-414d-a50b-bb29e2d706b5.png)

Si vamos al navegador ya veremos la lista de Personajes.

![image](https://user-images.githubusercontent.com/23094588/152493974-03feb7e4-5928-4b81-8802-92e1b73b2184.png)

Lo que no funciona es agregar un Personaje al presionar el botón lo haremos en la siguiente lección.

![image](https://user-images.githubusercontent.com/23094588/152494230-e6bf719d-335b-4b27-987c-2c856435f965.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/152494518-b42be2a3-3db3-4438-9166-27d28496c4bd.png)


## Métodos en el servicio 05:33

En esta lección vamos a añadir en el Servicio **`dbz.service.ts`** el método para agregar los personajes en la lista.

![image](https://user-images.githubusercontent.com/23094588/152495459-591339a8-7ffd-47b6-b660-68efbf789a6a.png)

Se agrega en **`_personajes`** y no en **`personajes`** para almacenarlo en la lista original de Personajes, de esta forma el GETTER también va a retornar los nuevos elementos añadidos en los Componentes que lo utilicen. 

Vamos a **`agregar.component.ts`** que actualmente lo tenemos así:

![image](https://user-images.githubusercontent.com/23094588/152496066-56299749-afdd-44de-b3c7-587a67545722.png)

Tenemos cosas que ya no debemos utilizar como lo estabamos haciendo hasta ahora como por ejemplo ya no vamos a emitir el nuevo personaje, por lo que lo vamos a comentar. Y vamos a inyectar el Servicio para poder usar el método recien creado que agrega los personajes.

![image](https://user-images.githubusercontent.com/23094588/152497187-f25946ac-37a5-4685-85e5-ff95dce87a61.png)

Si cargamos el navegador:

![image](https://user-images.githubusercontent.com/23094588/152497278-e38f5f2b-bbde-4f66-9033-93d14384cc7a.png)

Al presionar el botón Agregar se añade el personaje.

![image](https://user-images.githubusercontent.com/23094588/152497334-c0102d02-b07b-412b-b62e-45d5ec96f455.png)

La ventaja de trabajar con Servicios es que los datos y la lógica para manipularlos esta en el Servicio, de esta manera los componentes pueden acceder al Servicio para recuperar los datos y manipular la información. 

### GIT

![image](https://user-images.githubusercontent.com/23094588/152498386-f35d2016-523b-4500-8ae8-a952539e3698.png)


## Subida código a GITHUB

En esta lección vamos a subir todo el código de la sección al repositorio GIT, actualmente lo tenemos así:

![image](https://user-images.githubusercontent.com/23094588/152500000-25e920ee-c26e-494a-aefe-d250e85c4c46.png)

Vamos a pulsar el siguiente comando para hacer un PUSH.

```sh
git push -u origin main
```

![image](https://user-images.githubusercontent.com/23094588/152500214-f9b65ef1-ced6-4e61-a6e4-c23bc1b3d3c1.png)

Al actualizar GIT tenemos nuestro repositorio actualizado.

![image](https://user-images.githubusercontent.com/23094588/152500405-cd6fbc1e-6e33-407a-a3d9-9fb44f81d8d4.png)

### Creación de un Tag y Release

Adicionalmente vamos a crear un **Release Tag** que nos permite tener una versión del código que esta en este momento y poder descargarlo. El comando **Git** que vamos a usar es:

```sh
git tag -a v0.2.0 -m "Fin sección 5"
```

Este comando crea un **Tag** el atributo **`-a`** significa que es "anotado" con el texto **`v0.2.0`** que es una forma de nombrar nuestras versiones y con **`-m`** le damos el título de **`Fin sección 5`**

Si después de pulsar el comando anterior pulsamos:

```sh
git tag
```

vamos a tener:

![image](https://user-images.githubusercontent.com/23094588/152501302-6cf18281-b88a-4b10-b15e-1da2e96be11e.png)

Si retornamos al navegar en **GitHub** no vamos a ver ninguna diferencia.

![image](https://user-images.githubusercontent.com/23094588/152503726-a9010381-9e65-408f-9d04-34a96c416332.png)

Para subir el  **Tag** a **GitHub** lo hacemos con el comando:

```sh
git push --tags
```

![image](https://user-images.githubusercontent.com/23094588/152503896-21645a78-525a-473e-8e0b-40119c5eb84b.png)

Esto simplemente nos sube un **Tag** a **GitHub** no un **Release Tag**.

![image](https://user-images.githubusercontent.com/23094588/152504015-f40928ad-b427-470a-8a72-f81706c37e17.png)

Ya podemos ver que nos sale **`2 tags`** si pulsamos en **Releases** y en la pestaña **Tags** tenemos:

![image](https://user-images.githubusercontent.com/23094588/152504365-a7f26ee3-2ab1-49d5-8b03-b189756f5137.png)

Si pulsamos en el **Tag v0.2.0**  nos lleva a los detalles:

![image](https://user-images.githubusercontent.com/23094588/152504470-0cd2c319-a332-4498-82b4-b5367a49f191.png)

En esta pantalla podemos crear un **Release** a partir de un **Tag** pulsando en el botón **`Create release from tag`**.

![image](https://user-images.githubusercontent.com/23094588/152504689-ed041595-fe2c-4d1a-b8b9-a3b758737bbc.png)

Metemos la información que nos solicita:

![image](https://user-images.githubusercontent.com/23094588/152505117-d8ee0059-e378-492f-9e74-32c4e45c6428.png)

Y podemos pulsar en el botón verde **`Public release`**

![image](https://user-images.githubusercontent.com/23094588/152505241-5e456cf6-c00c-4c97-be75-d660bd1c574f.png)

Ahora si ya tenemos un **Release**

Como podemos ver en el **Release** tenemos la sección **Assets** donde podemos descargar el código fuente, vamos a pulsar en **`Source code (zip)`** el código se descarga:

![image](https://user-images.githubusercontent.com/23094588/152505666-370c7793-c6da-4477-b506-da90e3c0e92d.png)

![image](https://user-images.githubusercontent.com/23094588/152505760-0fe014bd-717d-48c7-a53a-bce52d70915c.png)


## Código fuente de la sección 00:12

https://github.com/adolfodelarosades/125-01-bases/releases/tag/v0.2.0

