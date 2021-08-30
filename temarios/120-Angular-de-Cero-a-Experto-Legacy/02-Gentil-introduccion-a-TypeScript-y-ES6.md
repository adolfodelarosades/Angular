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

En esta lección vamos a ver las **Funciones de Flecha** que aparecierón en ES6 las cuales se deberían usar hasta donde sea posible. Vamos a crear unas funciones normales y luego vamos a ver como se escribiran como funciones de fecha.

![image](https://user-images.githubusercontent.com/23094588/131213465-2910d4d5-6103-48dd-b9e4-d229faa2cb65.png)

Las funciones de flecha se aplican sobre las funciones asignadas a variables o constantes, no tanto a una función tradicional pura. Veamos como es la representación de la función de fecha:

![image](https://user-images.githubusercontent.com/23094588/131213626-863dfdaf-bd5a-4732-a385-0cd66273e8bf.png)

A primera vista son muy similares en la función de flecha ya no sea la palabra **`function`** pero lo que si se usa es **`=>`**, fuera de eso no más diferencias.

Pero las funciones de flecha tienen una característica interesante que es que si ustedes sólo tienen una línea de código y esa línea de código es lo que ustedes quieren retornar pueden ahorrarse las llaves **`{ }`** y el **`return`**, el código quedaría así:

![image](https://user-images.githubusercontent.com/23094588/131213819-2e79f8ec-50f3-4cf4-96ff-0b7b2fe2b40e.png)

Vamos a ver como se invocan estas funciones:

![image](https://user-images.githubusercontent.com/23094588/131214044-80981a03-6066-4de5-918c-70eaf211c327.png)

La salida de la APP es:

![image](https://user-images.githubusercontent.com/23094588/131214056-2abe6248-64d0-4c87-9760-a7c0d52e7f63.png)

Inclusive podemos aplicar "algo" en el valor que se retorna:

![image](https://user-images.githubusercontent.com/23094588/131214137-3ce4e38e-b4fe-4cdc-a466-1b1303ba414e.png)

![image](https://user-images.githubusercontent.com/23094588/131214126-f7252d40-020a-4350-8d88-35313336979a.png)

Empezamos a apreciar que la función de flecha es considerablemente más compacta. 

Vamos a ver otro ejemplo de función.

![image](https://user-images.githubusercontent.com/23094588/131214322-311dce54-4886-4176-bd0d-0791522e47c6.png)

![image](https://user-images.githubusercontent.com/23094588/131214332-55c4c99b-ec21-4f24-8b15-428c3a8c047d.png)

Veamos como ha compilado el archivo TS.

![image](https://user-images.githubusercontent.com/23094588/131214863-217235ca-59a4-4f94-9e6b-08a5d3cacc92.png)

Recordemos que estamos usando ES5 en nuestro archivo de configuración, podríamos cambiarlo a ES6 y la compilación sería diferente.

Ahora lo que vamos a hacer es crear un Objeto con una propiedad y un método e invocaremos ese método para mostrar el valor de la propiedad:

![image](https://user-images.githubusercontent.com/23094588/131215150-043fe1ba-1a4e-4243-8040-ed32e0ba0650.png)

![image](https://user-images.githubusercontent.com/23094588/131215166-698051ae-be04-4312-a78d-5b2cdb859458.png)

### `setTimeout(...)`

Vamos a cambiar un poco el código para insertar un **`setTimeout(...)`** ***es una función que permite ejecutar un `callback` (una función) en determinado tiempo(ms)***

![image](https://user-images.githubusercontent.com/23094588/131215315-1973ca79-fa90-4ad4-b181-48ed53d074ff.png)

Aquí se nos esta detectando un problema con **`this`**.

![image](https://user-images.githubusercontent.com/23094588/131215342-e3581dde-9791-4507-8c05-3bb2dc2b1b26.png)

Aquí **`this`** ya no apunta al objeto como antes por que lo hemos metido dentro de la función **`setTimeout(...)`**, en este caso estamos apuntando a la función anonima autoinvocada. Vamos a ejecutar la APP y ver la salida:

![image](https://user-images.githubusercontent.com/23094588/131215453-e14e316b-8092-4f4c-bc5d-b4c8f99f6d4f.png)

Después de 1 segundo aparece el mensaje **`undefined smash!!!`** el **`undefined`** aparece por que no esta reconociendo el **`this`** como el objeto. Vamos a ver que pasa si la función la usamos como una función de flecha:

![image](https://user-images.githubusercontent.com/23094588/131215513-aed15e03-7eb1-4b31-a646-130aeb898b01.png)

La APP nos muestra:

![image](https://user-images.githubusercontent.com/23094588/131215532-37a0200b-2605-4458-9733-5c9a2016a181.png)


**Esta es otra característica propia de las funciones de flecha. Las funciones de flecha no modifican a lo que apunta `this`**. En este caso aun que **`this`** este dentro del **`setTimeout`** apunta al objeto gracias a que esta dentro de una función de flecha.

Respaldamos nuestro ejemplo en **`06-Funciones-de-Flecha.ts`** y limpiamos el archivo **`app.ts`** el cual nos queda así:

![image](https://user-images.githubusercontent.com/23094588/131243596-b5232f66-003f-49fa-8758-5bd2e56ed5cb.png)


Incluso esta función anónima autoinvocada la podemos convertir a una función de flecha.

![image](https://user-images.githubusercontent.com/23094588/131243645-384487bb-b6b5-4c6a-9f43-601f187ecfd9.png)


#### GIT

![image](https://user-images.githubusercontent.com/23094588/131215693-bed4ec94-9fe5-4c64-94da-beaf8fc41ea2.png)

## Desestructruación de Objetos y Arreglos 10:56

### Desestructuración de Objetos

En esta lección vamos a hablar sobre la desestructuración de Objetos y Arreglos. Vamos a crear el siguiente objeto:

![image](https://user-images.githubusercontent.com/23094588/131243789-5881dd88-2867-49d5-ac20-7c934512e977.png)

![image](https://user-images.githubusercontent.com/23094588/131243802-ef10c9d9-5dda-44ce-b0d9-67f2265e8c72.png)

El Objeto tiene ciertas propiedades y vemos como obtener el valor de las misma. Estamos usando la palabra **`avenger`** en cada una de las propiedades.

Con la ***Desestructruación de Objetos*** podemos extraer las propiedades del objeto que nos interesen y crear variables inmediatamente. Por ejemplo (podemos usar **`let`** o **`const`**).

```js
const { nombre, clave, poder } = avenger;
```

Básicamente lo que digo es que del objeto **`avenger`** extrae las propiedades y las asigna a las variables que indicamos, con lu cual ya no necesito usar **`avenger`** en la salida a la consola. ***Es importante que las variables tengan en mismo nombre que las propiedades***

![image](https://user-images.githubusercontent.com/23094588/131244157-78791ab1-364c-4901-ba28-8190c6dec6c5.png)

![image](https://user-images.githubusercontent.com/23094588/131244163-d89c5071-7346-4999-aea7-cafeda8e86de.png)

Cabe indicar que no importa el orden en que se coloquen los nombres de las variables.

![image](https://user-images.githubusercontent.com/23094588/131244409-67718e2c-fa21-4bbb-979b-73fceeb05dfa.png)

![image](https://user-images.githubusercontent.com/23094588/131244163-d89c5071-7346-4999-aea7-cafeda8e86de.png)

O inclusive no es necesario extraer todas las propiedades, podemos extraer solo las que necesitemos.

![image](https://user-images.githubusercontent.com/23094588/131244471-c4dbf431-fe4d-4b7d-b331-1228d2875382.png)

![image](https://user-images.githubusercontent.com/23094588/131244476-91f310db-d62d-4b74-974a-ab04715fc9d0.png)

Esto también funciona en los argumentos de una función. Primero vamos a crear una función de extraer.

![image](https://user-images.githubusercontent.com/23094588/131244591-b9bb0571-ddb7-4d2a-8031-3d40f9fcbc9e.png)

![image](https://user-images.githubusercontent.com/23094588/131244606-0f6615af-561b-41c3-acd9-d455f61ad8d0.png)

Aquí simplemente creamos la función y dentro extraemos las propiedades, aquí no hay nada nuevo de lo visto anteriormente, realmente lo interesante es que en lugar de recibir directamente el objeto **`avenger`** vamos a extraer las propiedades directamente:

![image](https://user-images.githubusercontent.com/23094588/131244689-386e97b4-f64f-428a-9a54-b534f3b8d7d2.png)

![image](https://user-images.githubusercontent.com/23094588/131244606-0f6615af-561b-41c3-acd9-d455f61ad8d0.png)

Como vemos nos ahorramos la sentencia de extraerlos nosotros, ***la desestructuración se ha hecho en la pasada del argumento***.

### Desestructuración de Arreglos

Vamos a crear un array de Strings e imprimir sus valores a la consola.

![image](https://user-images.githubusercontent.com/23094588/131244962-27fe6348-ff3b-4fd5-97ba-a205afb415ac.png)

![image](https://user-images.githubusercontent.com/23094588/131244954-bee66d3e-8ab4-48eb-827c-87f5c2ab1616.png)

Al igual que desestructurabamos un Objeto podemos desestructurar un Array de la siguiente forma. Cabe aclarar que con los arreglos si se debe especificar el orden y aquí los nombres de las variables son los que queramos poner ya que solo estan relacionados con el orden.

![image](https://user-images.githubusercontent.com/23094588/131245147-1efcbbc9-ec52-41ba-8f8e-c5bcbd82f839.png)

![image](https://user-images.githubusercontent.com/23094588/131245156-f58e3386-d284-4899-a713-58cb2b25d61e.png)

Si solo nos interesa la última propiedad lo tendríamos que hacer así:

![image](https://user-images.githubusercontent.com/23094588/131245181-5d65c0c6-b78a-414b-91e8-6ac7a48b601d.png)

![image](https://user-images.githubusercontent.com/23094588/131245192-e440764d-2010-4d44-937e-2113a4f25f76.png)

Vamos a crear la función extraer arreglo.

![image](https://user-images.githubusercontent.com/23094588/131245388-397ef6d9-b549-469b-b9a0-83bf797fb7a5.png)

![image](https://user-images.githubusercontent.com/23094588/131245255-c8505e19-18d6-4972-8ab7-8c08821d1189.png)

De igual forma como lo haciamos con los Objetos podemos hacer la desestructuración en el paso de parámetros de la siguiente forma:

![image](https://user-images.githubusercontent.com/23094588/131245430-4f0c71ca-0d93-4c4c-8d8a-60bc0cb485c2.png)

![image](https://user-images.githubusercontent.com/23094588/131245462-2673a8d5-dce3-40f4-8d81-08b97c9f7cea.png)

Vamos a ver como es el archivo compilado JS ES5.

![image](https://user-images.githubusercontent.com/23094588/131245512-c31001bb-db58-4b55-a9ef-6ff2999be85c.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/131245580-2d0c295c-10ee-421a-8de8-4908d2bc81a6.png)

## Promesas 07:37

El tema de las Promesas es un tema muy amplio aquí solo veremos algo muy básico. ***Las Promesas sirven para ejecutar un código sin bloquear la aplicación***. Vamos a ver el siguiente ejemplo:

**NOTA:** TS no puede compilar las Promesas a ES5 por que no existe nada a lo que lo pueda convertir. Se necesitaría implementar una librería de terceros para que sea posible. 

Para este ejercicio vamos a cambiar el archivo de configuración **`tsconfig.json`** de **`es5`** a **`es6`**. El ES6 es el que incluyo las promesas por lo cual vamos a poder trabajar con ellas directamente.

Las Promesas son muy usadas cuando hacemos peticiones a Servicios Web.

### Sintaxis de la Promesa 

Una Promesa contiene una función que recibe dos argumentos, **`resolve`** y **`reject`** las cuales a su vez son dos funciones. **`resolve`** es lo que vamos a retornar cuando todo funciona correctamente y **`reject`** lo llamaremos en caso de algún error. Vamos a meter el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/131246745-3249bdfe-88d8-408f-993f-a32731acdba8.png)


Cuando usamos una promesa esta tiene los siguientes métodos:

![image](https://user-images.githubusercontent.com/23094588/131246645-419b537d-ab49-43fc-a1c6-4b153b2870a4.png)

Usaremos la parte del **`then`** cuando se realiza todo exitosamente y el **`catch`** nos va a servir para ejecutar "algo" cuando sucede un error.

Vamos a insertar la parte del **`then`**, en el que vamos a recibir el mensaje que se manda en el **`resolve`**, 

![image](https://user-images.githubusercontent.com/23094588/131246891-6fa7d6fe-727c-4cd2-bc3d-9aa094f8d98b.png)

El **`.then`** se va a disparar cuando se resuelva la promesa. Al ejecutar la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/131246898-7a55ad92-b922-4ba3-91cc-90d147d313db.png)

Después de 1 segundo sale el mensaje **`se terminó el timeout`**. Con esto apreciamos que la ejecución de la Promesa no es bloqueante, ejecuta el código que le sigue y cuando se resuelve la Promesa ejecuta su código, por eso el orden en que se despliegan los mensajes de salida.

***¿Qué pasaría si en logar de llamar al `resolve` llamo al `reject`?***.

![image](https://user-images.githubusercontent.com/23094588/131247006-1e3e7c78-3b4a-495e-88d6-c7f6786d5f19.png)

![image](https://user-images.githubusercontent.com/23094588/131247021-5e125db2-61b3-4c8e-b930-c24d2b5e1f11.png)

Nos marca **`Uncaught`** por que no estamos atrapando el error, el no manejar errores en las promesas puede detener la ejecución del programa por lo que es importante manejar el **`.catch`**, es decir lo que queremos que haga cuando existe un error. Vamos a incluirlo:

![image](https://user-images.githubusercontent.com/23094588/131247126-e79306d3-e6b1-495b-9e58-6704ae988a24.png)

![image](https://user-images.githubusercontent.com/23094588/131247138-100b6eed-61da-492c-85fc-0028cc078240.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/131247200-339866fa-944e-4952-a1cc-5eaa521af532.png)

## Promesas y su tipado en TypeScript 09:06

Vamos a realizar otro ejemplo de promesas para comprenderlas mejor. Vamos a insertar la siguiente función que retorna una promesa:

![image](https://user-images.githubusercontent.com/23094588/131247352-0bea3b7e-7209-49ff-bf3f-0a84a0bfd116.png)

Si cargamos la APP tenemos:

![image](https://user-images.githubusercontent.com/23094588/131247366-27c73fb2-19c9-48f1-9e9c-e4a0a9213944.png)

que aparentemente no pasa nada, esto es realmente por que no estamos haciendo nada en caso de que la promesa sea correcta o incorrecta, es decir nos falta implementar **`.then`** y **`.catch`**, hagamoslo.

![image](https://user-images.githubusercontent.com/23094588/131247472-e9687a01-9b95-4a2b-aa95-d36c38b2fcba.png)

![image](https://user-images.githubusercontent.com/23094588/131247478-c16d286f-c6d1-4e84-b67c-72a67bbf8c3d.png)

Vamos a poner que queremos retirar 1500 en lugar de 500 y ejecutamos:

![image](https://user-images.githubusercontent.com/23094588/131247490-5e22af3e-e115-4413-8f98-7a878f5d6f11.png)


Nos pone que tenemos un error y que no lo estamos tratando **`Uncaught`**, no falta implementar el **`.catch`**.

![image](https://user-images.githubusercontent.com/23094588/131247537-d6bc3705-bccd-41d9-9665-02a7cf9dfe04.png)

![image](https://user-images.githubusercontent.com/23094588/131247547-cefff243-df8c-4a96-93de-0038a48a62dc.png)

Ahora si ya estamos tratando el error.

Cuando en una función de flecha se recibe solo un parámetro y es el que vamos a imprimir, podemos simplificar la función de flecha de la siguiente forma:

![image](https://user-images.githubusercontent.com/23094588/131247590-5ca27c14-fa31-4f07-b34a-a2f6b42244dd.png)

El resultado sigue siendo el mismo:

![image](https://user-images.githubusercontent.com/23094588/131247547-cefff243-df8c-4a96-93de-0038a48a62dc.png)

### Tipo de Retorno

Hay un pequeño detalle con nuestra función **`retirarDinero`** y es que no sabemos que tipo de retorno esta devolviendo, lo sabemos por que nosotros la hicimos pero TS no lo sabe como marca erl siguiente mensaje:

![image](https://user-images.githubusercontent.com/23094588/131247811-b73e87e5-63a2-44e6-b27c-5ba0120347be.png)

Lo que vemos es que la función **`retirarDinero`** nos esta retornando una **`Promise<unknown>`** que "resuelve" asi se leen los **`<...>`** un **`unknown`**, es decir no sabe cual es el tipo de resolución de la Promesa, nosotros como construimos la Promesa sabemos que va a retornar un **`number`** por que **`dineroActual`** es un número. 

Podría pensarse que podríamos tipar el **`saldo`** dentro del **`then`**, pero nos marca el siguiente error:

![image](https://user-images.githubusercontent.com/23094588/131248354-9b87ed6f-567d-4d45-b9e1-89bfc8749b7a.png)

lo que nos dice que el tipo **`unknown`** no es asignable al tipo **`number`**, por lo que esto no es la solución. Si vamos a la definicón de la función tenemos:

![image](https://user-images.githubusercontent.com/23094588/131248437-74479f71-2b66-4db6-8708-9e442af51e8a.png)

practicamente es lo mismo que ya habiamos visto, recibe un **`number`** y retorna **`Promise<unknown>`** una Promesa que resuelve el **`unknown`**, lo que nos hace falta es cambiar este **`unknown`** por el tipo de dato que yo se que la Promesa va a resolver (si lo hace correctamente, cuando lo hace mal siempre retorna un error), para definir el tipo de retorno vamos a colocarlo después de los argumentos que recibe:

![image](https://user-images.githubusercontent.com/23094588/131248620-cb95e348-2ebd-45c5-b8ce-3f60ece446ba.png)

Al hacerlo así ya sabe que el **`saldo`** que recibo en el **`then`** es un **`number`**, esto tiene como ventaja que puedo usar todos los métodos asociados a los **`number`** sobre mi **`saldo`**.

![image](https://user-images.githubusercontent.com/23094588/131248672-873056cf-82a8-43bf-8bb2-b70c498712f0.png)

Salvemos los cambios y ejecutemos sigue trabajando igual pero ya tenemos la función tipada.

![image](https://user-images.githubusercontent.com/23094588/131248776-4b72867e-9716-4d33-aa1b-0e0e4b4a503c.png)

![image](https://user-images.githubusercontent.com/23094588/131248791-bde77c06-898e-4b53-89be-d2830e93a8ee.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/131248813-4455f9f9-de95-44ac-9593-c64756fbd3de.png)

## Interfaces de TypeScript 07:52

Vamos a ver el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/131248914-620542ec-23fa-45fd-8ace-c57530fffec0.png)

Como podemos ver hay varias cosas potencialmente inseguras aquí, como que en **`xmen`** nos manden cualquier tipo de dato, que no se mande el nombre, etc.

Vamos a crear al objeto **`wolverine`** y lo mandamos a la misión:

![image](https://user-images.githubusercontent.com/23094588/131249067-494a96dc-308a-460e-979b-87eb7738c23b.png)

![image](https://user-images.githubusercontent.com/23094588/131249085-3b97dd41-65c2-444a-9057-16e3177e3337.png)

Todo trabaja como se esperaba.

Pero que pasa si hacemos este pequeño cambio en  **`wolverine`**, cambiar el nombre de la propiedad **`nombre`**

![image](https://user-images.githubusercontent.com/23094588/131249112-9630299a-5a95-4f5d-a17a-1bb092ad8e0b.png)

![image](https://user-images.githubusercontent.com/23094588/131249125-e9181d46-061a-49e7-bc01-b0657d870ca6.png)

Como la función recibe **`any`** puedo mandar a **`wolverine`** con este cambio pero dentro de la función hace referencia a un atributo llamado **`nombre`** y como no lo encuentra nos manda el mensaje **`Enviando a undefined a la misión`**.

Esto ya es un problema para la función **`enviarMision`**. ¿Qué podemos hacer para solucionarlo?. Hay una solución que se ve algo extraña pero que nos puede servir:

![image](https://user-images.githubusercontent.com/23094588/131249262-512a7fd6-5f69-4ebd-8178-bf6b832fdb71.png)

En lugar de poner **`any`** estamos poniendo **`{nombre: string}`** que simboliza que va a recibir un objeto y ese objeto por lo menos debe terer el atributo **`nombre`** de tipo **`string`**, se ve muy extraño pero para este caso nos puede servir. Por consecuencia TS nos marca el error ya que **`wolverine`** no cuenta con la propiedad **`nombre`**, si cambiamos la propiedad **`nombreXman`** por **`nombre`** y aunque tengamos más propiedades TS ya aceta a **`wolverine`** .

![image](https://user-images.githubusercontent.com/23094588/131249353-5cf214a2-396b-4a57-8efd-b0783ab5aa1c.png)

![image](https://user-images.githubusercontent.com/23094588/131249363-f1f6605b-3917-4627-a3c9-382bb7d32f64.png)

El problema de esto es que si tenemos otros métodos que reciban un **`xmen`** tendríamos que hacer lo mismo y si de repente quiero cambiar el nombre de una propiedad lo tengo que hacer entodos los objetos y todos los métodos que los usen, ademas si quiero meter más propiedades se hace más engorroso.

![image](https://user-images.githubusercontent.com/23094588/131249466-e8991e65-ce5f-4935-8a65-9b0d923fa2e7.png)

Este código para el mantenimiento se vuelve algo inmanegable, para esto suguieron las **Interfaces**

### Interfaces

Las **Interfaces** son parecidas a las **Clases**, pero son Clases tontas, una interface no le pueden definir lo que va a hacer, no tiene Constructores, ***simplemente son las reglas que quiere que cumpla un Objeto para poderlo usar como un tipo***, es como crearse un tipo de dato.

Vamos a crear la Interface **`Xmen`** 

![image](https://user-images.githubusercontent.com/23094588/131309539-899ebaeb-6b6a-494b-99f6-b2937f152f22.png)

Si abrimos el archivo compilado JS tenemos:

![image](https://user-images.githubusercontent.com/23094588/131309773-a316f2c7-33c3-492c-8c82-1f8056dfc112.png)

Observamos que en el archivo compilado JS no existe la Interface, ***No hay una representación física de una Interface en JS***.

Ahora lo que vamos a hacer es cambiar el tipo **`{nombre: string}`** por la Interface **`Xmen`**.

![image](https://user-images.githubusercontent.com/23094588/131310362-c1a46ead-ab40-41de-9d9c-b8da748e042b.png)

Si el objeto **`wolverine`** no cumple con lo definido en la Interface, TS se quejara cuando invoquemos los métodos que necesiten un parámetro de tipo **`Xmen`**.

![image](https://user-images.githubusercontent.com/23094588/131310727-42b5c5a3-d091-49df-97b7-6e02b83334a6.png)

Para forzar un poco más el tipado podemos tipar a **`wolverine`** con **`Xmen`** y así TS nos indicará los posibles fallos:

![image](https://user-images.githubusercontent.com/23094588/131312421-6091f65d-0bf0-4f09-abdd-4ad370b810a8.png)

De esta forma nos ponemos una especie de reglas para que nosotros mismos las cumplamos. En este caso vamos a crear un Objeto que cumpla las condiciones establecidas en la Interface. 

![image](https://user-images.githubusercontent.com/23094588/131313835-3d70dc00-a168-4ced-b55f-2c0e778ff72f.png)

![image](https://user-images.githubusercontent.com/23094588/131313904-de6122aa-24b1-4364-9b90-5b6b79f658ca.png)

Esto ayuda mucho al mantenimiento.

Si en la Interface agregamos una nueva propiedad TS nos lo va a indicar:

![image](https://user-images.githubusercontent.com/23094588/131314215-b424099d-1a35-48dd-92d1-ab6143164282.png)

Aquí en teoría deberíamos añadir la nueva propiedad al objeto de tipo **`Xmen`**, pero también podemos indicar que esta nueva propiedad es opcional, es decir los objetos creados pueden tenerla o no.

![image](https://user-images.githubusercontent.com/23094588/131314631-21ffecbe-c8f2-4a11-a310-4f76e302b5b8.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/131315135-817c79fb-a6a9-42dd-9b21-dca85976324a.png)

## Introducción a las Clases de la POO 07:52

Una Clase es una abstracción de algún objeto de la vida real. Una Clase puede tener:

* Propiedades
* Métodos

Herencia: Consiste en que cuando una clase que desciende de otra, hereda todos sus propiedades y meétodos.

## Definición de una clase básica en TypeScript 04:49

Vamos a ver un ejemplo de clases en TS. Los nombres de las clases comienzan con mayúscula por convención. Vamos a crear la clase **`Avenger`**.

![image](https://user-images.githubusercontent.com/23094588/131317002-c18ec8c6-c853-4f36-909f-22aa97f8551d.png)

La clase **`Avenger`** tiene 3 propiedades y dos métodos. 

Si abrimos el archivo compilado JS tenemos:

![image](https://user-images.githubusercontent.com/23094588/131318163-dcf6b6b7-99d8-45db-9b5a-0e099db0afed.png)

En el archivo compilado JS se crea una clase vacía, realmente solo definimos las propiedades y métodos pero como no los hemos usado para JS es como si no existieran. Pero en TS si tenemos todo.

Ahora lo que vamos es a crear un objeto en base a la Clase y lo sacamos a la consola:

![image](https://user-images.githubusercontent.com/23094588/131319031-893246a1-32aa-452c-877b-7152070926d2.png)

![image](https://user-images.githubusercontent.com/23094588/131319211-602cc0a4-c4b4-476a-9d7f-ea104dd073c3.png)

Tenemos un Objeto **`Avenger`** sin propiedades ni métodos. 

Como vemos nos esta marcando errores en las propiedades y en los métodos, esto es por que no estan inicializadas, vamos a inicializar la propiedad **`nombre`**:

![image](https://user-images.githubusercontent.com/23094588/131319640-f65f02c7-182d-47f5-b2d2-77d7ae0915ab.png)

![image](https://user-images.githubusercontent.com/23094588/131319725-58e77f8d-785a-47f3-9df8-8158fc2fdc3f.png)

Aquí ya nos pone un objeto con la Propiedad inicializada.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/131319934-fde49b03-7e26-4d6f-aa3e-cab8b8edfd18.png)

## Constructores de una clase en TypeScript 10:03
## Importaciones - URL 07:44
## Decoradores de Clases 06:05
## Tipado del retorno de una función 05:29
## Exámen práctico #1 00:52
## Explicación de la tarea 01:34
## Resolución del examen práctico #1 05:17
## Examen teórico #1 - 10 preguntas
## Código fuente de la sección 00:19
