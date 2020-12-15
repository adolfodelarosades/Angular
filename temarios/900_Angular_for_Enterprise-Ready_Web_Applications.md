# 900 Angular for Enterprise-Ready Web Applications

### Descripción del libro

**Segunda edición revisada y actualizada de la guía práctica más vendida para crear aplicaciones web listas para la empresa utilizando una plataforma Angular imperecedera**

#### Características clave

* Ejemplos actualizados, proyectos y una nueva descripción general de las herramientas, que incluyen NgRX e Ivy, pruebas automatizadas y autenticación de Firebase.
* Nuevo capítulo que resume la historia de los frameworks web y las actualizaciones de la versión Angular
* Implementación de API RESTful completamente nueva que aprovecha la pila MEAN con MongoDB, Express.js, Angular y Node.js

#### Descripción del libro

Esta segunda edición de Angular para aplicaciones web listas para empresas se actualiza con una cobertura en profundidad de la plataforma Angular siempre verde.

Comenzará por dominar los fundamentos de la programación angular. Con el método Kanban y las herramientas de GitHub, creará aplicaciones de gran apariencia con Angular Material y también aprovechará los patrones de programación reactiva con RxJS, descubrirá el patrón de flujo con NgRx, se familiarizará con las pruebas automatizadas, utilizará la integración continua con CircleCI e implementará su aplicación a la nube usando Vercel Now y GCloud.

Luego, aprenderá cómo diseñar y desarrollar aplicaciones de línea de negocio utilizando una arquitectura de enrutador primero con anclajes de datos observables, demostrados a través de recetas de uso frecuente como vistas maestras / detalladas y tablas de datos con paginación y formularios. A continuación, descubrirá un diseño sólido de autenticación y autorización demostrado a través de la integración con Firebase, la documentación de la API con Swagger y la implementación de la API con la pila MEAN.

Finalmente, aprenderá sobre DevOps usando Docker, creará una infraestructura en la nube de alta disponibilidad en AWS, capturará el comportamiento del usuario con Google Analytics y realizará pruebas de carga. Al final del libro, estará familiarizado con toda la gama de desarrollo web moderno y arquitectura de pila completa, patrones de aprendizaje y prácticas para tener éxito como desarrollador individual en la web o como equipo en la empresa.

#### Lo que vas a aprender

* Adopte un enfoque minimalista y prioritario para la entrega de aplicaciones web
* Domine los fundamentos del desarrollo angular, RxJS, herramientas CLI, GitHub y Docker
* Descubra el patrón de flujo y NgRx
* Implementar API RESTful mediante Node.js, Express.js y MongoDB
* Cree aplicaciones web seguras y eficientes para cualquier proveedor de nube o sus propios servidores
* Implemente su aplicación en una infraestructura en la nube de alta disponibilidad mediante DevOps, CircleCI y AWS

#### Para quien es este libro

Este libro está dirigido a desarrolladores que desean entregar con confianza aplicaciones angulares de alta calidad y grado de producción desde el diseño hasta la implementación. Los desarrolladores que tienen experiencia previa en la escritura de API RESTful también se beneficiarán, así como los desarrolladores que obtendrán una mayor conciencia de cómo encajan en el panorama general de la entrega de una aplicación web. Se desea tener experiencia previa con las API RESTful.

## Table of Contents
* Preface
   * Who this book is for 
   * What this book covers
   * To get the most out of this book
      * Download the example code files
      * Download the color images
      * Conventions used
   * Get in touch
      * Reviews
### Introduction to Angular and Its Concepts
* A brief history of web frameworks
* Introduction to Angular
   * Angular's philosophy
   * Angular Evergreen
   * TypeScript
   * Basic Angular architecture
* The reactive development paradigm
   * RxJS
   * Reactive data streams
* Advanced Angular architecture
   * The Angular Router
   * Lazy loading
   * State management
      * The Flux pattern
      * NgRx
   * React.js architecture
* Notable Angular features
   * Angular 6
   * Angular 8
   * Angular 9
* Summary
* Further reading
* Questions

### Setting Up Your Development Environment
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

### Creating a Basic Angular App
   * Planning using Kanban and GitHub projects
      * Setting up a GitHub project
      * Configuring a Kanban board
      * Creating a backlog for the Local Weather app
      * Wireframe design
      * High-level architecture
   * Crafting UI elements using components and interfaces
      * Adding an Angular component
      * Demystifying Angular components
      * Defining your model using interfaces
   * Using Angular Services and HttpClient to retrieve data
      * Creating a new Angular service
      * Injecting dependencies
      * Discovering OpenWeatherMap APIs
      * Storing environment variables
      * Implementing an HTTP GET operation
      * Retrieving service data from a component
   * Transforming data using RxJS
      * Implementing Reactive transformations
   * Null guarding in Angular
      * Property initialization
      * The safe navigation operator
      * Null guarding with *ngIf
