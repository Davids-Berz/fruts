#### 1.1. **ETL Totalmente Gestionado**

AWS Glue automatiza muchas de las tareas relacionadas con los procesos ETL. Puedes descubrir datos, definir esquemas, transformar y mover datos entre distintas fuentes sin necesidad de aprovisionar servidores o gestionar la infraestructura.

#### 1.2. **Catálogo de Datos**

AWS Glue incluye un **Catálogo de Datos** centralizado que actúa como un repositorio de metadatos para todas las fuentes de datos. Este catálogo permite descubrir y organizar tus datos para su posterior consulta y análisis. Cada vez que Glue realiza un proceso ETL, el catálogo se actualiza automáticamente con información sobre los esquemas y las tablas de los datos.

- **Descubrimiento Automático de Esquemas**: Glue puede explorar automáticamente las fuentes de datos, como archivos en Amazon S3 o bases de datos relacionales, y generar esquemas y particiones.

#### 1.3. **Transformaciones ETL Flexibles**

AWS Glue te permite realizar transformaciones complejas sobre los datos utilizando scripts en **Python** o **Scala**, que se ejecutan sobre **Apache Spark** en un entorno gestionado. Esto facilita la manipulación de los datos para adaptarlos a las necesidades de análisis, como normalización, filtrado, agregación, y más.

#### 1.4. **Glue Studio: Entorno Visual para ETL**

AWS Glue **Studio** proporciona una interfaz gráfica fácil de usar para crear, visualizar y ejecutar flujos de trabajo ETL. Los usuarios pueden diseñar pipelines de datos con transformaciones arrastrando y soltando componentes, sin necesidad de escribir código manual.

#### 1.5. **Glue DataBrew: Herramienta de Preparación de Datos**

**AWS Glue DataBrew** es una herramienta de preparación de datos visual que permite a los usuarios limpiar y normalizar datos sin necesidad de escribir código. Con DataBrew, los usuarios pueden realizar tareas como eliminar duplicados, formatear datos, tratar valores nulos, y visualizar datos en forma de gráficos para su análisis.

#### 1.6. **Soporte para Múltiples Fuentes de Datos**

Glue admite una amplia variedad de **fuentes de datos** como:

- **Amazon S3**: Para procesar datos no estructurados o semiestructurados.
- **Amazon Redshift**: Para mover o transformar datos de y hacia el almacén de datos de Redshift.
- **Bases de Datos Relacionales**: Conectividad con bases de datos como **Amazon RDS**, **MySQL**, **PostgreSQL**, **Oracle**, **SQL Server**, y **bases de datos on-premise** mediante **AWS Glue Elastic Views**.
- **Datos SaaS y Fuentes Externas**: Glue puede conectarse a fuentes de datos de aplicaciones SaaS (software como servicio) y otras aplicaciones externas.

#### 1.7. **Job Bookmarking**

Glue soporta **job bookmarking**, una característica que permite que los trabajos ETL procesen solo los datos nuevos o modificados desde la última vez que se ejecutaron. Esto es ideal para flujos de datos incrementales o para la sincronización de grandes volúmenes de datos de manera eficiente.

#### 1.8. **Glue Triggers y Flujos de Trabajo**

AWS Glue permite la creación de **triggers** y **flujos de trabajo** que automatizan la ejecución de trabajos ETL en función de eventos o condiciones específicas. Puedes programar trabajos para que se ejecuten en intervalos de tiempo determinados, o activar trabajos basados en la disponibilidad de nuevos datos.