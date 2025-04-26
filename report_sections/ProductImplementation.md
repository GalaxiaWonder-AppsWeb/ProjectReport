# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration

En Galaxia Wonder hemos adoptado una serie de herramientas tanto familiares como más recientes para el diseño, desarrollo y despliegue de nuestra solución de software. En la siguiente tabla a continuación, se presentan las principales herramientas a utilizar por el equipo.

<table>
    <thead>
        <tr>
            <th>Nombre</th>
            <th>Propósito de uso en el proyecto</th>
            <th>Enlace de referencia / descarga</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>UXPressia</td>
            <td><strong>UX/UI Design:</strong> Artefactos de UX</td>
            <td><a href="https://uxpressia.com/" target="_blank">UXPressia Web Application</a></td>
        </tr>
        <tr>
            <td>Miro</td>
            <td><strong>UX/UI Design:</strong> As-Is & To-Be Scenario Mapping</td>
            <td><a href="https://miro.com/es/app/" target="_blank">Descargar Miro</a></td>
        </tr>
        <tr>
            <td>Figma</td>
            <td><strong>UX/UI Design:</strong> Wireframes, Mockups & Prototyping</td>
            <td><a href="https://www.figma.com/es-la/downloads/" target="_blank">Descargar Figma</a></td>
        </tr>
        <tr>
            <td>LucidChart</td>
            <td><strong>UX/UI Design:</strong> Wireflows & Userflows</td>
            <td><a href="https://www.lucidchart.com/" target="_blank">LucidChart Web</a></td>
        </tr>
        <tr>
            <td>Vertabelo</td>
            <td><strong>Software Architecture Design:</strong> Database Diagram</td>
            <td><a href="https://vertabelo.com/" target="_blank">Vertabelo Web</a></td>
        </tr>
        <tr>
            <td>PlantUML</td>
            <td><strong>Software Architecture Design:</strong> UML y C4 Model</td>
            <td><a href="https://plantuml.com/es/" target="_blank">PlantUML Web</a></td>
        </tr>
        <tr>
            <td>VSCode</td>
            <td><strong>IDE:</strong> Editor de código ligero y versátil para múltiples lenguajes</td>
            <td><a href="https://code.visualstudio.com/" target="_blank">Descargar VSCode</a></td>
        </tr>
        <tr>
            <td>WebStorm</td>
            <td><strong>IDE:</strong> Desarrollo especializado en JavaScript y frameworks modernos</td>
            <td><a href="https://www.jetbrains.com/webstorm/" target="_blank">WebStorm Web</a></td>
        </tr>
        <tr>
            <td>Rider</td>
            <td><strong>IDE:</strong> Desarrollo en C# y .NET multiplataforma</td>
            <td><a href="https://www.jetbrains.com/rider/" target="_blank">Rider Web</a></td>
        </tr>
        <tr>
            <td>C#</td>
            <td><strong>Lenguaje de Programación:</strong> Backend moderno con tipado fuerte</td>
            <td><a href="https://learn.microsoft.com/en-us/dotnet/csharp/" target="_blank">Documentación de C#</a></td>
        </tr>
        <tr>
            <td>Node.js</td>
            <td><strong>Entorno de Ejecución:</strong> JavaScript del lado del servidor</td>
            <td><a href="https://nodejs.org/" target="_blank">Descargar Node.js</a></td>
        </tr>
        <tr>
            <td>npm</td>
            <td><strong>Gestor de Paquetes:</strong> Manejo de dependencias para proyectos JS</td>
            <td><a href="https://www.npmjs.com/" target="_blank">Sitio de npm</a></td>
        </tr>
        <tr>
            <td>Vue.js</td>
            <td><strong>Framework:</strong> Desarrollo de aplicaciones web SPA con JavaScript</td>
            <td><a href="https://vuejs.org/" target="_blank">Vue.js Web</a></td>
        </tr>
        <tr>
            <td>.NET</td>
            <td><strong>Framework:</strong> Plataforma para aplicaciones backend y frontend modernas</td>
            <td><a href="https://dotnet.microsoft.com/" target="_blank">Sitio oficial .NET</a></td>
        </tr>
    </tbody>
</table>

