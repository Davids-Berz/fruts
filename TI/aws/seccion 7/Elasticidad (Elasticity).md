**Definición**: La elasticidad es la capacidad de un sistema para ajustar dinámicamente los recursos aprovisionados de acuerdo con las demandas actuales. Un sistema elástico no solo puede escalar hacia arriba (cuando la demanda aumenta) sino también escalar hacia abajo (cuando la demanda disminuye) para optimizar el uso de recursos y costos.

#### Principios Clave:

- **Auto Scaling**: Automatizar el proceso de añadir o quitar recursos en función de la demanda, manteniendo un equilibrio entre el rendimiento y el costo.
- **Pagar por Uso**: En un entorno elástico, se paga solo por los recursos utilizados. Cuando la demanda disminuye, el sistema libera recursos automáticamente, reduciendo los costos.
- **Monitoreo y Respuesta en Tiempo Real**: Utilizar herramientas de monitoreo que rastrean la utilización de recursos en tiempo real y ajustan los recursos provisionados en consecuencia.

#### Ejemplo en AWS:

- **AWS Lambda**: Ejecuta código en respuesta a eventos y escala automáticamente según sea necesario. Se paga solo por el tiempo de ejecución que se consume.
- **Amazon Aurora**: Un servicio de base de datos relacional que puede escalar automáticamente la capacidad de almacenamiento sin tiempo de inactividad.
- **Amazon CloudFront**: Escala automáticamente para manejar un volumen variable de tráfico global para la distribución de contenido.

### Relación entre los Conceptos

- **Alta Disponibilidad** y **Escalabilidad** están estrechamente relacionadas, ya que un sistema diseñado para alta disponibilidad generalmente se basa en una arquitectura escalable para manejar fallos y asegurar que el servicio esté siempre disponible.
- **Elasticidad** es una forma avanzada de escalabilidad, donde el ajuste de recursos no es solo para manejar una carga aumentada, sino para optimizar el uso de recursos de manera continua en respuesta a cambios dinámicos en la demanda.
- **Costos**: La elasticidad y escalabilidad, cuando están bien implementadas, pueden optimizar significativamente los costos operativos al permitir que los sistemas utilicen solo los recursos necesarios en cada momento.