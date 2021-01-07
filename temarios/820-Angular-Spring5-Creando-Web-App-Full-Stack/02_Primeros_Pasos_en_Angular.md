# 02. Primeros Pasos en Angular - 13 Clases - 1 h 49 min

* Introducción a Angular 13:44
* Instalaciones y herramientas necesarias 11:37
* Una mirada al editor Atom e instalando algunos plugins 06:25
* Creando nuestra aplicación Angular 13:00
* Introducción a los Componentes 04:12
* Estructura de directorio del proyecto Angular 10:57
* Estructura de directorio del proyecto angular: Parte 2 el directorio src 06:47
* Integrar Bootstrap con Angular 06:54
* Creando nuevo componente HeaderComponent 10:37
* Separando el template del componente con TemplateUrl 02:31
* Creando nuevo componente FooterComponent 10:07
* Directiva estructural `*ngFor` 07:07
* Directiva estructural `*ngIf` 04:48

## Introducción a Angular 13:44

![02-01](images/02-01.png)

Antes comenzar con Angular y a ver las herramientas necesarias a comenzar la instalación, crear el proyecto, quería ver una introducción a Angular. ¿De qué se trata Angular? 

Bueno, la idea de esta parte del curso es aprender paso a paso cómo crear una aplicación web. Justamente Angular es un Framework de JavaScript por el lado del cliente en el FrontEnd, para crear aplicaciones web interactivas y sobretodo amistosas al usuario es decir, con interfaz gráfica bonita, reactivas, instantáneas, dinámicas, en fin, enriquece nuestra aplicación por el cliente, nuestra aplicación web, pero Angular mucho más que eso, aparte de ser un Framework para JavaScript, también es uno de los más utilizados, más populares en el mercado y es el que más piden en la industria, en las empresas para desarrollar este tipo aplicación. Cada vez está más posicionado como el Framework estándar de JavaScript o de Typescript, porque en realidad se programa en tal Typescript, pero finalmente se traspilas se convierte a JavaScript. Bueno, es el más estándar para desarrollar este tipo aplicaciones del lado cliente, del lado del FrontEnd y además desarrollado por un gigante, por Google.

![02-02](images/02-02.png)

Características de Angular

Crea aplicaciones web responsivas, que se adaptan a diferentes dispositivos, equipos, tanto a equipos móviles de celular o navegador de un PC o notebook, tablets, en fin, y están preparada para que se adapten según la resolución y según nuestro equipo, ya sea utilizando **Bootstrap** o **Angular Material** que es propio de Angular, hay diferentes herramientas.

Otra característica muy importante que es la esencia de Angular es **SPA Single Page Application**, es decir, aplicación de una sola página, al final construimos una gran aplicación con Angular, varios componentes que forman esta aplicación, pero siempre el usuario va a estar interactuando dentro de la misma página del navegador, esta nunca se va a actualizar, nunca va a realizar un refresh donde el contenido va cambiando de forma dinámica pero sin recargar la página, es instantáneo de forma asíncrona y reactiva y justamente esa es una de las grandes diferencias con un monolito. Por ejemplo, si desarrollamos una aplicación con Spring Web MVC con vistas **JSP** o **Thymeleaf** todo dentro del servidor, en el BackEnd, todo se ejecuta en el BackEnd, al final se genera el HTML, todo ocurre en el servidor. 

