#politicas 

PowerUserAccess

- **Descripción**: Permite acceso a todos los servicios de AWS excepto la administración de IAM.
- **Uso**: Para usuarios que necesitan gestionar servicios y recursos sin modificar IAM.
- **Ejemplo de Política**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "*"
      ],
      "Resource": "*",
      "Condition": {
        "StringNotEquals": {
          "iam:PassedToService": [
            "ec2.amazonaws.com",
            "elasticloadbalancing.amazonaws.com",
            "cloudwatch.amazonaws.com",
            "autoscaling.amazonaws.com",
            "rds.amazonaws.com",
            "iam.amazonaws.com",
            "cloudfront.amazonaws.com",
            "lambda.amazonaws.com"
          ]
        }
      }
    }
  ]
}
```

