#Principal 

AWS Identity and Access Management (IAM) es un servicio web que ayuda a controlar de forma segura el acceso a los recursos de AWS. IAM permite gestionar usuarios, grupos, roles y permisos para controlar quién puede acceder a qué recursos en la nube de AWS. A continuación se describen sus componentes y funcionalidades principales:

- [[Componentes de IAM]]
- [[Funcionalidades de IAM]]
- [[Ejemplos de Uso]]
- [[Beneficios de IAM]]

[[Estructura de una Política de IAM]]

## Politicas IAM

### Políticas Gestionadas de AWS

1. [[AdministratorAccess]]
2. [[PowerUserAccess]]
3. [[ReadOnlyAccess]]
4. [[AmazonS3FullAccess]]
5. [[AmazonEC2FullAccess]]
6. [[AWSLambdaExecute]]
7. [[Política Personalizada para Acceso Limitado a S3]]
8. [[Política Personalizada para Acceso Específico a EC2]]

### Consideraciones de Seguridad

- **Principio de Privilegio Mínimo**: Siempre otorgar el mínimo conjunto de permisos necesarios para realizar una tarea específica.
- **Revisión Regular**: Revisar y ajustar las políticas regularmente para asegurar que siguen siendo necesarias y no otorgan permisos excesivos.
- **Uso de Grupos y Roles**: En lugar de asignar políticas directamente a usuarios individuales, utilizar grupos y roles para una gestión más eficiente y segura de permisos.
- **Implementación de MFA**: Asegurar que se utiliza autenticación multifactor (MFA) para acceder a recursos críticos.

Las políticas de IAM son esenciales para gestionar el acceso a los recursos de AWS de manera segura y efectiva. La elección y configuración adecuada de estas políticas es fundamental para mantener la seguridad y el cumplimiento en la nube.

## Política de contraseñas de AWS IAM

La política de contraseñas de AWS IAM (Identity and Access Management) permite a los administradores establecer reglas que rigen la complejidad, longitud, y renovación de las contraseñas para los usuarios que acceden a la consola de administración de AWS. Configurar una política de contraseñas robusta es esencial para mejorar la seguridad de las cuentas de usuario.

- [[Configuración de la Política de Contraseñas]]

### La Autenticación Multifactor (MFA)

La Autenticación Multifactor (MFA) en AWS Identity and Access Management (IAM) agrega una capa adicional de protección a la seguridad de las cuentas de usuario. MFA requiere que los usuarios proporcionen no solo una contraseña o clave de acceso, sino también un código de autenticación generado por un dispositivo MFA, lo que reduce significativamente el riesgo de acceso no autorizado en caso de que las credenciales se vean comprometidas.

### Componentes de MFA en AWS

1. **Dispositivos MFA**:
    
    - **MFA Basada en Hardware**: Dispositivos físicos que generan códigos de autenticación (e.g., llave Yubikey).
    - **MFA Virtual**: Aplicaciones móviles que generan códigos de autenticación (e.g., Google Authenticator, Authy).
2. **Códigos MFA**:
    
    - **Códigos de Autenticación Temporal**: Códigos de 6 dígitos generados por el dispositivo MFA, válidos por un corto período (generalmente 30 segundos).


- [[Configuración de MFA para Usuarios de IAM]]

## Los roles de IAM (Identity and Access Management) en AWS

Los roles de IAM (Identity and Access Management) en AWS son conjuntos de permisos que los servicios de AWS pueden asumir para acceder a otros recursos de AWS. Los roles permiten delegar acceso sin compartir credenciales, lo que mejora la seguridad y la gestión de acceso. A continuación, se explica en detalle cómo funcionan los roles de IAM, cómo se configuran y algunos casos de uso comunes.

### Conceptos Claves de Roles de IAM

1. **Assume Role**: El proceso mediante el cual una entidad (usuario, servicio o aplicación) asume un rol y obtiene las credenciales temporales necesarias para realizar acciones en nombre del rol.
2. **Policy (Política)**: Documento JSON que define los permisos del rol. Incluye las acciones permitidas o denegadas y los recursos a los que se aplican.
3. **Trust Policy (Política de Confianza)**: Documento JSON que especifica qué entidades (usuarios, servicios o cuentas) pueden asumir el rol.

- [[Configuración de Roles de IAM]]

#### Casos de Uso Comunes

1. [[Rol para Instancias EC2]]
2. [[Rol para Funciones Lambda]]
3. [[Rol para AWS Glue]]
4. [[Asumir un Rol]]
5. [[Buenas Prácticas para Roles de IAM]]
6. [[Ventajas de Usar Roles de IAM]]

## Herramientas de Seguridad IAM

AWS Identity and Access Management (IAM) proporciona diversas herramientas y características que ayudan a asegurar la infraestructura en la nube. Aquí se describen algunas de las herramientas de seguridad más importantes en IAM y cómo pueden utilizarse para fortalecer la seguridad de los recursos de AWS.

1. [[IAM Policies]]
2. [[IAM Roles]]
3. [[IAM Groups]]
4. [[IAM Users]]
5. [[IAM Policies Simulator]]
6. [[IAM Access Analyzer]]
7. [[Credential Report]]
8. [[AWS CloudTrail]]
9. [[Multi-Factor Authentication (MFA)]]
10. [[Buenas Prácticas de Seguridad en IAM]]

## Modelo de la responsabilidad Compartida

El modelo de responsabilidad compartida de AWS IAM (Identity and Access Management) establece claramente las responsabilidades que son gestionadas por AWS y aquellas que son responsabilidad del cliente. Este modelo asegura que tanto el proveedor como el usuario comprendan sus roles en la seguridad y administración de los recursos en la nube.

- [[Modelo de Responsabilidad Compartida]]
