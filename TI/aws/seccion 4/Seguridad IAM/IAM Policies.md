#seguridad

**Descripción**: Documentos JSON que definen los permisos para los usuarios, grupos y roles. Las políticas determinan qué acciones pueden realizarse en qué recursos y bajo qué condiciones.

**Uso**:

- Crear políticas granulares que otorguen solo los permisos necesarios (principio de privilegio mínimo).
- Adjuntar políticas a usuarios, grupos y roles para controlar el acceso.

**Ejemplo de Política**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "arn:aws:s3:::example-bucket"
    }
  ]
}
```

