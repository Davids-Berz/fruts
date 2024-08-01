#politicas

- **Descripción**: Permite a un usuario iniciar y detener instancias EC2 específicas.
- **Ejemplo de Política**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "ec2:StartInstances",
        "ec2:StopInstances"
      ],
      "Resource": [
        "arn:aws:ec2:us-west-2:123456789012:instance/i-1234567890abcdef0",
        "arn:aws:ec2:us-west-2:123456789012:instance/i-0abcdef1234567890"
      ]
    }
  ]
}
```