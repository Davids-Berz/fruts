1. **Persistencia**:
    - Los volúmenes EBS son persistentes y mantienen sus datos incluso si se detiene o termina la instancia EC2 a la que están adjuntos.

2. **Escalabilidad**:
    - Puedes aumentar el tamaño de los volúmenes EBS, ajustar el rendimiento y cambiar el tipo de volumen según sea necesario, sin tiempo de inactividad.

3. **Copias de Seguridad**:
    - EBS permite crear snapshots (instantáneas) de los volúmenes en cualquier momento, proporcionando una manera fácil de respaldar y restaurar datos.

4. **Alto Rendimiento**:
    - Diseñado para cargas de trabajo que requieren alta IOPS (operaciones de entrada/salida por segundo) y baja latencia, como bases de datos y aplicaciones críticas.

5. **Seguridad**:
    - Soporta el cifrado de datos en reposo y en tránsito utilizando claves gestionadas por AWS o claves personalizadas.