* Summary
* Further reading
* Questions

#### Automated Testing, CI, and Release to Production
* Unit testing
* Angular unit tests
   * Jasmine
      * Fixtures
      * Matchers
   * Anatomy of auto-generated unit tests
   * Unit test execution
      * Compilation errors
      * Test results
   * Configuring TestBed
      * Declarations
      * Providers
      * Imports
   * Test doubles
      * Fakes
      * Mocks, stubs, and spies
   * Angular e2e tests
      * e2e test execution
      * The e2e page object and spec
   * Production readiness
      * Building for production
      * Setting environment variables
   * Continuous Integration
      * CircleCI
      * GitHub flow
   * Deploying to the Cloud
      * Vercel Now
      * Deploying static files
* Summary
* Further reading
* Questions

### Delivering High-Quality UX with Material
* Angular Material
* Angular Material setup and performance
   * Installing Angular Material
      * Automatically
      * Manually
   * Understanding Material's components
   * Manually configuring Angular Material
      * Importing modules
      * Importing themes
      * Adding the Material Icon font
* Angular Flex Layout
   * Responsive layouts
   * Installing Angular Flex Layout
   * Layout basics
      * Flex Layout APIs for DOM containers
      * Flex Layout APIs for DOM elements
      * Flex Layout APIs for any element
* Using Material components
   * Angular Material schematics
   * Modifying the landing page with Material Toolbar
   * Material cards
      * Card header and content
   * Material typography
      * Applying typography
   * Flex Layout Align
   * Flex Layout
      * Implementing layout scaﬀolding
   * Aligning elements with CSS
      * Individually styling elements
      * Fine-tuning styles
      * Tweaking to match design
   * Custom themes
   * Unit testing with Material
* Accessibility
   * Configuring automated pa11y testing
* Building an interactive prototype
   * MockFlow WireframePro
   * Building a mock-up
      * Home screen
      * Search results
      * Settings pane
   * Adding interactivity
      * Exporting the functional prototype
* Summary
* Further reading
* Exercises
* Questions

### Forms, Observables, and Subjects
* Reactive forms versus template-driven forms
   * Adding Angular reactive forms
   * Adding and verifying components
   * Adding a search option to the weather service
   * Implementing a search
   * Limiting user inputs with throttle/debounce
   * Input validation and error messages
      * Template-driven forms with two-way binding
* Component interaction with BehaviorSubject
   * Global events
   * Child-parent relationships with event emitters
   * Parent-child relationships with input binding
   * Sibling interactions with subjects
* Managing subscriptions
   * Exposé of a memory leak
   * Unsubscribing from a subscription
   * Unsubscribing using SubSink
* Implementing the reactive style
   * Binding to an observable with an async pipe
   * Tapping into an observable stream
* Multiple API calls
   * Implementing a postal code service
   * Chaining API calls
* Summary
* Exercises
* Questions

### Creating a Router-First Line-of-Business App

* The 80-20 solution
   * Understanding Line-of-Business apps
   * Disciplined and balanced approach
* Router-first architecture
   * Feature modules
   * Developing a roadmap and scope
   * Designing with lazy loading in mind
   * Implementing a walking-skeleton
   * Achieve a stateless, data-driven design
   * Enforce a decoupled component architecture
   * Differentiate between user controls and components
   * Maximize code reuse with TypeScript and ES
* Creating LemonMart
   * Creating a router-first app
   * Configuring Angular and VS Code
   * Configuring Material and Styles
   * Designing LemonMart
      * Identifying user roles
      * Identifying high-level modules with a site map
* Generating router-enabled modules
   * Designing the home route
      * Setting up default routes
      * RouterLink
      * Router outlet
* Branding, customization, and Material icons
   * Branding
   * Color palette
   * Implementing browser manifest and icons
   * Custom themes
   * Custom icons
   * Material icons
* Feature modules with lazy loading
   * Configuring feature modules with components and routes
   * Eager loading
   * Lazy loading
* Completing the walking skeleton
   * The manager module
   * User module
   * POS and inventory modules
      * POS module
      * Inventory module
   * Inspect the router tree
* Common testing module
* Designing around major data entities
   * Defining entities
* High-level UX design
   * Creating an artifacts Wiki
   * Leveraging mock-ups in your app
* Summary
* Further reading
* Questions

### Designing Authentication and Authorization
* Designing an auth workflow
   * JWT life cycle
* TypeScript operators for safe data handling
   * Null and undefined checking
   * The conditional or ternary operator
   * The null coalescing operator
   * The nullish coalescing operator
   * Optional chaining
* Reusable services leveraging OOP concepts
   * JavaScript classes
   * Abstraction and inheritance
      * Create the auth service
      * Implement an abstract auth service
      * Abstract functions
      * Abstract caching service using localStorage
      * Caching the JWT
   * Implement an in-memory auth service
      * Simple login
      * Logout
   * Resuming a JWT session
   * HTTP interceptor
