DynamoDB ofrece dos modos de capacidad para gestionar la carga de trabajo de tu aplicación:

#### 2.1. **Capacidad Aprovisionada**

En este modelo, defines explícitamente la cantidad de capacidad de lectura y escritura que tu aplicación necesita.

- **Lecturas y Escrituras por Segundo**: Configuras cuántas unidades de lectura y escritura necesita la tabla.
- **Auto Scaling**: Puedes habilitar el escalado automático para ajustar la capacidad según la demanda. Si el tráfico de la aplicación aumenta, el servicio ajusta la capacidad de manera automática.

#### 2.2. **Capacidad Bajo Demanda**

En el modo de **bajo demanda**, DynamoDB escala automáticamente sin necesidad de aprovisionar capacidad de lectura o escritura de antemano. Se factura por las solicitudes de lectura y escritura que realice la aplicación.

- **Ideal para cargas variables o impredecibles**: Útil si no tienes claro el volumen de tráfico que manejarás y prefieres pagar solo por lo que usas.
- **No requiere planificación de capacidad**: AWS se encarga de todo el escalado necesario para mantener el rendimiento.