1. **Almacenamiento de Objetos**:
    
    - S3 almacena datos como objetos dentro de "buckets" (contenedores). Cada objeto se compone de datos, metadatos y una clave única que lo identifica dentro del bucket.
    - Los objetos pueden ser cualquier tipo de archivo: texto, imágenes, videos, archivos de aplicación, backups, etc.

2. **Escalabilidad Automática**:
    
    - S3 es un servicio altamente escalable que puede manejar un volumen ilimitado de datos. No es necesario preaprovisionar capacidad, ya que S3 crece automáticamente con la demanda.

3. **Durabilidad y Disponibilidad**:
    
    - S3 está diseñado para ofrecer una durabilidad del 99.999999999% (11 nueves) y una alta disponibilidad mediante la replicación automática de datos en múltiples ubicaciones geográficas dentro de una región.

4. **Control de Acceso y Seguridad**:
    
    - S3 ofrece un control granular sobre el acceso a los datos a través de políticas de bucket, listas de control de acceso (ACL), y la integración con AWS Identity and Access Management (IAM).
    - Además, los datos pueden ser cifrados tanto en reposo como en tránsito utilizando claves gestionadas por AWS o claves propias del cliente.

5. **Versionado y Gestión del Ciclo de Vida**:
    
    - S3 soporta el versionado de objetos, lo que permite mantener múltiples versiones de un objeto en un bucket. Esto es útil para proteger contra la eliminación accidental o la corrupción de datos.
    - La gestión del ciclo de vida permite definir políticas para mover datos entre diferentes clases de almacenamiento o eliminarlos automáticamente después de un cierto período.

6. **Clases de Almacenamiento**:
    
    - S3 ofrece diferentes clases de almacenamiento para optimizar costos y rendimiento:
        - **S3 Standard**: Almacenamiento de uso general para datos que se acceden frecuentemente.
        - **S3 Intelligent-Tiering**: Mueve automáticamente los datos entre niveles de almacenamiento de acceso frecuente e infrecuente basado en patrones de acceso.
        - **S3 Standard-IA (Infrequent Access)**: Para datos a los que se accede con poca frecuencia pero que requieren un acceso rápido cuando son necesarios.
        - **S3 One Zone-IA**: Almacenamiento de bajo costo en una única zona de disponibilidad para datos a los que se accede con poca frecuencia.
        - **S3 Glacier**: Almacenamiento de bajo costo para archivado de datos con tiempos de recuperación que van desde minutos hasta horas.
        - **S3 Glacier Deep Archive**: La opción de almacenamiento más económica para datos a los que raramente se accede, con tiempos de recuperación de 12 horas.

7. **Eventos y Notificaciones**:
    
    - S3 puede enviar notificaciones basadas en eventos cuando ocurren ciertas acciones en un bucket, como la creación, eliminación o replicación de un objeto. Estas notificaciones se pueden integrar con otros servicios de AWS como Lambda, SNS o SQS.

8. **Integración con Otros Servicios de AWS**:
    
    - S3 se integra de manera fluida con otros servicios de AWS como Amazon CloudFront para la distribución de contenido, AWS Lambda para procesamiento de datos en tiempo real, Amazon Athena para consultas SQL directamente sobre los datos en S3, y muchos más.