* Dynamic UI components and navigation
   * Implementing the login component
   * Conditional navigation
   * Common validations for forms
   * UI service
   * Side navigation
* Role-based routing using guards
   * Router guards
   * Auth guards
   * Auth service fake and common testing providers
* Firebase authentication recipe
   * Add an application
   * Configure authentication
   * Implement Firebase authentication
* Providing a service using a factory
* Summary
* Further reading
* Questions

### DevOps Using Docker
* DevOps
* Containerizing web apps using Docker
   * Anatomy of a Dockerfile
   * Installing Docker
   * Setting up npm scripts for Docker
   * Build and publish an image to Docker Hub
   * NPM scripts in VS Code
   * Docker extensions in VS Code
* Deploying a Dockerfile to the cloud
   * Google Cloud Run
   * Configuring Docker with Cloud Run
   * Troubleshooting Cloud Run
* Continuous deployment
   * Deploying to Vercel Now using CircleCI
   * Deploying to GCloud using orbs
   * Gated CI workflows
* Advanced continuous integration
   * Containerizing build environments
   * Multi-stage Dockerfiles
      * Builder
      * Tester
      * Web server
   * CircleCI container-in-container
* Code coverage reports
   * Code coverage in CI
* Summary
* Exercise
* Further reading
* Questions

### RESTful APIs and Full-Stack Implementation 
* Full-stack architecture
   * Minimal MEAN
      * Angular
      * Express
      * Node
      * Mongo
      * Tooling
   * Configuring a monorepo
      * Monorepo structure
      * Git submodules
      * Configuring a Node project with TypeScript
      * CircleCI config
   * Docker Compose
      * Using Nginx as the web server
      * Containerizing the server
      * Configuring environment variables with DotEnv
      * Define Docker-Compose YAML
      * Orchestrating the Compose launch
      * Compose on CircleCI
* RESTful APIs
   * API design with Swagger
      * Defining a Swagger YAML file
      * Preview Swagger file
   * Implementing APIs with Express.js
      * Bootstrapping the server
      * Routes and versioning
      * Services
   * Configuring Swagger with Express
* MongoDB ODM with DocumentTS
   * About DocumentTS
   * Connecting to the database
   * Models with IDocument
* Implementing JWT auth
   * Login API
   * Authenticating middleware
   * Custom server auth provider
   * GET User by ID
* Generating users with Postman
   * Configuring Postman for authenticated calls
   * Postman automation
   * Put User
   * Pagination and filtering with DocumentTS
* Summary
* Exercise
* Further reading
* Questions

### Recipes – Reusability, Routing, and Caching
* Implementing a user service with GET
   * Implementing PUT with caching
* Multi-step responsive forms
   * Form controls and form groups
   * Stepper and responsive layout
   * Reusing repeating template behavior with directives
      * Attribute directives
      * Field error attribute directive
   * Calculated properties and DatePicker
   * Typeahead support
   * Dynamic form arrays
   * Creating shared components
   * Reviewing and saving form data
* Scaling architecture with reusable form parts
   * Base form component as an abstract class
   * Implementing a reusable form part
* Input masking
* Custom controls with ControlValueAccessor
   * Implementing a custom rating control
   * Using custom controls in forms
* Layouts using grid list
* Restoring cached data
* Exercise
* Summary
* Further reading
* Questions

### Recipes – Master/Detail, Data Tables, and NgRx
* Editing existing users
   * Loading data with resolve guard
   * Reusing components with binding and route data
* Master/detail view auxiliary routes
* Data table with pagination
   * Updating unit tests
* NgRx Store and Effects
   * Implementing NgRx for LocalCast Weather
   * Comparing BehaviorSubject and NgRx
   * Setting up NgRx
   * Defining NgRx actions
   * Implementing NgRx Effects
   * Implementing reducers
   * Registering with Store using selector
   * Dispatching store actions
   * Unit testing reducers and selectors
   * Unit testing components with MockStore
* NgRx Data
   * Implementing NgRx/Data in LemonMart
   * Configuring proxy in Angular CLI
   * Using Entity Service
   * Customizing Entity Service
* Summary
* Further reading
* Questions

### Highly Available Cloud Infrastructure on AWS
* Creating a secure AWS account
   * Securing secrets
* Right-sizing infrastructure
   * Optimizing instances
   * Simple load testing
* Deploying to AWS ECS Fargate
   * Configuring ECS Fargate
      * Creating a Fargate cluster
      * Creating a container repository
      * Creating a task definition
      * Creating an elastic load balancer
      * Creating a cluster service
      * Configuring the DNS
   * Adding npm scripts for AWS
   * Publish
   * Deploying to AWS using CircleCI
