# Contenido del curso

## Descripción

* 21 secciones
* 220 clases 
* 23 h 33 m de duración total

### [01. Introducción](01-Introduccion.md) - 2 Clases - 9 min

* Introducción 05:24
* Antes de comenzar 03:19

### [02. Primeros Pasos en Angular](02_Primeros_Pasos_en_Angular.md) - 13 Clases - 1 h 49 min

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

### 03. Angular: Componente Clientes - 11 Clases - 55 min

* Creando el componente clientes.component 03:28
* Listando los objetos del tipo Cliente 07:17
* Creando archivo clientes.json.ts con la lista de objetos 02:51
* Creando la clase de Servicio ClienteService y la Inyección de Dependencia 07:51
* Introducción a los Observables 09:56
* Implementando Observable en nuestra clase Servicio ClienteService 08:18
* Implementando Rutas en Angular y navegación 05:14
* Actualización: sobre el archivo angular.cli.json vs angular.json 00:39
* Configurando e integrando Bootstrap de forma local en nuestra app 05:32
* Actualización: configurando los styles y scripts en archivo angular.json 00:17
* Instalando Bootstrap utilizando el comando npm desde el terminal 03:55

### 04. Backend: Spring API REST - 16 Clases - 1 h 28 min 

* Demostración de lo que lograremos al finalizar las siguientes secciones 02:33
* Herramientas necesarias Backend 06:46
* Instalación y configuración del IDE Eclipse 06:40
* Actualización: Wizard para seleccionar dependencias en Spring Tools 02:25
* Creando Proyecto Backend API REST 10:23
* Configurando el Datasource a MySQL en el proyecto backend 06:46
* Instalando MySQL 04:12
* Creando la Base de Datos 03:11
* Añadiendo la clase Entity Cliente al Backend 08:20
* Añadiendo las clases Repository y Service de la lógica de negocio 11:48
* Creando controlador `@RestController` y EndPoint para listar 04:22
* Añadiendo Datos de pueba 02:54
* Usando Postman para probar nuestras APIs 04:09
* Uso de Cors para compartir recursos en API REST 04:02
* Implementando Servicio Angular con HttpClient 09:28
* Descargar Código Fuente 00:03

### 05. CRUD con Spring API Rest - 16 Clases - 1 h 17 min

* Escribiendo los métodos del CRUD en la clase ClienteService del Backend 03:44
* Escribiendo los métodos show y create en el Controlador Backend API Rest 05:26
* Escribiendo los métodos update y delete en el Controlador Backend API Rest 05:37
* Probando nuestro Backend API Rest con Postman 06:41
* Actualización: Modificadores de acceso en las variables public y private. 00:36
* Creando el componente form.component y la vista del formulario 10:46
* Configurando la ruta y navegación del formulario 04:55
* Escribiendo implementación crear en el cliente.service.ts y en form.component.ts 06:00
* Actualización: nueva versión de SweetAlert2 8.0.1 o superior 00:35
* Instalar SweetAlert2 para enviar mensajes de alerta en el cliente 05:06
* Cargando los datos en el formulario para actualizar 06:28
* Escribiendo el update en el cliente.service.ts y en form.component.ts 07:02
* Escribiendo el delete en la clase service y en el componente clientes 07:37
* Overflow en listado de clientes, ajustando layout 03:16
* Validando los clientes en la tabla HTML con directiva ngIf 02:41
* Descargar Código Fuente 00:03

### 06. Manejo de Errores en Backend Spring - 4 Clases - 27 min

* Manejo de error en el Backend en método handler show (obtener por id) 09:33
* Manejo de error en el Backend en método handler create 08:34
* Manejo de error en el Backend en método handler update 05:13
* Manejo de error en el Backend en método handler delete 03:46

### 07. Manejo de Errores en FrontEnd(Angular) - 3 Clases - 21 min

* Manejo de error en el Frontend Angular en obtener por id 06:02
* Manejo de error en el Frontend Angular en create, update y delete 05:46
* Customizando y arreglando los textos de éxito en crear y actualizar del frontend 09:08

### 08. Validando form por el FrontEnd(Angular) - 1 Clases - 10 min

* Validando form en el template 10:17

### 09. Validando form por el BackEnd(Spring) - 7 Clases - 27 min

* Anotaciones JavaBeans Validation en la clase Entity 03:28
* Implementando anotación @Valid en métodos handler create y update del controller 08:50
* Probando validación API REST en POSTMAN 02:30
* Manejando los error de validación en Angular 05:09
* Agregando los mensajes de errores en la plantilla form 04:42
* Customizar mensajes de validación en español 02:40
* Descargar Código Fuente 00:03

### 10. Transformando datos Observable: usando operador map y Pipes - 5 Clases - 27 min

* Operador map formato uppercase en Observable 03:50
* Operador map formato fecha en Observable 03:32
* Registrando el Locale y los diferentes Pattern para formatear fechas 06:43
* Uso de Pipe para formatear fecha y uppercase en las plantillas html 04:02
* Uso del operador tap en el Observable 08:53

