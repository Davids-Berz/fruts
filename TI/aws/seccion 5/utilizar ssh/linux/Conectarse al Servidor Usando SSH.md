Ahora que la clave pública está en el servidor, puedes conectarte sin necesidad de una contraseña.

#### Conectarse Usando SSH

1. Abre una terminal.
2. Ejecuta el siguiente comando:

```
ssh -i ~/.ssh/mykey usuario@direccion-ip-del-servidor
```

- `-i ~/.ssh/mykey`: Especifica la clave privada que deseas usar.
- `usuario@direccion-ip-del-servidor`: Especifica el nombre de usuario y la dirección IP del servidor.

