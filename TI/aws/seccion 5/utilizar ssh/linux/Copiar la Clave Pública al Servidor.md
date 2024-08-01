Para autenticarte en el servidor remoto, necesitas copiar tu clave pública al servidor.

#### Usando `ssh-copy-id`

1. Ejecuta el siguiente comando:

```
ssh-copy-id -i ~/.ssh/mykey.pub usuario@direccion-ip-del-servidor
```

- `-i ~/.ssh/mykey.pub`: Especifica la clave pública que deseas copiar.
- `usuario@direccion-ip-del-servidor`: Especifica el nombre de usuario y la dirección IP del servidor.

Copiar Manualmente

Si `ssh-copy-id` no está disponible, puedes copiar la clave manualmente:

1. Conéctate al servidor usando una contraseña:

```
ssh usuario@direccion-ip-del-servidor
```

2. Crea el directorio `.ssh` en el servidor si no existe:

```
mkdir -p ~/.ssh
chmod 700 ~/.ssh -- 04000 o 0400
```

3. Sal de la sesión SSH y copia la clave pública:

```
cat ~/.ssh/mykey.pub | ssh usuario@direccion-ip-del-servidor 'cat >> ~/.ssh/authorized_keys'
```

Asegúrate de que el archivo `~/.ssh/authorized_keys` tenga los permisos correctos:

```
ssh usuario@direccion-ip-del-servidor 'chmod 600 ~/.ssh/authorized_keys'
```

