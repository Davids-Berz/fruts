1. **Escalabilidad Automática**:
    
    - Un ASG puede escalar automáticamente hacia arriba (aumentar el número de instancias) cuando la carga de trabajo aumenta, y escalar hacia abajo (disminuir el número de instancias) cuando la carga de trabajo disminuye.

2. **Configuración Basada en Políticas**:
    
    - Puedes definir políticas de escalado en función de métricas como el uso de CPU, el tráfico de red, o métricas personalizadas. Estas políticas determinan cuándo y cómo escalar el grupo de instancias.

3. **Disponibilidad y Redundancia**:
    
    - Los ASGs están diseñados para distribuir instancias en múltiples zonas de disponibilidad (AZs), lo que mejora la resiliencia y asegura que tu aplicación permanezca disponible incluso si una zona de disponibilidad falla.

4. **Capacidad Mínima, Máxima y Deseada**:
    
    - **Capacidad Mínima**: El número mínimo de instancias que siempre estarán ejecutándose en el grupo.
    - **Capacidad Máxima**: El número máximo de instancias que pueden ejecutarse en el grupo.
    - **Capacidad Deseada**: El número objetivo de instancias que se ejecutarán en condiciones normales, y que se ajustará en función de las políticas de escalado.

5. **Integración con Elastic Load Balancing (ELB)**:
    
    - Un ASG se puede integrar con un Elastic Load Balancer para distribuir el tráfico entrante entre las instancias EC2 del grupo, asegurando una distribución equitativa de la carga.

6. **Balanceo de Carga de Lanzamiento**:
    
    - ASG distribuye las instancias nuevas de manera uniforme entre las zonas de disponibilidad configuradas, maximizando la resiliencia y la disponibilidad.

7. **Health Checks y Reemplazo Automático**:
    
    - El ASG realiza comprobaciones de salud periódicas en las instancias. Si detecta una instancia que no está saludable, la termina automáticamente y lanza una nueva para reemplazarla, asegurando que siempre haya una cantidad mínima de instancias en buen estado.