* AWS billing
* Summary
* Exercise
* Further reading
* Questions

### Google Analytics and Advanced Cloud Ops
* Collecting analytics
   * Adding Google Tag Manager to your Angular app
      * Setting up Google Tag Manager
      * Setting up Google Analytics
* Budgeting and scaling
   * Calculating the per-user cost
* Advanced load testing
* Reliable cloud scaling
   * Cost per user in a scalable environment
      * Calculating target server utilization
      * Revising estimates with metrics
* Measuring actual use
   * Creating a custom event
   * Adding custom events in Angular
   * Advanced analytics events
* Summary
* Further reading
* Questions

### Appendix A: Debugging Angular
* The most useful shortcut
* Troubleshooting errors in the browser
   * Leveraging Browser DevTools
   * Optimizing dev tools
   * Troubleshooting network issues
   * Investigating console errors
* Karma, Jasmine, and unit testing errors
   * NetworkError
   * Generic ErrorEvents
* Debugging with Dev Tools
* Debugging with Visual Studio Code
* Debugging with Angular Augury
   * Component Tree
   * Router Tree
   * NgModules
* Debugging with Redux DevTools
   * Implement NgRx Console Logger
   * Configuring NgRx Store DevTools
* Debugging RxJS
   * Tapping an RxJS Event Stream
   * Breakpoint debugging an RxJS Event Stream
* Further advice

### Appendix B: Angular Cheat Sheet
* Built-in directives
* Common pipes
* Starter commands, major components, and CLI scaffolds
   * Starter commands
   * Major component scaffolds
   * TypeScript scaffolds
* Common RxJS functions/operators
   * Functions
   * Operators
* Further Reading

### Another Book You May Enjoy
### Index