### 5.1.2. Source Code Management

En Galaxia Wonder, la gestión del código fuente se realiza mediante Git como sistema de control de versiones, y GitHub como plataforma de alojamiento colaborativo y descentralizado. Esta estructura facilita la colaboración entre equipos distribuidos y permite un control riguroso del ciclo de vida del software.

El proyecto está organizado en varios repositorios, según la arquitectura modular de las soluciones tecnológicas utilizadas:

- Landing Page (Vue.js + Tailwind CSS):  
  [https://github.com/GalaxiaWonder-AppsWeb/LandingPage](https://github.com/GalaxiaWonder-AppsWeb/LandingPage)

- FrontEnd Web Application (Vue.js SPA con Vite):  
  [https://github.com/GalaxiaWonder-AppsWeb/FrontEnd](https://github.com/GalaxiaWonder-AppsWeb/FrontEnd)

- RESTful API (C# + ASP.NET Core):  
  [https://github.com/GalaxiaWonder-AppsWeb/API](https://github.com/GalaxiaWonder-AppsWeb/API)

- ProP GMS Web Service (Arquitectura modular basada en .NET):  
  [https://github.com/GalaxiaWonder-AppsWeb/Platform](https://github.com/GalaxiaWonder-AppsWeb/Platform)

Para su gestión interna, se aplicará GitFlow. Se explican a continuación las ramas a crear, así como las convenciones a utilizar para nombrarlas:

**RAMAS PRINCIPALES**

- **main**: Rama principal de producción. Aquí se encuentran las versiones estables del proyecto, listas para ser desplegadas. Toda publicación oficial se hace desde esta rama.

- **develop**: Rama de desarrollo. Aquí se integran las nuevas funcionalidades antes de ser lanzadas a producción. Es la base para las ramas de tipo *feature*, *release* y *bugfix*.

**RAMAS SECUNDARIAS**

- **feature/**: Ramas para el desarrollo de nuevas funcionalidades. Se crean a partir de `develop` y, una vez completadas, se integran de nuevo en `develop`.  
  - **Convención de nombres**:  
    `feature/story-id`  
    Ejemplo: `feature/us77`

- **bugfix/**: Ramas para la correción de errores detectados en fase de desarrollo. Se crean a partir de `develop` y, una vez completadas, se integran de nuevo en `develop`.  
  - **Convención de nombres**:  
    `bugfix/story-id`  
    Ejemplo: `bugfix/us82`

- **release/**: Ramas para preparar una nueva versión de producción. Se crean desde `develop` cuando ya se ha alcanzado un conjunto estable de funcionalidades. Sirven para realizar pruebas, ajustes menores y documentación. Al finalizar, se integran en `main` y `develop`.  
  - **Convención de nombres**:  
    `release/x.y.z`  
    Ejemplo: `release/1.0.0`

- **hotfix/**: Ramas para corregir errores críticos detectados tardíamente en producción. Se crean desde `main` y se integran tanto en `main` como en `develop` (o en `release`, si hubiere alguna rama de ese tipo activa).  
  - **Convención de nombres**:  
    `hotfix/story-id`  
    Ejemplo: `hotfix/swr35`

### 5.1.3. Source Code Style Guide & Coding Conventions

En esta sección se establecen las guías de estilo y convenciones de codificación que el equipo adoptará para mantener la consistencia, legibilidad y calidad del código fuente.

**LENGUAJES DE PROGRAMACIÓN**

Para el desarrollo de la solución, se utilizarán los siguientes lenguajes de programación y marcado:
- HTML  
- CSS  
- JavaScript  
- C#

**CONVENCIONES GENERALES**  
Para todos los lenguajes de programación y marcado mencionados:
- Se aplicará el uso de nomenclaturas en inglés.
- Se nombrarán variables, constantes, elementos y clases de forma explícita.
- Se usarán saltos de línea vacíos para separar unidades lógicas diferentes del código.
- Se promoverá la reutilización de código.

**CONVENCIONES ESPECÍFICAS**

A continuación, se describen las convenciones principales a aplicar por lenguaje:

**HTML & CSS:** Se aplicarán las recomendaciones del HTML Style Guide and Coding Conventions y el Google HTML/CSS Style Guide:
- Escribir etiquetas y atributos en minúsculas.
- Utilizar indentación de 2 espacios.
- Utilizar clases con nombres descriptivos y en `kebab-case`.
- Evitar el uso de estilos en línea.
- Separar el contenido (HTML) de la presentación (CSS).

**JavaScript:** Se adoptarán las recomendaciones del Google JavaScript Style Guide.
- Usar `camelCase` para variables y funciones.
- Usar `PascalCase` para clases y componentes.
- Definir constantes en `UPPER_SNAKE_CASE`.
- Evitar el uso de `var`, preferir `let` y `const`.
- Usar funciones flecha (`=>`) siempre que sea posible.
- Documentar funciones y clases con comentarios JSDoc.
- Diseñar y codificar orientados al desacoplamiento.

**C# (con .NET):** Se seguirán las recomendaciones del Microsoft C# Coding Conventions y .NET documentation.
- Usar `PascalCase` para nombres de clases, métodos públicos y propiedades.
- Usar `camelCase` para variables locales y parámetros.
- Usar nombres descriptivos y evitar abreviaciones innecesarias.
- Organizar archivos en espacios de nombres (`namespace`) lógicos.
- Usar correctamente estructuras como `async/await`, `try/catch`, `LINQ`, y `using`.
- Promover el uso de inyección de dependencias, principios SOLID y separación de capas (por ejemplo: Controllers, Services, DTOs, etc.).

### 5.1.4 Software Deployment Configuration

**LANDING PAGE DEPLOYMENT**

La landing page del proyecto se desplegará utilizando GitHub Pages, una plataforma gratuita proporcionada por GitHub para alojar sitios web estáticos directamente desde un repositorio. Esta solución permite mostrar públicamente la interfaz sin necesidad de servidores externos o configuraciones complicadas.

1. El despliegue se realiza a partir de la rama principal del repositorio (main), asegurando que las versiones mas estables del equipo de desarrollo estén siempre disponibles para visualización inmediata.

<img src="../img/chapter5/Deploy/Gitpages.png">

Enlace para acceder a la landing page: [https://galaxiawonder-appsweb.github.io/LandingPage/](https://galaxiawonder-appsweb.github.io/LandingPage/)


<div style="page-break-before: always;"></div>

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

#### 5.2.1.1. Sprint Planning 1

<table cellpadding="6" cellspacing="0" style="border-collapse: collapse; width: 100%;">
  <tr>
    <th colspan="2"><strong>Sprint #</strong></th>
    <td colspan="2">Sprint 1</td>
  </tr>
  <tr>
    <th colspan="4" style="background-color: #d9d9d9;"><strong>Sprint Planning Background</strong></th>
  </tr>
  <tr>
    <th style="width: 20%;">Date</th>
    <td colspan="3">2025-04-22</td>
  </tr>
  <tr>
    <th>Time</th>
    <td colspan="3">07:40 PM</td>
  </tr>
  <tr>
    <th>Location</th>
    <td colspan="3">Mediante una videollamada en Discord.</td>
  </tr>
  <tr>
    <th>Prepared By</th>
    <td colspan="3">Orozco Torres, Álvaro Joaquín</td>
  </tr>
  <tr>
    <th>Attendees (to planning meeting)</th>
    <td colspan="3">Aponte Cruzado, Andrea Marielena / León Vivas, Fabrizio Amir / López Acuña, Mario Joaquín / Reaño Delgadillo, Henry Paolo</td>
  </tr>
  <tr>
    <th>Sprint 0 Review Summary</th>
    <td colspan="3">No hubo Sprint anterior (este es el primer sprint)</td>
  </tr>
  <tr>
    <th>Sprint 0 Retrospective Summary</th>
    <td colspan="3">No hubo Sprint anterior (este es el primer sprint)</td>
  </tr>
  <tr>
    <th colspan="4" style="background-color: #d9d9d9;"><strong>Sprint Goal & User Stories</strong></th>
  </tr>
  <tr>
    <th>Sprint 1 Goal</th>
    <td colspan="3">Nuestro foco está en dar visibilidad al producto, sus principales caracterísiticas y beneficios a nuestros usuarios. Creemos que expande nuestro alcance comercial y genera confianza e interés por parte de nuestros usuarios. Esto será confirmado cuando los usuarios comiencen a contactarnos mediante el envío del formulario en la landing page.</td>
  </tr>
  <tr>
    <th>Sprint 1 Velocity</th>
    <td colspan="3">20 Story Points</td>
  </tr>
  <tr>
    <th>Sum of Story Points</th>
    <td colspan="3">18 Story Points</td>
  </tr>
</table>

<div style="page-break-before: always;"></div>

#### 5.2.1.2. Aspect Leaders and Collaborators

Debido a la presión por completar el Sprint 1 a tiempo, no se manejó a gran detalle una coordinación de aspectos. Se acordó establecer como aspecto general el desarrollo de la Landing Page, del cual el lider fue Fabrizio León.

<table cellpadding="6" cellspacing="0" style="border-collapse: collapse; width: 100%;">
  <tr>
    <th>Team Member <br>(Last Name, First Name)</th>
    <th>GitHub Username</th>
    <th>Landing Page <br>Leader (L) / Collaborator (C)</th>
  </tr>
  <tr>
    <td>Aponte Cruzado, Andrea Marielena</td>
    <td>iconicmiau</td>
    <td>C</td>
  </tr>
  <tr>
    <td>León Vivas, Fabrizio Amir</td>
    <td>CodyLionVivo</td>
    <td>L</td>
  </tr>
  <tr>
    <td>López Acuña, Mario Joaquín</td>
    <td>tertegen</td>
    <td>C</td>
  </tr>
  <tr>
    <td>Orozco Torres, Álvaro Joaquín</td>
    <td>L1LZ4Z</td>
    <td>C</td>
  </tr>
  <tr>
    <td>Reaño Delgadillo, Henry Paolo</td>
    <td>PaoloHRRR</td>
    <td>C</td>
  </tr>
</table>

<div style="page-break-before: always;"></div>

#### 5.2.1.3. Sprint Backlog 1

<img src="../../img/chapter5/Sprint1/sprintbacklog.png">

<a href="https://galaxiawonder.youtrack.cloud/dashboard?id=213-2" target="_blank">Ver tablero en YouTrack</a>

<b>Credenciales:</b>
<ul>
  <li>
    Correo: 
    <span style="cursor: default; color: inherit; text-decoration: none;">
      invitadogw&#64;galaxiawonder.com
    </span>
  </li>
  <li>Contraseña: GA14x4W0nd3r</li>
</ul>

<table cellpadding="6" cellspacing="0">
  <tr>
    <th colspan="8">Sprint #</th>
    <td colspan="8">Sprint n</td>
  </tr>
  <tr>
    <th colspan="2">User Story</th>
    <th colspan="6">Work-Item / Task</th>
  </tr>
  <tr>
    <th>Id</th>
    <th>Title</th>
    <th>Id</th>
    <th>Title</th>
    <th>Description</th>
    <th>Estimation (Hours)</th>
    <th>Assigned To</th>
    <th>Status<br>(Done / In-Process / To-Review / Done)</th>
  </tr>
        <tr>
            <td>SWR01</td>
            <td>Cambiar segmento objetivo</td>
            <td>SWR01-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR01-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR06</td>
            <td>Call to action Contratista</td>
            <td>SWR06-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR06-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR07</td>
            <td>Call to action Cliente</td>
            <td>SWR07-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR07-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR05</td>
            <td>Hero Section Contratista</td>
            <td>SWR05-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR05-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR04</td>
            <td>Hero Section Cliente</td>
            <td>SWR04-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR04-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR09</td>
            <td>Overview contratista</td>
            <td>SWR09-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR09-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR08</td>
            <td>Overview cliente</td>
            <td>SWR08-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR08-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR11</td>
            <td>Beneficios contratista</td>
            <td>SWR11-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR11-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR10</td>
            <td>Beneficios cliente</td>
            <td>SWR10-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR10-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR16</td>
            <td>About The Product</td>
            <td>SWR16-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR16-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR03</td>
            <td>About Us</td>
            <td>SWR03-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR03-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR13</td>
            <td>Testimonios contratista</td>
            <td>SWR13-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR13-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
                <tr>
            <td>SWR12</td>
            <td>Testimonios cliente</td>
            <td>SWR12-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR12-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR02</td>
            <td>Internacionalización</td>
            <td>SWR02-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR02-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR18</td>
            <td>Planes</td>
            <td>SWR18-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR18-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR14</td>
            <td>Footer</td>
            <td>SWR14-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR14-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR17</td>
            <td>Términos y condiciones de uso</td>
            <td>SWR17-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR17-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td>SWR15</td>
            <td>Header</td>
            <td>SWR15-1</td>
            <td>Codear el HTML</td>
            <td>Crear las estructuras de marcado semántico correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
        <tr>
            <td></td><td></td>
            <td>SWR15-2</td>
            <td>Codear el CSS</td>
            <td>Crear y aplicar los estilos correspondientes al componente o sección</td>
            <td>1</td>
            <td>León Vivas, Fabrizio Amir</td>
            <td>Done</td>
        </tr>
</table>

<div style="page-break-after: always;"></div>

#### 5.2.1.4. Development Evidence for Sprint Review

En el Sprint 1, se realizó una primera implementación de la Landing Page utilizando HTML, CSS y JavaScript estándar.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Commit on |
| - | - | - | - | - | - |
| LandingPage | feature/swr14 | c0280860da324d508c57f2ce0f20f0d07c5c7fc8 | chore: add base html structure |   | 24/04/2025 |
| LandingPage | feature/swr14 | cdf3c43c2ae65a3b3d376533000745d943d11b36 | chore: add css style for the footer |   | 24/04/2025 |
| LandingPage | feature/swr14 | 391ef8145bd877cdab1cdd3ddbe526f64d5e2cc3 | feat(swr14): add html code for the footer |   | 24/04/2025 |
| LandingPage | feature/swr16 | ff602386552405addae234831b560ba6cfe5371d | feat(swr16): add css style for the testimonials section |   | 25/04/2025 |
| LandingPage | feature/swr16 | 44b11ecef00abbbdc146c617af644f10cfbbcc6a | feat(swr16): add responsive style for the testimonials section |   | 25/04/2025 |
| LandingPage | feature/swr16 | 83e52386354b64f4ad4ddbf5b7880c3cfdcc06c2 | feat(swr16): add html code and assets for the testimonials section |   | 25/04/2025 |
| LandingPage | feature/swr18 | 9c2ecce449679f5c0310553c80aa293c5949320b | feat(swr18): add css and responsive style for the plans section |   | 25/04/2025 |
| LandingPage | feature/swr18 | a308466d66e3a3a60c22fd39ade4ed80462498be | feat(swr18): add global styles to resize the landing |   | 25/04/2025 |
| LandingPage | feature/swr18 | 6409299a278f60e2f8b634578609d8fef11c8abc | feat(swr18): add html code and assets for the plans section |   | 25/04/2025 |
| LandingPage | feature/swr09 | ae6644ab5e17fc77edbd92796b1aa5a398804fa1 | feat(swr09): add css and responsive style for the overview contractor section |   | 25/04/2025 |
| LandingPage | feature/swr09 | 31d5ce0c9c306a796d60c24ab74d71492f91db2d | feat(swr09): import overview css file in style css file |   | 25/04/2025 |
| LandingPage | feature/swr09 | 9a9b43ea362684df35dc4b1bcf5638a1dd446c60 | feat(swr09): add html code and assets for the overview contractor section |   | 25/04/2025 |
| LandingPage | feature/swr09 | 99c188191c5213ad23a198f9d7824ec0de6ae3c3 | feat(swr09): add google font link and change the title |   | 25/04/2025 |
| LandingPage | feature/swr03 | ded4de2f86feedf1966f0654c22cd3e61f4950fc | feat(swr03): add assets for the about us section |   | 25/04/2025 |
| LandingPage | feature/swr03 | 62d562bbd563f07a35fe357e1f77aed1d948c404 | feat(swr03): add css and responsive style for the about us section |   | 25/04/2025 |
| LandingPage | feature/swr03 | 3c2226be5b31df871bc6f0a00041fa6707c8ac4d | feat(swr03): add html code for the about us section |   | 25/04/2025 |
| LandingPage | feature/swr05 | bb6c3af5abd72d36eb7470f425b15da3257e26f0 | feat(swr05): add assets for the hero contractor section |   | 25/04/2025 |
| LandingPage | feature/swr05 | 4c083ec09d305b04a6969e150d8bc9e4cd461c8d | feat(swr05): add css and responsive style for the hero contractor section |   | 25/04/2025 |
| LandingPage | feature/swr05 | 800b22233bae05a70ae26ffcc71c12c2fe9d84d6 | feat(swr05): add html code for the hero contractor section |   | 25/04/2025 |
| LandingPage | feature/swr15 | 394c46a3a439edbfdd06f511a88c2a4b18c7fc58 | feat(swr15): add assets for the header section |   | 25/04/2025 |
| LandingPage | feature/swr15 | f7b907d1e40d493826566de9618b476097fbd050 | feat(swr15): add css and responsive style for the header section |   | 25/04/2025 |
| LandingPage | feature/swr15 | 9ac4e3dfddb6d589860992c165337b43acf47a9a | feat(swr15): add html code for the header section |   | 25/04/2025 |
| LandingPage | feature/swr13 | b6b07c1830b3afa8f90b52817c6cb7dd0427c5be | feat(swr13): add assets for the about the product section |   | 25/04/2025 |
| LandingPage | feature/swr13 | 8a8d134c794d760725b1c25c8e1570ba631ec32c | feat(swr13): add css and responsive style for about the product section |   | 25/04/2025 |
| LandingPage | feature/swr13 | 458a2639f0c4bd29fae6ca75630717d843c9ee0a | feat(swr13): add html code for about the product section |   | 25/04/2025 |
| LandingPage | bugfix/all | c03ea566013981b5348731bffd448923bb6480d6 | bugfix(all): change html and css for better spacing and display |   | 26/04/2025 |

<div style="page-break-after: always;"></div>

#### 5.2.1.5. Execution Evidence for Sprint Review

Se presenta a modo de evidencia un video y capturas de las principales vistas implementadas. Enlace al video: [https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221e247_upc_edu_pe/EWyo-JabeMpAkW37lgNxTQwBG13dBIdjy05sSZCa00UfRw?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=MG98Hf](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221e247_upc_edu_pe/EWyo-JabeMpAkW37lgNxTQwBG13dBIdjy05sSZCa00UfRw?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=MG98Hf)

**HERO SECTION**

Contiene el formulario de contacto con una frase llamativa

<img src="../../img/chapter5/Sprint1/execution1.png">

<div style="page-break-after: always;"></div>

**ABOUT US**

Contiene información sobre nuestra startup

<img src="../../img/chapter5/Sprint1/execution2.png">

<div style="page-break-after: always;"></div>

**FEATURES**

Detalla, para grupo por segmento, cuales son las principales funcionalidades del producto

<img src="../../img/chapter5/Sprint1/execution3.png">

<div style="page-break-after: always;"></div>

**PLANS**

Se presentan los planes de suscripción (los diseñados provisionalmente)

<img src="../../img/chapter5/Sprint1/execution4.png">

<div style="page-break-after: always;"></div>

**FOOTER Y TESTIMONIALS**

Junto al footer con información de contacto, se presentan testimonios de usuarios

<img src="../../img/chapter5/Sprint1/execution5.png">

<div style="page-break-after: always;"></div>

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

No hubo desarrollo del API en este Sprint 1.

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

Para este primer versión de la Landing Page, el despliegue incluyó:

1. Creación del primer release a partir de lo avanzado en develop.
2. Integración del código en la branch de producción (main).
3. Configuración de GitHub Pages para su despliegue a partir de la rama de producción.

#### 5.2.1.8. Team Collaboration Insights during Sprint

Para este primer Sprint, el equipo ha fallado en tener una participación completa en el desarrollo de la Landing Page, cayendo la responsabilidad del desarrollo en León Vivas, Fabrizio Amir. Se añadió demás un trabajo de correción de emergencia previo despligue realizado por Orozco Torres, Álvaro Joaquín, fuera de lo planificado en el Sprint Planning.

<div style="page-break-before: always;"></div>



<div style="page-break-before: always;"></div>

