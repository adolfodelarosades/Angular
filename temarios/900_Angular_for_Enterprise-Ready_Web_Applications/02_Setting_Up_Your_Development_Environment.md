# 02. Setting Up Your Development Environment
* CLI package managers
   * Installing Chocolatey for Windows
   * Installing Homebrew for macOS
* Installing development tools
   * Git and GitHub Desktop
      * Why use GitHub?
      * Why use GitHub Desktop?
      * Installing Git and GitHub Desktop
      * Using your GitHub credentials in Git
   * Node.js
   * Existing Node.js installation
   * Installing Node.js
      * Global npm packages
   * Visual Studio Code
      * Installing Visual Studio Code
   * Docker
      * Installing Docker
   * Cloud services
      * Vercel Now
      * Google Firebase
      * Google Cloud
      * Amazon Web Services
* Setup automation for Windows and macOS
   * PowerShell script
   * Bash script
* The Angular CLI
   * Setting up your development directory
   * Generating your Angular application
      * Installing the Angular CLI
      * Initializing your Angular app
      * Publishing a Git repository using GitHub Desktop
      * Inspecting and updating package.json
      * Committing code using VS Code
   * Running your Angular app
   * Verifying your code
* Optimizing VS Code for Angular
   * Configuring your project automatically
      * VS Code auto save
      * IDE settings
      * IDE extensions
   * Scripting code styling and linting
      * Configuring tooling
      * Implementing a style checker and fixer
      * Implementing a lint checker and fixer
   * Configuring Angular CLI autocomplete
   * VS Code Auto Fixer
* Summary
* Further reading
* Questions

# 02. Configuración de su Entorno de Desarrollo

Este capítulo demuestra cómo usted y los miembros de su equipo pueden crear un entorno de desarrollo coherente para que todo su equipo tenga la misma gran experiencia de desarrollo web, cuya importancia se destaca en el prefacio del libro. Puede ser difícil para los principiantes crear el entorno de desarrollo adecuado, que es esencial para una experiencia de desarrollo sin frustraciones. Para los desarrolladores y equipos experimentados, lograr un entorno de desarrollo mínimo y consistente sigue siendo un desafío. Una vez logrado, dicho entorno de desarrollo ayuda a evitar muchos problemas relacionados con la TI, incluidos los costos continuos de mantenimiento, licencias y actualización.

Las instrucciones sobre la instalación de GitHub Desktop, Node.js, Angular CLI y Docker son una referencia útil para aquellos desde principiantes absolutos hasta equipos experimentados, junto con estrategias sobre cómo automatizar y garantizar la configuración correcta y consistente de su entorno de desarrollo.

> :blue_book: No dude en omitir este capítulo si ya tiene configurado un entorno de desarrollo sólido; sin embargo, tenga en cuenta que algunas de las suposiciones medioambientales declaradas en este capítulo pueden hacer que algunas instrucciones no le funcionen en capítulos posteriores. Vuelva a este capítulo como referencia si tiene problemas o necesita ayudar a un colega, alumno o amigo a configurar su entorno de desarrollo. Los scripts de instalación automatizados para configurar su entorno de desarrollo se pueden encontrar en https://github.com/duluca/web-dev-environment-setup.

Para aprovechar al máximo este libro, debe estar familiarizado con JavaScript ES2015+, los conceptos básicos del desarrollo de frontend y las API RESTful.

Los sistemas operativos recomendados son Windows 10 Pro v1903+ con PowerShell v7+ o macOS Sierra v10.15+ con Terminal (Bash o Oh My Zsh). La mayor parte del software sugerido en este libro también funciona en sistemas Linux, pero su experiencia puede variar según su configuración particular.

> :high_brightness: *Es una práctica estándar que los desarrolladores utilicen Google Chrome 80+ al desarrollar aplicaciones web. Sin embargo, también puede utilizar el navegador Microsoft Edge 80+ basado en Chromium. Definitivamente debería instalar PowerShell multiplataforma en Windows desde https://github.com/PowerShell/PowerShell/releases, que le da acceso a los operadores de cadena `&&` y `||`. Además, obtenga la nueva Terminal de Windows en Microsoft Store para una experiencia superior de línea de comandos en Windows.*