<hr>
<div id="sbo-rt-content"><div class="annotator-wrapper"><nav id="toc" epub:type="toc">
    <h2>Contents</h2>
    <ol>
      <li style="list-style-type: none;"><a href="../Text/Preface.xhtml#_idParaDest-5">Preface</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Preface.xhtml#_idParaDest-6">Who this book is for</a></li>
          <li style="list-style-type: none;"><a href="../Text/Preface.xhtml#_idParaDest-7">What this book covers</a></li>
          <li style="list-style-type: none;"><a href="../Text/Preface.xhtml#_idParaDest-8">To get the most out of this book</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Preface.xhtml#_idParaDest-9">Download the example code files</a></li>
              <li style="list-style-type: none;"><a href="../Text/Preface.xhtml#_idParaDest-10">Download the color images</a></li>
              <li style="list-style-type: none;"><a href="../Text/Preface.xhtml#_idParaDest-11">Conventions used</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Preface.xhtml#_idParaDest-12">Get in touch</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Preface.xhtml#_idParaDest-13">Reviews</a></li>
            </ol>
          </li>
        </ol>
      </li>
      <li value="1"><a href="../Text/Chapter_1.xhtml#_idParaDest-14">Introduction to Angular and&nbsp;Its Concepts</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-15">A brief history of web frameworks</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-16">Introduction to Angular</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-17">Angular's philosophy</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-18">Angular Evergreen</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-19">TypeScript</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-20">Basic Angular architecture</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-21">The reactive development paradigm</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-22">RxJS</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-23">Reactive data streams</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-24">Advanced Angular architecture</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-25">The Angular Router</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-26">Lazy loading</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-27">State management</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-28">The Flux pattern</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-29">NgRx</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-30">React.js architecture</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-31">Notable Angular features</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-32">Angular 6</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-33">Angular 8</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-34">Angular 9</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-35">Summary</a>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-36">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_1.xhtml#_idParaDest-37">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_2.xhtml#_idParaDest-38">Setting Up Your Development&nbsp;Environment</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-39">CLI package managers</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-40">Installing Chocolatey for Windows</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-41">Installing Homebrew for macOS</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-42">Installing development tools</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-43">Git and GitHub Desktop</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-44">Why use GitHub?</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-45">Why use GitHub Desktop?</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-46">Installing Git and GitHub Desktop</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-47">Using your GitHub credentials in Git</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-48">Node.js</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-49">Existing Node.js installation</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-50">Installing Node.js</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-51">Global npm packages</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-52">Visual Studio Code</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-53">Installing Visual Studio Code</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-54">Docker</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-55">Installing Docker</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-56">Cloud services</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-57">Vercel Now</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-58">Google Firebase</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-59">Google Cloud</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-60">Amazon Web Services</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-61">Setup automation for Windows and macOS</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-62">PowerShell script</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-63">Bash script</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-64">The Angular CLI</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-65">Setting up your development directory</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-66">Generating your Angular application</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-67">Installing the Angular CLI</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-68">Initializing your Angular app</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-69">Publishing a Git repository using GitHub Desktop</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-70">Inspecting and updating package.json</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-71">Committing code using VS Code</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-72">Running your Angular app</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-73">Verifying your code</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-74">Optimizing VS Code for Angular</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-75">Configuring your project automatically</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-76">VS Code auto save</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-77">IDE settings</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-78">IDE extensions</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-79">Scripting code styling and linting</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-80">Configuring tooling</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-81">Implementing a style checker and fixer</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-82">Implementing a lint checker and fixer</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-83">Configuring Angular CLI autocomplete</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-84">VS Code Auto Fixer</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-85">Summary</a>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-86">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_2.xhtml#_idParaDest-87">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_3.xhtml#_idParaDest-88">Creating a Basic Angular App</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-89">Planning using Kanban and GitHub projects</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-90">Setting up a GitHub project</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-91">Configuring a Kanban board</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-92">Creating a backlog for the Local Weather app</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-93">Wireframe design</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-94">High-level architecture</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-95">Crafting UI elements using components and interfaces</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-96">Adding an Angular component</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-97">Demystifying Angular components</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-98">Defining your model using interfaces</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-99">Using Angular Services and HttpClient to retrieve data</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-100">Creating a new Angular service</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-101">Injecting dependencies</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-102">Discovering OpenWeatherMap APIs</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-103">Storing environment variables</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-104">Implementing an HTTP GET operation</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-105">Retrieving service data from a component</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-106">Transforming data using RxJS</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-107">Implementing Reactive transformations</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-108">Null guarding in Angular</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-109">Property initialization</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-110">The safe navigation operator</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-111">Null guarding with *ngIf</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-112">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-113">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_3.xhtml#_idParaDest-114">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_4.xhtml#_idParaDest-115">Automated Testing, CI, and Release to Production</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-116">Unit testing</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-117">Angular unit tests</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-118">Jasmine</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-119">Fixtures</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-120">Matchers</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-121">Anatomy of auto-generated unit tests</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-122">Unit test execution</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-123">Compilation errors</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-124">Test results</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-125">Configuring TestBed</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-126">Declarations</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-127">Providers</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-128">Imports</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-129">Test doubles</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-130">Fakes</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-131">Mocks, stubs, and spies</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-132">Angular e2e tests</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-133">e2e test execution</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-134">The e2e page object and spec</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-135">Production readiness</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-136">Building for production</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-137">Setting environment variables</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-138">Continuous Integration</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-139">CircleCI</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-140">GitHub flow</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-141">Deploying to the Cloud</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-142">Vercel Now</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-143">Deploying static files</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-144">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-145">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_4.xhtml#_idParaDest-146">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_5.xhtml#_idParaDest-147">Delivering High-Quality UX&nbsp;with Material</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-148">Angular Material</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-149">Angular Material setup and performance</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-150">Installing Angular Material</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-151">Automatically</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-152">Manually</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-153">Understanding Material's components</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-154">Manually configuring Angular Material</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-155">Importing modules</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-156">Importing themes</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-157">Adding the Material Icon font</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-158">Angular Flex Layout</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-159">Responsive layouts</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-160">Installing Angular Flex Layout</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-161">Layout basics</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-162">Flex Layout APIs for DOM containers</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-163">Flex Layout APIs for DOM elements</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-164">Flex Layout APIs for any element</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-165">Using Material components</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-166">Angular Material schematics</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-167">Modifying the landing page with Material Toolbar</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-168">Material cards</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-169">Card header and content</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-170">Material typography</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-171">Applying typography</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-172">Flex Layout Align</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-173">Flex Layout</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-174">Implementing layout scaﬀolding</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-175">Aligning elements with CSS</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-176">Individually styling elements</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-177">Fine-tuning styles</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-178">Tweaking to match design</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-179">Custom themes</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-180">Unit testing with Material</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-181">Accessibility</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-182">Configuring automated pa11y testing</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-183">Building an interactive prototype</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-184">MockFlow WireframePro</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-185">Building a mock-up</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-186">Home screen</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-187">Search results</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-188">Settings pane</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-189">Adding interactivity</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-190">Exporting the functional prototype</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-191">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-192">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-193">Exercises</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_5.xhtml#_idParaDest-194">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_6.xhtml#_idParaDest-195">Forms, Observables, and&nbsp;Subjects</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-196">Reactive forms versus template-driven forms</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-197">Adding Angular reactive forms</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-198">Adding and verifying components</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-199">Adding a search option to the weather service</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-200">Implementing a search</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-201">Limiting user inputs with throttle/debounce</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-202">Input validation and error messages</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-203">Template-driven forms with two-way binding</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-204">Component interaction with BehaviorSubject</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-205">Global events</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-206">Child-parent relationships with event emitters</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-207">Parent-child relationships with input binding</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-208">Sibling interactions with subjects</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-209">Managing subscriptions</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-210">Exposé of a memory leak</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-211">Unsubscribing from a subscription</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-212">Unsubscribing using SubSink</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-213">Implementing the reactive style</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-214">Binding to an observable with an async pipe</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-215">Tapping into an observable stream</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-216">Multiple API calls</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-217">Implementing a postal code service</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-218">Chaining API calls</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-219">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-220">Exercises</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_6.xhtml#_idParaDest-221">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_7.xhtml#_idParaDest-222">Creating a Router-First Line-of-Business App</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-223">The 80-20 solution</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-224">Understanding Line-of-Business apps</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-225">Disciplined and balanced approach</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-226">Router-first architecture</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-227">Feature modules</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-228">Developing a roadmap and scope</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-229">Designing with lazy loading in mind</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-230">Implementing a walking-skeleton</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-231">Achieve a stateless, data-driven design</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-232">Enforce a decoupled component architecture</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-233">Differentiate between user controls and components</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-234">Maximize code reuse with TypeScript and ES</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-235">Creating LemonMart</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-236">Creating a router-first app</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-237">Configuring Angular and VS Code</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-238">Configuring Material and Styles</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-239">Designing LemonMart</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-240">Identifying user roles</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-241">Identifying high-level modules with a site map</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-242">Generating router-enabled modules</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-243">Designing the home route</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-244">Setting up default routes</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-245">RouterLink</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-246">Router outlet</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-247">Branding, customization, and Material icons</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-248">Branding</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-249">Color palette</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-250">Implementing browser manifest and icons</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-251">Custom themes</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-252">Custom icons</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-253">Material icons</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-254">Feature modules with lazy loading</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-255">Configuring feature modules with components and routes</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-256">Eager loading</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-257">Lazy loading</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-258">Completing the walking skeleton</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-259">The manager module</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-260">User module</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-261">POS and inventory modules</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-262">POS module</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-263">Inventory module</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-264">Inspect the router tree</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-265">Common testing module</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-266">Designing around major data entities</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-267">Defining entities</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-268">High-level UX design</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-269">Creating an artifacts Wiki</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-270">Leveraging mock-ups in your app</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-271">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-272">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_7.xhtml#_idParaDest-273">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_8.xhtml#_idParaDest-274">Designing Authentication and&nbsp;Authorization</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-275">Designing an auth workflow</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-276">JWT life cycle</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-277">TypeScript operators for safe data handling</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-278">Null and undefined checking</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-279">The conditional or ternary operator</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-280">The null coalescing operator</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-281">The nullish coalescing operator</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-282">Optional chaining</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-283">Reusable services leveraging OOP concepts</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-284">JavaScript classes</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-285">Abstraction and inheritance</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-286">Create the auth service</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-287">Implement an abstract auth service</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-288">Abstract functions</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-289">Abstract caching service using localStorage</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-290">Caching the JWT</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-291">Implement an in-memory auth service</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-292">Simple login</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-293">Logout</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-294">Resuming a JWT session</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-295">HTTP interceptor</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-296">Dynamic UI components and navigation</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-297">Implementing the login component</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-298">Conditional navigation</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-299">Common validations for forms</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-300">UI service</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-301">Side navigation</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-302">Role-based routing using guards</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-303">Router guards</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-304">Auth guards</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-305">Auth service fake and common testing providers</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-306">Firebase authentication recipe</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-307">Add an application</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-308">Configure authentication</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-309">Implement Firebase authentication</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-310">Providing a service using a factory</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-311">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-312">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_8.xhtml#_idParaDest-313">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_9.xhtml#_idParaDest-314">DevOps Using Docker</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-315">DevOps</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-316">Containerizing web apps using Docker</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-317">Anatomy of a Dockerfile</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-318">Installing Docker</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-319">Setting up npm scripts for Docker</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-320">Build and publish an image to Docker Hub</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-321">NPM scripts in VS Code</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-322">Docker extensions in VS Code</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-323">Deploying a Dockerfile to the cloud</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-324">Google Cloud Run</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-325">Configuring Docker with Cloud Run</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-326">Troubleshooting Cloud Run</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-327">Continuous deployment</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-328">Deploying to Vercel Now using CircleCI</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-329">Deploying to GCloud using orbs</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-330">Gated CI workflows</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-331">Advanced continuous integration</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-332">Containerizing build environments</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-333">Multi-stage Dockerfiles</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-334">Builder</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-335">Tester</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-336">Web server</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-337">CircleCI container-in-container</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-338">Code coverage reports</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-339">Code coverage in CI</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-340">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-341">Exercise</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-342">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_9.xhtml#_idParaDest-343">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_10.xhtml#_idParaDest-344">RESTful APIs and Full-Stack&nbsp;Implementation</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-345">Full-stack architecture</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-346">Minimal MEAN</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-347">Angular</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-348">Express</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-349">Node</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-350">Mongo</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-351">Tooling</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-352">Configuring a monorepo</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-353">Monorepo structure</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-354">Git submodules</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-355">Configuring a Node project with TypeScript</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-356">CircleCI config</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-357">Docker Compose</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-358">Using Nginx as the web server</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-359">Containerizing the server</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-360">Configuring environment variables with DotEnv</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-361">Define Docker-Compose YAML</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-362">Orchestrating the Compose launch</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-363">Compose on CircleCI</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-364">RESTful APIs</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-365">API design with Swagger</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-366">Defining a Swagger YAML file</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-367">Preview Swagger file</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-368">Implementing APIs with Express.js</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-369">Bootstrapping the server</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-370">Routes and versioning</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-371">Services</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-372">Configuring Swagger with Express</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-373">MongoDB ODM with DocumentTS</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-374">About DocumentTS</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-375">Connecting to the database</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-376">Models with IDocument</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-377">Implementing JWT auth</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-378">Login API</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-379">Authenticating middleware</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-380">Custom server auth provider</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-381">GET User by ID</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-382">Generating users with Postman</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-383">Configuring Postman for authenticated calls</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-384">Postman automation</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-385">Put User</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-386">Pagination and filtering with DocumentTS</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-387">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-388">Exercise</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-389">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_10.xhtml#_idParaDest-390">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_11.xhtml#_idParaDest-391">Recipes – Reusability, Routing, and Caching</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-392">Implementing a user service with GET</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-393">Implementing PUT with caching</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-394">Multi-step responsive forms</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-395">Form controls and form groups</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-396">Stepper and responsive layout</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-397">Reusing repeating template behavior with directives</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-398">Attribute directives</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-399">Field error attribute directive</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-400">Calculated properties and DatePicker</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-401">Typeahead support</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-402">Dynamic form arrays</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-403">Creating shared components</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-404">Reviewing and saving form data</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-405">Scaling architecture with reusable form parts</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-406">Base form component as an abstract class</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-407">Implementing a reusable form part</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-408">Input masking</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-409">Custom controls with ControlValueAccessor</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-410">Implementing a custom rating control</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-411">Using custom controls in forms</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-412">Layouts using grid list</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-413">Restoring cached data</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-414">Exercise</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-415">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-416">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_11.xhtml#_idParaDest-417">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_12.xhtml#_idParaDest-418">Recipes – Master/Detail, Data Tables, and NgRx</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-419">Editing existing users</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-420">Loading data with resolve guard</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-421">Reusing components with binding and route&nbsp;data</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-422">Master/detail view auxiliary routes</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-423">Data table with pagination</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-424">Updating unit tests</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-425">NgRx Store and Effects</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-426">Implementing NgRx for LocalCast Weather</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-427">Comparing BehaviorSubject and NgRx</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-428">Setting up NgRx</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-429">Defining NgRx actions</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-430">Implementing NgRx Effects</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-431">Implementing reducers</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-432">Registering with Store using selector</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-433">Dispatching store actions</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-434">Unit testing reducers and selectors</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-435">Unit testing components with MockStore</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-436">NgRx Data</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-437">Implementing NgRx/Data in LemonMart</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-438">Configuring proxy in Angular CLI</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-439">Using Entity Service</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-440">Customizing Entity Service</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-441">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-442">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_12.xhtml#_idParaDest-443">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_13.xhtml#_idParaDest-444">Highly Available Cloud Infrastructure on AWS</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-445">Creating a secure AWS account</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-446">Securing secrets</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-447">Right-sizing infrastructure</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-448">Optimizing instances</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-449">Simple load testing</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-450">Deploying to AWS ECS Fargate</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-451">Configuring ECS Fargate</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-452">Creating a Fargate cluster</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-453">Creating a container repository</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-454">Creating a task definition</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-455">Creating an elastic load balancer</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-456">Creating a cluster service</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-457">Configuring the DNS</a></li>
                </ol>
              </li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-458">Adding npm scripts for AWS</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-459">Publish</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-460">Deploying to AWS using CircleCI</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-461">AWS billing</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-462">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-463">Exercise</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-464">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_13.xhtml#_idParaDest-465">Questions</a></li>
        </ol>
      </li>
      <li><a href="../Text/Chapter_14.xhtml#_idParaDest-466">Google Analytics and Advanced Cloud Ops</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-467">Collecting analytics</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-468">Adding Google Tag Manager to your Angular&nbsp;app</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-469">Setting up Google Tag Manager</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-470">Setting up Google Analytics</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-471">Budgeting and scaling</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-472">Calculating the per-user cost</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-473">Advanced load testing</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-474">Reliable cloud scaling</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-475">Cost per user in a scalable environment</a>
                <ol style="list-style-type: none;">
                  <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-476">Calculating target server utilization</a></li>
                  <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-477">Revising estimates with metrics</a></li>
                </ol>
              </li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-478">Measuring actual use</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-479">Creating a custom event</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-480">Adding custom events in Angular</a></li>
              <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-481">Advanced analytics events</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-482">Summary</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-483">Further reading</a></li>
          <li style="list-style-type: none;"><a href="../Text/Chapter_14.xhtml#_idParaDest-484">Questions</a></li>
        </ol>
      </li>
      <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-485">Appendix A: Debugging Angular</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-487">The most useful shortcut</a></li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-488">Troubleshooting errors in the browser</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-489">Leveraging Browser DevTools</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-490">Optimizing dev tools</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-491">Troubleshooting network issues</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-492">Investigating console errors</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-493">Karma, Jasmine, and unit testing errors</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-494">NetworkError</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-495">Generic ErrorEvents</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-496">Debugging with Dev Tools</a></li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-497">Debugging with Visual Studio Code</a></li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-498">Debugging with Angular Augury</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-499">Component Tree</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-500">Router Tree</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-501">NgModules</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-502">Debugging with Redux DevTools</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-503">Implement NgRx Console Logger</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-504">Configuring NgRx Store DevTools</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-505">Debugging RxJS</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-506">Tapping an RxJS Event Stream</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-507">Breakpoint debugging an RxJS Event Stream</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_A.xhtml#_idParaDest-508">Further advice</a></li>
        </ol>
      </li>
      <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-509">Appendix B: Angular Cheat Sheet</a>
        <ol style="list-style-type: none;">
          <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-511">Built-in directives</a></li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-512">Common pipes</a></li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-513">Starter commands, major components, and CLI scaffolds</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-514">Starter commands</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-515">Major component scaffolds</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-516">TypeScript scaffolds</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-517">Common RxJS functions/operators</a>
            <ol style="list-style-type: none;">
              <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-518">Functions</a></li>
              <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-519">Operators</a></li>
            </ol>
          </li>
          <li style="list-style-type: none;"><a href="../Text/Appendix_B.xhtml#_idParaDest-520">Further Reading</a></li>
        </ol>
      </li>
      <li style="list-style-type: none;"><a href="../Text/Another_Book_You_May_Enjoy.xhtml#_idParaDest-521">Another Book You May Enjoy</a>
      </li>
      <li style="list-style-type: none;"><a epub:type="index" href="../Text/Index.xhtml#_idContainer817">Index</a></li>
    </ol>
  </nav>
  <nav epub:type="landmarks" id="landmarks" hidden="">
    <h1>Landmarks</h1>
    <ol>
      <li>
        <a epub:type="cover" href="../Text/cover.xhtml">Cover</a>
      </li>
      <li>
        <a epub:type="index" href="../Text/Index.xhtml#_idContainer817">Index</a>
      </li>
    </ol>
  </nav>
