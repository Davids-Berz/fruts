Para simplificar las conexiones SSH, puedes configurar el archivo `~/.ssh/config` para almacenar configuraciones de hosts.

#### Ejemplo de Configuración

1. Edita el archivo `~/.ssh/config` (crea el archivo si no existe):

```
nano ~/.ssh/config
```

2. Agrega la siguiente configuración:

```
Host miservidor
    HostName direccion-ip-del-servidor
    User usuario
    IdentityFile ~/.ssh/mykey
```

3. Guarda y cierra el archivo.

#### Conectarse Usando el Alias

1. Ahora puedes conectarte simplemente usando el alias definido en el archivo de configuración:

```
ssh miservidor
```