En este capítulo, aprenderá a hacer lo siguiente:

* Trabaje con los administradores de paquetes CLI Chocolatey y Homebrew para instalar y actualizar software
* Use esos administradores de paquetes para instalar GitHub, Node.js y otros programas esenciales
* Utilice secuencias de comandos para automatizar la instalación mediante PowerShell o Bash
* Genere una aplicación Angular usando la CLI Angular
* Consiga un entorno de desarrollo coherente y multiplataforma utilizando herramientas automatizadas

Comencemos por aprender acerca de los administradores de paquetes basados en CLI que puede usar para instalar sus herramientas de desarrollo. En la siguiente sección, verá que usar herramientas CLI es un método superior en comparación con tratar con instaladores individuales. Es mucho más fácil automatizar las herramientas CLI, lo que hace que las tareas de configuración y mantenimiento sean repetibles y rápidas.

## CLI package managers (Administradores de paquetes CLI)

La instalación de software a través de una **Graphical User Interface (GUI)** es lenta y difícil de automatizar. Como desarrollador full-stack, ya sea que sea un usuario de Windows o Mac, debe confiar en los administradores de paquetes de la interfaz de línea de comandos (CLI) para instalar y configurar de manera eficiente el software del que depende.

> :high_brightness: *Recuerde, cualquier cosa que pueda expresarse como un comando CLI también puede automatizarse.*

### Instalación de Chocolatey  para Windows
Chocolatey es un administrador de paquetes basado en CLI para Windows que se puede utilizar para la instalación automatizada de software. Para instalar Chocolatey en Windows, debe ejecutar un shell de comandos elevado:

1. Inicie el menú **Start**
2. Empiece a escribir en `PowerShell`
3. Debería ver la aplicación de escritorio **Windows PowerShell Desktop App** como resultado de la búsqueda
4. Haga clic con el botón derecho en **Windows PowerShell** y seleccione **Run as Administrator**
5. Esto dispara una advertencia de **User Account Control (UAC)** (Control de cuentas de usuario (UAC)); seleccione **Yes** para continuar
6. Ejecute el comando de instalación que se encuentra en https://chocolatey.org/install en **PowerShell** para instalar el administrador de paquetes de Chocolatey:

```sh
PS> Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

7. Verifique su instalación de Chocolatey ejecutando `choco`
8. Debería ver una salida similar a la que se muestra en la siguiente captura de pantalla:

![02-01](images/02-01.png)

> :high_brightness: *Todos los comandos de Chocolatey posteriores también deben ejecutarse desde un shell de comandos elevado. Alternativamente, es posible instalar Chocolatey en una configuración que no sea de administrador y que no requiera un shell de comandos elevado. Sin embargo, esto da como resultado un entorno de desarrollo no estándar y menos seguro, y es posible que ciertas aplicaciones instaladas a través de la herramienta aún requieran elevación.*

> :blue_book: *Scoop es una alternativa a Chocolatey que proporciona una experiencia más similar a Unix. Si prefiere las herramientas y los comandos de estilo Unix, puede instalar Scoop en https://scoop.sh/ o ejecutando:*

```sh
$ iwr -useb get.scoop.sh | iex
```

Para obtener más información sobre Chocolatey, consulte https://chocolatey.org/install.

### Instalación de Homebrew para macOS

Homebrew es un administrador de paquetes basado en CLI para macOS que se puede utilizar para la instalación automatizada de software. Para instalar Homebrew en macOS, debe ejecutar un shell de comandos:

1. Inicie la búsqueda de Spotlight con  Gato + Space
2. Escriba `terminal`
3. Ejecute el siguiente comando en la Terminal para instalar el administrador de paquetes Homebrew:

```sh
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

4. Verifique su instalación de Homebrew ejecutando `brew`
5. Debería ver un resultado similar al siguiente:

![02-02](images/02-02.png)

6. Para habilitar el acceso a software adicional, ejecute el siguiente comando:

```sh
$ brew tap caskroom/cask
```

En macOS, si tiene problemas de permisos al instalar paquetes brew, relacionados con chown'ing `/usr/local`, debe ejecutar el comando `sudo chown -R $(whoami) $(brew --prefix)/*`. Este comando restablece la propiedad a nivel de usuario para preparar paquetes, que es más seguro que el acceso amplio a nivel de superusuario.

