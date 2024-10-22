#### 4.1. **Cifrado en Reposo y en Tránsito**

- DocumentDB cifra los datos en reposo utilizando **AWS Key Management Service (KMS)**. Esto asegura que los datos almacenados estén protegidos incluso si son accedidos físicamente.
- Los datos en tránsito entre la base de datos y las aplicaciones están protegidos mediante **SSL/TLS**, asegurando que la comunicación esté cifrada y sea segura.

#### 4.2. **Control de Acceso con IAM**

DocumentDB se integra con **AWS Identity and Access Management (IAM)** para permitir un control detallado sobre quién puede acceder a las bases de datos. Puedes definir permisos granulares para operaciones como lecturas, escrituras o administración del clúster.

#### 4.3. **Amazon VPC**

Puedes implementar DocumentDB dentro de una **Amazon Virtual Private Cloud (VPC)** para aislar tu base de datos y controlar el tráfico de red entrante y saliente. Esto proporciona una capa adicional de seguridad al permitir que los datos solo sean accesibles desde direcciones IP o redes autorizadas.