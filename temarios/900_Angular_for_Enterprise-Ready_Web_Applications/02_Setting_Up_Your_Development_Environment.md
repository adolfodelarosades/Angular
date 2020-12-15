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



### Git and GitHub Desktop
#### Why use GitHub?
#### Why use GitHub Desktop?
#### Installing Git and GitHub Desktop
#### Using your GitHub credentials in Git
### Node.js
### Existing Node.js installation
### Installing Node.js
#### Global npm packages
### Visual Studio Code
#### Installing Visual Studio Code
### Docker
#### Installing Docker
### Cloud services
#### Vercel Now
#### Google Firebase
#### Google Cloud
#### Amazon Web Services
## Setup automation for Windows and macOS
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

![02-03](images/02-03.png)
![02-04](images/02-04.png)
![02-05](images/02-05.png)
![02-06](images/02-06.png)
![02-07](images/02-07.png)