<div class="annotator-outer annotator-viewer viewer annotator-hide">
  <ul class="annotator-widget annotator-listing"></ul>
</div><div class="annotator-modal-wrapper annotator-editor-modal annotator-editor annotator-hide">
	<div class="annotator-outer editor">
		<h2 class="title">Highlight</h2>
		<form class="annotator-widget">
			<ul class="annotator-listing">
			<li class="annotator-item"><textarea id="annotator-field-2" placeholder="Add a note using markdown (optional)" class="js-editor" maxlength="750"></textarea></li></ul>
			<div class="annotator-controls">
				<a class="link-to-markdown" href="https://daringfireball.net/projects/markdown/basics" target="_blank">?</a>
				<ul>
					<li class="delete annotator-hide"><a href="#delete" class="annotator-delete-note button positive">Delete Note</a></li>
					<li class="save"><a href="#save" class="annotator-save annotator-focus button positive">Save Note</a></li>
					<li class="cancel"><a href="#cancel" class="annotator-cancel button">Cancel</a></li>
				</ul>
			</div>
		</form>
	</div>
</div><div class="annotator-modal-wrapper annotator-delete-confirm-modal" style="display: none;">
  <div class="annotator-outer">
    <h2 class="title">Highlight</h2>
      <a class="js-close-delete-confirm annotator-cancel close" href="#close">Close</a>
      <div class="annotator-widget">
         <div class="delete-confirm">
            Are you sure you want to permanently delete this note?
         </div>
         <div class="annotator-controls">
            <a href="#cancel" class="annotator-cancel button js-cancel-delete-confirm">No, I changed my mind</a>
            <a href="#delete" class="annotator-delete button positive js-delete-confirm">Yes, delete it</a>
         </div>
       </div>
   </div>
</div><div class="annotator-adder" style="display: none;">
	<ul class="adders">
		
		<li class="copy"><a href="#">Copy</a></li>
		
		<li class="add-highlight"><a href="#">Add Highlight</a></li>
		<li class="add-note"><a href="#">
			Add Note
		</a></li>
		
	</ul>
</div></div></div>
