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

Es muy tedioso estar compilando el archivo TypeScript **`app.ts`** para generar el archivo JavaScript **`app.js`** debería haber una manera un poco más rápida de hacer eso y si lo hay.

Abramos la consola y vamos a escribir el siguiente comando:

```sh
tsc --init
```

![image](https://user-images.githubusercontent.com/23094588/130315592-e409bfd8-9bae-4130-adff-67871aa7a417.png)

Nos indica que se a creado el archivo **`tsconfig.json`** que es un archivo de configuración de TypeScript.

![image](https://user-images.githubusercontent.com/23094588/130315631-01f93fd9-2f31-440f-8174-bc03e8052b2a.png)

Con **`"target": "es5",`** especifica que estamos usando ES5 que es la versión universalmente aceptada por todos los navegadores, pero podemos poner la versión que nosotros necesitemos, esa es otra ventaja de TypeScript que podemos utilizar características nuevas de JavaScript y él se va a encargar de transformarlo a la versión compatible de la versión que seleccioné en el Target de JavaScript en este caso ES5, no hace falta tocar mucha cosa acá pero podemos descomentar las opciones deseadas para activarlas.

En la sección **`Strict Type-Checking Options`** hay opciones para verificar el Tipado Estricto. Por ejemplo si activamos la opción **`"noImplicitAny": true, `** lo que estamos indicando es que ninguna variable la podemos declarar como **`any`** que es tipo por default si no ponemos el tipo de la variable, esto puede probocar varios problemas por que una variable de tipo **`any`** puede recibir números, strings, objetos, etc.

Pero la importancia de tener este archivo para nosotros independientemente de activar varias características podemos ejecutar el siguiente comando en la terminal:

```sh
tsc -w 
```

o 

```sh
tsc --watch 
```

Con esto TypeScript entra en un modo de observación

![image](https://user-images.githubusercontent.com/23094588/130316183-df1792f1-680b-48a0-9034-ae541dbbda5c.png)

Con esto compila todo el TS a JS automáticamente cada que hacemos un cambio en el archivo **`app.ts`** y salvar el archivo se compila todo automáticamente.

![image](https://user-images.githubusercontent.com/23094588/130316372-9d877214-00eb-468f-9d44-a83aa788c9ef.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/130316471-20c9ba96-dcc9-41a4-a997-0829ca6c2d10.png)


## Variables `let` y `const` 07:30

### Variables `var` y `let`

Normalmente con JS definimos las variables así:

```js
var mensaje = 'Hola';

console.log( mensaje );
```

![image](https://user-images.githubusercontent.com/23094588/130316585-2143a2f8-68d8-4f43-84d1-46ceed0e1ac1.png)

Recordar que tenemos TypeScript en modo Observador

Al recarcar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/130316598-73b02425-d74c-4113-8340-898578c0d9fe.png)

Solo una cosa a observar en la Consola nos dice que el mensaje se imprime en la línea 4 pero en el código tenemos la insrtrucción en la línea 8, esto es importante tenerlo en cuenta para cuando se depure la APP.

Si nosotros eliminamos la palabra **`var`** en nuestro archivo **`app.ts`** tenemos lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/130316650-8cb76376-2b72-455f-b3c0-05c0e6132b8b.png)

Por un lado en TS me esta marcando un error pero al salvar el archivo se compila automáticamente el archivo y se genera el archivo JS. Si recargamos la aplicación tenemos:

![image](https://user-images.githubusercontent.com/23094588/130316703-bb9ff169-69d7-4725-bcd7-8918604cb3e0.png)

En ES6 surge una nueva forma de declarar variables que es usando **`let`**.

![image](https://user-images.githubusercontent.com/23094588/130316967-f0f6b9fa-b7e2-4edc-8a81-b7a5e730ce79.png)

Pero vemos que al compilarlo y por tener en nuestro archivo de configuración **`"target": "es5"`** en el archivo JS nos pone **`var mensaje = 'Hola';`**. Si recargamos el navegador tenemos:

![image](https://user-images.githubusercontent.com/23094588/130317048-d8c6767b-f069-4eab-8684-966760e61a07.png)

Donde usemos un **`var`** podemos usar **`let`**, que nos sirve para definir un lugar en memoría para las variables. Pero hay una diferencia de usar una u otra veamos el siguiente ejemplo para verlo más claro:

![image](https://user-images.githubusercontent.com/23094588/130317164-395088bb-9e38-4cac-9dd0-9a9c76ec23c3.png)

![image](https://user-images.githubusercontent.com/23094588/130317173-da058f79-6cf8-4ccb-85ec-ae9c5d1835b7.png)

Imprime **`Mundo`** que es lo que se esperaba. Si ponemos **`let`** a la variable que se encuentra dentro del **`if`** vamos a tener:

![image](https://user-images.githubusercontent.com/23094588/130317223-9a6f1923-b715-4a16-a48c-554d1f8d5451.png)

![image](https://user-images.githubusercontent.com/23094588/130317231-5415394f-a101-4198-b1d0-0410fef9d50b.png)

En este caso imprime **`Hola`**, esto pasa por que al usar **`let`** lo que se hace es declarar una nueva variable en el scope donde se encuentre, en este caso la variable **`mensaje`** definida dentro del **`if`** solo es válida dentro del propio **`if`**, observar que en el caso del archivo JS generado por la compilación a esa variable le pone el nombre **`mensaje_1`** para diferenciarla de **`mensaje`** por que realmente son dos variables diferentes. 

Si en lugar de usar **`let`** usamos **`var`** tenemos:

![image](https://user-images.githubusercontent.com/23094588/130317354-a3c649d1-13c6-441f-8d6b-2718d934d1d8.png)

![image](https://user-images.githubusercontent.com/23094588/130317362-407c99d6-c90a-4392-aac7-1507edbf567d.png)

Cuando usamos **`var`** ***Redefinimos*** el mismo espacio de memoría, por lo que lo que estamos realmente es cambiar el valor de la variable, y en el archivo JS compilado vemos que solo se esta usando la variable **`mensaje`**.

Otra cosa a tener en cuenta al usar **`let`** es que no podemos definir en el mismo scope dos variables con el mismo nombre, con **`var`** si que lo podemos hacer.

![image](https://user-images.githubusercontent.com/23094588/130317562-d98d8abe-5572-4db5-86c4-a0f5ca08a34a.png)

Con TS debemos acostumbrarnos a usar **`let`** ya que nos permite evitar posibles errores que podemos tener al usar **`var`**. 

### Constantes `const`

Cuando usemos una variable que no vaya a cambiar su valor más adelante es mejor declararla con **`const`** en lugar de usar **`let`**, esto es por que ***ocupa menor espacio*** por que no tienen funciones para establecer valores en ellas, como su nombre lo dice no la vamos a poder modificar. Es común que las constantes se declaren en mayúsculas.

![image](https://user-images.githubusercontent.com/23094588/130317814-5dfc811e-f9f4-45b6-a478-489ddef11630.png)

![image](https://user-images.githubusercontent.com/23094588/130317824-b3f79753-87d0-4b83-82ae-b8c9e4bae3df.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/130317890-8dc35f86-1516-4b88-a633-e77fbcfb6b16.png)

## Introducción a los tipos de datos 07:56

En esta lección vamos a ver los ***Tipos de Datos***, vamos a ver el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/130318927-e4addcf3-18c3-4af8-a062-d846e2e83cdc.png)

Si nos ponemos en el primer **`mensaje`** nos pone:

![image](https://user-images.githubusercontent.com/23094588/130318948-2a6b7a9f-c059-436e-af31-61c559704149.png)

Indica que **`mensaje`** que es de tipo **`string`**, TS esta infiriendo el tipo. Y si nos ponemos en el error que nos marca:

![image](https://user-images.githubusercontent.com/23094588/130318989-d2b2d23d-937a-464f-8e0d-4bf2b9a4cc96.png)

Nos indica **`Type 'number' is not assignable to type 'string'`**, ***con JavaScript esto sería totalmente valída, pero con TypeScript no lo es***. Para que la asignación fuera valida tendríamos que asignar un **`string`**.

![image](https://user-images.githubusercontent.com/23094588/130319080-e511b564-fa6c-44a0-bc74-613aeb764d96.png)

Ahora si definimos e inicializamos un número e intentamos asignarle un **`string`** tendremos el mismo problema.

![image](https://user-images.githubusercontent.com/23094588/130319133-cb06ebc1-439c-4fbe-a822-416488b1b92a.png)

En lugar de que TS infiera el tipo podemos indicar el tipo de dato:

![image](https://user-images.githubusercontent.com/23094588/130319188-7245304b-216d-4d12-8788-1f9abbb6b3bb.png)

aunque esto suele estar de más, suele ser más conveniente cuando no inicializmos la variable, el tipo por default es **`any`**:

![image](https://user-images.githubusercontent.com/23094588/130319239-a24cb547-685b-441f-9ac4-49a7475113f0.png)

**`any`** es un tipo especial de TS que acepta cualquier tipo pero deberíamos evitar este tipo de dato.

Otros tipos son **`boolean`** o **`Date`** que ya es una clase :

![image](https://user-images.githubusercontent.com/23094588/130319326-b6adba9e-ae0e-4c9b-9211-79c2587107cf.png)

Podemos ver que la variable de tipo **`any`** puede aceptar cualquier tipo que se le asigne.

También podemos indicar que una variable acepte por ejemplo dos o más tipos tipos de datos:

![image](https://user-images.githubusercontent.com/23094588/130319403-5ea98cbe-c72c-4022-890f-ce1c891c8163.png)

![image](https://user-images.githubusercontent.com/23094588/130319414-15d8dae3-4f4d-4361-a023-d06e782bc5ef.png)

TS hace algo muy interesante con los Objetos.

![image](https://user-images.githubusercontent.com/23094588/130319474-bc9176ed-1547-4e59-b7de-4b258ee9f818.png)

![image](https://user-images.githubusercontent.com/23094588/130319496-8a554031-f097-4f34-b4cf-66c1dcc42a79.png)

Vemos como TS infiere los tipos de las propiedades del objeto, pero además sirve como una especie de candado, esto sirve por si queremos modificar el objeto **`spiderman`**

![image](https://user-images.githubusercontent.com/23094588/130319554-5d33ca17-4546-4bca-bf68-f0642b650069.png)

nos va a indicar que nos faltan las dos propiedades declaradas inicialmente.

![image](https://user-images.githubusercontent.com/23094588/130319621-3895c495-96ae-4c55-a620-a67acabd8783.png)

el error desaparece, pero si meto tipos diferentes me indicara un error.

![image](https://user-images.githubusercontent.com/23094588/130319639-03578d37-c8f0-444d-9387-b440a013e272.png)

![image](https://user-images.githubusercontent.com/23094588/130319653-f952fce5-721a-4b1e-bfa3-40b8dd355117.png)

Tampoco me va a permitir nuevas propiedades en el objeto:

![image](https://user-images.githubusercontent.com/23094588/130319682-494ebb23-c421-428d-9c8e-b10f6e77479c.png)

Finalmente vamos a ver el archivo JS que se genera a partir del TS.

![image](https://user-images.githubusercontent.com/23094588/130319733-4f74b1a3-46f7-4f1e-bb78-7d9e5aac2b92.png)

En el archivo JS no tenemos nada tipado.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/130319773-9c7d788e-d60c-42ea-af19-170c01fb1ed7.png)


## Excluir archivos a traducir 02:22

En todos nuestros ejemplos estamos modificando el archivo **`app.ts`** y estamos perdiendo los ejemplos anteriores, para que no pase esto vamos a crear una nueva carpeta **`typescript`** y allí vamos a ir respaldando lo que vayamos haciendo solo por si lo queremos consultar después.

Dentro de la carpeta **`typescript`** vamos a copiar el archivo **`app.ts`** y le vamos a renombrar por **`03-tipos-de-datos.ts`**, pero vemos que apenas copiamos el archivo **`app.ts`** se genera su **`app.js`**, esto sucede por que tenemos activa el observador(watch) de TS.

![image](https://user-images.githubusercontent.com/23094588/130328164-f701eafc-b20b-4980-8e1a-4f23a7b5b33f.png)

Pero realmente no queremos que haga esto, la carpeta **`typescript`** nos sirve solo de respaldo no vamos a usar nada de lo que haya allí por lo que no queremos que sea compilado, vamos a ir al archivo de configuración de TS para agregar la siguiente línea:

```sh
"exclude": ["typescript"],
```

![image](https://user-images.githubusercontent.com/23094588/130328292-1acd7fb2-8abb-4f31-8afe-6cf7bf29bb35.png)

De esta manera si borramos el contenido de la carpeta **`typescript`** y volvemos a copiar el archivo **`app.ts`** ya no se genera el **`app.js`** por que esta carpeta a sido excluida para que compile su contenido.

![image](https://user-images.githubusercontent.com/23094588/130328357-91124372-c47f-4d95-9f27-21cc804a4509.png)

Ahora simplemente renombramos el archivo **`app.ts`** por **`03-tipos-de-datos.ts`**

![image](https://user-images.githubusercontent.com/23094588/130328393-b98dcf1b-1ea0-4305-94db-fca6dcfa08b4.png)

De esta manera vamos a ir respaldando nuestro código e ir modificando el archivo **`app.ts`** para futuros ejemplos.

#### GIT 

![image](https://user-images.githubusercontent.com/23094588/130328440-60e6c824-3277-42f1-9683-6210ae247e4d.png)


## Template literales del ES6 08:03

En esta lección vamos a ver que son los ***Templates Literales***.

Vamos a suponer que tenemos las siguientes constantes y queremos mostrar en la consola las constantes concatenadas:

```js
   const nombre   = 'Adolfo';
   const apellido = 'De la Rosa'
   const edad     = '20';

   // Adolfo De la Rosa(Edad: 20)
```

Para concatenar las constantes y mostrar el mensaje de salida lo haríamos así:

```js
   const nombre   = 'Adolfo';
   const apellido = 'De la Rosa'
   const edad     = '20';

   // Adolfo De la Rosa(Edad: 20)
   const salida = nombre + ' ' + apellido + '(Edad: ' + edad + ')';
   console.log(salida);
```

Si recargamos la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/130328724-ada649b1-a5f3-4723-afa6-1a9edf83363d.png)

Existe otra forma de hacer esto mismo pero más sencillo con los ***Templates Literales*** en los cuales se usan los "BackTicks" y la inyección de variables con **`$ { VARIABLE }`**. El código es:

![image](https://user-images.githubusercontent.com/23094588/130328956-2eea7f7f-e909-45da-bdd6-688f7522e4a9.png)

Si recargamos la APP tenemos el mismo resultado pero usando los ***Templates Literales*** en lugar de la ***Concatenación***:

![image](https://user-images.githubusercontent.com/23094588/130328724-ada649b1-a5f3-4723-afa6-1a9edf83363d.png)

Los ***Templates Literales*** los podemos usar en multíples líneas pero tenemos que tener cuídado con los Enters y Espacios en Blanco que pongamos por que los toma en cuenta:

![image](https://user-images.githubusercontent.com/23094588/130329076-87e5e647-5c95-4644-940a-108d1fbc6745.png)

![image](https://user-images.githubusercontent.com/23094588/130329090-af9a920f-6b05-4d41-8133-df77c8a30133.png)

![image](https://user-images.githubusercontent.com/23094588/130329109-a0fa305d-eef3-41a6-87fb-dcf40ce201b6.png)

![image](https://user-images.githubusercontent.com/23094588/130329116-da10dd3b-520c-48e4-ab80-bd4f5a0c9c51.png)

Otra cosa interesante que tienen los ***Templates Literales*** es que dentro de **`$ {  }`** se pueden hacer operaciones por ejemplo podemos tener **`$ { edad + 100 }`**

![image](https://user-images.githubusercontent.com/23094588/130329218-fbd398e3-ea2f-4303-8719-e0d13be29365.png)

![image](https://user-images.githubusercontent.com/23094588/130329223-b3b167f2-c5d3-499a-802c-0ec853e9826d.png)

También dentro de **`$ {  }`** podemos invocar una función:

![image](https://user-images.githubusercontent.com/23094588/130329321-bd3945cc-7ffd-4cb1-ac19-b70036aaed7e.png)

![image](https://user-images.githubusercontent.com/23094588/130329338-3b92a4c7-c45e-41d4-80e6-b2d89a24b36a.png)

Los ***Templates Literales*** se implementarón en ES6, por lo que si vemos como hace la compilación a ES5 que es lo que tenemos configurado en el archivo de Configuración de TS, tenemos:

![image](https://user-images.githubusercontent.com/23094588/130329433-a9d59461-e4d2-441b-80bc-52cc8399def3.png)

Hasta aquí lo de ***Templates Literales*** vamos a respaldar el archivo **`app.ts`** y lo llamaremos **`04-template-literal.ts`** y borras el contenido **`app.ts`** para la siguiente lección.

#### GIT 

![image](https://user-images.githubusercontent.com/23094588/130329570-50bd4d98-af80-4b96-8f9c-a5743f2d85a7.png)


## Funciones: Parámetros obligatorios, opcionales y por defecto 06:49

### Parámetro Obligatorios

En esta lección vamos a hablar sobre los ***Parámetros Opcionales, Obligatorios y Parámetros por Defecto***.

Vamos a crear una función tradicional.

![image](https://user-images.githubusercontent.com/23094588/130329673-9d6afe65-3928-4b56-9a21-0d93e9f9b1b3.png)

Tenemos una función que requiere un parámetro ***Obligatorio*** y al invocarla se lo estamos pasando, hasta aquí nada nuevo.

### Parámetros por Defecto

Si tenemos lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/130329794-d0090226-b3a2-4001-8e02-68419ae58f77.png)

Tenemos una función con dos parámetros obligatorios por eso al invocarla nos manda un error, pero para hacer que el segundo parámetro tenga un valor por defecto podemos hacer lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/130329856-787d9cfd-fc8a-4eff-8e6c-5c0058b2ada8.png)

Si le damos cuerpo a la función podemos tener:

![image](https://user-images.githubusercontent.com/23094588/130329914-86a8eefa-a6a1-4d47-a0d1-6a0adb07f58d.png)

Al cargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/130329937-9e7c5664-b5d0-4ed7-8353-073fa5f71ab1.png)

Como vemos estamos recibiendo el primer parámetro y usando el valor por defecto del segundo parámetro. Pero podríamos mandar el segundo parámetro en la invocación de la función:

![image](https://user-images.githubusercontent.com/23094588/130330032-ff4ed834-54f8-4e44-9541-240a379f9e3c.png)

Al cargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/130330047-9ddfc1c8-185d-4dbd-a5cb-7d38f0021fb3.png)


Observamos que si pasamos el segundo parámetro ya no toma su valor por default sino lo que le pasemos.

### Parámetro Opcional

Vamos a meter un tercer parámetro en la función

![image](https://user-images.githubusercontent.com/23094588/130330140-1aa4f195-fdfb-407c-8307-d755c5aea078.png)

En este caso el nuevo parámetro **`momento`** es obligatorio, en una función los parámetros de los diferentes **tienen un orden recomendado**:

1. Obligatorios
2. Opcionales
3. Por Defecto

![image](https://user-images.githubusercontent.com/23094588/130330383-f1eb47ad-c246-4e82-93f8-c6b114b82535.png)

En este caso tenemos un parámetro obligatorio, otro por default, y otro obligatorio y estamos intentando pasar el 1er y 3er parámetro, para que tome el segundo por default pero nos marca un error en la invocación, esto es por que el por default esta en medio y en este caso es necesario mandar su valor aun que sea el mismo que el por default para que entienda que va a recibir.

![image](https://user-images.githubusercontent.com/23094588/130330483-a515b345-c3be-424c-8ed4-4085dbea4213.png)

Al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/130330495-363c0776-da3a-4045-bbd1-eca21fc2b2cb.png)

Pero para hacer el parámetro **`momento`** sea opcional debemos añadir un **`?`**, es decir **`momento?`**.

![image](https://user-images.githubusercontent.com/23094588/130330658-9151625f-9768-4ca9-9f96-0e48505d2e46.png)

Dependiendo si **`momento`** existe o no mandaremos uno u otro mensaje, veamos que pasa al recargar la APP:

![image](https://user-images.githubusercontent.com/23094588/130330684-e92d3086-0cbb-4f67-87c8-09fe4c15d834.png)

Vamos a mandar el **`momento`**, para lo cual también tenemos que pasar el **`objeto`**:

![image](https://user-images.githubusercontent.com/23094588/130330728-e91eb294-8079-4d91-81dd-bedadb1f1f26.png)

Al recargar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/130330736-6bfa56e7-967c-433e-8eab-ddf5f457f33b.png)

Finalmente vamos a ordenar los parámetros de la función de acuerdo a su tipo Obligatorios, Opcionales y por Default, con esto tendremos la ventaja que ya no tenemos que mandar el parámetro por default sino que use el valor por defecto.

![image](https://user-images.githubusercontent.com/23094588/130330802-91296bbe-cd9c-47f6-872c-88a036e6fb34.png)

Al recargar la APP tenemos la misma salida:

![image](https://user-images.githubusercontent.com/23094588/130330828-e38ce265-84e9-4598-8f61-d9614d80c8b5.png)

pero tenemos la ventaja de no enviar los parámetros por default si no es necesario.

Si no mandamos el parámetro opcional tenemos:

![image](https://user-images.githubusercontent.com/23094588/130330934-493b9f06-74f1-4e09-823e-1ae181ce91c5.png)

![image](https://user-images.githubusercontent.com/23094588/130330930-28b51e1f-fec0-48a6-b2f8-59a3ef60441e.png)






#### GIT

![image](https://user-images.githubusercontent.com/23094588/130330885-d1fa73df-7b0a-4c51-a5ea-c6260990aa1e.png)

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
