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

En el archivo nos a importado los módulos **`NgModule`** y **`CommonModule`** este último se nos a agregado por que usualmente vamos a utilizar las directivas **`*ngIf`** y **`*ngIf`**, en **`declarations`** no tenemos nada por que es un módulo vacío por el momento y en **`imports`** ya incluye el **`CommonModule`**.



















```sh
```

```sh
```

```sh
```























## Diseño de la pantalla a trabajar 04:39
## **`FormsModule`** 08:37
## **`ngModel`** 09:03
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
