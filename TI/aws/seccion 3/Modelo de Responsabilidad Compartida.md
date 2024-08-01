El modelo de responsabilidad compartida en Amazon Web Services (AWS) establece qué responsabilidades son gestionadas por AWS y cuáles son responsabilidad del cliente. Este modelo ayuda a garantizar la seguridad y el cumplimiento de los recursos en la nube, aclarando qué aspectos de la infraestructura y la seguridad son gestionados por el proveedor de servicios en la nube y cuáles son responsabilidad del usuario.

### Responsabilidades de AWS

AWS se encarga de la **seguridad de la nube**, lo que incluye:

1. **Seguridad de la Infraestructura**:
    
    - Gestión de hardware, software, redes y centros de datos que ejecutan los servicios de AWS.
    - Mantenimiento de la infraestructura física y virtual.
2. **Seguridad Física**:
    
    - Protección de los centros de datos físicos contra accesos no autorizados.
    - Redundancia y recuperación ante desastres a nivel de centro de datos.
3. **Red de Infraestructura**:
    
    - Configuración y mantenimiento de la red de infraestructura.
    - Protección contra ataques DDoS y otras amenazas a nivel de red.
4. **Capa de Virtualización**:
    
    - Gestión y seguridad del hipervisor y los servicios de virtualización.
    - Mantenimiento y actualización de la capa de virtualización.
5. **Cumplimiento y Certificaciones**:
    
    - Adherencia a estándares de seguridad y normativas de cumplimiento (ISO 27001, SOC 1/2/3, GDPR, etc.).


### Responsabilidades del Cliente <a id="cliente-responsabilidades"></a>

El cliente se encarga de la **seguridad en la nube**, lo que incluye:

1. **Gestión de Identidades y Accesos (IAM)**:
    
    - Configuración y gestión de políticas de IAM para controlar el acceso a los recursos.
    - Implementación de la autenticación multifactor (MFA) y otras medidas de seguridad de acceso.
2. **Seguridad de los Datos**:
    
    - Cifrado de datos en tránsito y en reposo.
    - Gestión de claves de cifrado utilizando AWS Key Management Service (KMS) u otras soluciones.
3. **Configuración de la Red**:
    
    - Configuración y gestión de subredes, grupos de seguridad, y listas de control de acceso (ACLs).
    - Configuración de VPNs y otras soluciones de red seguras.
4. **Gestión de Sistemas Operativos y Aplicaciones**:
    
    - Instalación y actualización de sistemas operativos en las instancias EC2.
    - Gestión y actualización de aplicaciones, middleware y bases de datos.
5. **Monitoreo y Loggin**:
    
    - Configuración y gestión de Amazon CloudWatch, AWS CloudTrail y otros servicios de monitoreo y registro.
    - Implementación de alertas y respuesta a incidentes.
6. **Control de Configuraciones y Cumplimiento**:
    
    - Utilización de AWS Config para auditoría y gestión de configuraciones.
    - Asegurarse de que los recursos y configuraciones cumplan con las políticas internas y regulaciones externas.

### Ejemplos del Modelo de Responsabilidad Compartida <a id="ejemplos-responsabilidad"></a>

#### 1. **Amazon EC2**

- **AWS Gestiona**: Infraestructura física, virtualización, redes y seguridad física de los centros de datos.
- **Cliente Gestiona**: Seguridad del sistema operativo huésped (parches y actualizaciones), firewall de software, configuración de red, IAM, y seguridad de datos.

#### 2. **Amazon S3**

- **AWS Gestiona**: Infraestructura física y lógica de almacenamiento, red, y redundancia de datos.
- **Cliente Gestiona**: Gestión de políticas de acceso, cifrado de datos, y configuración de bucket policies y ACLs.

#### 3. **Amazon RDS**

- **AWS Gestiona**: Infraestructura física, red, sistema operativo, motor de base de datos (parches y actualizaciones automáticas), y backups automatizados.
- **Cliente Gestiona**: Gestión de la base de datos (esquemas, índices, usuarios), IAM, seguridad de la conexión (SSL), y cifrado de datos.

### Diagrama del Modelo de Responsabilidad Compartida

Para ilustrar mejor este modelo, a continuación se presenta un diagrama simple:

![[responsabilidad-compartida.png]]

### Beneficios del Modelo de Responsabilidad Compartida

1. **Claridad en la Seguridad**:
    
    - Define claramente las responsabilidades de AWS y del cliente, lo que facilita la implementación de medidas de seguridad efectivas.
2. **Mejora en la Gestión de Riesgos**:
    
    - Permite a las organizaciones enfocarse en la seguridad de sus aplicaciones y datos, mientras AWS gestiona la seguridad de la infraestructura subyacente.
3. **Cumplimiento Normativo**:
    
    - Ayuda a las organizaciones a cumplir con regulaciones y estándares de seguridad mediante la colaboración con AWS.
4. **Escalabilidad y Flexibilidad**:
    
    - Permite a las organizaciones escalar sus operaciones y adoptar nuevas tecnologías sin comprometer la seguridad.

El modelo de responsabilidad compartida de AWS es fundamental para entender cómo gestionar y asegurar los recursos en la nube de manera efectiva. Al conocer y asumir las responsabilidades adecuadas, las organizaciones pueden maximizar la seguridad y eficiencia de sus operaciones en la nube.