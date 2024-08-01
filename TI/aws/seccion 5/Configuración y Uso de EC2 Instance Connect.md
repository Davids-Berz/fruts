#EC2 #instance-connect

#### Paso 1: Configurar el Acceso SSH en la Instancia EC2

1. **Configurar Grupos de Seguridad**:
    
    - Asegúrate de que el grupo de seguridad asociado a tu instancia EC2 permite el tráfico SSH (puerto 22).
    - En la consola de administración de AWS, navega a **EC2** > **Security Groups**.
    - Selecciona el grupo de seguridad de tu instancia y verifica que haya una regla que permita el acceso SSH:

```
Inbound Rules: Type: SSH Protocol: TCP Port Range: 22 Source: 0.0.0.0/0 (o más restringido según tus necesidades)

```

2. **Configurar IAM Roles**:
    
    - EC2 Instance Connect requiere que la instancia EC2 tenga un rol de IAM asociado con los permisos necesarios.
    - En la consola de administración de AWS, navega a **IAM** > **Roles**.
    - Crea un nuevo rol o usa uno existente y adjunta la política **AmazonEC2RoleforSSM**.
    - Asocia este rol a tu instancia EC2.

#### Paso 2: Conectarse a la Instancia EC2 Usando EC2 Instance Connect

1. **Acceder a la Consola de Administración de AWS**:
    
    - Inicia sesión en la consola de administración de AWS.
    - Navega a **EC2** > **Instances**.

2. **Seleccionar la Instancia**:
    
    - Selecciona la instancia EC2 a la que deseas conectarte.

3. **Conectar Usando EC2 Instance Connect**:
    
    - Haz clic en el botón **Connect** en la parte superior de la página.
    - En el diálogo que aparece, selecciona la opción **EC2 Instance Connect**.
    - Verifica que el nombre de usuario predeterminado es correcto (por ejemplo, `ec2-user` para Amazon Linux, `ubuntu` para Ubuntu).
    - Haz clic en **Connect**.

#### Paso 3: Uso de EC2 Instance Connect desde la Línea de Comandos (Opcional)

También puedes usar EC2 Instance Connect desde la línea de comandos utilizando el AWS CLI.

1. **Instalar AWS CLI**:
    
    - Si no tienes el AWS CLI instalado, puedes descargarlo e instalarlo siguiendo las instrucciones de [AWS CLI Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).
2. **Configurar AWS CLI**:
    
    - Configura AWS CLI con tus credenciales de AWS:
        
        `aws configure`
        
    - Ingresa tu Access Key ID, Secret Access Key, región y formato de salida preferido.
3. **Conectar Usando EC2 Instance Connect**:
    
    - Utiliza el siguiente comando para conectarte a tu instancia EC2:

```
aws ec2-instance-connect send-ssh-public-key --instance-id i-0123456789abcdef0 --availability-zone us-east-1a --instance-os-user ec2-user --ssh-public-key file://~/.ssh/id_rsa.pub
```    

   - Reemplaza `i-0123456789abcdef0` con el ID de tu instancia.
   - Reemplaza `us-east-1a` con la zona de disponibilidad de tu instancia.
   - Reemplaza `ec2-user` con el nombre de usuario adecuado para tu AMI.
   - Reemplaza `~/.ssh/id_rsa.pub` con la ruta a tu clave pública SSH.