> :blue_book: *Para obtener más información, consulte https://brew.sh/.*

## Instalación de Herramientas de Desarrollo

En esta sección, instalará todas las herramientas de desarrollo que necesita para comenzar a desarrollar una aplicación web. ***Git*** y ***GitHub Desktop*** establecen un repositorio de código fuente en su máquina y le permiten sincronizar su código con un repositorio remoto. ***Node.js*** es un JavaScript runtime para su PC e incluye **Node Package Manager** o **npm** que gestiona el código fuente de terceros, incluido Angular. ***Visual Studio Code*** es un entorno de desarrollo integrado o IDE.

> :blue_book: *Para instalar automáticamente todas las herramientas de desarrollo web necesarias para este libro, ejecute los siguientes comandos para que su sistema operativo configure su entorno. En Windows PowerShell, ejecute:*

```sh
PS> Install-Script -Name setup-windows-dev-env
PS> setup-windows-dev-env.ps1
```
> *En MacOS Terminal, ejecute:*
```sh
$> bash <(wget -O - https://git.io/JvHi1)
```
> *Para más información refierase a https://github.com/duluca/web-dev-environment-setup.*

Una vez que instale su IDE, estará listo para comenzar el desarrollo. Esta sección también contiene instrucciones para instalar Docker, una plataforma de contenedorización liviana, y configurar varios servicios en la nube. Estas herramientas serán relevantes en capítulos posteriores. Si desea un comienzo más rápido para su aventura Angular, puede omitirlos por ahora.

### Git y GitHub Desktop

Esta sección tiene como objetivo establecer una configuración de Git de mejores prácticas que sea adecuada para la audiencia más amplia posible. Para hacer el mejor uso de esta sección y los capítulos posteriores de este libro, supongo que cumple con los siguientes requisitos previos:

* Comprensión de lo que realmente son la gestión de código fuente y Git
* Una cuenta gratuita creada en GitHub.com

#### ¿POR QUÉ USAR GITHUB?

Si eres un usuario de Git, es probable que también uses un repositorio en línea, como ***GitHub, Bitbucket o GitLab***. Cada repositorio tiene un nivel gratuito para proyectos de código abierto, junto con sitios web sólidos con diferentes conjuntos de funciones, incluidas las opciones empresariales en las instalaciones por las que puede pagar. GitHub, con más de 38 millones de repositorios alojados en 2016, es, con mucho, el repositorio en línea más popular. En general, se considera una utilidad básica que la comunidad nunca deja de estar fuera de línea.

Con el tiempo, GitHub ha agregado muchas características que lo han transformado de un mero repositorio a una plataforma en línea. A lo largo de este libro, haré referencia a las características y funcionalidades de GitHub para que pueda aprovechar sus capacidades para transformar la forma en que desarrolla, mantiene y lanza software.



#### ¿POR QUÉ USAR GITHUB DESKTOP?

La herramienta Git CLI es realmente poderosa, y estará bien si se apega a ella. Sin embargo, los desarrolladores full-stack estamos preocupados por una variedad de preocupaciones. Con prisa por completar la tarea en cuestión, puede arruinar fácilmente su día, y en ocasiones el de su equipo, si sigue un consejo incorrecto o incompleto.

