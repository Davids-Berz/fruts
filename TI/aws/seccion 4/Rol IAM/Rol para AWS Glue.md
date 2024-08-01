#Rol 

### Rol para AWS Glue

Permitir que AWS Glue acceda a datos almacenados en S3 y escriba resultados en otro bucket S3:

**Política de Permisos del Rol**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:PutObject"
      ],
      "Resource": [
        "arn:aws:s3:::input-bucket/*",
        "arn:aws:s3:::output-bucket/*"
      ]
    }
  ]
}
```

**Política de Confianza del Rol**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Service": "glue.amazonaws.com"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

