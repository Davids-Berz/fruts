#Rol 

Las entidades pueden asumir un rol de varias formas, dependiendo del contexto y el servicio. Por ejemplo, una instancia EC2 puede asumir un rol si se le asigna un perfil de instancia que contiene el rol. Una función Lambda puede asumir un rol si se le asigna ese rol en su configuración.

#### Ejemplo: Asumir un Rol desde la CLI

Para asumir un rol desde la línea de comandos, puedes usar el comando `assume-role` de AWS CLI:

```
aws sts assume-role --role-arn "arn:aws:iam::123456789012:role/example-role" --role-session-name "example-session"
```

Esto devolverá credenciales temporales que puedes usar para realizar acciones en nombre del rol asumido.