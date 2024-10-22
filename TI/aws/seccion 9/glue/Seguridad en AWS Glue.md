#### 4.1. **Cifrado de Datos en Reposo y en Tránsito**

AWS Glue cifra los datos tanto en reposo como en tránsito para garantizar la seguridad de los datos procesados. Utiliza **AWS Key Management Service (KMS)** para administrar claves de cifrado y proteger los datos almacenados en S3, Redshift, y otras fuentes de datos.

#### 4.2. **Control de Acceso con IAM**

AWS Glue se integra con **AWS Identity and Access Management (IAM)**, lo que permite definir permisos detallados sobre quién puede acceder y ejecutar trabajos de ETL, descubrir datos y consultar el Catálogo de Datos.

#### 4.3. **VPC y Seguridad de Red**

Glue puede ejecutarse dentro de una **Amazon Virtual Private Cloud (VPC)**, lo que garantiza que el procesamiento de datos esté aislado y controlado a nivel de red. Esto asegura que solo las fuentes y destinos autorizados puedan acceder a los datos procesados por Glue.