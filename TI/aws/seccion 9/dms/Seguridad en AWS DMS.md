#### 4.1. **Cifrado de Datos en Reposo y en Tránsito**

DMS cifra los datos tanto en **reposo** como en **tránsito** para garantizar que las migraciones y réplicas sean seguras. Puedes habilitar el cifrado para las bases de datos de destino utilizando **AWS Key Management Service (KMS)**, y los datos en tránsito están protegidos mediante **SSL/TLS**.

#### 4.2. **Control de Acceso con IAM**

DMS se integra con **AWS Identity and Access Management (IAM)** para controlar quién tiene acceso a las tareas de migración y los endpoints de base de datos. Las políticas de IAM permiten definir permisos detallados para usuarios y roles.

#### 4.3. **Red Privada con VPC**

DMS puede ejecutarse dentro de una **Amazon Virtual Private Cloud (VPC)**, lo que garantiza que las migraciones estén aisladas y protegidas en una red privada. Esto permite migrar datos entre bases de datos que están en diferentes entornos de red sin exponer los datos a internet.