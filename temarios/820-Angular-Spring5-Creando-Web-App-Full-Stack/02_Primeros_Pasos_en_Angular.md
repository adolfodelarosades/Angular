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

Pero bueno, antes comenzar con Angular y a ver las herramientas necesarias a comenzar la instalación.

En fin, crear el proyecto.

Bueno, quería ver una introducción Angular.

De qué se trata?

Angular?

Bueno, la idea de esta parte del curso es aprender paso a paso cómo crear una aplicación web.

Bueno, justamente Angular es un Framework de JavaScript por el ardiente en el FrontEnd para crear aplicaciones web interactivas y sobretodo amistosas al usuario. Es decir, con interfaz gráfica bonita, reactivas, instantáneas, dinámicas. En fin, enriquece nuestra aplicación por el cliente.

Nuestra aplicación web bien pero Angular mucho más que eso, aparte de ser un Framework para JavaScript, también es uno de los más utilizados, más populares en el mercado y es el que más piden en la industria, en las empresas para desarrollar este tipo aplicación. Cada vez está más posicionado como el Framework estándar de JavaScript o de script, porque en realidad se programa en tal script, pero finalmente se traspilas se convierte a JavaScript.

Bueno, es el más estándar para desarrollar este tipo aplicaciones del lado cliente, del lado del front y además desarrollado por un gigante, por Google.

Ven características para crear aplicaciones web responsive?

S que se adaptan a diferentes dispositivos, equipos, tanto a equipos móviles de celular o navegador de un PC o notebook, tablets, en fin, y están preparada para que se adapten según la resolución y según nuestro equipo, ya sea utilizando Bootstrap o Angular material propio de Angular. En fin, hay diferentes herramientas.

Otra característica muy importante que es la ausencia de Angular es SPA Single Page Application, es decir, aplicación de una sola página.

Al final construimos una gran aplicación con Angular, varios componentes que forman esta aplicación, pero siempre el usuario va a estar interactuando dentro de la misma página del navegador.

Esta nunca se ha de actualizar, nunca va a realizar un reflejo donde contenido va cambiando de forma dinámica pero sin recargar.

La página es instantáneo, de forma asíncrona y reactiva.

Bueno, y justamente eso es una de las grandes diferencias con un monolito.

Por ejemplo, si desarrollamos una aplicación con Spring Eeb m%s con pistas jsp o timeline dentro, bueno, todo dentro del servidor.

En el bakker todos ejecutan el Wacken.

Al final se genera el HTML.

Bueno, todo ocurre en el servidor.

Entonces el problema que por cada rico es que estamos realizando a nuestro Wacken, lo que hace el cliente es enviar todo el contenido HTML completo desde las primeras etiquetas del HTML, las hojas de estilos, los JavaScript, el contenido principal, el menú, los banner, menú lateral, las imágenes.

Todo se está enviando en cada request al backend y finalmente retorna lo mismo.

Devuelve exactamente lo mismo con el contenido dinámico que cambia según el controlador, según la ruta que estemos enviando o llamando.

Se fijan. Entonces envía todo y devuelve todo.

Es una carga bastante pesada al servidor y eso multiplicado por la cantidad de usuarios concurrentes que usan la aplicación. Bueno, el rendimiento podría no ser menor.

Hay que tener en cuenta, mientras que Angular todo ocurre en una sola página en el cliente, las hojas estilo todo permanece intacto en su mismo lugar.

Por ejemplo, el componente del menú, el menú de navegación, menú lateral, los banner, imágenes. Todos se quedan en clientes.

Solamente enviamos un Jaison al bokken. Los datos importantes nada más.

Enviamos los datos y nos regresan datos ya sea modificados o queremos hacer una consulta, nos retorna una lista de algo o el detalle de algo, pero solamente un Jetson, no todo el HTML, no todo el CSS ya scrip, el HTML. Entonces claro, es mucho más rabio.

Se mantiene forma de una sola página estática en el cliente.

Lo que cambia bueno es la parte dinámica, el contenido principal que va variando según las rutas que invoquemos en nuestro API rest en el paquete.

Por eso es S.P.A. Simplemente cambia nuestro contenido principal, que son otros componentes que están enrutador a jureles de Angular y está bueno mediante una clase servida angular de forma reactiva utilizando el API RX 10 se comunica con el Wacken.

Realiza esta comunicación con nuestro micro servicios mediante en paint y manejamos la respuesta de forma reactiva utilizando el API observable.

Ahí tenemos que suscribirnos y ahí implementar nuestro código.

Hoy se emite la respuesta que obtenemos del Wacken y podemos mostrar está en la vista de alguna forma, ya sea con un end Gifford y tirando con un loop, por ejemplo, o mostrar los objetos de este JSON mediante extrapolación de string.

Pero bueno, son puras cosas que vamos a ver en el curso, así que no se preocupen, esto es solamente una introducción.

Entonces estas serían las cuatro características principales.

Bueno, por supuesto, hay muchas más.

Otros deben importante en las versiones cuando se actualiza o cambio una versión a otra.

Acá tenemos la versión 9.0.2 hasta el momento.

