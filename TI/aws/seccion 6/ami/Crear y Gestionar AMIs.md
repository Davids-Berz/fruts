#### Crear una AMI desde una Instancia EC2

1. **Configurar la Instancia EC2**:
    
    - Lanza una instancia EC2 y configúrala según tus necesidades (incluyendo la instalación de software, configuraciones de red, y ajustes del sistema operativo).

2. **Crear la AMI**:
    
    - Accede a la consola de administración de AWS.
    - Navega a **EC2** > **Instances**.
    - Selecciona la instancia que deseas convertir en una AMI.
    - Haz clic en **Actions** > **Image** > **Create Image**.
    - Proporciona un nombre y una descripción para la AMI.
    - Configura las opciones de almacenamiento, como los volúmenes de EBS que se incluirán.
    - Haz clic en **Create Image**.

3. **Ver el Progreso**:
    
    - Navega a **EC2** > **Images** > **AMIs** para ver el progreso de la creación de la AMI.

#### Lanzar una Instancia desde una AMI

1. **Seleccionar la AMI**:
    
    - Accede a la consola de administración de AWS.
    - Navega a **EC2** > **AMIs**.
    - Selecciona la AMI desde la que deseas lanzar una instancia.

2. **Lanzar Instancia**:
    
    - Haz clic en **Launch**.
    - Configura los detalles de la instancia, como el tipo de instancia, configuración de red, y almacenamiento adicional.
    - Revisa y lanza la instancia.

#### Compartir una AMI

1. **Seleccionar la AMI**:
    
    - Navega a **EC2** > **AMIs**.
    - Selecciona la AMI que deseas compartir.

2. **Modificar Permisos**:
    
    - Haz clic en **Actions** > **Modify Image Permissions**.
    - Puedes compartir la AMI con cuentas específicas de AWS añadiendo el ID de la cuenta, o hacerla pública para que cualquier usuario de AWS pueda utilizarla.
    - Guarda los cambios.

#### Copiar una AMI entre Regiones

1. **Seleccionar la AMI**:
    
    - Navega a **EC2** > **AMIs**.
    - Selecciona la AMI que deseas copiar.

2. **Copiar la AMI**:
    
    - Haz clic en **Actions** > **Copy AMI**.
    - Selecciona la región de destino.
    - Configura las opciones adicionales, como el cifrado de los volúmenes.
    - Haz clic en **Copy AMI**.