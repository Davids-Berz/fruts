#### 1.1. **Totalmente Gestionado**

DynamoDB es un servicio administrado por AWS que elimina la necesidad de tareas operativas como la provisión de hardware, la instalación de software, la gestión de parches, la replicación, las copias de seguridad y la recuperación. Esto permite a los desarrolladores centrarse en el diseño y desarrollo de aplicaciones sin preocuparse por la infraestructura.

#### 1.2. **Alto Rendimiento con Escalabilidad Automática**

DynamoDB puede gestionar millones de solicitudes por segundo, escalando automáticamente según el tráfico de la aplicación. Puedes configurar el modo **auto scaling** para ajustar la capacidad de lectura y escritura automáticamente en función de la carga de trabajo.

#### 1.3. **Baja Latencia Consistente**

DynamoDB ofrece una latencia de respuesta en **milisegundos** para operaciones de lectura y escritura, incluso bajo cargas de tráfico muy altas. Esto lo hace adecuado para aplicaciones críticas donde la velocidad y la consistencia son esenciales.

#### 1.4. **Almacenamiento de Documentos y Clave-Valor**

- DynamoDB es compatible con el almacenamiento de datos de **clave-valor** y **documentos**. Los datos se almacenan en **tablas** que contienen **elementos** (filas) y **atributos** (columnas).
- DynamoDB admite estructuras de datos flexibles, lo que significa que cada elemento en una tabla no necesita tener los mismos atributos que otro.

#### 1.5. **Alta Disponibilidad y Tolerancia a Fallos**

- DynamoDB garantiza alta disponibilidad y durabilidad replicando los datos de forma automática en **múltiples zonas de disponibilidad (AZs)** dentro de una región de AWS.
- Con **DynamoDB Global Tables**, puedes replicar datos automáticamente entre varias regiones para asegurar la disponibilidad global y baja latencia.

#### 1.6. **Modelos de Consistencia de Lectura**

DynamoDB permite a los usuarios elegir entre dos modelos de consistencia:

- **Lecturas Eventualmente Consistentes**: Garantizan la alta disponibilidad y la baja latencia, pero es posible que los datos no estén completamente actualizados de forma inmediata.
- **Lecturas Fuertemente Consistentes**: Garantizan que las lecturas devuelvan los datos más actualizados, aunque pueden implicar un mayor tiempo de respuesta.

#### 1.7. **Integración con otros Servicios de AWS**

DynamoDB se integra perfectamente con otros servicios de AWS, como **Lambda**, **API Gateway**, **CloudWatch**, **S3**, y **IAM**. Estas integraciones permiten construir aplicaciones sin servidor y gestionar de manera más efectiva las operaciones de monitoreo y seguridad.

#### 1.8. **Índices Secundarios**

DynamoDB permite definir **Índices Secundarios** (Global Secondary Index y Local Secondary Index) para realizar consultas más avanzadas que no dependan solo de la clave primaria, lo que proporciona flexibilidad adicional para consultar los datos.

#### 1.9. **Eventos con DynamoDB Streams**

DynamoDB Streams captura cambios en la tabla en tiempo real, lo que permite activar eventos mediante **AWS Lambda** para crear aplicaciones reactivas. Por ejemplo, puedes procesar una actualización en la base de datos o replicar datos en otras regiones usando Streams.