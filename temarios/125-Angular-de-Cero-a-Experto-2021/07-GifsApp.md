# 07 GifsApp - Aplicación para buscar imágenes - • 20 clases • 2h 7m

* Introducción a la sección 02:58
* Temas puntuales de la sección 00:17
* Demostración del objetivo final de la sección 02:01
* Inicio de proyecto - GifsApp 04:59
* Diseño inicial de nuestra aplicación de Gifs 08:04
* Módulo Shared 07:39
* GifsModule y sus componentes 07:17
* **`@ViewChild`** - Obtener referencias a objetos del HTML 11:57
* GifsService 11:09
* Controlar el historial de búsquedas 06:57
* Giphy Api Key - Giphy Developers 07:14
* Realizar una petición HTTP 08:34
* Mostrar los resultados en pantalla 09:15
* Colocando un tipado a las peticiones **`http`** 09:47
* **`LocalStorage`** 10:25
* Cargar imágenes automáticamente 04:42
* Obtener imágenes desde el sidebar 03:31
* **`HttpParams`** 06:40
* Animate.style CSS 03:43
* Código fuente de la sección 00:07

## Introducción a la sección 02:58

En esta sección vamos a desarrollar una APP un poco más compleja, vamos a consumir un Servicio que nos va a regresar unas imágenes que vamos a manipular, tendremos un buscador, vamos a mantener información en el **`LocalStorage`** para mantener información persistente en el **`LocalStorage`**, ver cuales son las diferencias entre el **`LocalStorage`** y el **`SessionStorage`**, trabajaremos en base a módulos, consumiremos el API que es muy utilizado por Facebook, WhatsUp, Instragram, etc que nos retorna unos GIFs para poder usarlas en la aplicación, veremos para que sirve el **`@ViewChild`**, uso del paquete **`http`** y  **`observables`**. 

En la APP que construiremos veremos como consumir información del Servicio, como tomamos esa información y la mostramos, como reutilizamos componentes, como mandamos información a componentes.  

## Temas puntuales de la sección 00:17

#### ¿Qué veremos en esta sección?

La sección contendrá nuestra primera aplicación real de Angular, este es un breve listado de los temas fundamentales:

1. Modularización de la aplicación
2. Estructura de la aplicación de media a gran escapa
3. Componentes
4. **`@ViewChild`**
5. Servicios
6. Historial de búsquedas
7. Uso de Api Keys
8. **`LocalStorage`**
9. Peticiones HTTP
10. Animaciones mediante css

Recuerden que siempre tienen el código fuente al final de la sección para que lo puedan descargar y comparar contra el suyo en caso de que sea necesario.

## Demostración del objetivo final de la sección 02:01

Vamos a crear una APP que nos va permitir conectarnos a [GIPHY Developers](https://developers.giphy.com/)

![image](https://user-images.githubusercontent.com/23094588/153027383-3aaee3f5-6853-43ab-a2aa-2d37cc7c6303.png)

que es muy utilizado por Facebook, WhatsUp, Instragram, etc. para mostrar GIFs en sus aplicaciones.

Nuestra APP va a quedar parecida a la siguiente pantalla.

![image](https://user-images.githubusercontent.com/23094588/153040244-4c1fce7a-f560-4d46-a079-b1fdff8bbeb8.png)

Vemos que tenemos un Buscador y un Historial con las últimas 10 búsquedas, al recargar la página la información es persistente con la última búsqueda o el último historial seleccionado, tenemos limitado hasta 10 los resultados, nuestra APP aunque es sencilla va a ser modularizada con un módulo **`shared`** con un **`sidebar`**, un módulo **`gifs`** con nuestros componentes, servicios e interfaces, 

## Inicio de proyecto - GifsApp 04:59


## Diseño inicial de nuestra aplicación de Gifs 08:04
## Módulo Shared 07:39
## GifsModule y sus componentes 07:17
## **`@ViewChild`** - Obtener referencias a objetos del HTML 11:57
## GifsService 11:09
## Controlar el historial de búsquedas 06:57
## Giphy Api Key - Giphy Developers 07:14
## Realizar una petición HTTP 08:34
## Mostrar los resultados en pantalla 09:15
## Colocando un tipado a las peticiones **`http`** 09:47
## **`LocalStorage`** 10:25
## Cargar imágenes automáticamente 04:42
## Obtener imágenes desde el sidebar 03:31
## **`HttpParams`** 06:40
## Animate.style CSS 03:43
## Código fuente de la sección 00:07

