#### 1.1. **Compatibilidad con MongoDB**

Amazon DocumentDB es compatible con la API de MongoDB, lo que permite a los desarrolladores usar el mismo código de las aplicaciones, controladores y herramientas que se utilizan con MongoDB. DocumentDB admite versiones de MongoDB hasta la 3.6, 4.0 y 5.0, lo que facilita la migración de aplicaciones MongoDB existentes sin cambios significativos en la base de datos.

#### 1.2. **Arquitectura Escalable y Alta Disponibilidad**

DocumentDB está diseñado para escalar automáticamente tanto en almacenamiento como en capacidad de procesamiento:

- **Almacenamiento Escalable**: El almacenamiento crece automáticamente hasta 64 TB sin necesidad de gestión manual.
- **Clúster Multi-AZ**: DocumentDB replica los datos en **tres zonas de disponibilidad (AZs)** de forma automática para garantizar alta disponibilidad y durabilidad. En caso de fallos, se realiza un failover automático hacia una réplica en otra zona de disponibilidad.

#### 1.3. **Escalado de Lecturas con Réplicas**

Puedes añadir hasta **15 réplicas de lectura** a un clúster de DocumentDB, lo que permite escalar horizontalmente las operaciones de lectura. Las réplicas de lectura permiten distribuir las consultas de lectura entre varias instancias, mejorando el rendimiento y reduciendo la latencia para aplicaciones con muchas operaciones de lectura.

#### 1.4. **Totalmente Gestionado**

Amazon DocumentDB es un servicio totalmente gestionado, lo que significa que AWS se encarga de tareas como la **configuración de la base de datos**, el **parcheo**, el **backup**, la **recuperación** y el **monitoreo**. Esto permite a los desarrolladores concentrarse en el diseño y desarrollo de aplicaciones, sin preocuparse por la administración de la base de datos.

#### 1.5. **Consultas y Procesamiento Rápidos**

DocumentDB está optimizado para **consultas rápidas** en datos documentales de JSON. La arquitectura está diseñada para manejar grandes cargas de trabajo con bajas latencias, permitiendo un procesamiento eficiente de grandes volúmenes de datos.

#### 1.6. **Backup Automático y Recuperación en un Punto en el Tiempo**

DocumentDB realiza **backups automáticos continuos** de los datos y permite la recuperación hasta un punto en el tiempo dentro de los últimos 35 días. Los backups se almacenan en **Amazon S3** y no afectan al rendimiento de la base de datos, ya que no requieren paradas ni impacto en el tráfico.

#### 1.7. **Seguridad Avanzada**

DocumentDB proporciona varias capas de seguridad para proteger los datos, incluyendo:

- **Cifrado en reposo** con **AWS Key Management Service (KMS)**.
- **Cifrado en tránsito** utilizando SSL/TLS.
- **Control de acceso granular** mediante **AWS Identity and Access Management (IAM)** para gestionar permisos detallados sobre quién puede acceder a la base de datos y a los datos.

#### 1.8. **Integración con AWS Services**

DocumentDB se integra con otros servicios de AWS como **Amazon CloudWatch** para monitorear el rendimiento de la base de datos, **AWS CloudTrail** para auditar actividades, y **Amazon VPC** para aislar las bases de datos en una red privada segura.