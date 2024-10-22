#### 4.1. **Cifrado de Datos en Reposo y en Tránsito**

QLDB cifra todos los datos en reposo utilizando **AWS Key Management Service (KMS)**. Los datos en tránsito entre QLDB y las aplicaciones también están protegidos mediante **SSL/TLS** para garantizar la seguridad de las comunicaciones.

#### 4.2. **Control de Acceso Granular con IAM**

QLDB se integra con **AWS Identity and Access Management (IAM)** para definir permisos granulares sobre quién puede acceder, consultar o modificar datos en el libro mayor. Las políticas de IAM permiten controlar el acceso a nivel de tabla, permitiendo una gestión detallada de la seguridad.

#### 4.3. **Auditoría con AWS CloudTrail**

Todas las actividades de los usuarios y las transacciones realizadas en QLDB pueden ser auditadas utilizando **AWS CloudTrail**, lo que permite realizar un seguimiento detallado de todas las interacciones con la base de datos para cumplir con los requisitos de auditoría y seguridad.