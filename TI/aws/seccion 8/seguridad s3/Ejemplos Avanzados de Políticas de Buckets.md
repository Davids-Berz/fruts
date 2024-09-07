1. **Restringir el Acceso por IP y Requerir HTTPS**: Esta política permite acceso al bucket solo desde una IP específica y requiere que las solicitudes se realicen a través de HTTPS:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Deny",
      "Principal": "*",
      "Action": "s3:*",
      "Resource": "arn:aws:s3:::mi-bucket/*",
      "Condition": {
        "Bool": {
          "aws:SecureTransport": "false"
        },
        "NotIpAddress": {
          "aws:SourceIp": "192.168.1.0/24"
        }
      }
    }
  ]
}
```

2. **Política para Usuarios Autenticados en una Cuenta Específica**: Esta política permite acceso al bucket solo a los usuarios autenticados de una cuenta específica de AWS:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "AWS": "arn:aws:iam::123456789012:root"
      },
      "Action": "s3:*",
      "Resource": "arn:aws:s3:::mi-bucket/*"
    }
  ]
}
```

3. **Política de Solo Lectura para un Bucket Específico**: Esta política permite solo la lectura de los objetos en el bucket `mi-bucket`, restringiendo otras acciones:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::mi-bucket/*"
    }
  ]
}
```

