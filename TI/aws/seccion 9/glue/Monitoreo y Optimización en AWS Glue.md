#### 5.1. **Monitoreo con CloudWatch**

Glue se integra con **Amazon CloudWatch** para proporcionar métricas detalladas sobre el rendimiento de los trabajos ETL. Puedes supervisar la duración de los trabajos, el uso de recursos, y los errores, además de configurar **alarmas** para recibir notificaciones si se producen problemas.

#### 5.2. **Glue Cost Optimizer**

Glue cobra por la duración y los recursos utilizados durante la ejecución de los trabajos ETL. Para optimizar los costos, es importante:

- **Utilizar Bookmarks**: Procesar solo los datos nuevos o modificados.
- **Ajustar el Tamaño del Cluster**: Controlar el número de nodos de cómputo para evitar el sobredimensionamiento.