Entonces el problema es que por cada *request* que estamos realizando a nuestro BackEnd, lo que hace el cliente es enviar todo el contenido HTML completo desde las primeras etiquetas del HTML, las hojas de estilos, los JavaScript, el contenido principal, el menú, los banner, menú lateral, las imágenes, todo se está enviando en cada request al BackEnd y finalmente retorna lo mismo. Devuelve exactamente lo mismo con el contenido dinámico que cambia según el controlador, según la ruta que estemos enviando o llamando, se fijan envía todo y devuelve todo, es una carga bastante pesada al servidor y eso multiplicado por la cantidad de usuarios concurrentes que usan la aplicación, el rendimiento podría ser menor, hay que tener en cuenta, mientras que en Angular todo ocurre en una sola página en el cliente, las hojas estilo todo permanece intacto en su mismo lugar. Por ejemplo, el componente del menú, el menú de navegación, menú lateral, los banner, imágenes, todo se queda en el cliente, solamente enviamos un JSON al BackEnd, los datos importantes nada más, enviamos los datos y nos regresan datos ya sea modificados o queremos hacer una consulta, nos retorna una lista de algo o el detalle de algo, pero solamente un JSON, no todo el HTML, no todo el CSS, JavaScript, entonces claro es mucho más rápido, se mantiene forma de una sola página estática en el cliente, lo que cambia bueno es la parte dinámica, el contenido principal que va variando según las rutas que invoquemos en nuestro API Rest en el BackEnd, por eso es SPA, simplemente cambia nuestro contenido principal, que son otros componentes que están enrutados a URLs de Angular y está mediante una clase Service de Angular, de forma reactiva, utilizando el API RxJs se comunica con el BackEnd, realiza esta comunicación con nuestro micro servicios mediante EndPoins y manejamos la respuesta de forma reactiva utilizando el **API Observable** ahí tenemos que suscribirnos y ahí implementa nuestro código, ahí se emite la respuesta que obtenemos del BackEnd y podemos mostrar está, en la vista de alguna forma ya sea con un `ngFor` iterando con un loop, por ejemplo, o mostrar los objetos de este JSON mediante extrapolación de `string`, pero bueno, son puras cosas que vamos a ver en el curso, así que no se preocupen, esto es solamente una introducción.

Entonces estas serían las cuatro características principales, por supuesto, hay muchas más.

![02-03](images/02-03.png)

Otro tema importante son las versiones, cuando se actualiza o cambio una versión a otra, acá tenemos la versión 9.0.2 hasta el momento la última última versión, pero esto va cambiando día a día, semana a semana, incluso la versión mayor que la vamos a ver, cambia cada seis meses, esto es muy constante, pero no se preocupen, porque generalmente la mayoría de las veces no afecta nada a nuestro código.

***La versión consta de tres números***, de derecha a izquierda tenemos el **2**, esta versión es para ***arreglos de bugs***, mejoras, para solución el problema de versiones anteriores, pero solamente arregla algo y eso no afecta nada en nuestro código, nuestro código siempre va a seguir funcionando.

La segunda versión que tenemos acá, en este caso la **0**, es la ***versión menor*** que corresponde a nuevas características pero menores, nuevas funcionalidades, pero también nuestro código va a seguir funcionando sin ningún problema, solamente agrega nuevas características, nuevas función al framework, todo nuestro código que ya teníamos implementado, obviamente sigue funcionando tal cual, no afecta en nada.

Y por último, la versión **9** corresponde a la ***versión mayor***, esto más o menos ocurre cada seis meses a un año, pero lo típico 6 meses, 8 meses va cambiando la versión mayor que sí podrían afectar en nuestro código, pero las estadísticas, todos los cambio versiones que han ocurrido la verdad es que no ha afectado prácticamente en nada en las aplicaciones, pero también podría ocurrir cambios mayores, por ejemplo alguna librería que en alguna versión anterior estaba deprecated es decir obsoleta y está marcada como deprecated, puede que en una versión mayor posterior, esa clase o característica se elimine y ahí podríamos tener un problema, pero de momento no ha ocurrió de esa forma. Entonces, cualquier cambio de versión, incluso mayor, con cambio estructural o con cambio más robustos, por lo general no afecta al funcionamiento de nuestra aplicación que teníamos desarrollada con otra versió, la podemos emigrar sin ningún problema.

Si durante el curso llegan a tener algún problema con versiones posteriores, claro, porque ahora están en la 9, pero muy probable en el momento de que vean esta clase, quizá en qué versión esté Angular, quizá en la 10, 11, en fin, lo más probable que todo funcione tal cual, pero en caso de que cambie algo, algún import, alguna clase, bueno, simplemente me avisan y la actualiza, pero de todas formas, creo que es poco probable dado el historial de cambio de versiones. Por ejemplo, desde las 7 a la 8 y de la otra 9 no hubo ningún cambio en el código, ha funcionado de forma transparente.

Entonces, recuerden, de izquierda a derecha, la primera corresponde a la *versión mayor*, ambios estructurales podrían cambiar algunas clases, eliminar alguna clases deprecated, cambiar algún import, en fin, la *versión menor* nuevas característica y la última *arreglos de bugs*, de errores, optimizaciones del código, pero todo a nivel de Core del Framework.

