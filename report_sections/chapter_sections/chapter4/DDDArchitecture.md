## 4.6. Domain-Driven Software Architecture
Esta sección presenta una visión general de la arquitectura basada en DDD, desglosada en diferentes niveles de detalle que van desde el contexto general del sistema hasta los componentes más específicos que lo constituyen.

### 4.6.1. Software Architecture Context Diagram 

El sistema PropGMS es una aplicación diseñada para organizar archivos y actividades vinculadas al desarrollo de un expediente técnico en el sector de la construcción. Está orientada a contratistas independientes y pequeñas consultoras. El sistema se comunica con dos APIs externas: email para mandar notificaciones a los usuarios y una pasarela de pagos para efectuar el cobro de las suscripciones a los usuarios.

<img src="../../../img/chapter4/c4/context.png" alt="Diagrama de contexto de ProP GMS">

### 4.6.2. Software Architecture Container Diagrams

El sistema PropGMS se estructura en varios contenedores que colaboran entre sí para ofrecer una experiencia fluida a los usuarios. La Web Application, desarrollada en Vue, actúa como la interfaz principal donde interactúan los distintos perfiles: contratistas que gestionan proyectos, clientes que revisan avances y especialistas que ejecutan tareas asignadas. A esta aplicación se accede desde una Landing Page pública construida con HTML, CSS y JavaScript, la cual cumple una función informativa y redirige a los usuarios hacia la plataforma principal para la creación de cuentas.

El núcleo lógico del sistema reside en una RESTful API desarrollada en .NET Core. Esta API se encarga de procesar la lógica de negocio, responder a las peticiones del frontend y conectar con la base de datos mediante un túnel SSH seguro. Dicha base de datos, implementada en MariaDB, almacena toda la información relacionada con proyectos, usuarios, tareas, entregables y demás elementos críticos del sistema.

Además, PropGMS se comunica con dos servicios externos: una Email API, utilizada para enviar correos de validación de cuentas y notificaciones, y una Payment Gateway API, encargada de validar los pagos de suscripciones realizados por los usuarios. Toda la comunicación entre contenedores y sistemas externos se realiza mediante canales seguros como HTTPS, garantizando así la confidencialidad y la integridad de los datos.

<img src="../../../img/chapter4/c4/container.png" alt="Diagrama de contenedores de ProP GMS">

### 4.6.3. Software Architecture Components Diagrams

#### 4.6.3.1. Web Application Diagram

El sistema PropGMS se organiza a nivel interno mediante una arquitectura modular basada en componentes. Cada módulo se encarga de una funcionalidad específica, ofreciendo una experiencia segmentada pero coherente al usuario.

La interfaz se divide en distintos módulos como Organization Management UI, que permite gestionar la creación y edición de organizaciones y miembros; Project Management UI, donde se crean y organizan proyectos, hitos, tareas y reuniones; y Change Management UI, que permite a los usuarios generar y revisar solicitudes de cambio. Otros componentes destacados incluyen el Subscription Management UI para la gestión de suscripciones, el Billing UI que muestra el estado de las facturas, y el Payments UI, responsable del flujo de pagos.

Además, la plataforma incorpora módulos especializados como Files Management UI para la gestión de archivos de proyecto, Notifications UI para la visualización de notificaciones, y Identity & Access UI, encargado de todo lo relacionado con autenticación, registro y manejo del perfil del usuario.

Todos estos componentes se comunican de manera segura con la RESTful API mediante el protocolo HTTPS. Esta API centraliza la lógica del negocio, recibe las solicitudes de cada componente y responde con los datos necesarios, promoviendo una arquitectura desacoplada, escalable y fácil de mantener.

<img src="../../../img/chapter4/c4/componente/webApplication.png" alt="Diagrama de componentes de Web Application de ProP GMS">

#### 4.6.3.2. API Diagram

Este nivel descompone el backend de PropGMS, revelando cómo cada módulo de la interfaz web se comunica con un componente específico dentro del contenedor de la RESTful API, desarrollado con .NET Core. La arquitectura sigue un enfoque basado en controladores, cada uno especializado en una funcionalidad concreta del sistema.

Los componentes visuales desarrollados en Vue, como Organization Management UI, Project Management UI o Subscription Management UI, hacen peticiones directas mediante HTTPS hacia sus respectivos controladores: OrganizationController, ProjectController, SubscriptionController, entre otros. Estos controladores manejan operaciones clave como la gestión de organizaciones y miembros, planificación de tareas y reuniones, administración de suscripciones y procesamiento de pagos.

El InvoiceController se encarga de recuperar el estado de las facturas, mientras que el PaymentController interactúa con el Payment Gateway API para validar los pagos. Por su parte, el FileController permite cargar y listar archivos del proyecto, y el NotificationController expone los datos de notificaciones personalizadas para los usuarios. Finalmente, el UserAccountController maneja la autenticación, el registro y la actualización del perfil del usuario.

Además, se visualizan las conexiones entre los controladores y el servicio externo de correo electrónico (Email API), el cual se utiliza para enviar notificaciones como la creación de cuentas, generación de facturas o confirmaciones de pago. Esto asegura una experiencia de usuario informada y fluida.

Este nivel detalla cómo la lógica de negocio está organizada en unidades autónomas, fácilmente testeables y mantenibles, lo que aporta robustez y escalabilidad al sistema completo.

<img src="../../../img/chapter4/c4/componente/api.png" alt="Diagrama de componentes de Web Application de ProP GMS">