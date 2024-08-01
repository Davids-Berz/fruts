Para autenticarte en un servidor remoto de manera segura, primero necesitas un par de claves SSH (clave pública y clave privada). Si ya tienes un par de claves, puedes saltarte este paso.

#### Generar Claves en Linux y Mac

1. Abre una terminal.

2. Ejecuta el siguiente comando:

```
ssh-keygen -t rsa -b 2048 -f ~/.ssh/mykey
```

 - `-t rsa`: Especifica el tipo de clave (RSA).
 - `-b 2048`: Especifica el tamaño de la clave (2048 bits).
 - `-f ~/.ssh/mykey`: Especifica el archivo en el que se guardará la clave.

3. Sigue las indicaciones en la terminal. Se te pedirá que introduzcas una frase de contraseña para proteger tu clave privada (opcional pero recomendado).