Consulte la siguiente captura de pantalla para ver un ejemplo de dichos consejos de Stack Overflow (http://stackoverflow.com/questions/1125968/force-git-to-overwrite-local-files-on-pull):

![02-03](images/02-03.png)

Si ejecuta el comando anterior, esté preparado para perder los cambios locales no confirmados. Desafortunadamente, los usuarios novatos tienden a seguir las instrucciones más sencillas y directas, lo que puede provocar la pérdida de trabajo. Si cree que sus compromisos anteriores son seguros, ¡piénselo dos veces! Cuando se trata de Git, si puede imaginarlo, puede hacerlo a través de la CLI.

Afortunadamente, con GitHub, puede proteger las ramas e implementar el flujo de trabajo de GitHub, lo que implica ramificar, confirmar, fusionar, actualizar y enviar solicitudes de extracción. Las protecciones y el flujo de trabajo ayudan a evitar que los comandos de Git dañinos realicen cambios irreversibles y permiten un nivel de control de calidad para que su equipo siga siendo productivo. Realizar todas estas acciones a través de la CLI, especialmente cuando hay conflictos de fusión, puede resultar complicado y tedioso.

> :high_brightness: *Tenga en cuenta que Git se envía con una herramienta CLI llamada Git Bash, que es un shell basado en Unix que puede usar para ejecutar git y otros comandos. Bash está disponible en computadoras Linux y macOS. Windows 10 está mejorando rápidamente su soporte de terminal con el Subsistema de Windows para Linux (WSL) y alias para comandos Unix en PowerShell, por lo que la necesidad de usar Git Bash en Windows está desapareciendo rápidamente. Si desea obtener más información sobre Git Bash, consulte el tutorial en el sitio web de Atlassian en https://www.atlassian.com/git/tutorials/git-bash.*

Para una comprensión más profunda de los beneficios y las trampas de Git y GitHub, puede leer mi artículo de 2016 sobre el tema en Bit.ly/InDepthGitHub.

#### INSTALACIÓN DE GIT Y GITHUB DESKTOP

GitHub Desktop proporciona una GUI fácil de usar para ejecutar el flujo de trabajo de GitHub de forma coherente en Windows y macOS. La coherencia es muy valiosa al incorporar miembros nuevos o jóvenes al equipo, o si no es un colaborador frecuente de la base de código. Le recomendamos que instale GitHub Desktop 2.2+.

1. Ejecute el comando de instalación:

Para Windows:

```sh
PS> choco install git github-desktop -y
```

Para macOS:

```sh
$ brew install git && brew cask install github
```

2. Verifique su instalación de Git ejecutando `git --version` y observe el número de versión devuelto

> :high_brightness: *Debe reiniciar su Terminal después de la instalación de una nueva herramienta CLI. Sin embargo, puede evitar reiniciar su Terminal y ahorrar algo de tiempo al actualizar o obtener sus variables de entorno. En Windows, ejecute `refreshenv`; en macOS, ejecute `source ~/.bashrc` o `source ~/.zshrc`.

3. Verifique su instalación de GitHub Desktop iniciando la aplicación
4. Inicie sesión en https://github.com/ en GitHub Desktop
5. Una vez que haya creado un repositorio, puede iniciar la aplicación desde su Terminal ejecutando esto:

```sh
$ github path/to/repo
```
6. Si ya se encuentra en la carpeta correcta, puede escribir el siguiente comando en su lugar:

```sh
$ github .
```

Para Windows, en el inicio de GitHub Desktop, si se queda atascado en la pantalla de inicio de sesión, cierre la aplicación, vuelva a iniciarla como administrador, complete la configuración y luego podrá usarla normalmente, sin tener que volver a iniciarla como administrador. Para obtener más información, consulte https://desktop.github.com/.

A continuación, repasaremos varias estrategias para tener una experiencia más fluida con Git al registrar correctamente sus credenciales de GitHub.


#### USANDO SUS CREDENCIALES DE GITHUB EN GIT

Cuando interactúas con tu repositorio en GitHub, el comando git es aprovechado por las herramientas que estás usando, como tu IDE, para push o pull contenido. Para tener una experiencia fluida con Git, es una buena idea registrar sus credenciales de GitHub con Git correctamente.

Hay tres estrategias principales para lograr esto:

1. **Configure SSH**, que es la mejor y más segura forma de interactuar con cualquier sistema informático remoto, porque no se intercambian contraseñas. Puede seguir la guía más reciente de GitHub para configurar SSH en https://help.github.com/articles/connecting-to-github-with-ssh.

2. **Cache your GitHub password in Git**(Almacene en caché su contraseña de GitHub en Git); a veces, SSH no será compatible con la herramienta que usa, por lo que es posible que deba almacenar en caché su contraseña. Puede hacerlo ejecutando el siguiente comando:

Para Windows:

```sh
PS> git config --global credential.helper wincred
```

Para macOS:

```sh
$ git credential-osxkeychain
$ git config --global credential.helper osxkeychain
```

Para obtener más orientación, consulte la guía de GitHub en https://help.github.com/articles/caching-your-github-password-in-git.

3. **Crear un personal access token**: esta es una estrategia que se ubica entre SSH y el uso de contraseñas desde una perspectiva de seguridad porque las claves SSH y los tokens se pueden revocar en cualquier momento desde GitHub, pero una vez que su contraseña se filtra o se ve comprometida, puede perder el control de todo.

Si está utilizando autenticación de dos factores, que es absolutamente necesario, entonces, en lugar de almacenar en caché su contraseña, debe crear un token de acceso personal en https://github.com/settings/tokens y usar el token en lugar de su contraseña . En el Capítulo 3, Creación de una aplicación angular básica, cubrimos cómo puede configurar un token para que funcione con Visual Studio Code, el IDE preferido para este libro.

> :blue_book: *Consulte la herramienta git-extras de TJ Holowaychuk, que puede proporcionar un resumen del repositorio, la población del registro de cambios, el porcentaje de confirmación del autor y más información útil sobre sus repositorios en https://github.com/tj/git-extras.*

### Node.js

Esta sección tiene como objetivo establecer un entorno de desarrollo de JavaScript de mejores prácticas. Supongo que tiene conocimiento del ecosistema y las herramientas modernas de JavaScript. Como mínimo, asegúrese de familiarizarse con los siguientes recursos:

* Sitio web de Node.js: https://nodejs.org
* Sitio web de Npm: https://www.npmjs.com
* Sitio web de Angular: https://angular.io
* El sitio web heredado de AngularJS: https://angularjs.org/
* Sitio web de Yarn: https://yarnpkg.com
* Sitio web de React: https://facebook.github.io/react

Node.js es JavaScript que se ejecuta en cualquier lugar. Es un proyecto de código abierto que tiene como objetivo ejecutar JavaScript en el servidor, construido sobre el motor JavaScript V8 de Google Chrome. A finales de 2015, Node.js estabilizó y anunció ciclos LTS de 18 meses para empresas que aportaron previsibilidad y estabilidad a la plataforma, junto con una última rama actualizada con mayor frecuencia, pero más experimental.

Node también se incluye con npm, el Node Package Manager, y a partir de 2018, ***npm es el repositorio de paquetes JavaScript más grande del mundo***.

Para obtener una visión más detallada del historial de Node, lea mi artículo de dos partes sobre Node en Bit.ly/NodeJSHistory.

> :blue_book: *Es posible que haya oído hablar de Yarn y de que es más rápido o mejor que npm. A partir de npm 5, que se envía con el Nodo 8, npm tiene más funciones, es más fácil de usar y está a la par con Yarn en términos de rendimiento. Yarn es una publicación de Facebook, que también creó React. Debe tenerse en cuenta que Yarn se basa en el repositorio npm, por lo que sea cual sea la herramienta que use, obtendrá acceso a la misma biblioteca de paquetes.*

### Instalación existente de Node.js

Si ha instalado Node.js antes, cuando instale una nueva versión de Node usando choco o brew, asegúrese de leer los resultados del comando con atención. Su administrador de paquetes puede devolver advertencias o instrucciones adicionales a seguir para que pueda completar con éxito la instalación.

También es muy probable que los permisos de su sistema o carpeta se hayan editado manualmente en el pasado, lo que puede interferir con el funcionamiento sin frustraciones de Node. Si los siguientes comandos no resuelven sus problemas, use el instalador de GUI del sitio web de Node como último recurso.

> :high_brightness: *Para ver una lista de sus paquetes de instalación globales, ejecute `npm list -g --depth=0`. Para desinstalar un paquete global, ejecute `npm uninstall -g package-name`. Le recomendaría que desinstale todos los paquetes instalados globalmente y reinicie desde cero con las sugerencias que se proporcionan en la siguiente sección.*

Independientemente, debe tener cuidado de desinstalar todas las herramientas globales que se instalaron con `npm -g` anteriormente. Con todas las versiones principales de Node, existe la posibilidad de que se hayan invalidado los enlaces nativos entre su herramienta y Node. Además, las herramientas globales quedan obsoletas rápidamente y las herramientas específicas del proyecto se desincronizan rápidamente. Como resultado, la instalación de herramientas globalmente es ahora un anti-patrón que ha sido reemplazado con mejores técnicas, que se tratan en la siguiente sección y en la sección CLI angular en el Capítulo 3, Creación de una aplicación angular básica.


### Instalación de Node.js

Este libro asume que está usando Node 12.13 o una versión posterior. Las versiones impares de Node no están diseñadas para ser de larga duración. 8.x.x, 10.x.x, 12.x.x, etc. están bien, pero evite 9.x.x, 11.x.x, etc., a toda costa, ya que están destinados a ser experimentales.

1. Ejecute el comando de instalación:
   Para Windows:

```sh
PS> choco install nodejs-lts -y
```

Para macOS:

```sh
$ brew install node@10
```

2. Verifique la instalación de Node ejecutando `node -v`
3. Verifique npm ejecutando `npm -v`

> :blue_book: *Tenga en cuenta que en Windows, nunca debe actualizar su versión de npm usando `npm install -g npm`, como se destaca en el Apéndice C, Manteniendo Angular y Herramientas Evergreen. Puede encontrar este apéndice en línea en https://static.packt-cdn.com/downloads/9781838648800_Appendix_C_Keeping_Angular_and_Tools_Evergreen.pdf o en https://expertlysimple.io/stay-evergreen. Se recomienda encarecidamente que utilice el paquete npm-windows-upgrade npm.

Para este libro, asegúrese de tener npm v.6.12 +. Ahora, repasemos algunos paquetes prácticos de npm que quizás desee instalar globalmente.
   
#### PAQUETES GLOBALES DE NPM

El repositorio npm contiene numerosos comandos CLI útiles y maduros que a menudo son multiplataforma. A continuación se enumeran los en los que confío con frecuencia y elijo instalarlo globalmente por razones de rendimiento:

* `npx`: Ejecuta las herramientas CLI descargando la última versión bajo demanda o la carpeta `node_modules` local específica del proyecto. Npx se envía con npm 5+ y le permite ejecutar generadores de código que se actualizan con frecuencia sin una instalación global.

* `rimraf`: El comando de Unix `rm -rf` también funciona en Windows. Es muy útil para eliminar la carpeta `node_modules`, especialmente cuando Windows no puede hacerlo debido a la estructura de carpetas anidadas.

* `npm-check-updates`: Analiza la carpeta de tu proyecto e informa sobre qué paquete tiene versiones más nuevas o no, con la opción de poder actualizarlas todas si así lo deseas. `ncu` para abreviar.

* `n`: Una herramienta muy fácil de usar para cambiar entre versiones de Node rápidamente, sin tener que recordar el número de versión específico, que funciona en macOS/Linux. Para Windows, puede usar el paquete choco, `nvs`; tanto `n` como `nvs` se tratan en el Apéndice C, Manteniendo Angular y Tools Evergreen.

* `n`: Una herramienta muy fácil de usar para cambiar entre versiones de Node rápidamente, sin tener que recordar el número de versión específico, que funciona en macOS/Linux. Para Windows, puede usar el paquete choco, `nvs`; tanto `n` como `nvs` se tratan en el Apéndice C, Manteniendo Angular y Tools Evergreen.

* `http-server`: un servidor HTTP de línea de comandos simple, sin configuración, que es una excelente manera de probar localmente páginas HTML/CSS estáticas o incluso la carpeta `dist` de su proyecto Angular o React.

* `npm-windows-upgrade`: necesario para actualizar npm en Windows.

* `npkill`: encuentre y elimine fácilmente carpetas de `node_modules` viejas y pesadas y recupere gigabytes de espacio en disco.

> :high_brightness: *Puede usar npm-check-updates para mantener actualizados todos sus paquetes globales ejecutando `ncu -g`.*

Si se encuentra con errores de permisos EACCES al instalar paquetes globales en macOS, consulte la guía de npm en https://docs.npmjs.com/getting-started/fixing-npm-permissions.


   
### Visual Studio Code

**Visual Studio Code (VS Code)** es uno de los mejores editores de código/IDE que existen, creado y mantenido por Microsoft. Es gratuito y multiplataforma. Lo notable es que VS Code tiene el rendimiento ultrarrápido de un editor de código, piense en NotePad ++ o Sublime Text, pero el conjunto de características y la conveniencia de los IDE costosos, piense en Visual Studio o WebStorm. Para el desarrollo de JavaScript, esta velocidad es esencial y es una tremenda mejora en la calidad de vida para un desarrollador que cambia con frecuencia entre diferentes proyectos. VS Code reúne un terminal integrado, un sistema de extensión fácil de usar, configuraciones transparentes, excelentes funcionalidades de búsqueda y reemplazo y, en mi opinión, el mejor depurador de Node.js que existe.

> :high_brightness: *Este libro no requiere que use VS Code. Si desea utilizar otro IDE como WebStorm, puede hacerlo. WebStorm es un producto pago y ofrece una gran experiencia de desarrollo lista para usar, mientras que VS Code requiere mucha personalización. Este libro ofrece scripts automatizados para configurar VS Code para una experiencia de desarrollo angular óptima.*

> *Puede encontrar más información sobre WebStorm en https://www.jetbrains.com/webstorm.*

#### INSTALACIÓN DEL CÓDIGO DE ESTUDIO VISUAL

Para el desarrollo angular, este libro aprovecha VS Code v1.42 +. Le recomiendo que también use la última versión de VS Code.

1. Ejecute el comando de instalación:

Para Windows:

```sh
PS> choco install VisualStudioCode -y
```

Para macOS:

```sh
$ brew cask install visual-studio-code
```

> :high_brightness: *Una de las mejores características de VS Code es que también puede iniciarlo desde la CLI. Si está en una carpeta que le gustaría editar, simplemente ejecute `code .` o un archivo en particular ejecutando el `code ~/.bashrc` o `code readme.md`.

2. Verifique la instalación iniciando VS Code
3. Navegue a una carpeta y ejecute `code`
4. Esto abre una nueva ventana de Código VS con el **Explorador** mostrando el contenido de la carpeta actual

Para obtener más información, consulte https://code.visualstudio.com.

> :high_brightness: *Con VS Code instalado, está listo para comenzar el desarrollo. Si desea un comienzo más rápido para su aventura Angular, salte a la sección CLI de Angular y consulte esta sección cuando necesite Docker y las herramientas para varios servicios en la nube.*

### Docker

Docker es una plataforma de virtualización de contenedores liviana con flujos de trabajo y herramientas que ayudan a administrar e implementar aplicaciones.


#### INSTALACIÓN DE DOCKER

Para poder construir y ejecutar contenedores, primero debe instalar el entorno de ejecución de Docker en su computadora.

El soporte de Windows para Docker puede ser un desafío. Debe tener una PC con una CPU que admita extensiones de virtualización, lo cual no es una garantía en las computadoras portátiles. También debe tener una versión Pro de Windows con Hyper-V habilitado. Por otro lado, Windows Server tiene soporte nativo para Docker, que es una cantidad sin precedentes de soporte mostrado por Microsoft hacia la iniciativa de la industria para adoptar Docker y la contenedorización.

1. Instale Docker ejecutando el siguiente comando:
Para Windows:

```sh
PS> choco install docker docker-for-windows -y
```

Para macOS:

```sh
$ brew install docker
```

Ejecute `docker -v` para verificar la instalación




### Cloud services

A lo largo del libro, usaremos varios proveedores de nube para realizar implementaciones de las aplicaciones que va a crear. Cada servicio se envía con una herramienta CLI que facilita la implementación de su aplicación desde su Terminal o un **entorno de integración continua (CI) - continuous integration (CI) ** en la nube.

#### VERCEL AHORA

***Vercel Now*** es una plataforma en la nube para sitios estáticos y funciones sin servidor. Con un simple comando CLI, puede alojar sitios web e implementar servicios web al instante. Este libro aprovecha una cuenta Vercel Now de nivel gratuito.

1. Cree una cuenta de Vercel Now en https://vercel.com.
2. Instale la herramienta CLI ejecutando:

```sh
$ npm i -g now
```

3. Verifique la instalación ejecutando:

```sh
$ now login
```

4. Siga las instrucciones para completar el proceso de inicio de sesión. Debería ver un mensaje similar al siguiente:

```sh
> We sent an email to xxxxx@gmail.com. Please follow the steps provided inside it and make sure the security code matches Classical Slow Worm
√ Email confirmed
> Congratulations! You are now logged in. In order to deploy something, run `now`
```

Para obtener más información, consulte https://vercel.com.


#### Google Firebase

Firebase es la plataforma en la nube de Google diseñada para alojar aplicaciones móviles y web con autenticación, notificaciones push, funciones en la nube, bases de datos, aprendizaje automático y soporte de análisis. Este libro aprovecha una cuenta de Firebase de nivel gratuito.

1. Cree una cuenta de Firebase en https://firebase.google.com/.
2. Instale la herramienta CLI ejecutando:

```sh
$ npm i -g firebase-tools
```
3. Verifique la instalación ejecutando:

```sh
$ firebase login
```

4. Siga las instrucciones para completar el proceso de inicio de sesión. Debería ver un mensaje similar al siguiente:

```sh
Waiting for authentication...
+  Success! Logged in as xxxxxx@gmail.com
```

Para obtener más información, consulte https://firebase.google.com/.



#### Google Cloud

Google Cloud es la infraestructura de nube de clase mundial de Google para empresas. Este libro aprovecha Google Cloud Run para implementaciones administradas de contenedores en la nube. Cuando se registra por primera vez, puede recibir créditos gratuitos para usar Google Cloud. Sin embargo, este es un ejercicio opcional, ya que puede incurrir en cargos por utilizar este servicio si se olvida de down su implementación.

1. Cree una cuenta de Google Cloud en https://cloud.google.com/
2. Ejecute el comando de instalación:

Para Windows:

```sh
PS> choco install gcloudsdk -y
```

> :high_brightness: *Si tiene problemas para instalar `gcloudsdk` desde choco, pruebe `scoop`, como se mencionó anteriormente en el capítulo. Ejecute los comandos que siguen:*

```sh
$ scoop bucket add extras
$ scoop install gcloud
```

Para macOS:

```sh
$ brew install google-cloud-sdk
```

3. Verifica la instalación ejecutando `gcloud --version`
4. Ejecute `gcloud init` para finalizar la configuración

Para obtener más información, consulte https://cloud.google.com/run/.

#### Amazon Web Services

**Amazon Web Services (AWS)** es una infraestructura de nube implementada globalmente proporcionada por Amazon. AWS es una herramienta muy popular entre empresas y gobiernos, lo que la convierte en un servicio lucrativo para los profesionales de TI. El Capítulo 13, Infraestructura en la nube de alta disponibilidad en AWS, profundiza en cómo trabajar con AWS y realizar una implementación escalable basada en contenedores.

1. Ejecute el comando de instalación:
Para windows:


```sh
PS> choco upgrade awscli -y
```

Para macOS:

```sh
$ brew install awscli
$ brew upgrade awscli
```

> :high_brightness: *Tenga en cuenta que ejecutar el comando de actualización en choco y brew garantiza que tenga la última versión de cualquier herramienta dada si se instalaron previamente en su entorno.*

2. Verifique la instalación ejecutando `aws --version`

ara obtener más información, consulte https://aws.amazon.com/.

## Setup automation for Windows and macOS
AQUIIIIIIII
### PowerShell script
### Bash script
## The Angular CLI
### Setting up your development directory
### Generating your Angular application
#### Installing the Angular CLI
#### Initializing your Angular app
#### Publishing a Git repository using GitHub Desktop
#### Inspecting and updating package.json
#### Committing code using VS Code
### Running your Angular app
### Verifying your code
## Optimizing VS Code for Angular
### Configuring your project automatically
#### VS Code auto save
#### IDE settings
#### IDE extensions
### Scripting code styling and linting
#### Configuring tooling
#### Implementing a style checker and fixer
#### Implementing a lint checker and fixer
### Configuring Angular CLI autocomplete
### VS Code Auto Fixer
## Summary
## Further reading
## Questions

![02-04](images/02-04.png)
![02-05](images/02-05.png)
![02-06](images/02-06.png)
![02-07](images/02-07.png)
