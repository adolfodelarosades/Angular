# 02 Gentil introducción a TypeScript y ES6 - 25 clases • 2h 35m

* Introducción a la sección 01:28
* ¿Qué aprenderemos en esta sección? 00:29
* Introducción a TypeScript 07:05
* Demostración de TypeScript 09:26
* Configuración de TypeScript 07:20
* Variables let y const 07:30
* Introducción a los tipos de datos 07:56
* Excluir archivos a traducir 02:22
* Template literales del ES6 08:03
* Funciones: Parámetros opcionales, obligatorios y por defecto 06:49
* Funciones de Flecha 11:00
* Desestructruación de Objetos y Arreglos 10:56
* Promesas 07:37
* Promesas y su tipado en TypeScript 09:06
* Interfaces de TypeScript 07:52
* Introducción a las Clases de la POO 07:52
* Definición de una clase básica en TypeScript 04:49
* Constructores de una clase en TypeScript 10:03
* Importaciones - URL 07:44
* Decoradores de Clases 06:05
* Tipado del retorno de una función 05:29
* Exámen práctico #1 00:52
* Explicación de la tarea 01:34
* Resolución del examen práctico #1 05:17
* Examen teórico #1 - 10 preguntas
* Código fuente de la sección 00:19

## Introducción a la sección 01:28

Aquí vamos a tener un reforzamiento sobre lo que es **TypeScript** y **ECMAScript 6**, ambos son sumamente usados en cualquier aplicación Angular. El objetivo es que nosotros dominemos primero lo que es  **TypeScript** y **ECMAScript 6** porque es lo más usado es muy común ver la aplicación de otra persona y que utilice ***funciones de flecha*** que use ***promesas*** o que use un ***tipado fuerte*** en sus funciones o en sus tipos de datos y nosotros ocupamos saber eso, algo que asusta es el uso de los ***decoradores*** cuando nosotros vemos un **`@`** y una función después, qué es, con qué se come, para qué me puede servir.

Todo eso está explicado en esta sección y el objetivo es que ustedes sientan la curva de aprendizaje de Angular lo más fácil posible.

## ¿Qué aprenderemos en esta sección? 00:29

Si tu conoces TypeScript y ES6, puedes saltarte esta sección y comenzar con Angular2 directamente, pero si no estas familiarizado con esos temas, te recomiendo que completes esta sección primero.

En esta sección aprenderas sobre:

1. ¿Qué es TypeScript?
2. ¿Cómo usar TypeScript y utilizar ECMAScript 6?
3. Declaración de variables con **"let"** y constantes **"const"**
4. ¿Qué es y para qué sirve el archivo **`tsconfig.json`**?
5. Uso de los tipos de datos que ofrece TypeScript.
6. Strings de multilinea.
7. Parámetros obligatorios, por defecto y opcionales.
8. Beneficios de las funciones de flecha.
9. Uso y creación de interfaces.
10. Uso de módulos y ejemplos de los mismos.
11. Decoradores de clase.
12. Entre otros temas importantes para adentrarnos en Angular 2.

Al final de la sección, hay un examen práctico y otro teórico.

Animo y mucha suerte!

## Introducción a TypeScript 07:05

