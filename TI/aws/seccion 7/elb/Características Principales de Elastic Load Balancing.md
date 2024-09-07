- **Distribución de Tráfico**:
    
    - ELB distribuye el tráfico de entrada entre múltiples instancias de destino, como EC2, contenedores en ECS o Kubernetes, direcciones IP, y funciones Lambda, mejorando la disponibilidad y redundancia de la aplicación.
- **Escalabilidad Automática**:
    
    - ELB escala automáticamente su capacidad de manejo de tráfico en función de las demandas de la aplicación, asegurando que siempre haya suficientes recursos para manejar el tráfico sin interrupciones.
- **Tolerancia a Fallos**:
    
    - Si una instancia o recurso falla, ELB detecta el fallo y redirige el tráfico a instancias o recursos en buen estado, minimizando el impacto del fallo en los usuarios finales.
- **Integración con AWS Auto Scaling**:
    
    - ELB se integra con AWS Auto Scaling, permitiendo la adición o eliminación automática de instancias en función de la demanda. Esto asegura que la aplicación se mantenga receptiva y optimiza el uso de recursos.
- **Soporte para HTTPS y SSL/TLS**:
    
    - ELB puede manejar la terminación de SSL/TLS, descargando esta tarea de las instancias EC2 y mejorando la seguridad al centralizar la gestión de certificados.
- **Monitoreo y Logs**:
    
    - ELB se integra con Amazon CloudWatch, permitiendo el monitoreo de métricas clave como latencia, conteo de conexiones activas, y más. También se pueden habilitar logs de acceso para análisis de tráfico y seguridad.
- **Configuración de Políticas de Enrutamiento**:
    
    - Puedes configurar políticas de enrutamiento avanzado, como el enrutamiento basado en contenido en ALB, o redirigir el tráfico según reglas específicas.