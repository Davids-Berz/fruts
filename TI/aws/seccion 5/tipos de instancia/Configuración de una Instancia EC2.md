#Tipos-Instancia 

Aquí hay un ejemplo paso a paso para lanzar una instancia EC2 utilizando la consola de administración de AWS:

1. **Acceder a la Consola de AWS**:
    
    - Inicia sesión en la [Consola de administración de AWS](https://aws.amazon.com/console/).
    - Selecciona **EC2** en el menú de servicios.
2. **Lanzar una Nueva Instancia**:
    
    - Haz clic en **Launch Instance**.
    - Selecciona una Amazon Machine Image (AMI) (por ejemplo, Amazon Linux 2).
    - Selecciona el tipo de instancia (por ejemplo, t3.micro).
3. **Configurar Detalles de la Instancia**:
    
    - Configura las opciones de red, asignación de IP, y más según tus necesidades.
4. **Agregar Almacenamiento**:
    
    - Configura el volumen de almacenamiento, por ejemplo, un volumen EBS de 8 GiB.
5. **Configurar Grupos de Seguridad**:
    
    - Define las reglas de firewall para el tráfico entrante y saliente.
    - Por ejemplo, permite SSH (puerto 22) desde tu IP para acceder a la instancia.
6. **Revisar y Lanzar**:
    
    - Revisa los detalles de tu configuración y haz clic en **Launch**.
    - Selecciona un par de claves para acceder a la instancia.
    - Haz clic en **Launch Instances**.
7. **Conectar a la Instancia**:
    
    - Utiliza SSH para conectarte a la instancia si es Linux:

```
ssh -i "path/to/key-pair.pem" ec2-user@your-instance-public-dns
```

Utiliza RDP para conectarte a la instancia si es Windows.