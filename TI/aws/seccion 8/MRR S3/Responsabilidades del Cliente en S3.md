Los clientes son responsables de **seguridad en la nube**, lo que significa que son responsables de la seguridad de los datos que almacenan en S3 y de la forma en que configuran y utilizan los servicios proporcionados por AWS. Las áreas clave de responsabilidad del cliente incluyen:

#### 1. **Gestión de Identidades y Acceso (IAM)**:

- El cliente es responsable de definir y gestionar quién tiene acceso a los recursos en S3. Esto implica:
    - Crear políticas de control de acceso a los buckets (bucket policies) y listas de control de acceso (ACLs).
    - Configurar y aplicar políticas de IAM para usuarios, grupos y roles, controlando qué acciones pueden realizar en los buckets y objetos.
    - Usar **MFA (Autenticación Multifactor)** para proteger las cuentas y credenciales sensibles.
    - Implementar **bloqueo de acceso público** para prevenir que los buckets se expongan inadvertidamente.

#### 2. **Cifrado de Datos en Reposo**:

- Aunque AWS puede manejar el cifrado si se habilita, el cliente debe decidir si habilitar o no el cifrado y qué método usar:
    - **SSE-S3** (claves gestionadas por Amazon S3).
    - **SSE-KMS** (claves gestionadas por AWS Key Management Service).
    - **SSE-C** (claves proporcionadas por el cliente).
- El cliente debe gestionar las claves en el caso de usar **SSE-C** o **KMS**, controlando su rotación y acceso.

#### 3. **Cifrado de Datos en Tránsito**:

- El cliente debe garantizar que todas las comunicaciones con Amazon S3 estén cifradas mediante HTTPS (SSL/TLS) para proteger los datos mientras se transfieren entre el cliente y el bucket.
- El cliente puede configurar políticas para denegar cualquier solicitud que no utilice HTTPS, protegiendo así las comunicaciones.

#### 4. **Configuración de Políticas de Retención y Replicación**:

- El cliente es responsable de definir políticas de ciclo de vida y replicación para gestionar la retención de datos y el movimiento entre regiones.
- Usar **S3 Object Lock** para garantizar la inmutabilidad de los objetos, y **S3 Glacier Vault Lock** para proteger los datos archivados contra eliminaciones prematuras.

#### 5. **Monitoreo y Auditoría**:

- Los clientes deben configurar y monitorear el acceso a sus datos mediante herramientas como:
    - **AWS CloudTrail**: Para registrar todas las solicitudes realizadas a Amazon S3, lo que permite auditar quién accedió o modificó los datos.
    - **Amazon CloudWatch**: Para monitorear el uso de los buckets y crear alertas en función de actividades sospechosas o inusuales.
    - **Amazon Macie**: Para descubrir y proteger datos sensibles almacenados en S3, asegurando que no estén expuestos inadvertidamente.

#### 6. **Protección contra Eliminaciones Accidentales o Maliciosas**:

- Configurar **versionado de objetos** en S3 para mantener un historial de versiones de los objetos y permitir la recuperación de datos en caso de eliminación accidental o modificación no autorizada.
- Usar **S3 Object Lock** para prevenir la eliminación de objetos durante un período específico de tiempo, protegiendo los datos sensibles o críticos.

#### 7. **Control de Acceso Basado en IP y Condiciones**:

- El cliente puede aplicar restricciones adicionales utilizando condiciones en las políticas de acceso, como limitar el acceso a los buckets solo desde rangos de IP específicos, o requerir que las solicitudes se realicen a través de HTTPS.