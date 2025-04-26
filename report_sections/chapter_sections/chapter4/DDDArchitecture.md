## 4.6. Domain-Driven Software Architecture
Esta sección presenta una visión general de la arquitectura basada en DDD, desglosada en diferentes niveles de detalle que van desde el contexto general del sistema hasta los componentes más específicos que lo constituyen.

### 4.6.1. Software Architecture Context Diagram 

El sistema PropGMS es una aplicación diseñada para organizar archivos y actividades vinculadas al desarrollo de un expediente técnico en el sector de la construcción. Está orientada a contratistas independientes y pequeñas consultoras. El sistema se comunica con dos APIs externas: email para mandar notificaciones a los usuarios y una pasarela de pagos para efectuar el cobro de las suscripciones a los usuarios.

<img src="../../../img/chapter4/c4/context.png" alt="Diagrama de contexto de ProP GMS">

<div style="page-break-after: always;"></div>

### 4.6.2. Software Architecture Container Diagrams

El sistema PropGMS se estructura en varios contenedores que colaboran entre sí para ofrecer una experiencia fluida a los usuarios. La Web Application, desarrollada en Vue, actúa como la interfaz principal donde interactúan los distintos perfiles: contratistas que gestionan proyectos, clientes que revisan avances y especialistas que ejecutan tareas asignadas. A esta aplicación se accede desde una Landing Page pública construida con HTML, CSS y JavaScript, la cual cumple una función informativa y redirige a los usuarios hacia la plataforma principal para la creación de cuentas.

El núcleo lógico del sistema reside en una RESTful API desarrollada en .NET Core. Esta API se encarga de procesar la lógica de negocio, responder a las peticiones del frontend y conectar con la base de datos mediante un túnel SSH seguro. Dicha base de datos, implementada en MariaDB, almacena toda la información relacionada con proyectos, usuarios, tareas, entregables y demás elementos críticos del sistema.

Además, PropGMS se comunica con dos servicios externos: una Email API, utilizada para enviar correos de validación de cuentas y notificaciones, y una Payment Gateway API, encargada de validar los pagos de suscripciones realizados por los usuarios. Toda la comunicación entre contenedores y sistemas externos se realiza mediante canales seguros como HTTPS, garantizando así la confidencialidad y la integridad de los datos.

<img src="../../../img/chapter4/c4/container.png" alt="Diagrama de contenedores de ProP GMS">

<div style="page-break-after: always;"></div>

### 4.6.3. Software Architecture Components Diagrams

#### 4.6.3.1. Web Application Diagram

El núcleo de la aplicación, el AppComponent, actúa como el esqueleto que mantiene unida la interfaz, incluyendo navegación principal (ToolbarComponent), pie de página (FooterComponent) y el enrutamiento dinámico (RouterView) que carga componentes específicos según la navegación del usuario.

Cada funcionalidad clave del sistema, como la gestión de organizaciones, miembros, proyectos, tareas, cambios y reuniones, se orquesta a través de componentes especializados: por ejemplo, OrganizationComponent, ProjectComponent, TaskComponent y MeetingComponent, cada uno complementado por subcomponentes como listas de ítems (ListComponents) y formularios de edición (EditComponents).

Para manejar las operaciones de backend, la aplicación utiliza servicios como OrganizationService, UserService, ProjectService y otros, que abstraen la comunicación con la Web API y transforman respuestas API en modelos frontend mediante ensambladores como OrganizationAssembler o TaskAssembler.

Los flujos críticos de usuario, como autenticación (LoginComponent, RegisterComponent) y administración de suscripciones (SubscriptionComponent, BillingComponent), están centralizados en componentes dedicados, asegurando una navegación intuitiva y un acceso seguro a las funcionalidades del sistema.

Esta arquitectura basada en componentes y servicios fomenta una modularidad impecable, permitiendo que PropGMS no solo sea altamente mantenible y escalable, sino también adaptable a futuras expansiones o personalizaciones sin comprometer la estabilidad de la plataforma.

<img src="../../../img/chapter4/c4/componente/webApplication.png" alt="Diagrama de componentes de Web Application de ProP GMS">

#### 4.6.3.2. API Diagram

Cada módulo de la plataforma web, como la gestión de organizaciones, proyectos o pagos, se comunica de manera segura con un controlador dedicado: OrganizationController, ProjectController, TaskController, entre otros. Estos controladores delegan la lógica de negocio a servicios internos como OrganizationService, ProjectService o PaymentService, cada uno encargado de una funcionalidad crítica del sistema, desde la administración de proyectos hasta el procesamiento de pagos.

Los servicios, a su vez, interactúan con repositorios específicos —por ejemplo, OrganizationRepository, ProjectRepository o PaymentRepository— que manejan las operaciones de lectura y escritura sobre una base de datos relacional en MariaDB, asegurando la persistencia confiable de la información.

Además, la API integra servicios externos estratégicos: NotificationService se comunica con el Email API para enviar correos electrónicos de notificaciones, mientras que PaymentService interactúa con el Payment Gateway API para validar las transacciones de pago de las suscripciones de los usuarios.

Esta organización en capas —controladores, servicios y repositorios— promueve un diseño altamente modular, testeable y escalable, permitiendo a PropGMS evolucionar de forma robusta ante futuras necesidades de crecimiento y adaptación tecnológica.

<img src="../../../img/chapter4/c4/componente/api.png" alt="Diagrama de componentes de Web Application de ProP GMS">