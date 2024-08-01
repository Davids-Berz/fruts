Generar un Par de Claves SSH:

```
ssh-keygen -t rsa -b 2048 -f ~/.ssh/mykey
```

Esto crea dos archivos:

- `~/.ssh/mykey`: La clave privada.
- `~/.ssh/mykey.pub`: La clave pública.

#### Copiar la Clave Pública al Servidor

```
ssh-copy-id -i ~/.ssh/mykey.pub usuario@direccion-ip-del-servidor
```

Si `ssh-copy-id` no está disponible, puedes copiar manualmente:

```
cat ~/.ssh/mykey.pub | ssh usuario@direccion-ip-del-servidor 'cat >> ~/.ssh/authorized_keys'
```

