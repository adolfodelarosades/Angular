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


## Estructura HTML de nuestro juego 9 min
## Creando letras de forma dinámica 8 min
## Lógica de la palabra oculta y la palabra hasta el momento 5 min
## Mostrar letras correctas en la palabra oculta 8 min
## Cambiar la imagen y contar los intentos fallidos 6 min
## Verificar si el usuario gana o pierde 6 min
## Mostrar mensaje de victoria o derrota 5 min
## Códigos fuente de todo el curso 1 min


