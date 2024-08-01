#### Conectar a un Servidor Remoto

**Comando Básico**:
```
ssh -i /ruta/a/clave.pem usuario@direccion-ip-del-servidor
```

- `-i /ruta/a/clave.pem`: Especifica la clave privada para la autenticación.
- `usuario`: El nombre de usuario en el servidor remoto.
- `direccion-ip-del-servidor`: La dirección IP o nombre de dominio del servidor remoto.

**Ejemplo**:

```
ssh -i ~/keys/mykey.pem ec2-user@ec2-54-123-45-67.compute-1.amazonaws.com
```

#### Transferencia Segura de Archivos con SCP

**Comando para Copiar un Archivo al Servidor**:

```
scp -i /ruta/a/clave.pem archivo-local usuario@direccion-ip-del-servidor:/ruta/destino
```

**Ejemplo**:

```
scp -i ~/keys/mykey.pem archivo.txt ec2-user@ec2-54-123-45-67.compute-1.amazonaws.com:/home/ec2-user
```

**Comando para Copiar un Archivo desde el Servidor**:

```
scp -i /ruta/a/clave.pem usuario@direccion-ip-del-servidor:/ruta/archivo-remoto /ruta/destino-local
```

**Ejemplo**:

```
scp -i ~/keys/mykey.pem ec2-user@ec2-54-123-45-67.compute-1.amazonaws.com:/home/ec2-user/archivo.txt ~/descargas
```

#### Túneles SSH

**Crear un Túnel SSH**:

```
ssh -L puerto-local:servidor-remoto:puerto-remoto -i /ruta/a/clave.pem usuario@direccion-ip-del-servidor
```

- `-L puerto-local:servidor-remoto:puerto-remoto`: Redirige el puerto local al servidor remoto y puerto especificados.

**Ejemplo**:

```
ssh -L 5901:localhost:5901 -i ~/keys/mykey.pem ec2-user@ec2-54-123-45-67.compute-1.amazonaws.com
```

Esto redirige el puerto 5901 en tu máquina local al puerto 5901 en el servidor remoto, útil para acceder a un escritorio remoto.