La última última versión.

Pero esto va cambiando día a día, semana a semana.

Incluso la versión mayor que la vamos a ver, cambia cada seis meses.

Entonces esto es muy constante.

Pero no se preocupen, porque generalmente la mayoría de las veces no afecta nada a nuestro código.

La versión consta de tres números.

Acá tenemos, por ejemplo, el 2.

Podemos comenzar primero de derecha a izquierda.

Esta versión es para arreglos de bugs, mejoras para solución al problema de versiones anteriores,

pero solamente arregla algo y eso no afecta nada en nuestro código.

Nuestro código siempre va a seguir funcionando.

La segunda versión que tenemos acá, en este caso la 0, es la versión menor que corresponde a nuevas

características pero menores nuevas funcionalidades.

Pero también nuestro código también va funcionando sin ningún problema.

Solamente agrega nueva característica, nueva función al framework.

Todo nuestro código que ya teníamos implementado, obviamente sigue funcionando tal cual, no afecta

a nada.

Y por último, la versión 9 corresponde a la versión mayor.

Esto más o menos ocurre cada seis meses a un año, pero lo típico 6 meses, 8 meses va cambiando.

Traccion mayor son cambia un poco más importantes que sí podrían afectar en nuestro código, pero las

estadísticas todos los cambio versiones que han ocurrido.

La verdad es que no ha afectado prácticamente nada en las aplicaciones, pero también podría ocurrir

cambios mayores.

Por ejemplo, alguna librería que en alguna versión anterior estaba de pruébatela, es decir, obsoleta

y está marcada como despégate.

Puede que en una versión mayor posterior, esa clase o característica se elimine.

Ya podríamos tener un problema, pero este momento no ocurrió de esa forma.

Entonces, cualquier cambio de versión, incluso mayor, con cambio estructural o con cambio más robustos,

por lo general no afecta al funcionamiento de nuestra aplicación que teníamos desarrollada con otra

versión.

La podemos emigrar sin ningún problema y durante el curso, si llegan a tener algún problema con versiones

posteriores, claro, porque ahora están en la nube, pero muy probable en el momento de que vean esta

clase, quizá en qué versión esté angulas.

Quizá en la diez y la once.

En fin, lo más probable que todo funcione tal cual.

Pero en caso de que cambie algo, algún import, alguna clase, bueno, simplemente me avisan y la actualiza.

Pero de todas formas, creo que es poco probable dado el historial de cambio de versiones.

Por ejemplo, desde las 7 a la 8 y de la otra 9 no hubo ningún cambio en el código.

Ha funcionado de forma transparente.

Entonces, recuerden, de izquierda a derecha, la primera corresponde a la versión mayor.

Cambios estructurales podrían cambiar algunas clases, eliminar alguna clase que te de pruébatela,

cambiar algún import.

En fin, la menor nueva característica y la última arreglo de bugs, de errores, optimizaciones del

código.

Pero todo a nivel de Kor del framework.

Bueno, Angular utiliza el lenguaje de programación TypeScript, que es un super conjunto de JavaScript.

Bueno, por supuesto también incluye Mac Script 6.

Bueno, también 5.

La acción 5 es el Jack Deep nativo que se ejecuta.

Interpreta los navegadores en Eclipse.

Es un poco más avanzado, más orientado.

Objeto.

Nueva característica.

Creo que actualmente estamos en la versión 10 de Eggman Script o versión 2019.

También muy característica, pero todo relacionado a la programación orientada a objetos, librerías

mucho más robusto.

Entonces lo que hace de script es juntar todo esto hasta versiones de ya.

Este super conjunto y le agrega una abstracción mucho más robusta, mucho más orientÃ objeto mucho más

al nivel de Yaba.

Por ejemplo, los tipos de datos se basan en clases e interfaces.

Podemos usar clases interface, clases abstracta.

Los principios orientÃ objeto de Java o Deshechar o C++.

Bueno, acá se aplican exactamente igual.

Tenemos modificadores, visibilidad, abstracción, polimorfismo bueno y todo lo que polimorfismo,

todo lo que herencia, sobrecarga, métodos o escritura, interfaces en fin, tipos de datos más fuerte

fuertemente tipado tenemos atributos métodos constructores, métodos GET métodos set muy parecido también

en Java vemos tipo generics.

Podemos implementar nuestro generics para poder reutilizar mejor nuestra clases en la herencia, decoradores,

anotaciones y mucho más.

Es un lenguaje bien robusto.

La escrit a y por último desarrollado por Microsoft se utiliza en Angular, se integra en Angular como

el lenguaje principal.

Pero bueno, por supuesto que cuando generamos el código nuestro proyecto en producción con el comando

ng build.

Bueno, lo que hace es traducir, convertir tras Pilato este código TypeScript e JavaScript nativo HTML

y hoja de estilos para que lo ejecuten los navegadores estándar y se puede interpretar.

Componentes principales de Angular del framework, muchos entre ellos y lo más importante, son los

componentes, los componentes mismos de Angular.

Una aplicación de Angular está compuesta por muchos componentes, básicamente componentes, una página,