![02-04](images/02-04.png)

Bueno, Angular utiliza el lenguaje de programación **TypeScript**, que es un super conjunto de JavaScript, por supuesto también incluye ECMAScript 6, también ECMAScript 5, ECMAScript 5 es el JavaScript nativo que se ejecuta, interpreta en los navegadores, ECMAScript 6 es un poco más avanzado, más orientado a Objetos, nueva característica, creo que actualmente estamos en la versión 10 de ECMAScript o versión 2019, también muchas características, pero todo relacionado a la programación orientada a objetos, librerías mucho más robusto. Entonces lo que hace TypeScript es juntar todas estas versiones de JavaScript, este super conjunto y le agrega una abstracción mucho más robusta, mucho más orientada a objetos, mucho más al nivel de Java, por ejemplo, los tipos de datos se basan en clases e interfaces, podemos usar clases interface, clases abstractas, los principios orientados a objetos de Java o C++ acá se aplican exactamente igual. Tenemos modificadores, visibilidad, abstracción, polimorfismo, herencia, sobrecarga de  métodos, sobreescritura, interfaces, tipos de datos más fuertemente tipados, tenemos atributos, métodos, constructores, métodos GET, métodos SET, muy parecido también a los de Java, tenemos tipos **Generics**, podemos implementar nuestro generics para poder reutilizar mejor nuestra clases en la herencia, decoradores, anotaciones y mucho más, es un lenguaje robusto y por último **desarrollado por Microsoft** se utiliza en Angular, se integra en Angular como el lenguaje principal, pero por supuesto que cuando generamos el código de nuestro proyecto en producción con el comando:

```sh
ng build
```

Lo que hace es traducir, convertir, ***traspilar*** este código TypeScript a JavaScript nativo, HTML y hoja de estilos para que lo ejecuten los navegadores estándar y se puede interpretar.

![02-05](images/02-05.png)

Componentes principales de Angular del framework, muchos entre ellos y los más importante, son los **Componentes**, los Componentes mismos de Angular, una aplicación de Angular está compuesta por muchos componentes, *básicamente  un componente es una página*, pero podemos tener un componente principal, que está formado por otros componentes, por sus componentes, por ejemplo, un menú de navegación, un banner, un calendario, alguna tabla con datos, algún gráfico, un pie de página, en fin, cada uno de estos elementos de nuestra aplicación es un componente, pero también tiene un componente principal que es dinámico, que va cambiando según rutas, según link que tengamos de Angular, entonces, a medida que hacemos un clic en algún botón, en el menú de navegación, nuestro contenido principal va cambiando.

Podemos enrutar un componente a una ruta URL en Angular, y estas cambian de forma dinámica y también muy importante sin recargar la página, la página jamás se actualiza, se refresca, no, siempre se mantiene en una sola página, hace que nuestra aplicación sea instantánea, asíncrona, por supuesto, con características reactivas.

En Angular una clase Componente, es una clase de TypeScript común y corriente, pero que tiene un decorador, una anotación específica **`component`** con algunas configuraciones, un selector con la plantilla que vamos a utilizar para reutilizar el contenido del componente, en fin, cosas que vamos a ver.

También puede implementar algunas interfaces, algunos contratos, ***otra característica del componente es que son asíncronos***, es decir, se ejecutan cada uno en su propio proceso, se ejecutan y se cargan, por lo tanto, entre sí no se interrumpen, un componente no tiene que estar esperando a que se carguen los demás componentes para poder iniciarse, no todos se ejecutan, se inicializan de forma paralela. 

**Las plantillas**, las plantillas también son parte del componente, el componente en la clase que hay por detrás y la plantilla, la presentación que se muestra al usuario, el HTML, ahí podemos imprimir variables de la vista que son atributos del componente y podemos mostrar, imprimir estos atributos mediante extrapolación de strings utilizando llaves, también podemos utilizar directivas como `ngIf` para evaluar una expresión booleana y de esa forma poder mostrar o no mostrar un componente, un elemento html, ocultarlo, por ejemplo, o mostrarlo según una condición, `ngFor` para iterar.

