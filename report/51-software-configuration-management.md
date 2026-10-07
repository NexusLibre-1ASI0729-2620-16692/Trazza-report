## 5.1. Software Configuration Management

En esta sección el equipo NexusLibre establece las decisiones y convenciones que permiten mantener la consistencia de Trazza durante todo su ciclo de vida. Se describen las herramientas que utiliza cada integrante para colaborar, la organización de los repositorios en GitHub, el flujo de trabajo GitFlow, las convenciones de versionamiento y de mensajes de commit, las guías de estilo de cada lenguaje y la configuración de despliegue de los productos digitales de la solución: Landing Page, Frontend Web Application y RESTful Web Services.

### 5.1.1. Software Development Environment Configuration

A continuación se presentan los productos de software que utiliza el equipo, agrupados por tipo de actividad. Para cada producto se indica el propósito de uso dentro del proyecto y la ruta de referencia (productos SaaS) o la ruta de descarga (productos que se instalan en el computador de cada integrante). La selección respeta las restricciones tecnológicas establecidas para el proyecto.

#### Project Management

| Producto | Propósito en el proyecto | Tipo | Ruta |
| :--- | :--- | :--- | :--- |
| Jira Software | Gestión del Product Backlog, planificación de Sprints, tablero ágil (To-do / In-Process / To-Review / Done) y seguimiento de las tareas asignadas a cada integrante. | SaaS | [https://trazza.atlassian.net](https://trazza.atlassian.net/jira/software/projects/SCRUM/boards/1) |
| GitHub (Organization) | Organización `NexusLibre-1ASI0729-2620-16692`, que agrupa los repositorios del proyecto y la gestión de Pull Requests y revisiones de código. | SaaS | [https://github.com/NexusLibre-1ASI0729-2620-16692](https://github.com/NexusLibre-1ASI0729-2620-16692) |
| Microsoft Teams | Reuniones de Sprint Planning, Daily Scrum, Sprint Review y Sprint Retrospective. | SaaS / Desktop | [https://teams.microsoft.com](https://teams.microsoft.com) |

#### Requirements Management

| Producto | Propósito en el proyecto | Tipo | Ruta |
| :--- | :--- | :--- | :--- |
| Jira Software | Registro de Epics y User Stories, estimación en Story Points (escala Fibonacci) y priorización del Product Backlog. | SaaS | [https://trazza.atlassian.net](https://trazza.atlassian.net/jira/software/projects/SCRUM/boards/1) |
| Gherkin | Lenguaje para redactar los criterios de aceptación de cada User Story bajo la estructura Given / When / Then. | Especificación | [https://cucumber.io/docs/gherkin/reference/](https://cucumber.io/docs/gherkin/reference/) |
| GitHub Markdown | Documentación versionada de requisitos y del Project Report bajo el enfoque document as code. | SaaS | [https://docs.github.com/en/get-started/writing-on-github](https://docs.github.com/en/get-started/writing-on-github) |

#### Product UX/UI Design

| Producto | Propósito en el proyecto | Tipo | Ruta |
| :--- | :--- | :--- | :--- |
| UXPressia | Elaboración de User Personas, Empathy Maps, User Journey Maps e Impact Maps. | SaaS | [https://uxpressia.com](https://uxpressia.com) |
| Figma | Diseño de Wireframes, Mock-ups y Prototypes del Landing Page y de la Web Application (Desktop y Mobile). | SaaS | [https://www.figma.com](https://www.figma.com) |
| FigJam | Elaboración del EventStorming, Wireflow Diagrams y User Flow Diagrams. | SaaS | [https://www.figma.com/figjam/](https://www.figma.com/figjam/) |
| Material Design 3 | Lenguaje de diseño base para la interfaz del Landing Page y de la Web Application. | Guía | [https://m3.material.io](https://m3.material.io) |

#### Software Architecture & Design

| Producto | Propósito en el proyecto | Tipo | Ruta |
| :--- | :--- | :--- | :--- |
| PlantUML (C4-PlantUML) | Diagramas como código (Diagram-as-Code) para el C4 Model (Context, Container y Component), el Class Diagram y el Database Diagram. Los archivos `.puml` se versionan en `assets/diagram-as-code` del repositorio del informe. | Open source | [https://plantuml.com](https://plantuml.com) |
| Visual Studio Code + extensión PlantUML | Edición y previsualización local de los diagramas `.puml`. | Desktop | [https://code.visualstudio.com/download](https://code.visualstudio.com/download) |

#### Software Development

| Producto | Propósito en el proyecto | Tipo | Ruta |
| :--- | :--- | :--- | :--- |
| Git | Sistema de control de versiones distribuido utilizado por todos los integrantes. | Desktop | [https://git-scm.com/downloads](https://git-scm.com/downloads) |
| JetBrains WebStorm | IDE para el desarrollo del Landing Page (HTML5, CSS3, JavaScript) y de la Frontend Web Application (Angular). | Desktop | [https://www.jetbrains.com/webstorm/download/](https://www.jetbrains.com/webstorm/download/) |
| Visual Studio Code | Editor alternativo para el Landing Page, la Web Application y los archivos Markdown del informe. | Desktop | [https://code.visualstudio.com/download](https://code.visualstudio.com/download) |
| Node.js (LTS) + npm | Entorno de ejecución y gestor de paquetes para construir la Web Application con Angular CLI. | Desktop | [https://nodejs.org/en/download](https://nodejs.org/en/download) |
| Angular + Angular CLI | Framework y herramienta de construcción de la Frontend Web Application con TypeScript. | Librería | [https://angular.dev](https://angular.dev) |
| Angular Material | Biblioteca de componentes de UI para la Web Application, basada en Material Design. | Librería | [https://material.angular.dev](https://material.angular.dev) |
| Angular Router · Signals · ngx-translate | Navegación entre vistas, manejo de estado por bounded context e internacionalización (en_US por defecto, es_419). | Librería | [https://angular.dev/guide/routing](https://angular.dev/guide/routing) · [https://angular.dev/guide/signals](https://angular.dev/guide/signals) · [https://github.com/ngx-translate/core](https://github.com/ngx-translate/core) |
| Angular HttpClient | Cliente HTTP para consumir el Fake API (Sprint 2) y luego la RESTful API. | Librería | [https://angular.dev/guide/http](https://angular.dev/guide/http) |
| json-server | Fake API basado en un archivo `db.json`, utilizado mientras se implementan los Web Services en Spring Boot. | Librería | [https://github.com/typicode/json-server](https://github.com/typicode/json-server) |
| IntelliJ IDEA | IDE para el desarrollo de la RESTful API en Java con Spring Boot y Spring Data JPA. | Desktop | [https://www.jetbrains.com/idea/download/](https://www.jetbrains.com/idea/download/) |
| JDK + Maven | Kit de desarrollo de Java y gestor de dependencias para compilar y ejecutar los Web Services en Spring Boot. | Desktop | [https://adoptium.net](https://adoptium.net) |
| MySQL Server + MySQL Workbench | Motor de base de datos relacional y herramienta de administración y consultas. | Desktop | [https://dev.mysql.com/downloads/](https://dev.mysql.com/downloads/) |

#### Software Testing

| Producto | Propósito en el proyecto | Tipo | Ruta |
| :--- | :--- | :--- | :--- |
| Swagger UI (OpenAPI Specification) | Documentación y prueba manual de los endpoints de la RESTful API, integrada en Spring Boot mediante springdoc-openapi. | Librería | [https://swagger.io/tools/swagger-ui/](https://swagger.io/tools/swagger-ui/) |
| Chrome DevTools | Pruebas de responsive design (Desktop 1280 px / Mobile 390 px), revisión de atributos ARIA y depuración de llamadas HTTP. | Desktop | [https://developer.chrome.com/docs/devtools](https://developer.chrome.com/docs/devtools) |
| Lighthouse | Auditoría de accesibilidad, rendimiento y SEO del Landing Page y la Web Application. | Desktop | [https://developer.chrome.com/docs/lighthouse](https://developer.chrome.com/docs/lighthouse) |
| Jasmine + Karma | Pruebas unitarias de la Frontend Web Application (por ejemplo, `route-matching.service.spec.ts`). | Librería | [https://angular.dev/guide/testing](https://angular.dev/guide/testing) |
| JUnit 5 | Pruebas unitarias y de integración de la RESTful API en Spring Boot. | Librería | [https://junit.org/junit5/](https://junit.org/junit5/) |

#### Software Deployment

| Producto | Propósito en el proyecto | Tipo | Ruta |
| :--- | :--- | :--- | :--- |
| AWS Amplify Hosting | Publicación continua del Landing Page y de la Frontend Web Application a partir de la rama `main` de cada repositorio. | SaaS (Cloud) | [https://aws.amazon.com/amplify/hosting/](https://aws.amazon.com/amplify/hosting/) |
| Render (Web Service) | Publicación temporal del Fake API (json-server) consumido por la primera versión de la Web Application. | SaaS (Cloud) | [https://render.com](https://render.com) |
| AWS EC2 · AWS RDS for MySQL | Infraestructura planificada para la RESTful API y su base de datos a partir del Sprint 3. | SaaS (Cloud) | [https://aws.amazon.com](https://aws.amazon.com) |

#### Software Documentation

| Producto | Propósito en el proyecto | Tipo | Ruta |
| :--- | :--- | :--- | :--- |
| GitHub (Trazza-report) | Redacción y control de versiones del Project Report en Markdown. | SaaS | [https://github.com/NexusLibre-1ASI0729-2620-16692/Trazza-report](https://github.com/NexusLibre-1ASI0729-2620-16692/Trazza-report) |
| Microsoft Stream | Publicación de los videos de exposición, entrevistas y navegación por Sprint. | SaaS | [https://www.microsoft.com/microsoft-365/microsoft-stream](https://www.microsoft.com/microsoft-365/microsoft-stream) |
| OpenAPI (Swagger) | Documentación de los Web Services desde el propio proyecto Spring Boot mediante springdoc-openapi. | Especificación | [https://swagger.io/specification/](https://swagger.io/specification/) |

### 5.1.2. Source Code Management

El equipo utiliza GitHub como plataforma y sistema de control de versiones. Todos los repositorios pertenecen a la organización `NexusLibre-1ASI0729-2620-16692`, y cada producto digital tiene un repositorio independiente, lo que permite que cada uno tenga su propio historial, su propia configuración de despliegue y sus propias versiones.

| Producto | Repositorio | Contenido |
| :--- | :--- | :--- |
| Project Report | [https://github.com/NexusLibre-1ASI0729-2620-16692/Trazza-report](https://github.com/NexusLibre-1ASI0729-2620-16692/Trazza-report) | Informe en Markdown, imágenes y diagramas como código (`.puml`). |
| Landing Page | [https://github.com/NexusLibre-1ASI0729-2620-16692/Trazza-landingPage](https://github.com/NexusLibre-1ASI0729-2620-16692/Trazza-landingPage) | Sitio estático en HTML5, CSS3 y JavaScript con i18n (EN / ES). |
| Frontend Web Application | [https://github.com/NexusLibre-1ASI0729-2620-16692/Trazza-webApp](https://github.com/NexusLibre-1ASI0729-2620-16692/Trazza-webApp) | Aplicación Angular + Angular Material organizada por bounded context (`iam`, `matchmaking`, `execution`, `billing`, `reputation` y `shared`) y Fake API en `server/db.json`. |
| Web Services (RESTful API) | `https://github.com/NexusLibre-1ASI0729-2620-16692/Trazza-webServices` (se crea en el Sprint 3) | Proyecto Spring Boot + Spring Data JPA y sus pruebas unitarias y de integración/aceptación. |

#### GitFlow Workflow

El equipo aplica el modelo de ramificación GitFlow propuesto por Vincent Driessen en A successful Git branching model. Este modelo separa el trabajo en progreso de las versiones estables y define el camino que recorre cada cambio hasta llegar a producción.

**Main branches**

| Rama | Propósito | Regla |
| :--- | :--- | :--- |
| `main` | Contiene únicamente versiones estables y desplegadas. Cada merge a `main` dispara el despliegue automático en AWS Amplify. | Solo recibe merges desde `release/*` o `hotfix/*`, y cada merge se etiqueta con su versión (`vX.Y.Z`). |
| `develop` | Rama de integración en la que se consolidan las funcionalidades terminadas antes de un release. | Recibe merges desde `feature/*` mediante Pull Request revisado por al menos un integrante. |

**Supporting branches**

| Tipo | Se crea desde | Se integra en | Convención de nombre | Ejemplos |
| :--- | :--- | :--- | :--- | :--- |
| Feature | `develop` | `develop` | `feature/<nombre-del-aspecto>` en kebab-case e inglés: el bounded context en la Web Application o la sección en el Landing Page. | `feature/matchmaking-routing`, `feature/loyalty-reputation`, `feature/hero-section` |
| Release | `develop` | `main` y `develop` | `release/v<MAJOR>.<MINOR>.<PATCH>` | `release/v1.1.0`, `release/v0.1.0` |
| Hotfix | `main` | `main` y `develop` | `hotfix/v<MAJOR>.<MINOR>.<PATCH>-<short-description>` | `hotfix/v1.1.1-mobile-menu-overflow` |

En el repositorio del informe se aplica la misma estrategia: cada sección del informe se trabaja en una rama `feature/<número-de-sección>-<nombre>` (por ejemplo `feature/44-web-applications-ux-ui-design` o `feature/51-software-configuration-management`) y se integra a `develop` mediante Pull Request.

#### Semantic Versioning

Los releases de cada producto se nombran con Semantic Versioning 2.0.0 (`MAJOR.MINOR.PATCH`):

* **MAJOR**: cambios incompatibles con la versión anterior (por ejemplo, un cambio en el contrato de la API).
* **MINOR**: nuevas funcionalidades compatibles con la versión anterior.
* **PATCH**: corrección de errores que no altera la funcionalidad.

Mientras la Web Application y la RESTful API estén en desarrollo inicial se usa la serie `0.y.z`; la versión `1.0.0` se reserva para el primer release completo con los Web Services integrados.

| Producto | Versión | Entrega | Alcance |
| :--- | :--- | :--- | :--- |
| Landing Page | `v1.0.0` | AV1 – Sprint 1 | Primera versión del Landing Page desplegada en AWS Amplify. |
| Landing Page | `v1.1.0` | TB1 – Sprint 2 | Inglés como idioma por defecto, selector EN / ES funcional, rediseño según el mock-up actualizado y fotografías reales en las secciones para transportistas y comerciantes. |
| Frontend Web Application | `v0.1.0` | TB1 – Sprint 2 | Primera versión desplegada: Sign up / Sign in, dashboards por rol, rutas de retorno, solicitudes de flete, vehículos e historial de envíos sobre el Fake API. |
| RESTful API | `v0.1.0` | AV2 – Sprint 3 | Primera versión de los Web Services documentados con OpenAPI. |

#### Conventional Commits

Los mensajes de commit siguen la especificación Conventional Commits 1.0.0, con el mensaje redactado en inglés y en modo imperativo:

```text
<type>(<optional scope>): <short description>

<optional body: qué cambió y por qué>

<optional footer: Refs #issue / BREAKING CHANGE>
```

| Tipo | Uso |
| :--- | :--- |
| `feat` | Nueva funcionalidad (User Story o task). |
| `fix` | Corrección de un error. |
| `docs` | Cambios en el informe o en la documentación. |
| `style` | Cambios de formato que no afectan la lógica. |
| `refactor` | Mejora interna del código sin cambiar su comportamiento. |
| `test` | Creación o modificación de pruebas. |
| `chore` | Configuración, dependencias o tareas de mantenimiento. |

Ejemplos tomados del historial del proyecto:

* `feat(matchmaking): add route-matching domain service` (Trazza-webApp)
* `test(matchmaking): add route-matching service unit tests` (Trazza-webApp)
* `feat(i18n): add language engine and base translations` (Trazza-landingPage)
* `style(header): add responsive navigation styles` (Trazza-landingPage)

### 5.1.3. Source Code Style Guide & Conventions

En todos los productos de la solución se utiliza el **inglés** para nombrar archivos, carpetas, variables, funciones, clases, componentes, tablas, columnas, endpoints y mensajes de commit. Los textos que ve el usuario se manejan con i18n (en_US por defecto y es_419). A continuación se indican las guías adoptadas por lenguaje.

**HTML5**

Referencias: [W3Schools HTML Style Guide and Coding Conventions](https://www.w3schools.com/html/html5_syntax.asp) y [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html).

* Declarar `<!DOCTYPE html>` y el atributo `lang` en la etiqueta `<html>` (`lang="en"` por defecto).
* Elementos y atributos en minúsculas, valores de atributos entre comillas dobles e indentación de 2 espacios.
* Uso de etiquetas semánticas (`header`, `nav`, `main`, `section`, `footer`).
* Todas las imágenes incluyen `alt`, y los controles sin texto visible incluyen `aria-label` (a11y).
* Los textos traducibles se marcan con `data-i18n`, por ejemplo `<a href="#plans" data-i18n="nav.plans">Plans</a>`.

**CSS3**

Referencias: [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html).

* Clases e IDs en kebab-case y con nombres que describen su función (`.split-media`, `#how-it-works`).
* Colores, tipografía y espaciados definidos como variables en `:root` (por ejemplo `--color-primary: #0037B0`).
* Sin estilos en línea; enfoque mobile first con media queries para tablet y desktop.

**JavaScript**

Referencias: [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html), [MDN JavaScript guidelines](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/JavaScript) y [W3Schools JavaScript Style Guide](https://www.w3schools.com/js/js_conventions.asp).

* `const` por defecto, `let` solo cuando la variable se reasigna; no se usa `var`.
* camelCase para variables y funciones (`applyLanguage`, `returnRoutes`), PascalCase para clases y UPPER_SNAKE_CASE para constantes (`STORAGE_KEY`).
* Punto y coma al final de cada sentencia, comillas simples y funciones flecha en callbacks.
* Uso de `async/await` para operaciones asíncronas.

**Angular Framework y TypeScript**

Referencias: [Angular coding style guide](https://angular.dev/style-guide) y [Google TypeScript Style Guide](https://google.github.io/styleguide/tsguide.html).

* Standalone components con clases en PascalCase y archivos en kebab-case (`freight-request-form.ts`, `freight-request-form.html`, `freight-request-form.css`).
* Estructura de carpetas por bounded context: `src/app/iam`, `src/app/matchmaking`, `src/app/execution`, `src/app/billing`, `src/app/reputation` y `src/app/shared`, y dentro de cada uno `domain/model`, `application`, `infrastructure` y `presentation`.
* Sufijos según el rol del archivo: `*.entity.ts`, `*.value-object.ts`, `*.store.ts`, `*-api.ts`, `*-api-endpoint.ts`, `*-assembler.ts` y `*.routes.ts`.
* Estado por bounded context con Signals e inyección de dependencias con `inject()`; rutas con lazy loading protegidas con `iamGuard`.
* Componentes de Angular Material para la UI; textos de la interfaz siempre a través de ngx-translate (`public/i18n/en.json` y `es.json`).

**Java y Spring Boot**

Referencias: [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html) y [Spring Boot Features](https://docs.spring.io/spring-boot/reference/features/index.html).

* PascalCase para clases e interfaces (`ReturnRoute`, `ReturnRouteRepository`); camelCase para métodos, variables y parámetros (`findByCarrierId`); UPPER_SNAKE_CASE para constantes.
* Paquetes en minúsculas organizados por bounded context, con capas `domain`, `application`, `infrastructure` e `interfaces` (controllers REST en plural, por ejemplo `/api/v1/return-routes`).
* Una clase por archivo e inyección de dependencias por constructor.
* Persistencia con Spring Data JPA y endpoints documentados con OpenAPI mediante springdoc-openapi (Swagger UI).

**Gherkin**

Referencia: [Gherkin Conventions for Readable Specifications](https://specflow.org/gherkin/gherkin-conventions-for-readable-specifications/).

* Palabras clave `Feature`, `Scenario`, `Given`, `When`, `Then`, `And`.
* Un solo `When` por escenario y escenarios con nombres que describen el comportamiento esperado.
* Uso de `Examples` en tablas cuando un escenario se repite con distintos datos.

### 5.1.4. Software Deployment Configuration

La solución Trazza se compone de tres productos que se despliegan de forma independiente. La siguiente tabla resume la configuración vigente al Sprint 2.

| Producto | Repositorio / rama | Tecnología | Servicio de despliegue | URL pública |
| :--- | :--- | :--- | :--- | :--- |
| Landing Page | `Trazza-landingPage` / `main` | HTML5, CSS3, JavaScript | AWS Amplify Hosting | `[URL de Amplify del Landing Page]` |
| Frontend Web Application | `Trazza-webApp` / `main` | Angular, Angular Material, TypeScript, ngx-translate | AWS Amplify Hosting | `[URL de Amplify de la Web Application]` |
| Fake API (temporal) | `Trazza-webApp` / `main` (carpeta `server`) | json-server | Render (Web Service) | `[URL de Render del Fake API]` |
| RESTful API (Sprint 3) | `Trazza-webServices` / `main` | Spring Boot, Java, Spring Data JPA | AWS EC2 | Pendiente |
| Base de datos (Sprint 3) | — | MySQL | AWS RDS for MySQL | Pendiente |

#### Landing Page (AWS Amplify Hosting)

1. Ingresar a la consola de AWS Amplify y seleccionar **Create new app → GitHub**.
2. Autorizar a AWS Amplify en la organización `NexusLibre-1ASI0729-2620-16692` y seleccionar el repositorio `Trazza-landingPage` y la rama `main`.
3. Al ser un sitio estático, no se configura comando de build y el directorio de salida es la raíz del repositorio (`/`).
4. Guardar y desplegar. Amplify publica el sitio en un dominio `*.amplifyapp.com` con HTTPS.
5. Cada merge en `main` dispara automáticamente un nuevo despliegue (despliegue continuo).

#### Frontend Web Application (AWS Amplify Hosting)

1. En AWS Amplify, crear una nueva app conectada al repositorio `Trazza-webApp`, rama `main`.
2. Configurar el build en `amplify.yml`:

```yaml
version: 1
frontend:
  phases:
    preBuild:
      commands:
        - npm ci
    build:
      commands:
        - npm run build
  artifacts:
    baseDirectory: dist/trazza-web-application/browser
    files:
      - '**/*'
  cache:
    paths:
      - node_modules/**/*
```

3. Configurar en `src/environments/environment.ts` la propiedad `platformProviderApiBaseUrl` con la URL pública del Fake API (en el Sprint 3 se reemplazará por la URL de la RESTful API).
4. Agregar la regla Rewrites and redirects para que Angular Router funcione al recargar cualquier ruta:

| Source address | Target address | Type |
| :--- | :--- | :--- |
| `</^[^.]+$\|\.(?!(css\|gif\|ico\|jpg\|js\|png\|txt\|svg\|woff\|woff2\|ttf\|map\|json\|webp)$)([^.]+$)/>` | `/index.html` | `200 (Rewrite)` |

5. Guardar y desplegar. Cada merge en `main` genera un nuevo build y despliegue.

#### Fake API (Render)

1. Crear un **Web Service** en Render conectado al repositorio `Trazza-webApp`.
2. Configurar Root Directory `server`, Build Command `npm install` y Start Command `npx json-server db.json --routes routes.json --host 0.0.0.0 --port $PORT` (el archivo `routes.json` agrega el prefijo `/api/v1`).
3. Copiar la URL pública generada y registrarla en la propiedad `platformProviderApiBaseUrl` de `src/environments/environment.ts`.

#### RESTful API y base de datos (planificado para el Sprint 3)

1. Aprovisionar una instancia de AWS RDS for MySQL y restringir su Security Group para aceptar conexiones solo desde la instancia EC2 de la API.
2. Empaquetar el proyecto Spring Boot con `./mvnw clean package` y ejecutar el `.jar` generado (`java -jar target/*.jar`) en una instancia AWS EC2 detrás de Nginx como proxy inverso.
3. Configurar como variables de entorno `SPRING_PROFILES_ACTIVE=prod`, la conexión a MySQL (`SPRING_DATASOURCE_URL`, `SPRING_DATASOURCE_USERNAME` y `SPRING_DATASOURCE_PASSWORD`) y la clave para la generación de tokens JWT, sin exponer credenciales en el repositorio.
4. Habilitar Swagger UI (springdoc-openapi) en `/swagger-ui/index.html` como evidencia de la documentación OpenAPI.
