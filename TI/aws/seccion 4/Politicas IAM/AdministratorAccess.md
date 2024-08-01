#politicas
**AdministratorAccess**

- **Descripción**: Proporciona acceso completo a todos los servicios y recursos de AWS.
- **Uso**: Se utiliza para usuarios que necesitan administrar completamente la cuenta de AWS.
- **Ejemplo de Política**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "*",
      "Resource": "*"
    }
  ]
}
```
