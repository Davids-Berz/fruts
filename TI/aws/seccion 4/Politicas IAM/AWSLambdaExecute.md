#politicas 

AWSLambdaExecute

- **Descripción**: Proporciona permisos para invocar y gestionar funciones de Lambda, además de acceso a los logs asociados.
- **Uso**: Para usuarios y servicios que necesitan ejecutar y gestionar funciones Lambda.
- **Ejemplo de Política**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "lambda:InvokeFunction",
        "lambda:GetFunction"
      ],
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": [
        "logs:CreateLogGroup",
        "logs:CreateLogStream",
        "logs:PutLogEvents"
      ],
      "Resource": "arn:aws:logs:*:*:*"
    }
  ]
}
```
