#Rol 
#### **Rol para Funciones Lambda**

Permitir que una función Lambda acceda a una base de datos RDS:

**Política de Permisos del Rol**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "rds:DescribeDBInstances",
        "rds:Connect"
      ],
      "Resource": "arn:aws:rds:us-west-2:123456789012:db:example-db"
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
        "Service": "lambda.amazonaws.com"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```
