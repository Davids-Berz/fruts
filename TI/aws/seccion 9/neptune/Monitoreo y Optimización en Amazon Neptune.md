#### 5.1. **Amazon CloudWatch**

Amazon Neptune se integra con **Amazon CloudWatch** para proporcionar métricas detalladas sobre el rendimiento del clúster, como el uso de CPU, latencia de consultas, número de conexiones y rendimiento de almacenamiento. Puedes configurar **alarmas de CloudWatch** para notificarte si alguna métrica crítica excede los umbrales definidos.

#### 5.2. **Escalabilidad Automática**

Neptune puede escalar horizontalmente añadiendo réplicas de lectura, lo que permite manejar más consultas de lectura sin afectar el rendimiento de la instancia principal. Además, el almacenamiento se ajusta automáticamente en función del tamaño de los datos.