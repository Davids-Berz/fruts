#### 6.1. **Amazon CloudWatch**

- DynamoDB se integra con **Amazon CloudWatch** para proporcionar métricas detalladas sobre el rendimiento, como la tasa de lecturas y escrituras, el uso de la capacidad y las tasas de error.
- Puedes configurar **alarmas de CloudWatch** para recibir notificaciones si las métricas superan ciertos umbrales (por ejemplo, si se acerca a la capacidad máxima aprovisionada).

#### 6.2. **DynamoDB Accelerator (DAX)**

- **DynamoDB Accelerator (DAX)** es un servicio de caché en memoria que acelera las lecturas de DynamoDB, reduciendo la latencia de milisegundos a microsegundos.
- Es ideal para aplicaciones que realizan muchas lecturas repetitivas y donde la baja latencia es crítica (como sistemas de juegos o aplicaciones en tiempo real).