### 11. Paginación desde el Backend - 13 Clases - 1 h 10 min

* Implementando paginación en API REST y Repository 09:25
* Probar paginación API REST en POSTMAN 04:38
* Modificando el Observable de Clientes en el FrontEnd 06:35
* Agregando la ruta page del paginador y el Observable ActivatedRoute 06:55
* Creando el componente paginador 02:38
* Inyectar paginador usando decorador @Input en el componente Paginador 08:33
* Implementando los links de las páginas 05:13
* Implementando botones siguiente y atrás 04:10
* Implementando links para la primera y última página 03:53
* Paginador con muchas páginas: overflow 03:38
* Implementando rangos de páginas en el componente Paginador 10:12
* Afinando más el evento ngOnChanges para refrescar los rangos en el paginador 03:42
* Descargar Código Fuente 00:03

### 12. Añadiendo campo fecha en el formulario - 2 Clases - 19 min

* Añadiendo el campo para la fecha 06:34
* Añadiendo DatePicker de Angular Material 12:40

### 13. Subida de imagen (Upload) - 17 Clases - 2 h 9 min

* Upload en el API Rest Controller (Backend) 11:12
* Probar upload en POSTMAN y configurando el tamaño máximo de subida 06:26
* Borrar imagen anterior al actualizar 04:32
* Añadiendo método handler ver imagen en el Controlador 08:00
* Añadiendo Logger en back-end 02:34
* Añadiendo componente detalle para el upload en el front-end 09:11
* Implementando la subida de archivo en el front-end 10:48
* Añadiendo la foto y detalle del cliente en angular * 07:12
* Validando imagen antes de subir 05:52
* Añadiendo Barra de Progreso 10:23
* Implemementando Modal como componente anidado (hijo) 05:28
* Convertiendo a Modal de Bootstrap 09:00
* Añadiendo estilos y animación de difuminado al Modal 07:24
* Añadiendo la foto en el listado 10:12
* Implementando EventEmitter para actualizar la foto en el listado 07:07
* Creando la clase Service UploadFileService en el Backend para optimizar 13:14
* Descargar Código Fuente 00:03

### 14. Agregando campo en el formulario y relación de tablas - 8 Clases - 44 min

* Creando nueva clase entity Region 12:34
* Añadiendo las regiones en la clase service y controller del backend 03:16
* Probando API Rest de las regiones en Postman 05:14
* La clase TypeScript Region en Angular 06:14
* Añadiendo el campo select region en el formulario 05:01
* Comparando la región en el campo select para marcarla como seleccionada 09:02
* Añadiendo opción por defecto con el texto seleccionar 03:00
* Descargar Código Fuente 00:03

### 15. Autenticación OAuth2 con JWT: Backend Spring - 20 Clases - 2h 46 min

* Introducción a JSON Web Token (JWT) 10:29
* Algo más sobre los JWT 10:57
* Introducción a OAuth2 y añadiendo las dependencias 10:48
* Creando las entidades necesarias Usuario y Role 16:09
* Creando el repositorio JPA IUsuarioDao 05:37
* Creando la clase de servicio UsuarioService 11:07
* Añadiendo la clase SpringSecurityConfig y registrando UserDetailsService JPA 05:56
* Actualización Clase Nº 123: Configuración para el servidor de autorización 00:32
* Añadiendo la configuración para el servidor de autorización 10:52
* Añadiendo configuración de las aplicaciones clientes y acceso a endpoints 09:02
* Añadiendo la configuración para el servidor de recurso 07:06
* Probando la autenticación con Postman y obteniendo el token JWT 09:50
* Asignando la llave secreta Mac para firmar el token JWT 06:55
* Creando y asignando certificado RSA para firmar el token JWT 07:25
* Añadiendo más datos en el token JWT 09:52
* Complementando con más información adicional del usuario autenticado 05:03
* Agregando seguridad a nuestras rutas de forma programática con HttpSecurity 11:09
* Añadiendo seguridad a nuestras ruta del controlador usando anotaciones @Secured 05:36
* Configurando Cors en Spring Security 11:47
* Descargar Código Fuente 00:03

### 16. Autenticación OAuth2 con JWT: Frontend Angular - 20 Clases - 2h 8 min

* Demostración de lo que lograremos al finalizar esta sección de OAuth2 con JWT 02:10
* Creando componente login y formulario 08:28
* Manejo de error no autorizado y redirección al login 05:48
* Añadiendo el método login() en el componente y nueva clase Usuario 06:10
* Creando la clase de servicio AuthService y su método login() 08:21
* Implementando la autenticación en el componente login 09:18
* Guardando datos del usuario y token en el sessionStorage 12:53
* Manejando error de credenciales incorrectas en componente login 02:53
* Chequear en el componente login si el usuario ya ha iniciado sesión 05:56
* Añadiendo en el layout el links logout para cerrar la sesión 10:14
* Enviando token al backend para acceder a los recursos protegidos 07:52
* Manejando código de error 403 de Accedo Denegado o Prohibido (Forbidden) 03:06
* Ocultando botones en las plantillas según el role del usuario 05:54
* Cerrar sesión en angular cuando haya expirado el token en el backend 01:30
* Añadiendo seguridad en las rutas con Guard 06:20
* Crear Guard router RoleGuard 07:27
* Validando fecha de expiración del token en el AuthGuard 03:44
* HttpInterceptor para añadir el token en las cabeceras HTTP Authorization 10:37
* HttpInterceptor para códigos HTTP 401 y 403 09:28
* Descargar Código Fuente 00:03

