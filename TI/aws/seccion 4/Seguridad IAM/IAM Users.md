#seguridad 

**Descripción**: Entidades que representan a personas o aplicaciones que necesitan acceso a recursos de AWS.

**Uso**:

- Crear usuarios con permisos específicos.
- Proveer credenciales seguras (contraseñas, claves de acceso) y habilitar MFA.

**Ejemplo de Creación de Usuario**:

```
aws iam create-user --user-name JohnDoe
aws iam create-login-profile --user-name JohnDoe --password Passw0rd!
```

