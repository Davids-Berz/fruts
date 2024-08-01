#politicas 

ReadOnlyAccess

- **Descripción**: Proporciona acceso de solo lectura a todos los servicios y recursos de AWS.
- **Uso**: Para usuarios que necesitan visualizar recursos y datos sin realizar cambios.
- **Ejemplo de Política**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "ec2:Describe*",
        "s3:List*",
        "s3:Get*",
        "rds:Describe*",
        "cloudwatch:List*",
        "cloudwatch:Get*"
      ],
      "Resource": "*"
    }
  ]
}
```

