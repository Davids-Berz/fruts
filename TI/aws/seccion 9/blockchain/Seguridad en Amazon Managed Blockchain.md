#### 3.1. **Cifrado en Reposo y en Tránsito**

Todos los datos en Managed Blockchain están **cifrados en reposo** utilizando **AWS Key Management Service (KMS)**. Los datos en tránsito entre los nodos también están protegidos mediante **SSL/TLS**, lo que asegura que las transacciones sean seguras.

#### 3.2. **Control de Acceso con IAM**

Managed Blockchain se integra con **AWS Identity and Access Management (IAM)**, lo que permite gestionar el acceso a los nodos y definir políticas detalladas sobre quién puede crear, unirse y administrar redes de blockchain. Puedes otorgar permisos granulares basados en roles de usuario, asegurando que solo los usuarios autorizados puedan interactuar con la red.

#### 3.3. **Auditoría y Monitoreo**

Con **AWS CloudTrail**, todas las acciones realizadas en Managed Blockchain, como la creación de nodos o la validación de transacciones, pueden ser auditadas. Esto permite rastrear el historial completo de acciones y eventos para garantizar la transparencia y cumplir con normativas de seguridad y auditoría.

#### 3.4. **Red Privada con Amazon VPC**

Puedes implementar Managed Blockchain dentro de una **Amazon Virtual Private Cloud (VPC)** para asegurar que los nodos de blockchain estén aislados y controlados dentro de un entorno de red privado, lo que añade una capa adicional de seguridad.