pero podemos tener un componente principal que está formado por otro componente por sus componentes.

Por ejemplo, un menú de navegación, un banner, un calendario, alguna tabla con datos, algún gráfico,

un pie de página, en fin.

Cada uno de estos elementos de nuestra aplicación es un componente, pero también tiene un componente

principal que es dinámico, que va cambiando según rutas, según link que tengamos de Angular.

Entonces, a medida que hacemos un clic en algún botón en el menú de navegación, nuestro contenido

principal va cambiando.

Podemos enrutar un componente a una ruta.

°L En Angular Yetta cambian de forma dinámica y también muy importante sin recargar la página.

La página jamás se actualiza, se refresca.

No siempre se mantiene en una sola página.

Hace que nuestra aplicación sea instantánea.

Asíncrona, por supuesto, con características reactivas.

Bueno, y en Angular una clase componente es una clase de tag script común y corriente, pero que tiene

un decorador.

Una anotación específica component con algunas configuraciones, un selector con la plantilla que vamos

a utilizar para reutilizar el contenido del componente.

En fin, cosa que vamos a ver.

Y también puede implementar algunas interfaces, algunos contrato y otra característica del componente

es que son asíncrono, es decir, se ejecutan cada uno en su propio proceso, se ejecutan y se cargan.

Por lo tanto, entre sí no se interrumpe un componente.

No tiene que estar esperando a que se cargue lo demás componentes para poder iniciarse.

No todos se ejecutan.

Se inicializa de forma paralela.

Bueno, la plantillas, la plantilla también son parte del componente, el componente en la clase que

hay por detrás y la plantilla la presentación que se muestra al usuario, el HTML.

Ahí podemos imprimir variables de la vista que son atributos del componente y podemos mostrar imprimir

estos atributos mediante extrapolación de strings utilizando llaves.

También podemos utilizar directivas como mji if en Gifford en Gifford para iterar en gif para evaluar

una expresión booleana y de esa forma poder mostrar o no mostrar un componente, un elemento html,

ocultarlo, por ejemplo, o mostrarlo según una condición.

También los eventos muy importantes eventos para que el usuario pueda interactuar con la aplicación,

eventos en los botones en nuestras tablas, es decir, en las filas o registros en nuestros enlaces.

En fin, por ejemplo, el evento típico change cuando cambia algún elemento en un campo del formulario

o una lista desplegable en un check box, también el evento click cuando hacemos un clic en un botón,

en fin, para que llame o invoque un método de la clase componente en cuestión.

Los pipe también son filtros que nos permite modificar y dar formato a los datos de nuestra vista.

Por ejemplo, dar formato a una fecha, a una moneda, a números y convertir en mayúscula minúscula.

Podemos hacer muchas cosas y angula trae varios pips por defecto que ya vienen construidos rutas de

navegación.

Tal como explicaba, podemos mapear componentes a rutas para que nuestro contenido principal cambie

de forma dinámica.

A medida que hacemos clic en estas rutas, ejecute el contenido.

Muestre contenido de forma instantánea sin recargar la página.

Decoradores, anotaciones, servicios que se encarga de la lógica negocio.

Se trabajan con datos que vienen desde el Wacken utilizando el http kylian de forma reactiva o utilizando

el observable.

Entonces básicamente el http client nos permite comunicarnos mediante verbos del request post put get

delight con el Wacken para guardar datos, para eliminar, para enviar, en fin, subir imágenes.

Y todo esto de forma síncrona orientado a eventos sin recargar la página.

También podemos crear nuestra propia clase Theta Script, ya sea de utilidad Halpert o clase del modelo

que representa nuestros datos mapeado a los Yeison que corresponden a los Entity, por ejemplo, o a

los pocos en Java.

En Spring manejo formulario también muy importante data binding para poblar datos en Timol, una directiva

que nos permite mapear un formulario a una clase de Tai-Chi de forma automática para que se vayan poblando

los campos.

Los datos a medida que vayamos escribiendo, validad también estos datos con sus respectivos mensaje

de error.

Effi módulos angular material para todo lo que lavista un montón de cosas.

Bueno, y precisamente cosas que vamos a ver en el curso en detalle.

Bueno, sin extenderme más, nos vemos en la siguiente clase.


Acerca de este curso
Desarrollo frontend con Angular 11 y backend Spring 5, Spring Boot 2, API REST, JPA, Spring Security OAuth2, JWT, Socket



## Instalaciones y herramientas necesarias 11:37
## Una mirada al editor Atom e instalando algunos plugins 06:25
## Creando nuestra aplicación Angular 13:00
## Introducción a los Componentes 04:12
## Estructura de directorio del proyecto Angular 10:57
## Estructura de directorio del proyecto angular: Parte 2 el directorio src 06:47
## Integrar Bootstrap con Angular 06:54
## Creando nuevo componente HeaderComponent 10:37
## Separando el template del componente con TemplateUrl 02:31
## Creando nuevo componente FooterComponent 10:07
## Directiva estructural `*ngFor` 07:07
## Directiva estructural `*ngIf` 04:48
