#politicas 

AmazonS3FullAccess

- **Descripción**: Proporciona acceso completo a Amazon S3.
- **Uso**: Para usuarios que necesitan gestionar completamente los buckets y objetos en S3.
- **Ejemplo de Política**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:*",
      "Resource": "*"
    }
  ]
}
```

