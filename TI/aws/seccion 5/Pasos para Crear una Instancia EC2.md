#### Paso 1: Acceder a la Consola de AWS

1. Inicia sesión en la [Consola de administración de AWS](https://aws.amazon.com/console/).
2. En el menú de servicios, busca y selecciona **EC2**.

#### Paso 2: Lanzar una Nueva Instancia

1. En el panel de EC2, haz clic en **Launch Instance**.

#### Paso 3: Elegir una Amazon Machine Image (AMI)

1. Selecciona una AMI que contenga el sistema operativo que deseas usar. AWS proporciona varias AMIs, incluyendo:
    
    - Amazon Linux 2
    - Ubuntu
    - Microsoft Windows Server
    - AMIs personalizadas si has creado alguna previamente.
    
    Para este ejemplo, seleccionaremos **Amazon Linux 2 AMI (HVM), SSD Volume Type**.
    

#### Paso 4: Elegir un Tipo de Instancia

1. Selecciona el tipo de instancia que mejor se adapte a tus necesidades. AWS ofrece varios tipos de instancias categorizadas en diferentes familias según su propósito (general, computación optimizada, memoria optimizada, etc.).
    - Para este ejemplo, seleccionaremos **t2.micro**, que está incluido en el nivel gratuito de AWS y es adecuado para cargas de trabajo ligeras.

#### Paso 5: Configurar los Detalles de la Instancia

1. Configura las opciones de red, grupo de Auto Scaling, y más. Para configuraciones básicas:
    
    - **Number of instances**: 1
    - **Network**: Selecciona la VPC predeterminada o una VPC específica.
    - **Subnet**: Selecciona una subred específica si es necesario.
    - **Auto-assign Public IP**: Asegúrate de que esté habilitado para que la instancia obtenga una IP pública.
2. Deja las demás configuraciones con los valores predeterminados y haz clic en **Next: Add Storage**.
    

#### Paso 6: Agregar Almacenamiento

1. Configura los volúmenes de almacenamiento para tu instancia. Por defecto, se proporciona un volumen EBS para el sistema operativo.
    
    - **Size (GiB)**: 8 (o ajusta según tus necesidades).
    - **Volume Type**: General Purpose (GP2).
2. Puedes agregar más volúmenes si es necesario, luego haz clic en **Next: Add Tags**.
    

#### Paso 7: Agregar Etiquetas

1. Agrega etiquetas para identificar y organizar tus instancias. Las etiquetas son pares clave-valor.
    
    - Ejemplo: **Key**: Name, **Value**: MyFirstInstance.
2. Haz clic en **Next: Configure Security Group**.
    

#### Paso 8: Configurar Grupos de Seguridad

1. Configura un grupo de seguridad para definir las reglas de firewall que controlan el tráfico entrante y saliente.
    
    - **Security group name**: MySecurityGroup
    - **Description**: Security group for my first instance.
    - **Type**: SSH
    - **Protocol**: TCP
    - **Port Range**: 22
    - **Source**: Anywhere (0.0.0.0/0, ::/0) (Ten en cuenta que esto permite el acceso SSH desde cualquier lugar. Para mayor seguridad, restringe esto a tu IP).
2. Haz clic en **Review and Launch**.
    

#### Paso 9: Revisar y Lanzar

1. Revisa los detalles de tu configuración.
2. Haz clic en **Launch**.

#### Paso 10: Seleccionar un Par de Claves

1. AWS te pedirá que selecciones un par de claves para acceder a tu instancia.
    
    - Si ya tienes un par de claves, selecciónalo de la lista.
    - Si no tienes uno, selecciona **Create a new key pair**, ingresa un nombre y haz clic en **Download Key Pair**. Guarda este archivo en un lugar seguro; lo necesitarás para conectarte a tu instancia.
2. Haz clic en **Launch Instances**.
    

#### Paso 11: Conectar a la Instancia EC2

1. En el panel de EC2, selecciona **Instances** en el menú de la izquierda.
    
2. Encuentra tu nueva instancia en la lista y espera a que su estado cambie a **running**.
    
3. Selecciona la instancia y haz clic en **Connect**.
    
4. Sigue las instrucciones para conectarte a tu instancia utilizando SSH.
    
    - Para Linux/Mac:

	- ``ssh -i "path/to/key-pair.pem" ec2-user@your-instance-public-dns``

	- Para Windows, utiliza un cliente SSH como PuTTY.

### Ejemplo de Conexión a una Instancia EC2 (Linux/Mac)

1. Abre una terminal y navega al directorio donde guardaste tu archivo `.pem`.

2. Concede permisos de lectura al archivo `.pem`:
    
    bash:
    
    `chmod 400 path/to/key-pair.pem`
    
3. Conéctate a la instancia utilizando SSH:
    
    bash:
    
    `ssh -i "path/to/key-pair.pem" ec2-user@your-instance-public-dns`
    

Reemplaza `path/to/key-pair.pem` con la ruta al archivo `.pem` descargado y `your-instance-public-dns` con el DNS público de tu instancia (disponible en la consola de EC2).