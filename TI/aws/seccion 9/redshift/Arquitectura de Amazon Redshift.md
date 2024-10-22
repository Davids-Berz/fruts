Redshift sigue una arquitectura basada en clústeres compuestos por uno o más **nodos**. Los nodos se dividen en dos categorías:

1. **Nodo Líder (Leader Node)**: Este nodo coordina todas las actividades del clúster. Recibe las consultas de los usuarios, las analiza y planifica cómo se distribuirán entre los nodos de procesamiento.
2. **Nodos de Cómputo (Compute Nodes)**: Son responsables de almacenar los datos y ejecutar las consultas distribuidas por el nodo líder. Estos nodos se dividen en subprocesos para ejecutar consultas en paralelo.

#### Distribución de Datos:

- Los datos se distribuyen entre los nodos de cómputo en función de la **clave de distribución** definida al crear las tablas. Esto asegura que las consultas se ejecuten de manera eficiente y paralela.

#### Procesamiento Masivamente Paralelo (MPP):

- Redshift aprovecha el **procesamiento masivamente paralelo (MPP)** para ejecutar las consultas rápidamente. Los nodos de cómputo trabajan en paralelo para procesar grandes volúmenes de datos y devolver los resultados al nodo líder.