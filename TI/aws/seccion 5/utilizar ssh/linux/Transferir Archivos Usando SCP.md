Puedes utilizar `scp` para transferir archivos de manera segura entre tu máquina local y el servidor remoto.

#### Copiar un Archivo al Servidor

1. Ejecuta el siguiente comando:

```
scp -i ~/.ssh/mykey archivo-local usuario@direccion-ip-del-servidor:/ruta/destino
```

#### Copiar un Archivo desde el Servidor

1. Ejecuta el siguiente comando:

```
scp -i ~/.ssh/mykey usuario@direccion-ip-del-servidor:/ruta/archivo-remoto /ruta/destino-local
```

