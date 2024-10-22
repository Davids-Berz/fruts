#### 4.1. **Cifrado en Reposo y en Tránsito**

- **Cifrado en reposo**: Neptune cifra los datos en reposo utilizando **AWS KMS**, asegurando que los datos almacenados estén protegidos contra accesos no autorizados.
- **Cifrado en tránsito**: Neptune cifra los datos en tránsito entre las aplicaciones y la base de datos mediante **SSL/TLS**.

#### 4.2. **Control de Acceso con IAM**

- **Autenticación y Autorización**: Neptune se integra con **AWS IAM** para controlar el acceso a la base de datos. Puedes definir permisos detallados para controlar qué usuarios y aplicaciones pueden realizar operaciones de lectura, escritura o administración sobre los grafos.

#### 4.3. **Implementación en Amazon VPC**

- Neptune puede ser implementado dentro de una **Amazon Virtual Private Cloud (VPC)** para asegurar que las conexiones a la base de datos sean privadas y estén controladas mediante configuraciones de red específicas. Esto permite aislar la base de datos y definir reglas de acceso basadas en IP o subredes.