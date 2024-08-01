- **Uso de Claves SSH**:
    
    - Genera un par de claves (pública y privada) usando `ssh-keygen` y almacena la clave pública en `~/.ssh/authorized_keys` en el servidor.
    - Mantén la clave privada segura y no la compartas.
- **Deshabilitar Autenticación por Contraseña**:
    
    - Configura el servidor SSH para deshabilitar la autenticación basada en contraseñas añadiendo o modificando la línea `PasswordAuthentication no` en `/etc/ssh/sshd_config`.
- **Autenticación Multifactor (MFA)**:
    
    - Utiliza MFA para agregar una capa adicional de seguridad.
- **Cambio del Puerto SSH Predeterminado**:
    
    - Cambia el puerto predeterminado 22 a otro puerto menos conocido para evitar ataques de fuerza bruta comunes.