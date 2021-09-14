# 04 Aplicación #2: Aplicación de una sola página (SPA) - 26 clases • 2h 24m

* Introducción a la sección 00:55
* ¿Qué veremos en esta sección? 00:30
* Demostración de lo que lograremos en esta sección 01:21
* Iniciar el proyecto - SPA 03:49
* Creando la estructura de nuestro proyecto 06:24
* Instalando el bootstrap cuando usamos el Angular-CLI 14:58
* Configurando el navbar y otros componentes 06:34
* Rutas en Angular 08:23
* RouterLink y RouterLinkActive - Completando las rutas 09:10
* Componente Heroes - diseño 05:31
* Introducción a los Servicios 02:39
* Creando nuestro primer servicio - HeroesService 10:55
* Página de Heroes - Diseño con **`*ngFor`** 04:57
* Rutas con parametros - Router 09:12
* Recibiendo parámetros por URL - ActivatedRoute 06:53
* Tarea práctica #1 - Componente del héroe 02:50
* Resolución de la tarea práctica #1 - Componente del héroe 05:14
* Pipes: Transformación visual de la data. 03:20
* Buscador de Héroes 06:14
* Tarea práctica #2: Crear la pantalla de búsqueda de héroes. 02:02
* Resolución de la tarea 2 - Buscador de Héroes 07:55
* Plus: Mostrando un mensaje cuando no hay resultados. 02:01
* **`@Input`** - Recibir información de un componente padre a un hijo 10:38
* **`@Output`** - Emitir un evento del hijo hacia el padre 05:40
* Arreglar detalles de la búsqueda 05:50
* Código fuente de la sección 00:24

## Introducción a la sección 00:55

En esta sección vamos a trabajar para crear una aplicación de una sola página conocida como **SPA Single Page Aplication**. Trabajaremos con rutas con **Routers links** como se llama ahora, crearemos nuestro primer **servicio** de forma local. Instalaremos Bootstrap, trabajaremos con **Angular CLI** haremos una introducción a los **Pipes**.

## ¿Qué veremos en esta sección? 00:30

A continuación vamos a aprender sobre los siguientes temas:

1. Crearemos una aplicación de una sola página (Single Page Application)
2. Creación de proyectos de Angular usando el CLI (Command Line Interface)
3. Instalando Bootstrap o librerías de terceros usando el Angular-CLI
4. Creación de rutas de nuestra aplicación
5. Uso de RouterLink y RouterLinkActive para movernos de página y colocar clases a los elementos activos.
6. Uso del modulo Router, que nos permite movernos de página mediante código.
7. Obtención de parámetros vía URL.
8. Configuración de nuestro primer servicio en Angular para el manejo de la data.
9. Breve introducción a los Pipes 
10. Uso del buscador del Navbar para realizar una consulta a nuestro arreglo de héroes.

Durante la sección, tendremos una tarea práctica bastante retadora pero servirá de reforzamiento de todo lo que veremos en esta sección.

## Demostración de lo que lograremos en esta sección 01:21

Aplicación de una sola página.

