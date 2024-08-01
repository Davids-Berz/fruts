#### Cambiar el Puerto SSH

Para mejorar la seguridad, puedes cambiar el puerto predeterminado 22 a otro puerto en el archivo de configuración del servidor SSH (`/etc/ssh/sshd_config`).

1. Abre el archivo de configuración del servidor SSH:

```
sudo nano /etc/ssh/sshd_config
```

2. Encuentra la línea que dice `#Port 22` y cámbiala a otro puerto, por ejemplo:

```
Port 2222
```

3. Guarda y cierra el archivo.
 
4. Reinicia el servicio SSH:

```
sudo systemctl restart sshd
```

5. Para conectarte usando el nuevo puerto:

```
ssh -i ~/.ssh/mykey -p 2222 usuario@direccion-ip-del-servidor
```

#### Deshabilitar Autenticación por Contraseña

Para mayor seguridad, puedes deshabilitar la autenticación por contraseña en el servidor SSH.

1. Abre el archivo de configuración del servidor SSH:

```
sudo nano /etc/ssh/sshd_config
```

2. Encuentra la línea que dice `#PasswordAuthentication yes` y cámbiala a:

```
PasswordAuthentication no
```

3. Guarda y cierra el archivo.
 
4.  Reinicia el servicio SSH:

```
sudo systemctl restart sshd
```

