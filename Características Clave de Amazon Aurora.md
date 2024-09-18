- **Alto Rendimiento**:
    
    - Aurora ofrece hasta **5 veces más rendimiento** que MySQL estándar y hasta **3 veces más** que PostgreSQL, manteniendo la compatibilidad con ambos motores.
    - Es capaz de procesar millones de lecturas y escrituras por segundo, lo que lo hace ideal para aplicaciones intensivas en datos.
- **Alta Disponibilidad y Escalabilidad**:
    
    - **Multi-AZ y Multi-Region**: Aurora replica los datos automáticamente en seis copias distribuidas en tres zonas de disponibilidad, garantizando alta disponibilidad.
    - **Auto Scaling de Lectura**: Permite hasta 15 réplicas de lectura distribuidas en múltiples regiones, lo que mejora el rendimiento de lectura y reduce la latencia.
    - **Escalabilidad Automática de Almacenamiento**: El almacenamiento en Aurora escala automáticamente en incrementos de 10 GB según las necesidades de la aplicación, hasta un máximo de 128 TB, sin interrumpir las operaciones.
- **Recuperación y Respaldo**:
    
    - **Backups Continuos**: Aurora realiza copias de seguridad automáticas y continuas en Amazon S3, lo que permite recuperar datos hasta cualquier punto en el tiempo.
    - **Recuperación Ante Fallos**: Si una zona de disponibilidad falla, Aurora redirige automáticamente el tráfico a una réplica en otra zona de disponibilidad sin tiempo de inactividad apreciable.
- **Compatibilidad con MySQL y PostgreSQL**:
    
    - **Aurora MySQL-Compatible Edition**: Totalmente compatible con MySQL, lo que permite migraciones de bases de datos MySQL a Aurora sin cambios significativos en el código.
    - **Aurora PostgreSQL-Compatible Edition**: Totalmente compatible con PostgreSQL, lo que facilita la migración desde PostgreSQL a Aurora, con mejoras en el rendimiento y la escalabilidad.
- **Seguridad**:
    
    - **Cifrado de Datos en Reposo y en Tránsito**: Aurora cifra automáticamente los datos utilizando claves de KMS, tanto en reposo como en tránsito.
    - **Integración con IAM y VPC**: Aurora permite controlar el acceso a las bases de datos utilizando IAM, y puede implementarse en Amazon VPC para mayor control sobre la red.