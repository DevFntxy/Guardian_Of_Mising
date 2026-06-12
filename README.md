# Guardian of Missing - Ecosistema de Seguridad Personal (En Desarrollo)
## Descripción General
Guardian of Missing es un proyecto actualmente en fase de desarrollo para la creación de un ecosistema integral de seguridad personal multiplataforma. Una vez concluido, el sistema integrará una aplicación móvil, una aplicación para smartwatch y una API web centralizadora para ofrecer respuestas inmediatas ante emergencias, monitoreo de personas vulnerables y reporte ciudadano.

## Arquitectura del Sistema
El ecosistema se está construyendo sobre una arquitectura basada en Microservicios e interfaces API RESTful asíncronas, estructurada internamente bajo los principios de Clean Architecture. Para optimizar la comunicación entre el hardware y los futuros servidores, se implementará el patrón BFF (Backend For Frontend) con capas de orquestación intermedias para Wearables, Mobile y Web.

## Stack Tecnológico Planificado
- Backend Core: Python 3.10.x con FastAPI (Soporte asíncrono para concurrencia masiva).

- Frontend (Multiplataforma): React (Web) y React Native (Mobile/Smartwatch) con Node.js 18.x LTS.

- Base de Datos Relacional: MySQL 8.0 (Gestión de usuarios, roles, contactos de confianza).

- Base de Datos No Relacional: MongoDB 6.0 con índices geoespaciales (Telemetría y Mapas de Calor).

- Caché y WebSockets: Redis 7.0 (Orquestación en tiempo real).

- Infraestructura: AWS S3 (Almacenamiento de evidencias multimedia) y Firebase Cloud Messaging (Notificaciones Push).

## Módulos Core y Funcionalidades (En Construcción)

1. Núcleo de Emergencia (Botón de Pánico): Activación atómica desde el reloj o el celular, diseñada para enlazar notificaciones masivas a redes cercanas en milisegundos a través de WebSockets.

2. Grabación Silenciosa: Transmisión de streaming de audio/video en segundo plano con almacenamiento encriptado.

3. Motor de Geolocalización y Geocercas (Módulo 1): Delimitación de zonas seguras y lógica estricta de las 3 reglas de la "Última Ubicación Conocida", orientada a optimizar el consumo de batería en wearables.

4. Reportes Ciudadanos Anónimos (Módulo 2): Ingesta de datos en desarrollo para incluir algoritmos de moderación y filtros anti-spam/difamación.

## Configuración del Entorno Local
### Requisitos Previos para el Equipo
- Python 3.10+ y gestor de paquetes poetry.

- Node.js 18.x LTS.

- Servidores locales de MySQL, MongoDB y Redis.

- Entorno de emulación (Android Studio / Xcode).

- Git 2.x.

## Flujo de Trabajo (Git Flow)
Durante toda la fase de construcción, este repositorio operará estrictamente bajo la metodología Git Flow para garantizar la integridad de los entregables planificados en cada Sprint.

- main: Producción estable y testeada. (Bloqueada para push directos)

- develop: Rama base de integración continua de Sprints. (Bloqueada para push directos)

- feature/<nombre-tarea>: Desarrollo activo de nuevos módulos (ej. feature/polling-gps).

- release/<version>: Preparación y estabilización de entregas previas a producción.

- hotfix/<incidencia>: Resolución inmediata de problemas críticos.

Todo código debe integrarse mediante un Pull Request (PR) hacia develop y requiere revisión técnica.

# Equipo de Desarrollo (Equipo MR)
| Integrante | Rol Técnico | Responsabilidades Core |
| --- | --- | --- |
| [**Derek Sesni Carreño**](https://github.com/DevFntxy) | Scrum Master / Lead Backend | Arquitectura de servidores, WebSockets. |
| [**Diego Miguel Rivera**](https://github.com/DiegoMiguel04) | Lead Frontend / DB Co-Designer | UI/UX multiplataforma, mapas de calor, consumo de estados. |
| [**José Arturo Garcia**](https://github.com/ppyo1234) | DBA & QA | Modelado relacional y geoespacial, almacenamiento encriptado (AWS). |
| [**Mauricio Rosales Gabriel**](https://github.com/elmau0834x) | Backend Developer (Geolocalización) | Motor de Polling GPS, consumo de batería, Última Ubicación Conocida. |
| [**Erick Matias Granillo**](https://github.com/EMATIAS230045) | Backend Developer (Seguridad) | Algoritmos anti-spam, streaming discreto en segundo plano. |