### 17. Sistema de Facturación - 31 Clases - 3h 27 min

* Demostración de lo que lograremos al finalizar esta sección 03:13
* Análisis y Diseño OO con UML Diagrama de Clases del Dominio 13:30
* Asociaciones: ManyToOne Bidireccional - Clases Entity Factura y Cliente 10:33
* Asociaciones: OneToMany Unidireccional - Clases Entity Factura y ItemFactura 07:10
* Asociaciones: ManyToOne Unidireccional - Clases Entity ItemFactura y Producto 08:12
* Analizando y revisando las tablas y relaciones en MySQL Workbench 09:41
* Listando las facturas del Cliente en Postman 08:25
* Añadiendo las clases TypeScript Factura, ItemFactura y Producto en Angular 06:00
* Listando las facturas en el componente de detalle del Cliente 05:32
* Añadiendo CrudRepository para Factura e implementando métodos en el Service 04:19
* Creando controlador FacturaRestController con la acción handler show 05:06
* Creando Componente detalle de la factura y su clase Service relacionada 06:10
* Añadiendo el detalle de la Factura 07:50
* Añadiendo las Líneas y Observación en el detalle de la Factura 06:46
* Eliminando la factura y sus líneas (Backend) 01:35
* Eliminando la factura y sus líneas (Frontend) 06:56
* Creando el componente formulario de la factura 06:51
* Añadiendo campos al formulario factura 05:34
* Escribiendo código para el Autocomplete usando Angular Material 12:19
* Consulta JPA para buscar productos en el Autocomplete 11:31
* Modificando el autocomplete para que filtre los productos desde el Backend 13:21
* Creando las líneas de la Factura 06:59
* Actualizando la cantidad de un item de la factura 04:34
* Incrementando la cantidad si el producto existe en el detalle 04:57
* Eliminar linea de la factura 03:28
* Calculando el Gran Total de la Factura 04:36
* Implementando el crear factura 06:14
* Validando el formulario de la factura 06:56
* Reglas de Spring Security 05:06
* Solucionando un problema de recursión al editar el cliente 03:58
* Descargar Código Fuente 00:03

### 18. Deployment: despliegue en servidores de producción - 6 Clases - 33 min

* Modificando y preparando nuestros proyectos (backend y fronend) para producción 07:29
* Generando el jar y realizando el despliegue del Backend 04:50
* Transpilando nuestra aplicación angular y preparandonos para el despliegue 05:15
* Realizando el despliegue del frontend Angular en servidor Apache 24 (httpd) 07:17
* Realizando el despliegue de nuestra app angular con NodeJS y Express 07:38
* Descargar Código Fuente 00:03

### 19. Deployment: despliegue en servidores en la nube Heroku y Google Firebase Hosting - 4 Clases - 30 min

* Creando app en Heroku 06:54
* Deploy Backend Spring en Heroku 12:16
* Deploy Frontend Angular en Firebase Hosting 10:17
* Descargar Código Fuente 00:03

### 20. Sistema de Chat: en tiempo real con WebSocket - 20 Clases - 2h 17 min

* Demostración visual de lo que lograremos al finalizar la sección 02:04
* Introducción a la tecnología WebSocket 07:24
* ¿Qué es el Protocolo Stomp y cómo se relaciona con WebSocket? 09:41
* Actualización: Nueva ubicación dependencia WebSocket al crear el proyecto 00:15
* Creando el proyecto backend y configurando el servidor WebSocket (el Broker) 09:56
* Creando el controlador ChatController y el Mensaje 07:41
* Creando el proyecto frontend Angular 08:32
* Instalando librerías para el cliente WebSocket en Angular (sockjs y stompjs) 07:54
* Maquetando y escribiendo el contenido HTML para el chat 05:44
* Implementando el conectar y desconectar del servidor WebSocket 04:29
* Implementando el enviar y recibir mensajes del Chat 10:46
* Notificar cuando un nuevo usuario se conecta al chat 08:58
* Dando un color al username cuando se conecta al servidor 06:38
* Notificar cuando un usuario está escribiendo 07:40
* Instalación Mongo DB 03:32
* Qué es Mongo y algunos ejemplos 07:18
* Instalando Robo 3T una herramienta GUI para MongoDB 02:30
* Agregando Clases del Modelo Document y Repository 11:00
* Historial de mensajes del chat con MongoDB 14:42
* Descargar Código Fuente 00:03

### 21. Fin del Curso - 1 Clases - 1 min

* Agradecimientos y despedida 00:56