![image](https://user-images.githubusercontent.com/23094588/130271726-8097da09-1a1f-4abc-8814-d195922b2ce5.png)

JavaScript como lenguajes de programación ha ido creciendo conforme los años y cada vez es más demandado y cada vez se utiliza más para crear aplicaciones, ya no sólo se utiliza para crear aplicaciones web, ahora se crean ***Backends***, se crean ***aplicaciones móviles*** y otro montón de cosas.

![image](https://user-images.githubusercontent.com/23094588/130272068-4834cbd8-ecf8-478d-ba07-d37cd0f28de9.png)

El problema es que JavaScript no fue diseñado para crear aplicaciones de mediana y gran escala. Originalmente sólo se creó para ser validaciones de formularios antes de enviar la información al servidor, pero al ver que las necesidad íban creciendo, de que cada vez se podía hacer más cosas en JavaScript, pero al no ser pensado para crear aplicaciones tan grandes surgieron Frameworks y librerías como **Angular**, **`React`**, **`Vue`** entre otras, con el objetivo de ayudarnos a poder crear aplicaciones de mediana y gran escala que nos permitan sacar el máximo provecho del poder que tienen JavaScript.

![image](https://user-images.githubusercontent.com/23094588/130272592-28f3a209-7e0f-491d-b898-09c38871e4c9.png)


Como les mencioné originalmente JavaScript fue diseñado para tener unas cuantas líneas de código, tal vez cientos de líneas de código por mucho. Pero hoy en día es muy fácil superar miles de líneas de código y el problema es que **JS** que al ser ***un lenguaje de programación de tipado débil*** en el cual es muy fácil cometer errores, especialmente cuando las aplicaciones empiezan a crecer en complejidad.

![image](https://user-images.githubusercontent.com/23094588/130272783-7f4a4680-ee43-4bbe-9939-c4082331bc5b.png)

Vamos a suponer un pequeño panorama, ustedes llegan a una empresa les dan una función y les dice Ok simplemente llama a la función calcular y eso se encarga de todo, ok dicen ustedes perfecto. Llega el momento de utilizarla y algo no funciona bien. Puede ser que dicha función no esté bien documentada y nos toca entrar al código y todo lo vemos en Chino, puede ser que nos tome mucho tiempo encontrar el problema y al fin del día nos damos cuenta de que lo que pasaba es que estábamos mandando mal el argumento porque nos pedía digamos un objeto y estábamos mandando números, strings u otra cosa, pero como JS acepta prácticamente cualquier tipo de dato, por eso nos costó encontrar este problema.

![image](https://user-images.githubusercontent.com/23094588/130273157-debf2efc-fe66-40e0-a49c-daaea3b91cc2.png)

JS carece de muchas características como por ejemplo ***tipado de variables estricto***, ***errores en tiempo de escritura***, ***autocompletado*** dependiendo de la variable, ***métodos estáticos de programación***, ***clases y módulos***. Aunque después del estándar del ECMAScript 6 ya los incorporó pero todavía hacen falta ciertas características.

![image](https://user-images.githubusercontent.com/23094588/130273388-3fd2c136-21b5-4f36-88c0-817a4e8f96f6.png)

Sería excelente que cuando nosotros estemos trabajando en JavaScript podamos tener el poder como en **Visual Studio NET**, **NetBeans**, **Eclipse** que a la hora de escribir el código nos va diciendo, "Hey esta línea está mal", "Aquí te falta algo", "falta cerrar esto", "Eso no puede ser válido", "eso no se puede asignar a esta variable", etc, tener todo ese poder en JavaScript sería súper conveniente.

Tenemos **Web Storm** que es un editor de código bastante poderoso que a todo esto no sé si considerarlo un IDE porque también tiene formas de compilar entre otras cosas es básicamente todo lo que ustedes necesitan. Pero el problema es que **Web Storm** no es gratuito, existen otros programas como **Visual Studio Code**, **Atom** entre otros que son muy poderosos para trabajar en JavaScript pero el problema es que nos faltan todas esas características que IDEs robusto de desarrollo ya tienen.

Miremos ciertos problemas que tienen JavaScript

![image](https://user-images.githubusercontent.com/23094588/130274238-126569ad-52ad-4a30-8395-9c93b9525a60.png)

![image](https://user-images.githubusercontent.com/23094588/130274513-a22c6173-d6d7-412e-a88e-29c14ebea308.png)

![image](https://user-images.githubusercontent.com/23094588/130274661-14c9fdbf-4f3e-4c89-a472-e744d2a5d904.png)


Todos los problemas anteriores se pueden resolver con **TypeScript**

![image](https://user-images.githubusercontent.com/23094588/130274755-f1370625-b30f-4535-a59a-cc8fccddda3b.png)

Pueden tener la experiencia de programar en un lenguaje al que ya estás acostumbrado como, **C**, **C#**, **Visual Basic**, **Java** entre otros, que son ***lenguajes de programación de tipado estricto*** por lo cual el IDE de desarrollo o editor de código les puede dar a ustedes toda la información de los errores de escritura junto con sus sugerencias y cómo se llaman los métodos porque sabe qué cosas son permitidas y qué cosas no.

![image](https://user-images.githubusercontent.com/23094588/130274990-c12086b4-c4ce-4940-abf9-ed5220ab6036.png)

El problema es que **TypeScript** no corre directamente en el navegador web, por lo cual hay que ***compilarlo**, ***traducirlo*** o ***transpilarlo***, cualquiera de esos términos es básicamente lo mismo, es tomar nuestro código TypeScript y generarlo como un archivo de JavaScript.

![image](https://user-images.githubusercontent.com/23094588/130275356-3ca4ff4a-1d71-4074-b5ed-d91b33f23f40.png)

TypeScript que es básicamente un super set de JavaScript, a qué me refiero con eso, tenemos el estándar de JavaScript como la mayoría lo conoce JS, luego el estándar evolucionó y agregó bastantes características nuevas en el ECMAScript 6, luego vino el ES7 el ES8 y así sucesivamente, pero al ser un super set envuelve todo de tal manera que tú puedas utilizar características nuevas de JavaScript y traducirlo al estándar global de la industria de JavaScript qué sería básicamente el ECMAScript 5.

Pero hay que comprender que TypeScript va implementando características inclusive más rápido que los navegadores web. Pero todavía hay cosas del nuevo estándar de JavaScript que no son incorporadas en TypeScript, pero la verdad para hacerlos honestos yo no he tenido ese inconveniente, de que necesito algo del ECMAScript nuevo que acaba de salir y que yo no necesito implementar en TypeScript, usualmente eso no sucede y en lo personal a mí no me ha pasado.

![image](https://user-images.githubusercontent.com/23094588/130275745-d9af62f8-9283-4e1f-a8ba-8e5271c83921.png)

Veamos la gráfica la cual explica sobre la evolución de JavaScript en la industria y el estado actual del estándar ECMAScript.

El problema es que si nos vamos allá afuera éste es el estado de JavaScript actualmente en la web.

![image](https://user-images.githubusercontent.com/23094588/130275862-6eed8636-272e-4de7-88c7-94d41caa65fc.png)

Estamos muy cerca de que el estándar del ECMAScript 5 sea mundialmente aceptado en todos los navegadores.

![image](https://user-images.githubusercontent.com/23094588/130275957-b1c460ee-7f90-416a-b436-bfd6746ad412.png)

Lo cual hace que el rango de productividad JavaScript sea entre el estándar del ECMAScript 5 y el estándar del ECMAScript 2015 que sería el ES6. 

![image](https://user-images.githubusercontent.com/23094588/130276099-08071654-30b7-454f-8bba-413d0692711e.png)

Pero hay muchas cosas del nuevo estándar de JavaScript que realmente valen la pena aprovechar y sería ideal que nosotros  estuviéramos en ese rango, pero realmente no es así.

![image](https://user-images.githubusercontent.com/23094588/130276236-f4207cf7-a1d3-4e89-bcde-01ef8f7bb0bf.png)

En la realidad estamos algo como por este lado y esto conlleva a muchos, muchos problemas porque puede ser que ustedes quieran trabajar con características nuevas como el Async el AWait o hacer peticiones Fetch, trabajar con Services Workers entre otro montón de cosas, pero eso todavía no es mundialmente aceptado.

![image](https://user-images.githubusercontent.com/23094588/130276388-392b3925-8dc6-4fe7-a47b-f619629e6190.png)

Pero la ventaja es que TypeScript pueden utilizar características nuevas de JavaScript y trabajarlas con confianza porque TypeScript se va a encargar de pasarlo al estándar de JavaScript que nosotros especificamos y no haber que hacer ninguna modificación a nuestro código para que sea compatible con versiones muy viejas de JavaScript.

## Demostración de TypeScript 09:26

Para trabajar con TypeScript vamos a tener una carpeta llamada **`typescript`** con dos archivos **`index.html`** y **`app.js`**.

![image](https://user-images.githubusercontent.com/23094588/130276997-c32335cc-bd7f-434a-aa08-9529e4f1e016.png)

Vamos a abrir esa carpeta en VSC.

![image](https://user-images.githubusercontent.com/23094588/130277121-2148d5a1-fea7-4e5c-88d8-61b96e0b85e6.png)

El contenido de estos archivos es el siguiente:

```html
<!DOCTYPE html>
<html lang="en">

<head>
   <meta charset="UTF-8">
   <title>Introducción</title>
</head>

<body>

   <script src="app.js"></script>
</body>

</html>
```

```js
function saludar( nombre ) {
   console.table( 'Hola ' + nombre ); // Hola Logan
}

const wolverine = {
   nombre: 'Logan'
};

saludar(  );
```

Vamos a abrir el archivo **`index.html`** con el navegador y abrimos las herramientas del desarrollador.

![image](https://user-images.githubusercontent.com/23094588/130278304-24595790-6254-490e-852e-24d860240cfc.png)

Nos aparece **`Hola undefined`**. Si vemos el código JS que escribimos

![image](https://user-images.githubusercontent.com/23094588/130278541-8b7302e4-f16c-4e17-9327-0fdcc007ae64.png)

tenemos que invocamos el método **`saludar(  );`** sin ningún argumento y la función **`function saludar( nombre )`** espera un parámetro para mandar a consola el saludo **`console.table( 'Hola ' + nombre );`**, como no mandamos nada nos sale **`Hola undefined`**, por que en **JS cualquier variable que no esta definida tiene el valor `undefined`**.

Como vemos VSC no me manda ningún aviso de que me falta el argumente para evitar resultados no esperados, ***nos damos cuenta del fallo hasta que ejecutamos la APP**.

Para evitar estos errores vamos a usar **TypeScript** en lugar de **JavaScript** para lo cual vamos a renombrar nuestro archivo **`app.js`** por **`app.ts`**, tan solo con hacer esto notaremos que en el VSC ya nos esta marcando un error.

![image](https://user-images.githubusercontent.com/23094588/130279530-7cdee582-6b6f-4dc6-ba79-c3e3a326ee4b.png)

Si pongo el cursor encima me indica el error concreto **`Expected 1 arguments, but got 0.`**, se esperaba un argumento pero se mandarón 0, **`An argument for 'nombre' was not provided.`** nos indica que el argumento para **`'nombre'`** no lo hemos proporcionado.

![image](https://user-images.githubusercontent.com/23094588/130279646-b5cfc596-eaf1-43c7-b832-eb9439ca56f8.png)

De esta manera sin ejecutar la aplicación ya estamos viendo el error que tenemos cosa que no pasaba con JS.

Vamos a mandar en el argumento lo siguiente:

```js
saludar( wolverine );
```

El error desaparece:

![image](https://user-images.githubusercontent.com/23094588/130280275-ee9b7609-6123-49a0-ab78-8feeeae29588.png)

Si abrimos el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/130280364-b416954e-c772-49ee-a7d0-f0a40a3d0b29.png)

Podría pensarse que en nuestro archivo **`index.html`**

![image](https://user-images.githubusercontent.com/23094588/130280442-9b842895-856e-4646-9e19-4c70016aa35e.png)

Deberíamos cambiar **`app.js`** por **`app.ts`**, si lo hacemos y abrimos la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/130280549-0ffac686-a498-4503-ab64-820e85581aef.png)


***Funcionó***, NO debería de funcionar, pero lo que pasa es que intentó cargar el archivo de TypeScript **`app.ts`** como si fuera JavaScript y como el código que tengo no tiene nada de TypeScript por eso es que en teoría lo aceptó, pero si ahora en la funcion de saludar ponemos:

![image](https://user-images.githubusercontent.com/23094588/130281358-d149ae25-937f-47cf-ab8d-f7c6d9ff81c3.png)

Por un lado estamos tipando el parámetro de la función saludar:

```js
function saludar( nombre:string ) {
```

Esto nos marca un error el la invocación de la función saludar por que nos indica que lo que debemos mandar el un **`string`** por lo que reamente lo debemos invocar así:

![image](https://user-images.githubusercontent.com/23094588/130281570-a818ca5e-a8be-4261-806f-7ca4d11cbe10.png)

ya no tenemos ningún error en nuestro código, recargamos el navegador y tenemos el error:

![image](https://user-images.githubusercontent.com/23094588/130281680-bf91292d-7366-43dd-92b8-9ee60aa2a3fc.png)

El problema es que en nuestro **`index.html`** estamos invocando a **`app.ts`** y por el momento los navegadores no soportan archivos de TypeScript. Lo primero que hacemos es cambiar nuevamente a **`app.js`** y lo que tenemos que hacer es que en base a nuestro **`app.ts`** generar un  **`app.js`**, esta es la razón de que nosotros instalamos TypeScript en el ordenador.

Abrimos la terminal y damos **`tsc --version`**:

![image](https://user-images.githubusercontent.com/23094588/130282150-c20da65c-b137-4501-acee-315c0effd1fd.png)

Vemos la versión instalada de TypeScript, ahora para compilar nuestro archivo **`app.ts`** damos el comando **`tsc app.ts`**

![image](https://user-images.githubusercontent.com/23094588/130282413-4ba32fea-e9ad-4e77-81d0-14eba7940392.png)


No nos dice nada pero si vemos el contenido de la carpeta nos genero el archivo **`app.js`**

![image](https://user-images.githubusercontent.com/23094588/130282487-2d96ab3b-7ad5-4049-a5cf-5a29e4ad1112.png)

![image](https://user-images.githubusercontent.com/23094588/130282587-26b5ea3b-66ae-49ad-8697-32b6ca926ec0.png)

Lo genero tal cual lo teniamos originalmente sin el tipado.

Si cargamos la APP ahora ya vemos el resultado:

![image](https://user-images.githubusercontent.com/23094588/130282885-034b8052-7a37-4668-9342-f0ec1eb6be06.png)

Solo un detalle, cuando tenemos abiertos ambos archivos **`app.js`** y **`app.ts`** nos marca un error

![image](https://user-images.githubusercontent.com/23094588/130283165-97d2f920-5189-49b1-b901-618ba9118162.png)

esto es por que TypeScript trabaja con Módulos y en teoría junta todo en un mismo archivo y como en ambos archivos tenemos los mismos nombres de las funciones existe un conflicto.

Vamos a poner lo siguiente en **`app.ts`** para evitar dicho error:

![image](https://user-images.githubusercontent.com/23094588/130283661-7d7df732-d8b8-4323-ba4a-74f945eaaf97.png)

Hemos metido todo nuestro código en una ***Función Anonima Autoinvocada***, es la base del ***Patrón Módulo*** de JS. El error ha desaparecido pero como hemos cambiado el archivo **`app.ts`** debemos volver a ejecutar el comando **`tsc app.ts`**, lo hacemos y recargamos la APP.

El archivo **`app.js`** generado quedo así:

![image](https://user-images.githubusercontent.com/23094588/130284061-0bb7a63a-cea6-4444-b5a4-3943f3931003.png)

Si recargamos el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/130284222-e79f424d-386a-4606-8342-fac50337552b.png)

Todo perfecto!!!

## Configuración de TypeScript 07:20


## Variables let y const 07:30
## Introducción a los tipos de datos 07:56
## Excluir archivos a traducir 02:22
## Template literales del ES6 08:03
## Funciones: Parámetros opcionales, obligatorios y por defecto 06:49
## Funciones de Flecha 11:00
## Desestructruación de Objetos y Arreglos 10:56
## Promesas 07:37
## Promesas y su tipado en TypeScript 09:06
## Interfaces de TypeScript 07:52
## Introducción a las Clases de la POO 07:52
## Definición de una clase básica en TypeScript 04:49
## Constructores de una clase en TypeScript 10:03
## Importaciones - URL 07:44
## Decoradores de Clases 06:05
## Tipado del retorno de una función 05:29
## Exámen práctico #1 00:52
## Explicación de la tarea 01:34
## Resolución del examen práctico #1 05:17
## Examen teórico #1 - 10 preguntas
## Código fuente de la sección 00:19