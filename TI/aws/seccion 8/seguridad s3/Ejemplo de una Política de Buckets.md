Aquí tienes un ejemplo básico de una política de bucket que permite el acceso de solo lectura a cualquier usuario:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::mi-bucket/*"
    }
  ]
}
```

**Explicación**:

- **Effect**: `Allow`, permite la acción especificada.
- **Principal**: `*`, aplica a cualquier usuario (es público).
- **Action**: `s3:GetObject`, permite la acción de obtener objetos desde el bucket.
- **Resource**: `arn:aws:s3:::mi-bucket/*`, aplica a todos los objetos (`*`) dentro del bucket `mi-bucket`.