# 110 Creación de un Juego de Ahorcado


#### Tiempo: 1h 13min

* Introducción a la sección 2 min
* Demostración de lo que realizaremos al final de la sección 2 min
* Etiquetas comunes del HTML 1 min
* Instalaciones adicionales 6 min
* Inicio de nuestro juego 5 min
* Estilo de nuestra aplicación 5 min
* Estructura HTML de nuestro juego 9 min
* Creando letras de forma dinámica 8 min
* Lógica de la palabra oculta y la palabra hasta el momento 5 min
* Mostrar letras correctas en la palabra oculta 8 min
* Cambiar la imagen y contar los intentos fallidos 6 min
* Verificar si el usuario gana o pierde 6 min
* Mostrar mensaje de victoria o derrota 5 min
* Códigos fuente de todo el curso 1 min

## Introducción a la sección 2 min

Vamos a crear un ***Juego de Ahorcado***, esto me va a servir para explicarles un tema que hablamos muy poco durante el curso y es el tema de los Frameworks existen muchos frameworks en Internet especialmente cuando estamos hablando de la programación web.

Hay tres predominantes **VueJS**, **React** y **Angular**.

También tenemos otros que la verdad ya cada vez están bajando un poco su intensidad como es el **Backbone** o **EverJS** pero en si los tres que les mencioné son muy populares, en este curso vamos a hacer una pequeña aplicación de Angular que es un framework, que nos va a permitir a nosotros poder hacer toda la interacción del HTML con nuestro código de JavaScript.

No es que Angular sea el más sencillo, no es que sea el más complicado pero esto me va a servir a mí para explicarles ustedes cómo pueden ustedes trabajar con un framework especializado.

No se asusten, el contenido puede ser abrumador, pero vamos a hacerlo todos juntos al pie de la letra y van a ver que vamos a emplear todo lo que hemos visto hasta el momento en este curso. 

## Demostración de lo que realizaremos al final de la sección 2 min