También los **Eventos** muy importantes, eventos para que el usuario pueda interactuar con la aplicación, eventos en los botones, en nuestras tablas, es decir, en las filas o registros en nuestros enlaces, en fin, por ejemplo, el evento típico `change` cuando cambia algún elemento en un campo del formulario o una lista desplegable en un check box, también el evento `click` cuando hacemos un clic en un botón para que llame o invoque un método de la clase componente en cuestión.

Los **Pipe** son filtros que nos permite modificar y dar formato a los datos de nuestra vista por ejemplo, dar formato a una fecha, a una moneda, a números y convertir en mayúsculas, minúsculas, podemos hacer muchas cosas y Angular trae varios Pipes por defecto.

**Rutas de Navegación** tal como explicaba, podemos mapear componentes a rutas para que nuestro contenido principal cambie de forma dinámica, a medida que hacemos clic en estas rutas, ejecute el contenido, muestre el contenido de forma instantánea sin recargar la página.

**Decoradores**, **Anotaciones**, **Servicios** que se encarga de la lógica negocio, se trabajan con datos que vienen desde el BackEnd utilizando el **HttpClient** de forma reactiva o utilizando el Observable, básicamente el HttpClient nos permite comunicarnos mediante verbos del request POST, PUT, GET, DELETE con el BackEnd para guardar datos, para eliminar, para enviar, en fin, subir imágenes y todo esto de forma asíncrona, orientado a eventos sin recargar la página.

También podemos crear nuestra propia clase TypeScript, ya sea de utilidad, **Helpers** o clases del modelo que representa nuestros datos mapeado a los JSon que corresponden a las **Entity**, por ejemplo, o a los POJOS en Java o Spring, manejo de **Formularios**, también muy importante **Data Binding** para poblar datos `ngModel` una directiva que nos permite mapear un formulario a una clase de TypeScript de forma automática, para que se vayan poblando los campos, los datos a medida que vayamos escribiendo, **Validar** también estos datos con sus respectivos mensaje de error.

**Módulos**, **Angular Material** para todo lo que es la vista, un montón de cosas, cosas que vamos a ver en el curso en detalle.

## Instalaciones y herramientas necesarias 11:37
## Una mirada al editor Atom e instalando algunos plugins 06:25
## Creando nuestra aplicación Angular 13:00

Ahora sí que estamos listos para comenzar para crear nuestra aplicación con Angular desde cero utilizando **Angular CLI**, lo primero es ir a la página  https://angular.io/ 

![02-06](images/02-06.png)
![02-07](images/02-07.png)
![02-08](images/02-08.png)

Para crear un proyecto usamos el comando 

```sh
ng new my-app
```

El comando `ng` de la consola de angular lo tenemos disponible con la instalación de Angular CLI que realizamos en la clase anterior, ahora simplemente vamos al terminal de nuestro sistema operativo y vamos a crear el proyecto, ***pero primero tenemos que crear un directorio en el cual vamos a guardar todos nuestros ejemplos y proyectos del curso***.

![02-09](images/02-09.png)

Ahí tenemos nuestro directorio raíz de Angular.

### :computer: Crear el Proyecto `clientes-app`

Vamos a crear el proyecto, le vamos a llamar `clientes-app` con el comando 

```sh
ng new clientes-app
```

![02-10](images/02-10.png)

Lo primero que pregunta es...

Lo segundo que pregunta es si queremos agregar en nuestra aplicación Angular el componente `routing`, le indicamos que NO porque eso después lo vamos a agregar de forma manual, la idea es aprender cómo se configura, así que lo dejamos para después, por ahora simplemente no.

La tercer pregunta es qué formato de estilos vamos a querer utilizar, por defecto marca CSS, ese es más que suficiente y aceptamos simplemente con un Enter. 

Crear el proyecto, va a descargar todas las dependencias por lo tanto se puede demorar un buen rato.

![02-11](images/02-11.png)

Una vez que haya finalizado en Windows pueden aparecer un par de warnings.

![02-12](images/02-12.png)

Se debe a que Windows no tiene soporte a esa librería pero sí en Mac en OS X y acá tenemos otro warning típico de Windows que no hay que dar ninguna importancia.

Una vez que se haya creado con éxito el siguiente paso es abrir con VSC. 

![02-13](images/02-13.png)

En la pestaña izquierda tenemos el proyecto con todos sus archivos, Si se fijan aparece un icono distinto por cada tipo de archivo eso es porque instalamos la Extensión.

