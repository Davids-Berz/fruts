#### Crear una Instancia con Almacén de Instancias

1. **Acceder a la Consola de AWS**:
    
    - Inicia sesión en la [Consola de administración de AWS](https://aws.amazon.com/console/).
2. **Seleccionar una AMI**:
    
    - Selecciona la Amazon Machine Image (AMI) que prefieras para lanzar la instancia.
3. **Elegir el Tipo de Instancia**:
    
    - Elige un tipo de instancia que soporte almacenamiento de instancias (por ejemplo, `m5d`, `i3`, `c5d`).
4. **Configurar Almacenamiento de Instancias**:
    
    - Durante el proceso de configuración de la instancia, en la sección **Add Storage**, verás volúmenes etiquetados como "Instance Store".
    - Puedes ajustar el tamaño de los volúmenes según las opciones disponibles.
5. **Lanzar la Instancia**:
    
    - Revisa la configuración y lanza la instancia.

#### Montar y Usar el Almacén de Instancias

1. **Conectar a la Instancia**:
    
    - Conéctate a tu instancia EC2 utilizando SSH.

2. **Verificar Dispositivos de Almacenamiento**:
    
    - Utiliza el siguiente comando para listar los dispositivos de almacenamiento:
    - `lsblk`
    - Los volúmenes del almacén de instancias suelen aparecer como `/dev/nvme*` o `/dev/xvdb`, `/dev/xvdc`, etc.

3. **Formatear el Volumen (si es necesario)**:

- Si el volumen del almacén de instancias no está formateado, puedes formatearlo:
- `sudo mkfs -t ext4 /dev/nvme0n1`

4. **Montar el Volumen**:

- Monta el volumen en un directorio de tu elección:
- `sudo mkdir /mnt/instancestore
	sudo mount /dev/nvme0n1 /mnt/instancestore`

5. **Configurar el Montaje Automático (opcional)**:

- Si deseas que el volumen se monte automáticamente en cada reinicio de la instancia, añade una entrada en `/etc/fstab`:
- `echo '/dev/nvme0n1 /mnt/instancestore ext4 defaults,nofail 0 2' | sudo tee -a /etc/fstab`

