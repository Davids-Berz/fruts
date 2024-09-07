1. **Plantilla de Lanzamiento**:
    
    - Crear una Plantilla de Lanzamiento que utilice una AMI de Amazon Linux 2, con un tipo de instancia `t3.micro` y un disco de almacenamiento EBS de 8 GiB.

2. **Crear el Auto Scaling Group**:
    
    - Definir el ASG con una capacidad mínima de 2 instancias, una capacidad máxima de 10 instancias, y una capacidad deseada de 3 instancias.
    - Seleccionar dos zonas de disponibilidad (por ejemplo, `us-east-1a` y `us-east-1b`) para distribuir las instancias.

3. **Configurar Políticas de Escalado**:
    
    - Configurar una política para escalar hacia arriba si el uso promedio de CPU excede el 70% durante 5 minutos.
    - Configurar otra política para escalar hacia abajo si el uso promedio de CPU cae por debajo del 30% durante 5 minutos.

4. **Integrar con un Load Balancer**:
    
    - Asociar el ASG con un Application Load Balancer (ALB) para distribuir el tráfico entrante.