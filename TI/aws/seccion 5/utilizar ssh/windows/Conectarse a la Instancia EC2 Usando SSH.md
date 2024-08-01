- **Abrir PowerShell o CMD**:
    
    - Abre PowerShell o la línea de comandos (CMD).
- **Conectarse a la Instancia EC2**:
    
    - Utiliza el siguiente comando para conectarte a tu instancia EC2:

```
ssh -i "C:\ruta\a\EC2Tutorial.pem" ec2-user@direccion-ip-del-servidor
```

- Reemplaza `"C:\ruta\a\EC2Tutorial.pem"` con la ruta completa a tu archivo PEM.
- Reemplaza `ec2-user` con el nombre de usuario adecuado para tu AMI (por ejemplo, `ubuntu` para Ubuntu AMIs).
- Reemplaza `direccion-ip-del-servidor` con la dirección IP pública de tu instancia EC2.

### Ejemplo Completo

Supongamos que tu archivo PEM está en el escritorio y tu nombre de usuario en Windows es `juan`, la dirección IP de tu servidor es `54.123.45.67`, y estás usando la AMI de Amazon Linux. Aquí están los pasos completos:

1. **Mover el archivo PEM al escritorio**:
    
    - Asegúrate de que el archivo `EC2Tutorial.pem` está en el escritorio: 
    
    - `C:\Users\juan\Desktop\EC2Tutorial.pem`.
    
2. **Configurar Permisos del Archivo PEM**:
    
    - Abre PowerShell y ejecuta:
        
        `icacls "C:\Users\juan\Desktop\EC2Tutorial.pem" /inheritance:r /grant:r juan:F`
        
3. **Conectarse a la Instancia EC2**:
    
        `ssh -i "C:\Users\juan\Desktop\EC2Tutorial.pem" ec2-user@54.123.45.67`

### Solución de Problemas Comunes

1. **Permisos del Archivo PEM**:
    
    - Asegúrate de que los permisos del archivo PEM son correctos. El archivo solo debe ser legible por tu usuario. Utiliza `icacls` como se describe arriba para ajustar los permisos.
2. **Conectividad de Red**:
    
    - Verifica que tu instancia EC2 tiene una IP pública asignada y que el grupo de seguridad asociado permite el tráfico SSH (puerto 22) desde tu dirección IP.
3. **Usuario Correcto**:
    
    - Asegúrate de usar el nombre de usuario correcto para tu AMI:
        - `ec2-user` para Amazon Linux, RHEL, CentOS.
        - `ubuntu` para Ubuntu.
        - `admin` para Debian.
        - `root` para otros AMIs.