Si vemos la carpeta `src` es el más importante es donde tenemos nuestra aplicación, todo nuestro código dentro de `app` donde tenemos nuestro ***componente principal***.

#### Ejecutar la Aplicación

Ahora vamos a ejecutar nuestra aplicación utilizando el comando:

```sh
ng serve --open
```

o la versión abreviada 

```sh
ng serve -o
```

Nos vamos a la consola y dentro del directorio angular donde tenemos creado nuestro proyecto `clientes-app` ejecutamos el comando.

![02-14](images/02-14.png)

Es muy parecido a Spring Boot en el sentido que incluye un servidor embebido para desplegar nuestra aplicación Angular.

Tenemos nuestra página de bienvenida con un prototipo por defecto.

![02-15](images/02-15.png)

AQUIIIIIIIIIIIIIIIIIIIIIIIIIII

que prácticamente

podemos quitar eliminar todo lo que aparece y reemplazarlo por nuestro propio contenido.

Ahora este servidor en dicer por supuesto que es para desarrollar no es para un ambiente de producción

cuando llevamos nuestra aplicación a producción lo que hacemos es transpirar convertir todo nuestro

script en JavaScript en código estático HTML y ya escrituró que es interpretado y lo entienden los navegadores

y eso lo podemos llevar lo podemos subir a cualquier servidor que pueda publicar este contenido estático

como por ejemplo Google storage.

O también tenemos Amazon S3 en fin hay varias alternativas de toda forma en el curso.

Más adelante vamos a ver cómo llevar a producción y publicar nuestra aplicación.

Incluso lo podríamos hacer con Nott con el servidor que trae no guíes con Apache con cualquiera con

cualquiera que pueda servir contenido estático.

Básicamente lleva scrip HTML y hojas de estilos ya que levantamos nuestra aplicación.

El siguiente paso es modificar el contenido que tenemos lo que está cargando es el componente principal.

El app component acá tenemos la clase componente y acá vemos varias cosas pero antes de entrar en detalle

lo primero que observamos es que está asociada a un template a una vista HTML.

Después vamos a analizar el decorador componen y todo lo demás pero primero vamos a la vista acá tenemos

la vista a component punto HTML y todo lo que se visualiza en el navegador.

Acá es justamente el código HTML que tenemos en esta plantilla.

Por lo tanto vamos a quitar todo.

Por ahora vamos a dejar solamente el H1.

Nada más.

Todo lo demás lo vamos a quitar e igual con tu también vamos a guardar con control s y volvemos al navegador

observamos que aparecen solamente clientes App el nombre de nuestra obligación.

Perfecto vamos a abrir nuevamente el app component con doble click y como paréntesis aparte cualquier

sugerencia o pregunta para instalar algún tipo de Plains le colocan que sí que instale todos los Playitas

necesarios como por ejemplo.

Lo más probable que te va a pedir instalar el límite necesario para detectar errores de sintaxis en

nuestro código en tiempo de desarrollo a medida que está escribiendo nuestro código con tal script.

El Lipper se encarga de evaluar los errores detectarlos y mostrar cualquier mensaje de estos errores

en el editor.

Entonces si nos pide instalar el Inter lo tenemos que instalar.

De todas maneras el Inter y todas sus dependencias y también techos o cualquier dependencia que necesite

simplemente le colocan bien pero ahora analicemos el componente es un decorador una anotación con cierta

configuración metadata muy parecido a las anotaciones en sprint.

Es para lo mismo para configurar por ejemplo acá tenemos una clase a component que está marcada con

el decorador.

Es una clase componente de angulas tiene un selector.

El selector corresponde a una etiqueta HTML esta etiqueta HTML la podemos incluir en otros componentes.

En este caso como es el componente root o principal la tenemos que incluir en el índex HTML que es la

página principal en la puerta de entrada a nuestra aplicación.

Si se fijan en el body la estamos incluyendo simplemente una etiqueta HTML que contiene el nombre del

selector AP Ruto.

Por lo tanto si colocamos cualquier cosa cualquier nombre que queramos acá tenemos que reflejar ese

mismo nombre.

Y acá se incluye.

Estamos viviendo todo el contenido de este componente todo el HTML que tiene y toda la programación

