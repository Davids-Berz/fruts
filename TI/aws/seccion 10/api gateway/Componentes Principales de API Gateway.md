#### 3.1. **Recursos**

Un **recurso** en API Gateway representa una ruta en la URL de la API (por ejemplo, `/usuarios`, `/productos`). Cada recurso puede tener múltiples **métodos HTTP** asociados (como GET, POST, etc.).

#### 3.2. **Métodos**

Cada **recurso** puede estar asociado a uno o más **métodos HTTP** (GET, POST, PUT, DELETE). Un método define cómo se procesa una solicitud HTTP y hacia qué servicio backend se envía.

#### 3.3. **Integraciones Backend**

Las **integraciones backend** definen cómo API Gateway debe interactuar con servicios externos o internos:

- **Lambda Function**: API Gateway invoca una función Lambda para manejar la solicitud.
- **HTTP Proxy**: API Gateway reenvía la solicitud a un endpoint HTTP externo.
- **Mock Integration**: API Gateway responde sin enviar la solicitud a un backend (útil para pruebas).
- **AWS Service Proxy**: Puedes integrar directamente servicios como DynamoDB o S3 sin un intermediario.

#### 3.4. **Staging y Versionamiento**

Las **stages** en API Gateway permiten versionar y desplegar una API en diferentes entornos, como **desarrollo**, **prueba** o **producción**. Cada stage puede tener configuraciones y límites diferentes, como la cantidad de **throttling** o **caching**.

#### 3.5. **Autorización**

API Gateway permite varios mecanismos de **autorización** para controlar el acceso a las APIs:

- **Autorizadores Lambda**: Son funciones Lambda que ejecutan lógica personalizada para validar la autenticación o autorización antes de que la API procese la solicitud.
- **Amazon Cognito**: Puedes usar **Amazon Cognito User Pools** para gestionar la autenticación de usuarios.
- **IAM Roles y Policies**: Usar roles y políticas de **AWS IAM** para controlar quién puede invocar la API.