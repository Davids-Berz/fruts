#### 1.1. **Soporte para APIs RESTful y WebSocket**

API Gateway permite crear y gestionar dos tipos de APIs:

- **RESTful APIs**: Para acceder a recursos a través de HTTP, utilizando los métodos tradicionales como **GET**, **POST**, **PUT**, **DELETE**.
- **WebSocket APIs**: Permiten la comunicación bidireccional en tiempo real entre el cliente y el servidor, ideal para aplicaciones de mensajería, notificaciones en tiempo real o IoT.

#### 1.2. **Integración con AWS Lambda y Otros Backends**

API Gateway se integra perfectamente con **AWS Lambda**, lo que permite crear APIs sin necesidad de gestionar servidores. También se puede integrar con otros servicios backend, como **Amazon EC2**, **AWS Fargate**, **DynamoDB**, **Amazon S3** y otros servicios HTTP o HTTPS.

#### 1.3. **Gestión de API a Gran Escala**

API Gateway simplifica la gestión de APIs de manera escalable:

- **Versionamiento de APIs**: Puedes crear nuevas versiones o "stages" de tu API (por ejemplo, desarrollo, prueba y producción).
- **Throttle y Caching**: API Gateway permite limitar el número de solicitudes por cliente y habilitar el almacenamiento en caché de respuestas para mejorar el rendimiento.
- **Seguridad**: API Gateway admite autenticación y autorización mediante **AWS IAM**, **Amazon Cognito**, **API Keys**, y **OAuth**.

#### 1.4. **Monitoreo y Registro con CloudWatch**

API Gateway se integra con **Amazon CloudWatch** para proporcionar métricas detalladas sobre el tráfico de API, tiempos de respuesta y errores. También permite habilitar el registro de peticiones y respuestas, lo que facilita la depuración y auditoría.

#### 1.5. **Control de Acceso y Autenticación**

API Gateway ofrece varias formas de controlar el acceso a las APIs:

- **API Keys**: Se pueden generar claves API para limitar el acceso a la API.
- **AWS IAM**: Controla el acceso mediante políticas IAM que definen qué usuarios o servicios pueden acceder a los recursos.
- **Amazon Cognito**: Gestiona usuarios y sesiones mediante autenticación basada en OAuth, integración con proveedores de identidad como Google, Facebook, etc.
- **Autorizadores Lambda**: Puedes crear autorizadores personalizados con funciones Lambda que se ejecutan antes de que se procese la solicitud de API para validar tokens o credenciales.

#### 1.6. **API Gateway Throttling**

API Gateway permite **limitar** (throttling) el número de solicitudes entrantes por segundo a una API para evitar que se sobrecargue el backend. Esto asegura que una API pueda manejar de forma segura y eficaz un gran volumen de tráfico o picos repentinos.

#### 1.7. **Caching de Respuestas**

API Gateway puede **almacenar en caché** las respuestas de las API para reducir la carga en el backend y mejorar el rendimiento de la API. Esto es útil cuando los datos no cambian con frecuencia, permitiendo que las solicitudes futuras obtengan las respuestas desde el caché en lugar de llegar al backend.