![image](https://user-images.githubusercontent.com/23094588/133232010-c9c4dcbc-a22a-4580-b7d2-8ddd445f2ae3.png)

Podemos movernos a través de las diferentes páginas las cuales tienen sus respectivas rutas.

![image](https://user-images.githubusercontent.com/23094588/133232173-782f20bf-04c6-4ff5-8479-465921f93cf4.png)

Podemos consultar la información de cada Heroe

![image](https://user-images.githubusercontent.com/23094588/133232363-27f7a51d-046a-447f-acca-1e954a5fe6d9.png)

![image](https://user-images.githubusercontent.com/23094588/133232062-191ad596-a764-45b0-927e-9149ddf04c41.png)

Podemos hacer búsquedas por medio del buscador.

![image](https://user-images.githubusercontent.com/23094588/133232537-7be58fc0-89f6-4690-9aa6-18db765109c5.png)

Esta diseñado para que se vea bien en los móviles.

![image](https://user-images.githubusercontent.com/23094588/133232690-08e9a7ff-cf80-4586-9bda-382a83bdd24c.png)

Todo esto lo lograremos utilizando Angular, Rutas, Servicios, Pipes y algunas cosas más.

## Iniciar el proyecto - SPA 03:49

Desde la terminal en la carpeta de los Proyectos Angular vamos a escribir el comando:

```sh
ng new spa
```

para crear el nuevo proyeyecto llamado **spa**.

![image](https://user-images.githubusercontent.com/23094588/133233334-f1f91e2c-3085-42bf-9fc4-a9d776db0183.png)

![image](https://user-images.githubusercontent.com/23094588/133234793-f65eb28e-4087-481a-825f-a2a50b399194.png)

![image](https://user-images.githubusercontent.com/23094588/133235830-14515c05-7506-4ff5-ae05-608977f73de3.png)

Una vez que termina vamos a renombrar la carpeta creada **`spa`** por **`02-spa`**.

![image](https://user-images.githubusercontent.com/23094588/133236320-574ddd7c-e08c-456f-9c90-5271e66c2fb2.png)

Vamos a meternos a la carpeta **`02-spa`** y levantamos el servidor con **`ng serve -o`**.

![image](https://user-images.githubusercontent.com/23094588/133236621-bb73b0fc-f090-4498-b56d-a136c9c80516.png)

![image](https://user-images.githubusercontent.com/23094588/133236978-6069ed3f-5a32-4c94-b253-2b440f27563f.png)

![image](https://user-images.githubusercontent.com/23094588/133237088-b61dbeaa-478f-45cc-91c8-1a78ee286d4b.png)


## Creando la estructura de nuestro proyecto 06:24

Vamos a abrir el proyecto **`02-spa`** en VSC.

![image](https://user-images.githubusercontent.com/23094588/133238023-82598a9f-5368-48df-acdc-68e1a2ff4b8d.png)

Dentro de la carpeta **`app`** vamos a crear las siguientes carpetas **`components/shared`** que va a ir conteniendo los nuevos componentes que vayamos creando.

![image](https://user-images.githubusercontent.com/23094588/133238341-a6a819dc-d784-487d-9543-4405cab0ec40.png)

### Crear el Componente `Navbar`

Vamos a crear el componente Navbar con el comando:

```sh
ng g c components/shared/navbar
```

Le estamos indicando que genere el componente en la carpeta **`components/shared`** (la que creamos) y se llamara **`navbar`**.

![image](https://user-images.githubusercontent.com/23094588/133239051-4ce8dc85-2e57-4bdc-a64a-e1620d95e5db.png)

Los crea los 4 archivos y actualiza **`app.module.ts`**.

![image](https://user-images.githubusercontent.com/23094588/133239253-f2dbf3c9-812b-4047-87cc-c06b0e1c625c.png)

Vamos a eliminar **`navbar.component.css`** y **`navbar.component.spec.ts`** que no los vamos a usar en esta APP y hacemos los respectivos ajuestes en **`navbar.component.ts`**.

### Crear el Componente `Home`

Vamos a crear el componente `Home` con el comando:

```sh
ng g c components/home
```

Observese que este componente no va dentro de la carpeta de compartidos **`shared`**, si por equivocación lo crearamos dentro de esa carpeta tendríamos que mover la carpeta **`home`** a **`components`** y editar el **`app.modules.ts`** para indicar la ruta correcta.

De igual manera vamos a eliminar **`home.component.css`** y **`home.component.spec.ts`** y hacemos los ajuestes en **`home.component.ts`**.

![image](https://user-images.githubusercontent.com/23094588/133240966-828f49ae-d97f-4836-bb6e-769a0bacbbfd.png)

![image](https://user-images.githubusercontent.com/23094588/133241096-c7cd2195-65f7-4630-9cda-6af1d0a21aaf.png)

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133241241-e2591524-ae5d-4a3a-b97b-4052264f93af.png)

## Instalando Bootstrap cuando usamos el Angular-CLI 14:58

En esta lección vamos a aprender a instalar **Bootstrap** de tres formas diferentes. Esto se aplica para todas las librerías de terceros para que funcionen en su aplicación de Angular.

**NOTA:** En la versión 6 de Angular el archivo **`angular-cli.json`** paso a llamarse **`angular.json`**.

### 1er Forma de Usar Bootstrap con CDN

Vamos a Instalar Bootstrap v4.1.1.

![image](https://user-images.githubusercontent.com/23094588/133242455-16e440d7-c2b5-43ea-8ec5-caea3e330d9d.png)

La forma más sencilla de usar una librería es utilizar el **CDN** o un **Servidor Gestor de Contenidos** 

![image](https://user-images.githubusercontent.com/23094588/133243014-ca52b1ff-bbf2-4d6c-98e2-fde925028321.png)

por lo general esto se recomienda si la aplicación está en Internet, por que esto se almacena en el cache y si ya loo había usado el usuario anteriormente ya no lo volvera a cargar.

Vamos a copiar los CSS y los JS en nuestro **`index.html`**.

![image](https://user-images.githubusercontent.com/23094588/133243594-2a97d457-793b-41de-8cdd-7279a3804323.png)

Movemos el Script de Bootstrap también abajo del todo

![image](https://user-images.githubusercontent.com/23094588/133243733-f2072679-c648-4316-8d42-b7f0c0e78763.png)

Al recargar la APP ya usa los estilos de Bootstrap.

![image](https://user-images.githubusercontent.com/23094588/133244697-932d536e-a550-4d05-abe7-f1eda42645a9.png)

La una restricción de usar el CDN es que siempre debemos estar conectados a Internet.

#### GIT 

![image](https://user-images.githubusercontent.com/23094588/133247245-abd3424f-58b1-48f7-8654-bc0b112c2080.png)

### 2da Forma de Usar Bootstrap Descargandolo.

![image](https://user-images.githubusercontent.com/23094588/133245203-62e4dc11-fd8c-4b41-ba1c-7d7db8c496a9.png)

Otra forma es descargar la librería.

![image](https://user-images.githubusercontent.com/23094588/133245392-bcba712e-d6e2-4fda-a5ab-f324d8b71c5a.png)

Vamos a copiar esta carpeta dentro del proyecto en la carpeta **`assets/libs`** y la renombraremos simplemente como **`bootstrap`**.

![image](https://user-images.githubusercontent.com/23094588/133245922-4a9c72f2-991e-49dc-9031-42877031bf09.png)

Vamos a comentar lo que metimos del CDN y el estilo retorna a su origen.

![image](https://user-images.githubusercontent.com/23094588/133246287-b70b038e-06d9-4859-a892-79bdd0b01cdd.png)

Para usar la librería localmente indicamos la ruta de los archivos descargados:

![image](https://user-images.githubusercontent.com/23094588/133247744-56b37022-13e3-45ef-81a1-0e585d5ab899.png)

![image](https://user-images.githubusercontent.com/23094588/133247785-582adafe-b5de-45d1-8ab5-44bc0292c84d.png)

**NOTA:** Abría que descargarse ademas de la librería de Bootstrap la de JQuery y Popper y meterlos localmente para indicarlos en las rutas de los Scripts localmente. Esta tarea no se ha realizado.

#### GIT

![image](https://user-images.githubusercontent.com/23094588/133248151-0e3590ec-dde8-4eab-9f9e-cc9cad07379c.png)


### 3ra Forma de Usar Bootstrap Instalarlo mediante el `npm`

Lo primero que vamos a hacer es eliminar del **`index.html`**, todo lo que habíamos metido con las dos opciones anteriores e inclusive vamos a eliminar lo que habíamos metido en el **`assets`**

![image](https://user-images.githubusercontent.com/23094588/133248420-9c6365f9-758b-4dca-8c2d-1ee3baac3964.png)

Vamos a pulsar el comando 

```sh
npm install bootstrap --save
```

El **`--save`** esto le indica a la APP que es una librería que va a necesitar, esto descarga Boostrap y los coloca en los Modulos de Node.

![image](https://user-images.githubusercontent.com/23094588/133249263-13a91514-a119-424a-8a0d-b947388f998b.png)

Como no hemos indicado que versión de Bootstrap instalar, instalo la más reciente es decir la v5.1, la ventaja de esta versión es que ya no necesita JQuery y Popper que también tendríamos que instalar con:

```sh
npm install jquery --save
npm install popper.js --save
```

Si nos vamos a los Modulos de Node, seguro lo veremos allí.

![image](https://user-images.githubusercontent.com/23094588/133249692-9ccf68be-1cf8-4296-877d-5f01127dae0c.png)

![image](https://user-images.githubusercontent.com/23094588/133252147-ebd4b283-8365-4f4f-afc5-2cf37e40533c.png)

Ahora lo que tenemos que hacer es indicarle a Angular que vamos a trabajar con el Bootstrap que se encuentra en los Modulos de Node

![image](https://user-images.githubusercontent.com/23094588/133251590-caba2a3d-e366-484d-83b1-42f6184dae86.png)

Esto lo vamos a hacer en el archivo **`angular.json`** que actualmente esta así:

![image](https://user-images.githubusercontent.com/23094588/133250970-4a1745a7-d5fd-4302-8612-64bb2bc34217.png)

Vamos a añadir lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/133252248-8a4f26b3-828c-4ccd-80b6-74d0b7981cd7.png)

Hemos elegido esa librería por la documentación de Bootstrap.

![image](https://user-images.githubusercontent.com/23094588/133252712-b31b397a-63d2-4e84-ab05-4a7cc2d64109.png)

Cuando se modifica el archivo **`angular.json`** hay que dar de baja el Servidor y volverlo a cargar para que tome los cambios.

La APP esta tomando Bootstrap del Node Modules.

![image](https://user-images.githubusercontent.com/23094588/133253634-f4f0d024-6a00-44d3-9a46-7abb5f993b3b.png)


La ventaja de usar esta forma es que si creamos otro proyecto simplemente instalamos Bootstrap con el **`npm`** y copiamos lo que hemos insertado en el **`angular.json`** y ya estaría listo Bootstrap para usarse.








Por qué.

Porque si usamos el si bien es muy probable que otro usuario o nuestro usuario haya navegado a algún

sitio de Internet donde ya tenía esta referencia por lo cual toda esta referencia o todo ese archivo

ya se encuentra en el caché del navegador web del cliente.

Entonces el navegador web no lo va a volver a cargar porque es el mismo para instalarlo.

Simplemente copiamos esta maltratamos este botón de Copping a que abrir el proyecto el proyecto este

en lo particular yo lo tengo en el escritorio como una versión aparte porque les dije que esto es una

actualización del mismo en este caso yo voy a utilizar Atom pero es indiferente.

El editor de texto que ustedes utilicen en el curso siempre es lo mismo abrimos la carpeta SMS nos vamos

al índex punto HTML y aquí vamos a pegar estas librerías ok.

Todo lo que copiamos del Bushra lo pegamos acá regresemos nos hace falta también estados lo que es el

Vickery Slim y el popero apuntó J.S.

Estas dos librerías QWERTY hace como ayuda a la interacción más dinámica del sitio web y el poppers

simplemente ayuda a ubicar ciertas cosas.

Realmente no vamos a usar mucho de estas dos cosas pero son necesarias para todas las funcionalidades

que trae el Bushra.

Entonces la voy a copiar y los escribes usualmente siempre van al final de la página todos los scripts

incluyendo este script que tenemos del Bushra este también lo voy a cortar de acá y lo voy a poner al

final que al final lo voy a colocar aquí tenemos lo que es el busto al final Popper y el recovery graven

los cambios y esto debería hacer que se recargue automáticamente mi sitio web y ya vemos que el vostra

está funcionando con todas sus librerías.

No hay ningún error en la consola y en teoría ya terminamos si usáramos él.

Si bien la única consideración adicional que ustedes deben de tener es que cuando hacen referencia a

sitios web si bien su aplicación va a requerir internet para poder utilizar estas librerías ok.

Ustedes lo tienen que tener en consideración.

Ahora les voy a enseñar otra forma de trabajar con el Bushra u otras librerías de forma local.

Esta es una de dos formas de hacerlo local ok vamos a ir a la documentación del Bushra vamos a tocar

este botón que dice descargas descargamos la librería y vamos a descomprimir la descarga este archivo

comprimido que ya lo tenemos.

Usualmente estas librerías vienen en una carpeta de distribución por eso se llama disto.

Voy a copiar la carpeta completa estadista que trae dos carpetas del CSS y el J.V que adentro está el

bootstrap.

Ok las copian y abran la carpeta del proyecto como yo les dije.

Yo estoy trabajando en una actualización y por eso no lo tengo dentro de la carpeta de angulado ok.

Pero ustedes lo hacen en su proyecto.

Nos vamos a la carpeta SRS assets y aquí creé un nuevo folder este folder por lo general se llama Lips

cuando son librerías externas y cosas que nosotros no hicimos peguen el código acá.

Esta carpeta es el bootstrap la vamos a renombrar a eso Boot Strap esto que estoy haciendo este patrón

no es que sea obligatorio ustedes pueden poner esto en donde se dé la regalada gana siempre y cuando

esté dentro de aceptais okay assets como yo les dije originalmente es ese lugar donde vamos a poner

contenido estático y esto es un contenido estático.

Ahora hay que hacer que el vostra entre aquí de forma local comente esta línea y comenten también estas

tres para que no nos estorben graben los cambios asegúrese de que se mira horrendo el estilo.

Eso quiere decir que efectivamente lo hemos removido.

Ya no estamos usando el Cydia.

Ok entonces clonicos esta línea y hay que cambiar la referencia al CSS sea ya no va a apuntar a esto.

Ahora tiene que apuntar al archivo que nosotros tenemos en este archivo se encuentra en assets.

Entonces ponemos punto Pk aceptais el punto es porque es relativo a donde me encuentro actualmente en

el archivo índex.

Entonces apuntó Plex assets.

Luego viene el Lips luego de Lips viene el bus Trap explica Bootstrap.

Luego del vostra viene CSS Pekka CSS pk ya que dentro del CSS yo le recomiendo que si la librería ustedes

no la han creado entonces utilicen los archivos minimizados o comprimidos en este caso vostra .1.000

punto CSS Bootstrap .1.000 CSS graven los cambios.

Si todo salió bien entonces deberíamos de ver el estilo aplicado acá de forma local o hasta cargando

localmente nada de internet.

Si ustedes escribieran una letra mal por ejemplo no pusieron en la carpeta CSS y graban los cambios

van a tener este error en el bus vostra y tenemos un error 4 0 4 acá que dice que no pudo encontrar

ese archivo.

Entonces vamos a regresar acá dejamos el CSS los cambios y asegurémonos de que esto funcione hay que

hacer lo mismo con los scripts del Bushra apuntó J.V.

Hay que descargarse el popero y el recovery.

Todo eso habría que tenerlo acá y es una labor un poco de carpintería.

Es un poco pesada pero de esa manera lo tenemos o lo tendríamos todo localmente.

Qué queda de tareas si ustedes quieren poner las otras librerías aquí adentro y hacer la misma cosa

que acabamos de hacer.

La ventaja de esto es que los archivos quedan locales en esta carpeta de Lips es fácil de reconocer

es fácil de utilizar.

La última es usar lo que es el no Package Manager como este que tenemos acá.

Esto es ideal porque el proyecto queda grabado de quien necesita el Bushra y otras cosas.

Voy a copiarme esta línea MPM instó Strap.

Pero antes de eso antes de eso déjeme quitar esta otra instalación.

Voy a comentar todas regresemos a la terminal.

Cancelamos esto y tengamos la terminal en el proyecto.

Noten que estoy en la carpeta del escritorio Spa pero ustedes deberían de estar apuntando en esta de

acá.

Ok bien para hacer la instalación voy a pegar el NPA.

Pero menos SOIB para decirle que esta es una librería que mi aplicación va a necesitar.

Esto lo voy a descargar y lo voy a colocar en los módulos de Nott.

No se preocupen por estos warnings aquí simplemente me dice que ya es necesario y que el popera es necesario

Ok podemos ir al sitio web para buscar la instalación de cada uno de estos pero básicamente es escribir

este código.

Ya lo vamos a hacer ahorita mismo al hacer esta instalación entonces aquí en los módulos de Noth aquí

ya tendríamos lo que es el bootstrap aquí está allí tendríamos el vostra la carpeta de distribución

y toda la cosa ya les voy a enseñar cómo hacerlo hay que instalar lo que es el Goiko y el hagámoslo

de una vez.

MPM lanzó espacio Swery menos menos gente.

Esto debería ser sumamente rápido y esperamos un segundo descargo un montón de cosas pero realmente

sólo nos interesa un archivo.

La otra va a ser el popero punto J.V.

Entonces MPM instó espacio Popper punto J.V menos menos se enter eso a descargar la librería y bajar

lista para que nosotros la podamos usar directamente de el archivo de los módulos.

O mejor dicho de las carpetas de los módulos.

Perfecto ya están todos aquí en los módulos de Nott.

Aquí va a estar el popper bastarle G4 y están postra ahora esta instalación que les voy a enseñar.

Es muy común también que es que tendríamos que modificar el archivo del angular apuntó Jayson.

Este es el archivo que vamos a modificar para decirle angular que cuando creé toda la aplicación o cuando

estemos probando use unas librerías que yo te voy a especificar que están aquí adentro.

Entonces abramos ese archivo.

Voy a cerrar esto voy a cerrar esto noten que yo comenté el los estilos aquí no hay nada es como que

eso no existiera.

Noten que el estilo de la página no no va a entrar.

Ok está así no se preocupen por esos errores.

Le expliqué qué es lo que sí me interesa ahora que hagamos es que trabajemos en el archivo angular punto

Jayson.

Ese es el archivo que describe la aplicación como arranca como lo debe de hacer y que es Crips tiene

por defecto si nota aquí está la referencia al ícono la carpeta donde están los assets.

El estilo por defecto que sería el archivo que tenemos en la raíz que es mi archivo de Stiles pero ya

se me perdió la moral Jayson quizá el archivo estimes.

Y también tenemos unos scripts.

Aquí es donde le vamos a especificara angular.

O mejor dicho al angular celar que tiene estos scripts y estas librerías que voy a poner aquí una coma

y aquí dentro voy a hacer referencia empezando al Bootstrap al CSS.

Entonces comenzamos aquí voy a hacer un par relativo a dónde se encuentra este archivo y este archivo

está en la mera mera raíz.

Este archivo está en la mera raíz de mi proyecto aquí adentro también están los módulos de Noc y no

voy a hacer así no son módulos Leca viene el bootstrap hay que buscarlo.

Déjenme mostrárselos acá

modelode no noten que aquí está el archivo de Jayson y aquí están los módulos de.

Vamos a buscar aquí el bootstrap aquí está el bootstrap dentro del vostra está la carpeta Tiz y la misma

cuestión entonces Bootstrap Leca de placa CSS CSS y vamos a apuntar al archivo del busto apuntó mi punto.

CSS lo voy a pegar acá grabo los cambios para que esto entre en efecto yo necesito bajar el Engineer

y volverlo a subir.

Ser más Server es ser ok.

Si algo sale mal en paz aquí voy a tener un error que me va a decir que no logró encontrar ese archivo

pero estoy casi seguro que lo puse bien ok cuando sale eso quiere decir que lo hizo todo sin problemas.

Recargó y aquí noten que ya entró el vostra.

Eso hace que yo no tenga que modificar el archivo índex junto a HTML.

Eso es parte del Bondone que se crea cuando se monta la aplicación.

Hay que hacer lo mismo con los scripts.

Por ejemplo voy a copiar esta línea la voy a pegar acá.

Eso está dentro de Jota ese Bushra .1.000 punto JS Pero el Bushra punto Jota ese va a requerir lo que

es el cuero y el Popea.

Voy a bajar el índice y lo vuelvo a levantar van a notar que es posible que cuando se levante la aplicación

y la recargamos me va a tirar esos mensajes de error de que busca el busto no necesitas librerías recargo

ya que está bueno me está tirando este error pero es lo mismo.

Yo sé que el buscaras necesita de librerías.

Entonces tenemos que importar lo que es el popper y el Jacquot.

Voy a clonar esta línea y voy a importar el Yai QWERTY.

Normalmente la librería que más dependencias tiene va al final.

Ok entonces yo sé que esos se encuentran QWERTY placa de esta placa y qwerty.

Punto.

Slim .1.000 punto J.S. Yo sé que ese es el archivo ustedes lo pueden buscar acá en su carpeta.

Vamos a ver aquí buscaríamos Cuadri y query.

Aquí está Cuadri vist y es este el archivo que me interesa el Slim apuntó.

Jota es lo mismo tengo que hacer con el popper aquí va una coma aquí también monocroma y vamos a poner

el popper que sería el popper.

Punto J.V PLE Cádiz.

Plica.

Y aquí el popper tiene una característica en particular déjeme mostrárselas Popper Popper viene a la

carpeta vist y normalmente podríamos pensar que es este Popper .1.000 punto J.V si lo usamos no es que

salga mal pero esto no está funcionando bien.

Usen el QMD entonces VMS Popper .1.000 punto J.

Esta sería la librería plica o MD o MD plica Popper .1.000 unpunto J es grabamos los cambios yo sé que

esto es mucho trabajo pero les estoy explicando las tres formas de hacerlo.

Ustedes pueden escoger cualquiera de estas.

La ventaja de esta es que podrían copiar ustedes simplemente esto después de una instalación y ya tienen

todo instalado pero también tiene una desventaja que todas estas librerías van a formar parte del Bondone

y si estas son librerías comunes podrían hacer que su aplicación P.C. Un poco más.

Ok pero bueno ya tenemos esa librerías todo está en teoría podría estar bien.

Voy a bajar el índice por verlo subir esperemos un segundo viene.

A ver si no nos tienen ningún error de la importación.

Y listo.

Aquí ya subió el recargo y tenemos la energía y todas las dependencias corriendo.

Ningún error en consola y eso es buena señal.

En teoría aquí termina la clase.

Solo déjenme mostrarles que pasaría o cómo aparece el error si yo no especificó algo.

Por ejemplo el quitar la palabra Tiz de Cuadri que grabó los cambios.

No voy a tener ningún error acá pero cuando baje el Engineer y lo vuelva a subir noten que es lo que

va a pasar me va a tirar un mensaje o un error acá vamos a ver aquí está me dice no logra encontrar

un Haceb el error es que no encontró el archivo no Schiffrin no se encuentra el archivo o directorio

y muestra todo el Paz hispano modelo Slim quiere decir que aquí falta algo que ese archivo no lo logró

encontrar.

Nosotros tendríamos que revisar dentro de los módulos de Noc a ver si efectivamente se descargó y está

ese archivo pero yo sé que aquí lo que falta es el disco voy a grabar los cambios.

Voy a volver a levantar esto con controlé para cancelarlo y lo vuelvo a subir pero ustedes pueden utilizar

cualquiera de las formas que ustedes dicen que se les haga mucho más fácil a ustedes o la que más se

apegue a los requerimientos que tiene su aplicación.




## Configurando el navbar y otros componentes 06:34

Este proyecto necesita que nos descarguemos los recursos de la sección que necesitaremos para realizar la sección.

![image](https://user-images.githubusercontent.com/23094588/133235388-66d749ce-fd66-4d80-a627-a01fb1f6a351.png)

Son imagenes de super heroes, un favicon, estilos css y datos de los super heroes.


## Rutas en Angular 08:23
## RouterLink y RouterLinkActive - Completando las rutas 09:10
## Componente Heroes - diseño 05:31
## Introducción a los Servicios 02:39
## Creando nuestro primer servicio - HeroesService 10:55
## Página de Heroes - Diseño con **`*ngFor`** 04:57
## Rutas con parametros - Router 09:12
## Recibiendo parámetros por URL - ActivatedRoute 06:53
## Tarea práctica #1 - Componente del héroe 02:50
## Resolución de la tarea práctica #1 - Componente del héroe 05:14
## Pipes: Transformación visual de la data. 03:20
## Buscador de Héroes 06:14
## Tarea práctica #2: Crear la pantalla de búsqueda de héroes. 02:02
## Resolución de la tarea 2 - Buscador de Héroes 07:55
## Plus: Mostrando un mensaje cuando no hay resultados. 02:01
## `@Input` - Recibir información de un componente padre a un hijo 10:38
## `@Output` - Emitir un evento del hijo hacia el padre 05:40
## Arreglar detalles de la búsqueda 05:50
## Código fuente de la sección 00:24
