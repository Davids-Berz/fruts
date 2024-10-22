#### 2.1. **Arquitectura Separada de Almacenamiento y Cómputo**

DocumentDB sigue un modelo de arquitectura en el que el **almacenamiento** y el **cómputo** están separados, lo que mejora la escalabilidad y el rendimiento:

- **Almacenamiento Distribuido**: Los datos se almacenan en un sistema distribuido que replica automáticamente los datos en tres AZs dentro de una región, asegurando durabilidad y alta disponibilidad.
- **Instancias de Cómputo Escalables**: Las instancias de cómputo (nodos) pueden ser escaladas de forma independiente para manejar cargas de trabajo intensivas en procesamiento. Las consultas de lectura pueden distribuirse entre las réplicas de lectura.

#### 2.2. **Replica Sets y Failover Automático**

DocumentDB utiliza un modelo de **réplica automática** en tres zonas de disponibilidad para garantizar la continuidad de las operaciones en caso de fallos. Si el nodo primario falla, el sistema realiza un **failover automático** hacia una de las réplicas de lectura en otra AZ, lo que minimiza el tiempo de inactividad.