![image](https://user-images.githubusercontent.com/23094588/129441503-a62b4f00-e810-44b0-8b87-ad986491664c.png)

![image](https://user-images.githubusercontent.com/23094588/129441512-e5e5c578-a1ac-431d-a59a-559338da1dcf.png)

![image](https://user-images.githubusercontent.com/23094588/129441515-795c6fa1-e8e3-49f4-97f8-eeea1fce5bcd.png)

![image](https://user-images.githubusercontent.com/23094588/129441528-107ac88d-ab4b-49c3-b56d-e88e85cb632d.png)

![image](https://user-images.githubusercontent.com/23094588/129441542-de505f48-6f54-438b-9e51-6c947b0b63ba.png)

## Etiquetas comunes del HTML 1 min

Abrir el siguiente enlace y tenerlo a la mano

[Mozilla Developer - Elementos HTML](https://developer.mozilla.org/es/docs/Web/HTML/Element)

## Instalaciones adicionales 6 min

### Instalación de Node

https://nodejs.org/es/

![image](https://user-images.githubusercontent.com/23094588/129442072-bbec35df-97bb-4be8-9a54-639c8f31c069.png)


Verificar versión de NodeJS si ya la tenemos instalada:

```sh
node -v
```

![image](https://user-images.githubusercontent.com/23094588/129441969-413dabe2-afa4-49cc-902e-ac2a6ad2676a.png)

Verificar versión de NPM que se instala al instalar Node:

```sh
npm -v
```

![image](https://user-images.githubusercontent.com/23094588/129442459-848073b6-de95-446c-8658-bb43589d3317.png)

### Instalar Angular Cli

https://angular.io/cli

![image](https://user-images.githubusercontent.com/23094588/129442141-1ca66aab-c18b-440a-bfef-44ab12d113f8.png)

Para instalarlo lo hacemos con:

```sh
npm install -g @angular/cli
```

Para MAC es con:

```sh
sudo npm install -g @angular/cli
```

En MAC es posible que tengamos restricciones en nuestro equipo, si nos manda algún error en la instalación previa, debemos realizar el siguiente comando:

![image](https://user-images.githubusercontent.com/23094588/129442298-42d19b1b-804f-4642-9009-8885dfbcad3e.png)


```sh
sudo npm install --unsafe -perm -g @angular/cli
```

Para verificar que todo se instalo bien o verificar que versión de Angular CLI teniamos instalada damos:

```sh
ng --version
```

![image](https://user-images.githubusercontent.com/23094588/129442567-8a6958ac-8bf1-4f8b-b8df-ac8acba0ef00.png)

La volvi a instalar y me sale:

![image](https://user-images.githubusercontent.com/23094588/129442619-8165e50f-2f2b-4cd0-94c9-3ab5d8b985fb.png)

## Inicio de nuestro juego 5 min

Con Angular CLI podemos generar la estructura de nuestro proyecto, abrimos la terminal y necesitamos estar ubicados en la carpeta donde queremos que se cree nuestro proyecto:

![image](https://user-images.githubusercontent.com/23094588/129442740-f293c491-1518-48aa-84a8-cb8148b846b3.png)

### Creación del Proyecto `110-Juego-de-Ahorcado`

Para crear el nuevo proyecto usamos el comando de Angular CLI:

```sh
ng new 110-Juego-de-Ahorcado
```

Como no deja que los nombres de los proyectos empiecen con números vamos a poner:

```sh
ng new Juego-de-Ahorcado
```

Nos hace dos preguntas a las cuales respondemos con No y Enter para coger el valor por default(en la V6 no los hacia)

![image](https://user-images.githubusercontent.com/23094588/129443081-037e3c6c-7cf4-4a39-95bf-5068d93ba93f.png)

Se empieza a crear toda la estructura del proyecto, se crea la carpeta **`Juego-de-Ahorcado`**.

![image](https://user-images.githubusercontent.com/23094588/129444420-ada6cefa-2e33-4cbc-88aa-4d7fcc5c8455.png)

Se ha creado automáticamente el repositorio GIT.

### Trabajar con la Terminal del MAC vs Terminal de VSC

Tenemos la posibilidad de trabajar desde ambas terminales, pero para algunas cosas la Terminal de VSC a veces falla, así que yo prefiero trabajar con la Terminal del MAC, nos cambiamos a la carpeta **`Juego-de-Ahorcado`**.

![image](https://user-images.githubusercontent.com/23094588/129444432-33ce60d7-ecfd-49a0-9691-df21b634c89c.png)

### Abrir en VSC la carpeta **`Juego-de-Ahorcado`**

Vemos todo lo que se ha creado dentro de la carpeta **`Juego-de-Ahorcado`**

![image](https://user-images.githubusercontent.com/23094588/129444547-d203ba47-c3db-4d69-8617-bc1b866f91c3.png)

### Ejecutar la APP creada

```sh
ng serve -o
```

La APP se ejecuta se carga un LiveServer

![image](https://user-images.githubusercontent.com/23094588/129444970-89a0188e-fa9e-41cd-af07-5c544f921b12.png)

y abre el navegador en la URL http://localhost:4200

![image](https://user-images.githubusercontent.com/23094588/129445005-7ddee797-f2e8-433e-a301-b8f7be9fa6fe.png)

Se muestra el aspecto generar de todas las APP nuevas que se crean. Podemos abrir las Herramientas de Desarrollo para ir viendo posibles errores.

![image](https://user-images.githubusercontent.com/23094588/129445044-3839c59e-9c44-4015-bbbd-4592d82aac06.png)

## Estilo de nuestra aplicación 5 min

### Imágenes 

Contamos con una serie de imagenes (**`0.png`** a **`9.png`**) en el material de apoyo del proyecto en una carpeta **`img`**, la cual vamos a copiar dentro de el proyecto creado en la carpeta **`src/assets`** 

![image](https://user-images.githubusercontent.com/23094588/129444797-b6635916-e10f-4c98-ad07-6df71db66cbe.png)

En la carpeta **`src/assets`** se colocan todos los recursos estáticos 

#### GIT

![image](https://user-images.githubusercontent.com/23094588/129445253-0362c7e6-3d7b-4d17-9b5f-d8db0827c5b8.png)

### Aplicar Bootstrap a nuestro proyecto

Abrir https://getbootstrap.com/ 

![image](https://user-images.githubusercontent.com/23094588/129445088-c16848f7-d7b0-44d3-b2ae-65158cc17e1a.png)

Pulsamos en ***Download***

![image](https://user-images.githubusercontent.com/23094588/129445115-8172d449-ef04-4cf1-9b6e-6fe8fa1b5a1f.png)

Vamos a copiar el enlace de los estilos CSS

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KyZXEAg3QhqLMpG8r+8fhAXLRk2vvoC2f3B09zVXn8CA5QIVfZOJ3BCsw2P0p/We" crossorigin="anonymous">
```

Abrimos en VSC el archivo **`index.html`**

![image](https://user-images.githubusercontent.com/23094588/129445170-978da127-fb75-4e77-8102-efb79b987067.png)

Después del tag **`<link ...`** copíamos la línea copiada de Bootstrap

![image](https://user-images.githubusercontent.com/23094588/129445305-fa63b83e-08b8-48b4-84fc-56d326a40a53.png)

Vemos como cambia la apariciencia, tenemos el original:

![image](https://user-images.githubusercontent.com/23094588/129445143-a0724918-30dc-470a-9c15-fa49ec162ff6.png)

Y el que tiene los estilos de Bootstrap

![image](https://user-images.githubusercontent.com/23094588/129445342-45582297-0dc6-43da-a2a0-cb5a9997c0a4.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/129445389-3144318d-4629-4c66-a8fb-c90b9c5a3ff1.png)

## Estructura HTML de nuestro juego 9 min

Si observamos el código del archivo **`index.html`** vemos el siguiente tag:

```html
<app-root></app-root>
```

Este tag representa un ***componente*** que es el que contiene todo lo que se visualizo cuando ejecutamos la APP y que deberíamos modificar para que en lugar de eso, se muestre nuestro Juego del Ahorcado, este ***componente*** esta contenido en ***src/app***

![image](https://user-images.githubusercontent.com/23094588/129453203-f3c82c5f-224b-428a-be02-bce808b45dfe.png)

En especial dentro del archivo **`app.component.html`**, el cual contiene 501 líneas de código es el contiene todo lo que se ve al ejecutar la APP.

![image](https://user-images.githubusercontent.com/23094588/129453263-386387fb-830e-4cdc-bc67-1e2e2ff0adb5.png)

Vamos a eliminarlo todo y en su lugar vamos a poner:

```html
<h1>Hola Mundo</h1>
```

La aplicación se sercarga y ahora vemos:

![image](https://user-images.githubusercontent.com/23094588/129453339-e0a2909b-be85-4cc5-94ca-c7d0dafd661e.png)

Vamos a aplicar un estilo de Bootstrap en el archivo **`index.html`** para que el texto no este tan pegado a los bordes vamos a poner:

```html
<body class="container">
  <app-root></app-root>
</body>
```

Y esto hace que la APP se vea así:

![image](https://user-images.githubusercontent.com/23094588/129453384-77027778-c881-4fef-b807-8ae2a5c226b3.png)

Ahora que ya vimos que pasa al modificar el archivo **`app.component.html`**, vamos a meter el siguiente código en el archivo en lugar del **`Hola Mundo`**:

```html
<div class ="row">
  <div class="col text-center">
    <img src="assets/img/9.png">
    <h3>Intentos <small>3 / 9</small></h3>
  </div>
</div>
```

La APP se ve así:

![image](https://user-images.githubusercontent.com/23094588/129453564-426277d1-60a0-413d-be3c-5ad0ac86e7c9.png)

Como la imagen se ve muy grande vamos a crear una clase personalizada que aplicaremos sobre la imagen para modificar su aspecto, modificamos la línea:

```html
    . . .
    <img src="assets/img/9.png">
    . . .
```

Por 

```html
    . . .
    <img src="assets/img/9.png" class="ahorcado-img">
    . . .
```

`class="ahorcado-img"` representa un estilo que aún no existe en ningún lugar, pero que vamos a insertar a continuación, contamos con el archivo **`styles.css`** en la raíz del proyecto.

![image](https://user-images.githubusercontent.com/23094588/129454581-420cee3a-d7e9-42a0-89bc-6fcb5a80bac1.png)

Y que podemos modificar para insertar estilos personalizados, vamos a crear el estilo para las imágenes:

```css
.ahorcado-img {
  height: 400px;
}
```

La APP se recarga para apreciar los cambios:

![image](https://user-images.githubusercontent.com/23094588/129454772-514375f9-02af-4623-bc1e-7ac67ea2d84e.png)

Vamos a añadir el siguiente código a **`app.component.html`** para que nos quede así:

```html
<div class ="row">
  <div class="col text-center">
    <img src="assets/img/9.png" class="ahorcado-img">
    <h3>Intentos <small>3 / 9</small></h3>
  </div>
</div>
<div class ="row">
  <div class="col text-center">
    <h3> _ _ _ _ _ _ _ _ _ _ </h3>
  </div>
</div>
<div class ="row">
  <div class="col text-center">
    <button class="btn btn-primary">A</button>
    <button class="btn btn-primary">A</button>
    <button class="btn btn-primary">A</button>
  </div>
</div>
```

La APP se recarga:

![image](https://user-images.githubusercontent.com/23094588/129454961-8da4aa9b-c054-4252-bfe1-98677d9a76e1.png)

Como podemos ver los botones salen todos pegados, vamos aplicarle un estilo en **`styles.css`**:

```css
button {
  margin-top: 5px;
  margin-left: 5px;
}
```

La APP se ve así:

![image](https://user-images.githubusercontent.com/23094588/129455034-b1cf1cec-b1fb-4c0e-8f8e-b5fdd15533b7.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/129455098-7ebf3c2a-e886-4fa2-93d0-94cacf55d2f1.png)

## Creando letras de forma dinámica 8 min

En esta sección vamos a crear todos botones de las letras de forma dinámica, para realizar estas tareas lo haremos en el archivo **`app.component.ts`**

![image](https://user-images.githubusercontent.com/23094588/129455185-403140da-e1aa-481c-9602-514de6818998.png)

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'Juego-de-Ahorcado';
}
```

Este archivo representa una clase la cual tiene un ***Decorador*** **`@Component`** el cual es propio de **TypeScript**, esto le agrega funcionalidades a la clase de forma externa, 

* Lo primero que me dice es que tengo un selector llamado **`app-root`** en la primer línea del decorador **`selector: 'app-root',`**, que si recordamos es lo que tenemos en nuestro archivo **`index.html`** en la línea **`<app-root></app-root>`**. Esto significa es que cuando alguien llame a **`<app-root></app-root>`**, realmente lo que quiere es renderizar todo lo que hay en este componente, especificamente en el archivo **`app.component.html`**.

* La parte **`templateUrl: './app.component.html',`** sirve para indicar cual es el archivo que contiene el código HTML que en este caso es **`app.component.html`** que es el archivo que hemos estado modificando para cambiar la apariencia de nuestra APP.

* Finalmente tenemos **`styleUrls: ['./app.component.css']`** para aplicar estilos personalizados que solo se apliquen al HTML contenido en **`app.component.html`**, que es diferente a lo que hace **`styles.css`** que se aplica a todos los archivos HTML. En este caso no lo vamos a ocupar y podríamos eliminar esta línea y el archivo **`app.component.css`**, pero lo vamos a dejar.

* La palabra **`export`** nos sirve para indicar que podemos usar esta clase en otros sitios, sino la marcamos como **`export`** no lo podríamos hacer.

* **`title`** es una propiedad de la clase que en este caso representa el título de la APP.

Una vez visto el código de **`app.component.ts`** que se nos creo por default, nosotros podemos modificarlo de acuerdo a nuestras necesidades, por ejemplo podemos crear un **`constructor`** para la clase, debajo de **`title`**:

```ts
  . . .
  title = 'Juego-de-Ahorcado';
  
  constructor(){
    console.log('Se acaba de crear el APP Component');
  }
  . . .
```

Esto nos mandará un mensaje a la consola cada que se cree este componente.

![image](https://user-images.githubusercontent.com/23094588/129455700-30cca22d-6045-46ea-a9a2-6bc1684d3268.png)

Vamos a meter una propiedad en nuestra clase que representa un array de letras, debajo de **`title`**::

```ts
 letras = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J',
            'K', 'L', 'M', 'N', 'Ñ', 'O', 'P', 'Q', 'R', 'S',
            'T', 'U', 'V', 'W', 'X', 'Y', 'Z'];
```

### Uso de la directiva `*ngFor` e *Interpolación de Strings*

Vamos a usar la directiva **`*ngFor`** para pintar todos los botones de las letras contenidas en la propiedad **`letras`** declarada anteriormente. Esto lo vamos a hacer en el archivo **`app.component.html`**.

**`*ngFor`** lo que hace es clonar una línea N cantidad de veces, en este caso queremos que el botón se clone por cada elemento existente en el array  **`*letras`**, entonces la línea de código queda así:

```html
   . . .
   <button *ngFor="let letra of letras" class="btn btn-primary">A</button>
   . . .
```

La APP se recarga:

![image](https://user-images.githubusercontent.com/23094588/129455967-51d28098-c952-4705-8c7c-29d59aa452f4.png)

Para indicar que en cada botón aparezca la letra que le corresponde vamos a usar la ***Interpolación de Strings*** que se representa con **`{{ }}`**:

```html
   . . .
   <button *ngFor="let letra of letras" class="btn btn-primary">
      {{ letra }}
    </button>
   . . .
```

La APP se recarga:

![image](https://user-images.githubusercontent.com/23094588/129456057-017ee416-2b8b-4b74-8d74-0a990a029edb.png)

#### GIT 

![image](https://user-images.githubusercontent.com/23094588/129456088-11ff5b5b-46f7-465e-8649-d3b9066319ed.png)

## Lógica de la palabra oculta y la palabra hasta el momento 5 min

Vamos a añadir dos propiedades a nuestra clase:

```ts
   . . .
   palabra = 'AGUACATE';
   palabraOculta = '';
   . . .
```

* **`palabra`** Contiene la palabra a averiguar.
* **`palabraOculta`** Va a contener los guiones bajos de la palabra a adivinar y las letras que se van descubriendo.

En el constructor vamos a meter la lógica, primero dinámicamente vamos a pintar los guiones adecuados de las letras a adivinar.

```ts
   . . .
   constructor(){
      this.palabraOculta = '_ '.repeat( this.palabra.length);
   }
   . . .  
```

En **`app.component.html`** vamos a cambiar

```html
   . . .
   <h3> _ _ _ _ _ _ _ _ _ _ </h3>
   . . . 
```

por 

```html
   . . .
   <h3>{{ palabraOculta }} </h3>
   . . . 
```

La APP se actualiza

![image](https://user-images.githubusercontent.com/23094588/129767080-46840db3-b15f-42a3-93de-7689d90a6a1a.png)

Vemos 8 guiones que representan las ocho letras de la palabra AGUACATE **`app.component.html`**, vamos cambiar:

### Crear Evento en el Botón

Ahora lo que vamos a crear es un Evento para cuando el usuario hace click en algún botón, para evaluar si la letra del botón pulsada se encuentra dentro de la palabra a adivinar en este caso AGUACATE. Si la palabra existe vamos a tener que mostrar la letra en su correspondiente posición.

Para añadir un evento al botón modificaremos el código del botón en **`app.component.html`** 

```html
   . . .
   <button *ngFor="let letra of letras" class="btn btn-primary">
      {{ letra }}
    </button>
   . . . 
```

por 

```html
   . . .
   <button (click)="comprobar(letra)" *ngFor="let letra of letras" class="btn btn-primary">
      {{ letra }}
    </button>
   . . . 
```

* **`(click)`** indica el evento a escuchar
* **`comprobar(letra)`** indica el método que se va a invocar cada que hagamos un click en el botón, le pasa como parámetro la **`letra`** del botón.

En **`app.component.ts`** vamos a crear ese método después del constructor como sigue:

```ts
   . . .
   comprobar(letra: string){
      console.log('Pulsaste la letra: ' + letra);
   }
   . . .   
```

* **NOTA:** En la versión 6 de Angular no era necesario indicar el tipo de la variable

Probando la APP:

![image](https://user-images.githubusercontent.com/23094588/129769794-eb8823a2-caa6-452d-8685-d44ccb8e3a93.png)

Hemos pulsado unas letras y se va viendo en la consola. Con esto hemos comprobado que el Evento funciona. 

#### GIT

![image](https://user-images.githubusercontent.com/23094588/129767407-85e26226-d32c-43d6-a937-8d383ddc3232.png)


## Mostrar letras correctas en la palabra oculta 8 min

Ahora vamos a meter la la lógica para validar que la letra que se pulse esta contenida en la palabra, el código es el siguiente:

```ts
   comprobar(letra: string){
      const palabraOcultaArr = this.palabraOculta.split(' ');
      console.log(palabraOcultaArr);
   }  
```

* Lo que estamos haciendo es crear un Array en base a **`palabraOculta`**, usar este Array auxiliar nos va a ayudar a buscar la letra de una forma más facil dentro de la palabra, cada uno de los elementos es lo que se encuentre separado por un **`' '`** espacio en blanco, en este caso son los guiones. Observece que al final hay un **`""`** que no debería esar, esto es por que al final de **`palabraOculta`** hay un espacio en blanco. Ya vemos como lo quitamos.
* Observese que **`palabraOcultaArr`** es una variable a diferencia de **`palabraOculta`** o **`palabra`** que son propiedades de la clase, a las variables hay que declararlas con **`let`** o con **`const`** si su valor no va a cambiar, por lo que en lugar de variable sería una constante.

![image](https://user-images.githubusercontent.com/23094588/129771406-02c212ad-2bc0-4572-99c3-e2714b2b4372.png)

La idea es que cuando localice una letra sustituya el guío por la letra en la posición correspondiente.

Lo siguiente que vamos a hacer es recorrer las letras dentro de la palabra y si una de ellas es igual a la letra pulsada vamos a sustituir el guíon en esa posición por la letra pulsada.

Al final de todo vamos a reconstruir la **`palabraOculta`** en base a **`palabraOcultaArr`** usando el método contrario a **`split`** que es  **`join`** el cual une los elementos de un array separandolos por el caracter que se indique como parametro:


```ts
   comprobar(letra: string){
      const palabraOcultaArr = this.palabraOculta.split(' ');

      for( let i = 0; i < this.palabra.length; i++){

         if( this.palabra[i] === letra ){
            palabraOcultaArr[i] = letra;
         }
      }

      this.palabraOculta = palabraOcultaArr.join(' ');
   } 
```

Probando la APP

![image](https://user-images.githubusercontent.com/23094588/129773363-9419e6d3-b651-4d2f-906e-9ea094b9dd89.png)

![image](https://user-images.githubusercontent.com/23094588/129773536-bde03f15-c02c-4aed-8a1f-76d2c032be49.png)

![image](https://user-images.githubusercontent.com/23094588/129773596-31923283-9d47-443d-8855-6dac1ab16c0d.png)

![image](https://user-images.githubusercontent.com/23094588/129773621-6883e148-e125-4d0e-a218-20e7dde80a96.png)

![image](https://user-images.githubusercontent.com/23094588/129773682-45f7a26d-27ce-4a50-ae48-0a91d5c3407d.png)

![image](https://user-images.githubusercontent.com/23094588/129773735-2ed2ccb9-6a4e-4110-a903-9e71b43d94ae.png)

![image](https://user-images.githubusercontent.com/23094588/129773773-821147a0-a991-4b8c-90fb-6a39d8e3a30b.png)

Al pulsar letras existentes van apareciendo en su correspondiente posición, si pulso letras que no existen por ahora no pasa nada, ya veremos que debe hacer en ese caso.

#### GIT

Hay un fallo en el mensaje deberia ser ""

![image](https://user-images.githubusercontent.com/23094588/129775507-02c1bdb0-98a1-4580-b5b2-59d1a48847d7.png)

## Cambiar la imagen y contar los intentos fallidos 6 min

En el caso de que el usuario introduzca una letra que no se encuuentra en la palabra el número de intentos debe incrementarse y la imagen debe ir cambiando si no acierta.

Vamos a declarar una nueva propiedad **`intentos`** en la clase:

```ts
intentos = 0;
```

En **`app.component.html`** vamos a cambiar el código Harcodeado que tenemos:

```html
   . . . 
   <h3>Intentos <small>3 / 9</small></h3>
   . . . 
```

por

```html
   . . .
   <h3>Intentos <small> {{ intentos }} / 9</small></h3>
   . . . 
```

La APP se actualiza para mostrar un 0.

![image](https://user-images.githubusercontent.com/23094588/129776427-d5218cd6-39a9-4eff-960d-c54deab105dc.png)


En **`app.component.ts`** vamos a crear un nuevo metodo llamado **`existeLetra(letra)`** que nos servira para saber si existe o no una letra, en caso de que la letra no exista lo que vamos a hacer es incrementar en q el número de intentos.

```ts
   . . .
   existeLetra( letra: string){
      if( this.palabra.indexOf( letra ) >= 0 ){
         console.log('La letra ' + letra + ' existe');
      }else{
         console.log('La letra ' + letra + ' NO existe');
         this.intentos++;
      }
   }
   . . .  
```

Esta función la vamos a llamar al inicio de nuestro método **``**

```ts
   . . . 
   comprobar(letra: string){

      this.existeLetra(letra);
    
      const palabraOcultaArr = this.palabraOculta.split(' ');

      for( let i = 0; i < this.palabra.length; i++){

         if( this.palabra[i] === letra ){
            palabraOcultaArr[i] = letra;
         }
      }

      this.palabraOculta = palabraOcultaArr.join(' ');
   }
   . . .   
```

Probar la APP

![image](https://user-images.githubusercontent.com/23094588/129778049-c0d85bda-0f78-405a-a05a-47a1fca630a4.png)

![image](https://user-images.githubusercontent.com/23094588/129778090-fe18a2d3-acd2-4098-b6da-42cf92e666dc.png)

![image](https://user-images.githubusercontent.com/23094588/129778135-40c05200-a378-405d-ae39-97d16437016d.png)

![image](https://user-images.githubusercontent.com/23094588/129778169-2035cbd8-21ed-451b-b761-3306cdb77095.png)

![image](https://user-images.githubusercontent.com/23094588/129778211-ccbdc44f-0324-4091-b630-1af3b13f943f.png)

![image](https://user-images.githubusercontent.com/23094588/129778250-5d99b3f5-6497-4a99-961a-5d406dcc2578.png)

![image](https://user-images.githubusercontent.com/23094588/129778280-abdd2d96-6eb8-41b3-8dac-51f3eefc945e.png)

![image](https://user-images.githubusercontent.com/23094588/129778328-a26baf29-7f83-4c89-8ad6-c3ee1e1ae731.png)

Por cada letra que pulsemos y que no se encuentre en la palabra a adivinar se va incrementando en 1 los intentos, aquí debemos controlar que no pasemos del total de letras de la palabra que sería lo que marca el fin del juego.

Por otro lado podemos cambiar la imagen que se muestre, ahora siempre mostramos la imagen 9, que es la que marca el final del juego eso pasa por que en **`app.component.html`** tenemos:

```html
   . . .
   <img src="assets/img/9.png" class="ahorcado-img">
   . . .
```

lo vamos a cambiar por:


```html
   . . .
   <img src="assets/img/{{ intentos }}.png" class="ahorcado-img">
   . . .
```

![image](https://user-images.githubusercontent.com/23094588/129784106-fd2f7b95-9bac-40de-a28a-fc21a5038276.png)

![image](https://user-images.githubusercontent.com/23094588/129784141-903134f1-4456-4317-a944-f6c1aa684ca6.png)

![image](https://user-images.githubusercontent.com/23094588/129784173-a77d31e1-dd7f-45b4-9375-55f761db6747.png)

![image](https://user-images.githubusercontent.com/23094588/129784211-e4532192-2462-4d72-88f6-5b299fbf1e7d.png)

![image](https://user-images.githubusercontent.com/23094588/129784259-a16f8af5-3b43-418f-a37e-f0da0ea34e52.png)

![image](https://user-images.githubusercontent.com/23094588/129784304-7b60af03-f6ec-4b8c-96ad-b72681150814.png)

![image](https://user-images.githubusercontent.com/23094588/129784347-c052c5c7-c18c-4a07-a671-e6610b3ff891.png)

![image](https://user-images.githubusercontent.com/23094588/129784383-b2c47e34-89ac-4076-a33d-96940784cb5e.png)

![image](https://user-images.githubusercontent.com/23094588/129784412-fdb52f2e-eca1-4dfb-8e43-29c4b6c67aeb.png)

![image](https://user-images.githubusercontent.com/23094588/129784454-559f8d38-b309-4a55-9eb1-c1e818afc888.png)

![image](https://user-images.githubusercontent.com/23094588/129784807-27ed541b-b21d-4266-bec8-9c4c0326306c.png)

![image](https://user-images.githubusercontent.com/23094588/129785020-f2e6e0e4-1539-413b-871e-a1e95d84ec03.png)

En caso de que siga pulsando letras incorrectas vamos a tener errores en la Imagen ya que empieza a buscar imágenes que no existen como **`10.png`**, **`11.png`**, etc. Debemos controlar esto.

#### GIT

Hay un fallo en el mensaje del Commit debería haber sido "Cambiar la imagen y contar los intentos fallidos"

![image](https://user-images.githubusercontent.com/23094588/129785408-13d2b355-d055-4b84-a140-aef13cb3682c.png)

## Verificar si el usuario gana o pierde 6 min

Aquí vamos a verificar si el usuario gana o pierde, si llega al Intento 9 el usuario PIERDE, si adivina la palabra antes de los 9 intentos GANA!.

Vamos a añadir dos propiedades a la clase:

```ts
 gano = false;
 perdio = false;
```

Vamos a crear un nuevo método **`verificaGane()`** el cual llamaremos al final del método **`comprobar(letra: string)`**, después de la sentencia **`this.palabraOculta = palabraOcultaArr.join(' ');`** y por ahora lo que vamos a hacer en el método **`verificaGane()`** es imprimir en consola el valor de **`this.palabraOculta`**, para ver algo que puede ser que no percibamos, el código es el siguiente:

```ts
   . . .
   comprobar(letra: string){

      this.existeLetra(letra);

      const palabraOcultaArr = this.palabraOculta.split(' ');

      for( let i = 0; i < this.palabra.length; i++){

         if( this.palabra[i] === letra ){
            palabraOcultaArr[i] = letra;
         }
      }

      this.palabraOculta = palabraOcultaArr.join(' ');
      this.verificaGane();
   }

   verificaGane(){
      console.log(this.palabraOculta);
   }
   . . .  
```
![image](https://user-images.githubusercontent.com/23094588/129787579-15eb9138-cadd-46a5-ac9a-205d1f0c72e5.png)

![image](https://user-images.githubusercontent.com/23094588/129787618-453d85af-15af-40ca-9991-1c96d7be2a7c.png)

![image](https://user-images.githubusercontent.com/23094588/129787654-613c08d2-5c3f-422f-a655-647af84501ef.png)

![image](https://user-images.githubusercontent.com/23094588/129787803-76c822ae-6ceb-4d0b-abd2-e54f55cd5333.png)


Como podemos ver la palabra oculta tiene espacios en blanco entre cada carácter, aún teniendo la palabra completa.

Lo que nosotros debemos hacer es quitar todos esos espacios en blanco entre caracteres, existen varias formas de hacerlo una sería con **Expresiones Regulares**, pero lo vamos a hacer de otro forma por la complejidad de las ExR. Vamos a meter el siguiente código en nuestfro método:

```ts
   . . .
   verificaGane(){
      const palabraArr = this.palabraOculta.split(' ');
      console.log(palabraArr);
   }
   . . .
```

La salida es:

![image](https://user-images.githubusercontent.com/23094588/129788403-b82cefae-f4aa-4cb1-b35e-e00a39ed1aab.png)

Lo que tenenos es un Array con cada letra como elemento, lo que debemos hacer es unir esos elementos para eliminar el espacio en blanco, eso lo logramos con:

```ts
   . . .
   verificaGane(){
      const palabraArr = this.palabraOculta.split(' ');
      const palabraEvaluar = palabraArr.join('');
      console.log(palabraEvaluar);
   }
   . . .
```

![image](https://user-images.githubusercontent.com/23094588/129788928-13a0e274-a957-432a-a9a2-6f0e74f82aaf.png)

![image](https://user-images.githubusercontent.com/23094588/129788985-040f4bc1-e72d-4870-a893-3a66cd5db4d2.png)

Vemos que ya tenemos la palabra sin espacios.

Ahora si vamos a poner las validaciones para ver si se gana o se pierde.

```ts
   . . .
   verificaGane(){
      const palabraArr = this.palabraOculta.split(' ');
      const palabraEvaluar = palabraArr.join('');

      if ( palabraEvaluar === this.palabra ){
         this.gano = true;
         console.log('Usuario GANO!!!');
      }

      if( this.intentos >= 9 ){
         this.perdio = true;
         console.log('Usuario PERDIO!!!');
      }
   }
   . . .
```

Probar la APP

Cuando GANA

![image](https://user-images.githubusercontent.com/23094588/129789862-1c0f5582-a9e1-4562-b7cf-0a8688ec4197.png)

Cuando Pierde

![image](https://user-images.githubusercontent.com/23094588/129789951-b489add1-acb5-4e06-be92-5db9995cb658.png)

Pero nada me impide seguir pulsando letras en caso de que Gane o Pierda

![image](https://user-images.githubusercontent.com/23094588/129791042-fed414fc-c9ea-40e3-a574-eed6ea350d22.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/129791242-9c04d7d4-edfd-402c-96a8-6afd388e2f33.png)

## Mostrar mensaje de victoria o derrota 5 min

Vamos a hacer que los menajes de Ganar o Perder salgan en la página del Navegador y no en la consola. En **`app.component.html`** vamos a añadir lo siguiente, después de la división de los botones:

```html
   . . .
   <div class ="row">
      <div class="col text-center">
         <h1> Felicidades Ganaste!!! </h1>
         <h4> :D </h4>
      </div>
   </div>
   <div class ="row">
      <div class="col text-center">
         <h1> Lo siento, Perdiste :( </h1>
         <h4> La palabra oculta es: {{ palabra }} </h4>
      </div>
   </div>
   . . .
```

![image](https://user-images.githubusercontent.com/23094588/129792073-2e69db4c-f040-4120-bb5f-7913b730c42c.png)

Pero estos mensajes los tengo que mostrar en base a si se gano o se perdio y ese dato lo tenemos almacenado en las propiedades(banderas) **`gano`** y **`perdio`** y usando la directiva **`*ngIf`** de la siguiente manera:

```html
   . . .
   <div class ="row" *ngIf="gano">
      <div class="col text-center">
         <h1> Felicidades Ganaste!!! </h1>
         <h4> :D </h4>
      </div>
   </div>
   <div class ="row" *ngIf="perdio">
      <div class="col text-center">
         <h1> Lo siento, Perdiste :( </h1>
         <h4> La palabra oculta es: {{ palabra }} </h4>
      </div>
   </div>
   . . .
```


![image](https://user-images.githubusercontent.com/23094588/129792790-b6954e21-5be0-4ae0-9541-9f9066c964e3.png)

Cuando Pierde

![image](https://user-images.githubusercontent.com/23094588/129792887-81026dbf-0474-4930-b5f5-18d7088607ed.png)

Pero puedo seguir pulsando letras

![image](https://user-images.githubusercontent.com/23094588/129792965-aad58414-2aee-42d2-b453-b5732575511e.png)


Cuando Gana

![image](https://user-images.githubusercontent.com/23094588/129793036-8052ca08-5bcc-41f0-a87d-eafb5e074d27.png)

Pero puedo seguir pulsando letras

![image](https://user-images.githubusercontent.com/23094588/129793098-343b97dc-b483-4543-a210-089426ee213d.png)

Lo último que falta es ocultar el teclado en caso de ganar o perder, o diciendo de otra forma mientras no gane y mientras no pierda el teclado se muestra en otro caso se oculta eso lo logramos con:

```ts
   . . .
   <div class ="row" *ngIf="!gano && !perdio">
      <div class="col text-center">
         <button (click)="comprobar(letra)" *ngFor="let letra of letras" class="btn btn-primary">
            {{ letra }}
         </button>
      </div>
   </div>
   . . .
```

Probando la APP

![image](https://user-images.githubusercontent.com/23094588/129794275-1d224f07-cc99-4fc0-9400-59ea0013ff3b.png)

Cuando Gana, vemos que ya desaparece el teclado:

![image](https://user-images.githubusercontent.com/23094588/129794357-d84261e9-b981-45f8-8e78-0f7ac5b0c29d.png)

Cuando Pierde, vemos también que desaparece el teclado:

![image](https://user-images.githubusercontent.com/23094588/129794442-ad8f38d2-a238-4b63-b0b8-ab82c58724f8.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/129794578-903e8706-4840-46f3-8ebc-4fed397c4393.png)

## Códigos fuente de todo el curso 1 min

## Repositorio Git

![image](https://user-images.githubusercontent.com/23094588/157073621-edc5e8f4-efb2-413a-ba57-23d3f3b958d9.png)

```sh
…or create a new repository on the command line
echo "# 110-Juego-de-Ahorcado" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/adolfodelarosades/110-Juego-de-Ahorcado.git
git push -u origin main
```

```sh
…or push an existing repository from the command line
git remote add origin https://github.com/adolfodelarosades/110-Juego-de-Ahorcado.git
git branch -M main
git push -u origin main
```

```sh
…or import code from another repository
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.
```

![image](https://user-images.githubusercontent.com/23094588/157073878-1abb0c4e-7d70-439e-927f-be0a13b2dac6.png)

![image](https://user-images.githubusercontent.com/23094588/157074425-79d6eb62-5da8-4fbb-83f1-4f7eb2a50235.png)

![image](https://user-images.githubusercontent.com/23094588/159295252-17fe67a9-d80e-4446-9b7f-61eea11c92f1.png)

![image](https://user-images.githubusercontent.com/23094588/159295486-98347790-e5db-42d9-b94c-3e887a886efc.png)

----

Ya tenemos todo nuestro código en el repositorio de **`GitHub`**.

Es importante notar que la carpeta **`node_modules`** no se sube al repositorio, entre otras cosas, gracias a lo que tenemos incluido en el archivo **`.gitignore`** del proyecto.

![image](https://user-images.githubusercontent.com/23094588/150824068-1b37f288-448e-4161-becc-e174e9742b1a.png)

La carpeta **`node_modules`** es importante para nuestro proyecto pero ocupa mucho espacio para subirlo al repositorio y lo podemos recuperar gracias a lo que tenemos en el archivo **`package.json`**.

![image](https://user-images.githubusercontent.com/23094588/150824767-d0bc9cf0-996e-47fc-9dc4-9535584a7bbb.png)

Si nosotros tenemos la necesidad de pasar este proyecto a alguien más lo descargamos del repositorio y simplemente ejecutamos el comando 

```sh
npm install
```

para que reconstruya todos los módulos de Node, ya lo veremos al final de esta sección.

### Creación de un Tag y Release

Adicionalmente vamos a crear un **Release Tag** que nos permite tener una versión del código que esta en este momento y poder descargarlo. El comando **Git** que vamos a usar es:

```sh
git tag -a v0.1.0 -m "Fin sección 4"
```

Este comando crea un **Tag** el atributo **`-a`** significa que es "anotado" con el texto **`v0.1.0`** que es una forma de nombrar nuestras versiones y con **`-m`** le damos el título de **`Fin sección 4`**

Si después de pulsar el comando anterior pulsamos:

```sh
git tag
```

vamos a tener:

![image](https://user-images.githubusercontent.com/23094588/150819762-52dd80d3-103f-4a6c-acd6-b957151daf2d.png)

Si retornamos al navegar en **GitHub** no vamos a ver ninguna diferencia.

![image](https://user-images.githubusercontent.com/23094588/150819991-b9097fc0-4703-4f03-9d0f-dbb605e85939.png)

Para subir el  **Tag** a **GitHub** lo hacemos con el comando:

```sh
git push --tags
```

![image](https://user-images.githubusercontent.com/23094588/150820305-d3179530-a3da-4088-8bcd-70f1c2966691.png)

Esto simplemente nos sube un **Tag** a **GitHub** no un **Release Tag**.

![image](https://user-images.githubusercontent.com/23094588/150820569-0647ad60-1450-4d49-aba5-0bcffaed259d.png)

Ya podemos ver que nos sale 1 tag si pulsamos en **Releases** vemos los detalles:

![image](https://user-images.githubusercontent.com/23094588/150820905-e3fe364e-cb22-4304-9c5e-b83bd43eeab5.png)

Como podemos ver en **Releases** no tenemos nada y en **Tags** tenemos:

![image](https://user-images.githubusercontent.com/23094588/150821099-2d66a7d9-2b09-4273-a6e6-e02249edf60c.png)

Si pulsamos en el **Tag v0.1.0**  nos lleva a los detalles:

![image](https://user-images.githubusercontent.com/23094588/150821401-efe6c50f-b486-462c-98ce-c2377e3dd5aa.png)

En esta pantalla podemos crear un **Release** a partir de un **Tag** pulsando en el botón **`Create release from tag`**.

![image](https://user-images.githubusercontent.com/23094588/150821786-643962bc-d936-460e-b945-85a41e7399b0.png)

Metemos la información que nos solicita:

![image](https://user-images.githubusercontent.com/23094588/150822068-b4dc1283-3551-4c7b-9983-3ada65d603d9.png)

Y podemos pulsar en el botón verde **`Public release`**

![image](https://user-images.githubusercontent.com/23094588/150822341-0f082087-1c4d-4810-9f03-e208633e88eb.png)

Ahora si ya tenemos un **Release**

Como podemos ver en el **Release** tenemos la sección **Assets** donde podemos descargar el código fuente, vamos a pulsar en **`Source code (zip)`** el código se descarga:

![image](https://user-images.githubusercontent.com/23094588/150823290-1b0711c0-c86a-4a69-8639-4b5c33da1ad0.png)

![image](https://user-images.githubusercontent.com/23094588/150823386-ef432452-2ada-4d79-bb9b-efbc0f5bb98a.png)


### Usar el proyecto Descargado

Vamos a copiar el ZIP descargado dentro de nuestra carpeta de Proyectos Angular y lo descomprimimos.

![image](https://user-images.githubusercontent.com/23094588/150835726-834f4a60-b282-4126-a275-ad60f77c01cd.png)

Observamos que al contrario de nuestro proyecto orignal este no tiene el **`node_modules`**.

![image](https://user-images.githubusercontent.com/23094588/150836031-b7e6fe95-de6b-4520-90d6-a64941f83eea.png)

En la consola vamosa meternos a la carpeta del proyecto descargado y para reconstruir los modulos de Node bastaría pulsar el comando:

```sh
npm install
```

![image](https://user-images.githubusercontent.com/23094588/150836447-2ecdbd08-df81-499d-b3c9-45347667a60f.png)

![image](https://user-images.githubusercontent.com/23094588/150838107-31ffd910-65e8-40ee-9a56-ada902f44726.png)

Si listamos los archivos en la carpeta veremos que ya aparece el **`node_modules`**.

![image](https://user-images.githubusercontent.com/23094588/150838560-34dd92cb-d961-4779-b3fb-1cf5fcb9e1c5.png)

Vamos a levantar el servidor con:


```sh
ng serve -o
```

Como ya tenia el puerto **4200** ocupado me pregunta si quiero abrir la APP en un puerto diferente, respondo **Y** y carga la aplicación en un nuevo puerto.

`http://localhost:64904/`

![image](https://user-images.githubusercontent.com/23094588/150839565-bb5e444b-428e-4f85-add7-db5db7ca8790.png)

La aplicación funciona con lo último que subimos al repositorio.

![image](https://user-images.githubusercontent.com/23094588/150839913-8fc60f19-577c-4764-84ea-3f0122a201b4.png)


Con esto hemos demostrado como descargar una APP del repositorio, la hemos generado o instalado y finalmente la hemos arrancado.


## Código fuente de la sección 00:17

https://github.com/adolfodelarosades/125-01-bases/releases/tag/v0.1.0