dinámica dentro de la clase con toda la lógica que le queremos dar.

Lo segundo es el temple R.L en la vista contenido HTML que está asociado a esta clase componente.

Luego tenemos Tails o R.L serían nuestras hojas estilos podríamos tener una o más.

Por eso el corchete se separa por comas por defecto una sola que es la que tenemos acá a components

puntos Esses.

Acá podemos tener solamente los estilos de este componente sin afectar a los demás componentes que tengamos

en nuestra aplicación sólo hacen efecto en el propio componente y no en los demás.

Después vamos a ver cómo aplicar estilos de forma global a todos nuestros componentes por ejemplo agregando

estilos en esta Helesponto CSS.

Acá en stays cualquier estilo que coloquemos se va a aplicar a toda nuestra aplicación a toda nuestra

página y a todo el componente.

Para resumir a component sería nuestro componente principal o por defecto raíz se tiene que dejar tal

cual.

Y a partir de este componente podemos incluir agregar otro componente y empezamos a crear y armar nuestra

aplicación.

Un componente angular son piezas de código que van a componer nuestra aplicación.

Un componente se puede anidar dentro de otro con un componente fijo o bien un componente padre podría

estar formado por varios componentes hijos se conoce como el patrón de diseño composites o compositor.

Por debajo implementa este patrón de diseño lo que lo hace bastante modular escalable y también fácil

de mantener.

Por ahora vamos a modificar un poco más nuestra clase acá vamos a colocar bienvenido angular

y también podríamos tener más atributos de la clase componentes por ejemplo curso podemos usar comilla

simple para hacer referencia en este link.

Como recomendación aunque no es obligación el punto y coma final ahora como buena práctica se recomienda

colocar entonces el curso sería

con angular 7 como había mencionado también una de las características que maneja el script es el tipado.

Si bien es opcional.

Por ejemplo acá asume que es una estreno porque le estamos asignando un valor del tipo Link pero también

lo podría manejar de forma estática por ejemplo.

2 punto 2 punto Streeck es opcional pero también es buena práctica definir los tipos lo hacemos un poco

más robusto

en los estrenos también podemos usar comilla doble o comilla simple.

Bueno en realidad a gusto de cada uno se ve más limpio utilizar comilla simple.

Así que durante el curso vamos a tratar los estrenos con comida simple pero no es tan relevante.

Perfecto vamos a guardar con control ese vamos a ir a la vista a componer.

Acá tenemos el título.

Vamos a tener una lista u el Helí

en el primer Lihn vamos a colocar el nombre del curso siempre usando doble llaves para interpolar las

variables interpolar es para que se imprima se imprime la variable en la salida en la respuesta en el

navegador simplemente hacemos referencia al nombre del atributo en este caso curso después profesor

vamos a copiar el Li

y guardamos entonces siempre las variables que vamos a imprimir es con doble llave una que guardamos.

Volvemos al navegador y vemos el cambio bienvenido vincular curso es principesco con angular 7 profesor

Andrés Guzmán.

Por ahora nada más.

Y en la próxima clase vamos a estudiar analizar la estructura de directorio explicar un poco en qué

consiste cada componente cada tipo de archivo cada directorio por ejemplo el modulos la carpeta ese

reces la carpeta app los asset y también cada tipo de archivo.

Todos los archivos importantes de nuestra aplicación y antes que me olvide un pequeño detalle es opcional

si nos vamos a la clase a component se me fue justamente el punto y coma como no lo marca como un error

porque en realidad no es un error simplemente es opcional es recomendable como buena práctica para mantener

un orden y nuestro código sea un poco más estricto entonces agregamos el punto y coma en el profesor.

Pero insisto es opcional y nuestra aplicación va a funcionar exactamente igual y volvemos a guardar.

Hemos llegado a su fin hasta la próxima.


## Introducción a los Componentes 04:12
## Estructura de directorio del proyecto Angular 10:57
## Estructura de directorio del proyecto angular: Parte 2 el directorio src 06:47
## Integrar Bootstrap con Angular 06:54
## Creando nuevo componente HeaderComponent 10:37
## Separando el template del componente con TemplateUrl 02:31
## Creando nuevo componente FooterComponent 10:07
## Directiva estructural `*ngFor` 07:07
## Directiva estructural `*ngIf` 04:48
