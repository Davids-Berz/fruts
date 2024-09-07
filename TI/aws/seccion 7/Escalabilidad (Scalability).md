**Definición**: La escalabilidad es la capacidad de un sistema para manejar un aumento en la carga de trabajo añadiendo recursos adicionales. Un sistema escalable puede crecer para manejar mayores volúmenes de datos, tráfico de usuarios, o procesamiento, sin afectar negativamente el rendimiento.

#### Tipos de Escalabilidad:

- **Escalabilidad Vertical (Scaling Up)**: Aumentar la capacidad de un solo recurso, como mejorar el hardware de un servidor (más CPU, memoria, etc.). Es útil para cargas de trabajo que requieren más recursos en un único nodo.
- **Escalabilidad Horizontal (Scaling Out)**: Añadir más instancias o nodos al sistema, distribuyendo la carga entre ellos. Esto es común en aplicaciones basadas en la nube y es clave para manejar grandes volúmenes de tráfico de manera eficiente.

#### Principios Clave:

- **Distribución de la Carga**: Utilizar equilibradores de carga (load balancers) para distribuir las solicitudes entre múltiples instancias, evitando sobrecargar una única instancia.
- **Diseño Sin Estado**: Crear aplicaciones que no dependan de un estado particular en un servidor para permitir que las instancias puedan ser añadidas o eliminadas sin afectar la experiencia del usuario.
- **Desacoplamiento de Componentes**: Separar los diferentes componentes de una aplicación (por ejemplo, frontend, backend, base de datos) para que puedan escalar de manera independiente.

#### Ejemplo en AWS:

- **Amazon EC2 Auto Scaling**: Permite escalar automáticamente el número de instancias EC2 hacia arriba o hacia abajo según las necesidades del tráfico.
- **Amazon S3**: Ofrece escalabilidad automática y almacenamiento ilimitado, gestionando el crecimiento del volumen de datos sin necesidad de intervención manual.
- **Amazon DynamoDB**: Proporciona escalabilidad automática para bases de datos NoSQL, ajustando el throughput de lectura y escritura según la demanda.