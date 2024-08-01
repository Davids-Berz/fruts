#politicas 

- **Descripción**: Proporciona acceso completo a Amazon EC2.
- **Uso**: Para usuarios que necesitan gestionar completamente las instancias, volúmenes y redes de EC2.
- **Ejemplo de Política**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "ec2:*",
      "Resource": "*"
    }
  ]
}
```

