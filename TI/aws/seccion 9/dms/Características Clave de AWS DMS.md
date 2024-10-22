#### 1.1. **Migración de Base de Datos con Tiempo de Inactividad Mínimo**

DMS está diseñado para realizar **migraciones con tiempo de inactividad mínimo**, manteniendo las bases de datos de origen y destino sincronizadas mientras la migración está en curso. Esto permite a las empresas migrar bases de datos de producción sin interrumpir las operaciones críticas del negocio.

#### 1.2. **Soporte para Diversos Motores de Bases de Datos**

DMS admite una amplia gama de bases de datos relacionales y NoSQL, tanto **homogéneas** (por ejemplo, de Oracle a Oracle) como **heterogéneas** (por ejemplo, de MySQL a PostgreSQL). Las bases de datos compatibles incluyen:

- **Bases de datos relacionales**: Amazon RDS, MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, y más.
- **Bases de datos NoSQL**: Amazon DynamoDB, MongoDB.
- **Almacenes de datos**: Amazon Redshift, Amazon S3.

#### 1.3. **Soporte para Migraciones Homogéneas y Heterogéneas**

DMS facilita la **migración homogénea** (de un motor de base de datos a otro idéntico) y la **migración heterogénea** (entre diferentes motores de base de datos). Para migraciones heterogéneas, AWS proporciona **AWS Schema Conversion Tool (AWS SCT)**, que convierte automáticamente el esquema de la base de datos y las consultas SQL al formato del motor de destino.

#### 1.4. **Replicación Continua**

DMS admite la **replicación continua** de datos, lo que permite migrar datos incrementales en tiempo real. Esto asegura que los datos estén constantemente actualizados en la base de datos de destino durante la migración. Es ideal para escenarios de replicación en entornos híbridos o multi-nube.

#### 1.5. **Totalmente Gestionado**

DMS es un servicio **totalmente gestionado**, lo que significa que AWS se encarga de las tareas operativas, como la configuración del servidor, parches, monitoreo y recuperación ante fallos, lo que permite que los usuarios se concentren en la lógica de migración sin preocuparse por la infraestructura subyacente.

#### 1.6. **Automatización de Procesos**

DMS automatiza muchas de las tareas involucradas en una migración de bases de datos, como la replicación de tablas, índices, procedimientos almacenados y otros objetos de la base de datos. La automatización reduce los errores manuales y agiliza el proceso de migración.

#### 1.7. **Monitoreo y Alertas en Tiempo Real**

DMS se integra con **Amazon CloudWatch** para proporcionar monitoreo en tiempo real del estado de la migración, rendimiento y métricas críticas, como el tiempo de latencia y el número de filas replicadas. Puedes configurar **alarmas** para ser notificado de cualquier problema que ocurra durante el proceso de migración.