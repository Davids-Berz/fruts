- **Usuarios**:
    
    - Representan a una persona o entidad que interactúa con los servicios de AWS.
    - Cada usuario puede tener un conjunto único de credenciales, como una contraseña para la consola de administración de AWS o claves de acceso para la API y CLI de AWS.
- **Grupos**:
    
    - Conjuntos de usuarios que tienen permisos similares.
    - Los permisos asignados a un grupo se aplican a todos los usuarios miembros de ese grupo.
- **Roles**:
    
    - Conjuntos de permisos que pueden ser asumidos por cualquier entidad confiable (usuarios, servicios de AWS, etc.).
    - Permiten delegar acceso a recursos de AWS sin compartir credenciales a largo plazo.
- **Políticas**:
    
    - Documentos JSON que especifican permisos, detallando qué acciones están permitidas o denegadas sobre qué recursos.
    - Se pueden adjuntar a usuarios, grupos o roles.
- **MFA (Autenticación Multifactor)**:
    
    - Añade una capa extra de seguridad, requiriendo que los usuarios proporcionen no solo su contraseña sino también un código generado por un dispositivo MFA.