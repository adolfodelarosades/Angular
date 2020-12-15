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
