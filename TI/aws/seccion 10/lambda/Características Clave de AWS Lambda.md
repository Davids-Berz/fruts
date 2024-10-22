#### 1.1. **Ejecución Basada en Eventos**

AWS Lambda permite ejecutar código en respuesta a una amplia variedad de eventos, como:

- Cambios en datos almacenados en **Amazon S3**.
- Actualizaciones en bases de datos **DynamoDB**.
- Solicitudes HTTP a través de **Amazon API Gateway**.
- Nuevos mensajes en colas de mensajes como **Amazon SQS** o **Amazon SNS**.
- Procesamiento en tiempo real de datos transmitidos a través de **Amazon Kinesis**.

#### 1.2. **Escalado Automático**

Lambda escala automáticamente para manejar el número de eventos entrantes. No importa si tienes un evento por hora o millones de eventos por segundo, AWS Lambda ajustará automáticamente el número de ejecuciones concurrentes necesarias para manejar la carga.

#### 1.3. **Sin Gestión de Infraestructura**

No es necesario aprovisionar ni gestionar servidores, parches, escalado o administración de infraestructura. AWS Lambda se encarga de la administración de la infraestructura subyacente, lo que permite a los desarrolladores concentrarse en el código.

#### 1.4. **Pago por Uso**

Con Lambda, solo pagas por el tiempo que tu código está en ejecución. Lambda cobra por la cantidad de invocaciones y el tiempo que tarda el código en ejecutarse, medido en incrementos de 1 milisegundo. Esto permite ahorrar costos, especialmente en aplicaciones que no están activas de forma continua.

#### 1.5. **Integración con Otros Servicios de AWS**

Lambda se integra con una gran cantidad de servicios de AWS, permitiendo automatizar tareas, procesar datos, construir APIs y mucho más. Algunas de las integraciones más comunes incluyen:

- **S3**: Ejecutar código al cargar o modificar archivos en un bucket de S3.
- **DynamoDB**: Procesar cambios en una tabla de DynamoDB.
- **API Gateway**: Ejecutar código en respuesta a solicitudes HTTP o WebSocket.
- **CloudWatch**: Automatizar tareas en función de métricas o eventos de monitoreo.

#### 1.6. **Soporte para Múltiples Lenguajes**

Lambda admite varios lenguajes de programación, incluidos **Python**, **Node.js**, **Java**, **C# (a través de .NET Core)**, **Go**, **Ruby**, y **PowerShell**. También puedes traer tu propio entorno de ejecución (custom runtime) para otros lenguajes no soportados de forma nativa.

#### 1.7. **Control de Acceso Granular**

Lambda se integra con **AWS Identity and Access Management (IAM)**, lo que permite definir políticas detalladas para controlar quién puede invocar las funciones y qué recursos pueden acceder las funciones Lambda.

#### 1.8. **Límites Flexibles**

AWS Lambda permite definir los límites de recursos asignados a una función, como la cantidad de **memoria** (desde 128 MB hasta 10 GB) y el tiempo máximo de ejecución (hasta 15 minutos). El uso de CPU se escala proporcionalmente a la cantidad de memoria asignada.