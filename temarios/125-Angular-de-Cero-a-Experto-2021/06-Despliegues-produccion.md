# 06 Despliegues rápidos a producción - • 4 clases • 11m

* Introducción a la sección 02:53
* Temas puntuales de la sección 00:17
* Generar build de producción 05:25
* Desplegando en Netlify 02:37

## Introducción a la sección 02:53

Estamos a las puertas de la sección 6 donde vamos a ver una pequeña introducción a cómo hacer los despliegues de una aplicación de Angular.

En pocas palabras, vamos a generar el Build de producción o la aplicación de producción y la vamos a subir a **Netlify**, después veremos como desplegarlo en otros lugares.

¿Entonces, cómo funciona esto?

Muchas personas piensan que nosotros vamos a tomar todo este montón de archivos, esos 100 o 200 megas o no sé cuántos megas serán que se encuentran dentro de los módulos de Node pero nada de eso llega a la versión final de producción.

Todos esos paquetes y módulos están hechos o están creados para que ustedes puedan hacer las inyecciones de los posibles paquetes que pueden necesitar para que una vez se construya todo el framework de Angular simplemente lo tomen y no hay que hacer ninguna otra importación.  Angular va a quitar todo lo que no es necesario de su aplicación, va a quitar todas las herramientas o las formas de hacer la depuración, va a quitar el Life Reload, va a quitar muchas cosas que en pocas palabras se conoce como el ***Three Shaking***, es decir, como sacudir un árbol, eso quita todas las hojas que ustedes no van a necesitar.

El objetivo de esta sección es que ustedes miren qué fácil es generar el Build de producción, esto crea una carpeta que se llama **`dist`**, en la cual está su aplicación que contiene los archivos de JavaScript, los archivos de CSS y los archivos de JavaScript necesarios para que su aplicación funcione.

Estos archivos ustedes lo despliegan mediante un FTP a cualquier lugar o puede que ustedes tengan el servidor físico, simplemente copian sus archivos y los ponen en su servidor en un IIS, en un Apache, en un servicio de Node o Express o donde ustedes quieran, así de fácil es, no necesitamos un servidor especial. Es una aplicación como si ustedes hubieran creado un **`index.html`** con un archivo JavaScript básico y un archivo de estilos básico. Si su servidor puede correr eso que básicamente son todos los que existen hoy en día, entonces van a poder desplegar su aplicación de Angular.

Vamos a hacer el Build de producción con la sección anterior que nosotros hicimos, con el producto final y desplegarlo en un servidor rápido que se encuentra en la nube para que ustedes lo puedan compartir con otras personas de manera casi instantánea.

Eso es lo que vamos a ver.

## Temas puntuales de la sección 00:17

¿Qué veremos en esta sección?

Este es un breve listado de los temas fundamentales:

1. Generar build de producción
2. Desplegarlo rápidamente
3. Netlify

Aquí aprenderemos como generar el build de producción de nuestra aplicación y la desplegaremos en la web rápidamente usando **Netlify**, el proceso de despliegue en otros servidores es virtualmente el mismo, tomar nuestra carpeta DIST (que contiene la aplicación con archivos HTML, CSS y JS) y desplegarla mediante FTP (preferiblemente SFTP) en el hosting deseado.

## Generar Build de Producción 05:25

Antes de construir el Build de Producción debemos ejecutar el servidor y observar que no tengamos ningún Warning ni ningún Error. También deberiamos revisar nuestro código para eliminar dependencias que no estemos utilizando como por ejemplo en **`personajes.component.ts`** 

![image](https://user-images.githubusercontent.com/23094588/152525606-e613d4e3-76c2-4bb7-86e3-c3b3c8707829.png)

Tenemos el **`Input`** y **`Personaje`** que no usamos, Angular nos lo muestra de un color más opaco, todo esto lo deberíamos eliminar del código, al igual que código comentantado que ya no se usa.

Una vez que ya hemos hecho todo lo anterior con el servidor parado vamos a pulsar el comando:

```sh
ng build --prod
```

![image](https://user-images.githubusercontent.com/23094588/152526609-0cfb4e89-c504-4f35-916b-81350cda030f.png)

Con este comando le estamos diciendo que nos cree la versión de Producción.

El archivo **`main`** de nuestra aplicación pesa **`155.79 kB`** no es muy grande, aun que lo podemos compactar un poco más. Una optimización es que la aplicación la separemos en pequeños módulos y los carguemos mediante Lasy Load o Carga Perezosa







## Desplegando en Netlify 02:37
