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

Nos hace dos preguntas a las cuales respondemos con Enter para coger el valor por default(en la V6 no los hacia)

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

![image](https://user-images.githubusercontent.com/23094588/129775507-02c1bdb0-98a1-4580-b5b2-59d1a48847d7.png)

## Cambiar la imagen y contar los intentos fallidos 6 min
## Verificar si el usuario gana o pierde 6 min
## Mostrar mensaje de victoria o derrota 5 min
## Códigos fuente de todo el curso 1 min


