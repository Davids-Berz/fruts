#seguridad 

**Descripción**: Conjuntos de permisos que los servicios de AWS pueden asumir para acceder a otros recursos de AWS sin necesidad de compartir credenciales.

**Uso**:

- Asignar roles a instancias EC2, funciones Lambda, y otros servicios para delegar acceso seguro.
- Crear políticas de confianza para definir quién puede asumir el rol.

**Ejemplo de Política de Confianza**:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Service": "ec2.amazonaws.com"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```
