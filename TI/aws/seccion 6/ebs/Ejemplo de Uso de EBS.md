#### Caso de Uso: Base de Datos MySQL en EC2 con EBS

1. **Crear un Volumen EBS gp2**:
    
    - Tamaño: 100 GiB
    - Tipo: gp2
    
2. **Adjuntar el Volumen a una Instancia EC2**:
    
    - Adjuntar el volumen como `/dev/xvdf`.
3. **Montar el Volumen**:
    
    - Crear un punto de montaje:
        
        `sudo mkdir /mnt/mysql`
        
    - Montar el volumen:
        
        `sudo mount /dev/xvdf /mnt/mysql`
        
4. **Configurar MySQL para Usar el Volumen EBS**:
    
    - Actualizar la configuración de MySQL para usar el nuevo punto de montaje:
        `datadir = /mnt/mysql/data`
        
    - Reiniciar MySQL.
	
5. **Crear Snapshots Regulares**:
    - Configurar snapshots automáticos para realizar copias de seguridad del volumen EBS.