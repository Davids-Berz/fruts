#### Paso 1: Crear una Cuenta de AWS

1. Visita [AWS](https://aws.amazon.com/) y crea una cuenta.
2. Completa el registro proporcionando la información necesaria.

#### Paso 2: Lanzar una Instancia EC2

1. **Acceder a la Consola de AWS**:
    
    - Inicia sesión en la consola de administración de AWS.
    - Navega a **EC2** en el menú de servicios.
2. **Elegir una AMI**:
    
    - Selecciona una Amazon Machine Image (AMI) que contenga el sistema operativo deseado (e.g., Amazon Linux 2, Ubuntu, Windows Server).
3. **Elegir un Tipo de Instancia**:
    
    - Selecciona el tipo de instancia que mejor se adapte a tus necesidades (e.g., t2.micro para uso general).
4. **Configurar Detalles de la Instancia**:
    
    - Configura las opciones de red, grupo de Auto Scaling, etc.
5. **Agregar Almacenamiento**:
    
    - Configura los volúmenes EBS adicionales si es necesario.
6. **Agregar Etiquetas**:
    
    - Agrega etiquetas para identificar y organizar tus instancias.
7. **Configurar Grupos de Seguridad**:
    
    - Define las reglas de tráfico entrante y saliente para tu instancia.
8. **Revisar y Lanzar**:
    
    - Revisa tu configuración y haz clic en **Launch**.
    - Selecciona o crea un par de claves (Key Pair) para acceder a tu instancia.

#### Paso 3: Conectar a la Instancia EC2

1. **Instancias Linux/Unix**:
    
    - Usa un cliente SSH para conectarte:

```
ssh -i "path/to/key-pair.pem" ec2-user@your-instance-public-dns
```

2. **Instancias Windows**:

- Usa un cliente RDP para conectarte:
    - Descarga la clave privada y descifra la contraseña de administrador en la consola de AWS.
    - Conéctate utilizando el cliente RDP con la IP pública de la instancia.
