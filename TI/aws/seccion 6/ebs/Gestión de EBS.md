#### Crear un Volumen EBS

1. **Acceder a la Consola de AWS**:
    
    - Inicia sesión en la [Consola de administración de AWS](https://aws.amazon.com/console/).
2. **Navegar a EBS**:
    
    - Ve a **EC2** en el menú de servicios y selecciona **Elastic Block Store** > **Volumes**.
3. **Crear un Nuevo Volumen**:
    
    - Haz clic en **Create Volume**.
    - Selecciona el tipo de volumen (gp2, gp3, io1, io2, st1, sc1).
    - Configura el tamaño del volumen y, si es aplicable, el rendimiento IOPS.
    - Selecciona la zona de disponibilidad (debe coincidir con la de la instancia EC2 a la que planeas adjuntar el volumen).
4. **Configurar Opciones Adicionales**:
    
    - Configura el cifrado si es necesario.
5. **Crear el Volumen**:
    
    - Haz clic en **Create Volume**.

#### Adjuntar un Volumen EBS a una Instancia EC2

1. **Seleccionar el Volumen**:
    
    - En la consola de EC2, selecciona el volumen que acabas de crear.
2. **Adjuntar el Volumen**:
    
    - Haz clic en **Actions** y selecciona **Attach Volume**.
    - Selecciona la instancia EC2 a la que deseas adjuntar el volumen.
    - Especifica el dispositivo (por ejemplo, `/dev/sdf`).
3. **Confirmar**:
    
    - Haz clic en **Attach**.

#### Montar el Volumen en la Instancia EC2

Después de adjuntar el volumen, necesitas montarlo en tu instancia EC2.

1. **Conectar a la Instancia**:
    - Conéctate a tu instancia EC2 usando SSH.

2. **Crear un Punto de Montaje**:
    - Crea un directorio para montar el volumen:
	    - `sudo mkdir /mnt/ebs`

3. **Montar el Volumen**:
- Monta el volumen en el punto de montaje:
	- `sudo mount /dev/xvdf /mnt/ebs`
- Nota: `/dev/xvdf` debe coincidir con el dispositivo especificado al adjuntar el volumen.

4. **Verificar el Montaje**:
- Verifica que el volumen está montado correctamente
- `df -h`

#### Crear y Restaurar Snapshots

**Crear una Instantánea**:

1. **Seleccionar el Volumen**:
    - En la consola de EC2, selecciona el volumen EBS.

2. **Crear Instantánea**:
    - Haz clic en **Actions** y selecciona **Create Snapshot**.
    - Proporciona una descripción para la instantánea.
    - Haz clic en **Create Snapshot**.

**Restaurar una Instantánea**:

1. **Crear un Volumen desde la Instantánea**:
    
    - En la consola de EC2, navega a **Snapshots**.
    - Selecciona la instantánea y haz clic en **Create Volume**.
    - Configura el tamaño y tipo del volumen (puede ser diferente al original si es necesario).

2. **Adjuntar el Volumen Restaurado**:
    - Sigue los mismos pasos descritos anteriormente para adjuntar y montar el volumen.