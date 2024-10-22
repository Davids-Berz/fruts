#### 1.1. **Serverless (Sin Servidor)**

Athena es completamente **sin servidor**, lo que significa que no necesitas gestionar ni aprovisionar ninguna infraestructura. Simplemente cargas tus datos en S3, defines un esquema, y puedes comenzar a ejecutar consultas SQL. AWS maneja toda la infraestructura en segundo plano, lo que permite a los usuarios centrarse exclusivamente en el análisis de datos.

#### 1.2. **Compatibilidad con SQL**

Athena permite ejecutar consultas utilizando **SQL estándar**, lo que facilita su uso para cualquier persona familiarizada con SQL. Las consultas pueden incluir operaciones complejas como agregaciones, uniones y filtros para analizar datos sin necesidad de conocimiento especializado en desarrollo.

#### 1.3. **Consulta Directa sobre Datos en S3**

Athena puede ejecutar consultas directamente sobre datos almacenados en **Amazon S3** sin necesidad de cargarlos o transformarlos previamente. Esto reduce la necesidad de mover grandes volúmenes de datos y permite un análisis rápido y económico.

- **Soporte para Múltiples Formatos de Datos**: Athena admite una variedad de formatos de datos populares, como **CSV**, **JSON**, **Parquet**, **ORC**, **Avro**, entre otros.

#### 1.4. **Integración con AWS Glue**

Athena se integra con **AWS Glue**, un servicio de ETL y catálogo de datos. AWS Glue puede catalogar los datos en S3, facilitando el descubrimiento y organización de los mismos. El catálogo de datos de Glue actúa como un **meta-store**, permitiendo a Athena consultar los datos almacenados en S3 como si fueran una base de datos tradicional.

#### 1.5. **Pago por Consulta**

Athena es un servicio de **pago por consulta**, lo que significa que solo pagas por las consultas que ejecutas. El precio se basa en la cantidad de datos escaneados por cada consulta, lo que incentiva la optimización de consultas y la compresión de los datos para minimizar los costos.

#### 1.6. **Cifrado y Seguridad**

Athena admite el **cifrado de datos en reposo** en S3 utilizando **AWS Key Management Service (KMS)**, lo que garantiza la seguridad de los datos almacenados. También puedes proteger los datos en tránsito utilizando **TLS** para todas las consultas.

- **Control de Acceso Granular con IAM**: Puedes controlar quién tiene acceso a Athena y a los datos en S3 mediante **AWS Identity and Access Management (IAM)**, definiendo políticas detalladas para consultas y acceso a datos.

#### 1.7. **Alta Disponibilidad**

Athena es un servicio altamente disponible que ejecuta las consultas en una infraestructura distribuida. AWS garantiza que el servicio esté disponible y que las consultas se ejecuten con baja latencia.

#### 1.8. **Soporte para Particiones**

Athena admite **particionamiento de datos**, lo que permite dividir los datos en categorías lógicas (por ejemplo, por fecha, región o tipo de archivo) para mejorar la eficiencia de las consultas. Cuando consultas un subconjunto específico de los datos, Athena escanea solo las particiones necesarias, lo que reduce el costo y mejora el rendimiento de las consultas.