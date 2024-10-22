#### 2.1. **Clúster de EMR**

El clúster es el corazón de Amazon EMR. Está compuesto por varios nodos que trabajan juntos para ejecutar aplicaciones distribuidas como Hadoop, Spark o Presto. Un clúster típico tiene:

- **Nodo Maestro**: Controla la distribución de tareas y supervisa el estado del clúster. Solo puede haber un nodo maestro por clúster.
- **Nodos Núcleo**: Ejecutan las tareas y almacenan los datos en el sistema de archivos distribuido (HDFS o S3).
- **Nodos de Tareas**: Solo ejecutan tareas de cómputo y no almacenan datos. Se utilizan para escalar la capacidad de procesamiento cuando es necesario.

#### 2.2. **Hadoop Distributed File System (HDFS)**

Aunque EMR se integra de manera nativa con S3 para el almacenamiento de datos, también puede utilizar **HDFS**, el sistema de archivos distribuido de Hadoop, para almacenar temporalmente los datos procesados en el clúster. Sin embargo, S3 es más comúnmente utilizado debido a su durabilidad y costos más bajos.

#### 2.3. **Amazon EMR File System (EMRFS)**

EMRFS permite a los clústeres de Amazon EMR interactuar directamente con **Amazon S3** para almacenar datos. Actúa como una extensión de HDFS, pero con las ventajas de la escalabilidad y durabilidad de S3.